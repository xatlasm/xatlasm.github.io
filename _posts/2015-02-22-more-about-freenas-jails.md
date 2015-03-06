---
layout: post
title: More about FreeNAS jails
tags:
- FreeNAS
---
My first attempt to upload a large tarball to Glacier was a success as described [here]({% post_url 2015-02-21-backing-up-freenas-to-aws-glacier %}), but subsequent ones failed because the FreeNAS server is headless. I get shell access to its jails in a browser tab from one of the Mac clients. If I launch a slow upload and I close the browser or the client goes to sleep while the upload is in progress, the shell session terminates and the upload is aborted.

One solution is to run these shell sessions in [`tmux`](http://tmux.sourceforge.net/). I have completed a second upload -- pics2012.tgz, weighing in at 1.4G -- in a `tmux` session that persisted through two browser shutdowns and one client sleep session, returning to work as expected with `tmux attach` every time. 

For this I had to install `tmux` on the `awsboss` jail first, and I ran into a problem: `pkg install tmux` would not work, and `pkg install <ANYTHING>` would not have worked either, for that matter. There are two possible fixes. One is to fix `pkg install` and try again `pkg install tmux`. The other is to ignore the problem and try `pkg_add tmux` instead. This is the old-school way of adding packages and it is [discouraged](http://doc.freenas.org/9.3/freenas_jails.html#installing-freebsd-packages) with the warning that it will "cause inconsistencies in the package management database." Whatever that means, it sounds serious, though a warning is not the same thing as an error, so I did it anyway. 

While I was at it, I also ran `pkg_add mosh`, because [MOSH](https://mosh.mit.edu/) seems to be another way to get state-preserving shell connections. This is of no use to me at the moment, but it will come up later. This post is motivated by my trying -- and failing -- to get `pkg install` to work properly on a FreeNAS 9.2.0 jail. I thought that would be easy, but I was wrong.

My googling turned up a fix that applies to FreeNAS 9.3, which allows two kinds of jails: port and standard. Port jails can run `pkg install <ANYTHING>`. Standard ones by design do not, but they can be persuaded as described [here](https://forums.freenas.org/index.php?threads/problem-installing-mysql-jail-pkg-conf-is-no-longer-supported.24048/). I thought that the fix would apply to FreeNAS 9.2 jails as well, but the steps outlined in this discussion rely on some source files being present at `/usr/src/share/keys` so that you can run

```
# cd /usr/src/share/keys && make && make install
```

There is no such directory path in a regular FreeNAS 9.2.0 jail, so this option, as far as I can tell, is out. But some pieces of the process did work, and may have been beneficial, as follows:

1. `# rm /usr/local/etc/pkg.conf`
2. `# pkg2ng`

The first step above gets rid of a useless `pkg.conf` that has one line that trips up `pkg install`, so no loss there. The second is more interesting: it did something to both `tmux` and `mosh`. I don't know, but I hope that whatever inconsistencies the FreeNAS documentation warns about when it discourages the use of `pkg_add` are fixed if you run `pkg2ng` immediately after you `pkg_add` anything. The job of `pkg2ng` seems to be that it converts installed packages from old-school `pkg_` style to the newer `pkgng` style that in theory should have worked out of the box.

That's all I have: the hope that `pkg_add` won't screw up anything in practice, and that `pkg2ng` will fix what `pkg_add` could have screwed up in theory.
