---
layout: post
title: The Martian
tags: science review reading
date: '2015-06-19 23:34'
---

I recently read [Andy Weir](http://www.andyweirauthor.com/)'s [_The Martian_](http://smile.amazon.com/dp/B00EMXBDMA), a novel about an astronaut who is marooned on Mars when his crew is forced to leave him for dead during an unexpected dust storm. The book chronicles his efforts to stay alive until a rescue team can bring him back to Earth.

<!--more-->

I very much enjoyed this book because the author went to great pains to ensure the scientific accuracy of the protagonist's survival actions. I felt that this enhanced my appreciation of the protagonist's choices because I could follow along with his thought process and see the realistic consequences of his actions.

_However_, the author made a very basic chemistry mistake that caught my attention. Though the author admitted in an [interview][b0a5267e] that he made some chemistry mistakes, given the amount of research and effort he put into the science throughout the book, I'm a bit disappointed that he overlooked such a simple mistake like this one. I'd like to set the record straight here once and for all!

This is the situation:

Our hero is trying to synthesize some extra water that he can use to grow potatoes so that he won't starve while he waits to be rescued. Taking inventory of his supplies, he notes that he has 2 25-liter tanks of liquid oxygen ($$ \mathrm{O_{2}} $$) and that he can combine it with hydrogen ($$ \mathrm{H_{2}} $$) to form water ($$ \mathrm{H_{2}O} $$). He then claims that he will be able to make 100 liters of water using his 50 liters of oxygen because "50 liters of ($$ \mathrm{O_{2}} $$) makes 100 liters of molecules that only have one O each."

This is incorrect!

This would be true if he was talking about gases, as long as the pressure and temperature remained the same. The behavior of gases is approximated by the ideal gas law: $$PV=NkT$$, where $$P$$ is pressure, $$V$$ is volume, $$N$$ is the number of gas particles, $$k$$ is Boltzmann's constant ($$1.38065 \times 10^{-23}$$ joules per kelvin), and $$T$$ is absolute temperature. For a given pressure and temperature, the volume of the gas is proportional to the number of gas particles. So if our hero doubles the number of gas particles (by using 1 $$ \mathrm{O_{2}} $$ molecule to make 2 $$ \mathrm{H_{2}O} $$ molecules), then he would double the volume accordingly. Of course, he would also need to add 100 liters of hydrogen gas (at the same temperature and pressure) as the other ingredient for the reaction, so he would be starting with 150 liters of ingredients and only getting 100 liters of product.

But, in this situation he is working with _liquid_ oxygen to form _liquid_ water! Liquids, unlike gases, have a fixed density (this is sometimes called incompressibility, meaning that you cannot squeeze most liquids into a smaller volume by applying pressure, as you can with gases). Consequently, the gas-like volume scaling does not apply to liquids. To properly calculate the volume of water that can be synthesized from the available liquid oxygen, a more careful analysis is required.

First, we can calculate the number of $$ \mathrm{O_{2}} $$ molecules contained in 50 liters of liquid oxygen. The density of liquid oxygen is 1146 grams per liter. The molecular weight of $$ \mathrm{O_{2}} $$ is 32 grams per mole. Thus:

$$ \mathrm{50 \, L \, O_{2} \times \frac{1146 \, g}{L} \times \frac{mol}{32 \, g} = 1790.625 \, mol \, O_{2}} $$

Assuming that we have more than enough hydrogen to use up all the oxygen, for every molecule of $$ \mathrm{O_{2}} $$, we can create 2 molecules of $$ \mathrm{H_{2}O} $$:

$$ 1790.625 \mathrm{\, mol \, O_{2} \times 2 = 3581.25 \, mol \, H_{2}O} $$

Finally, let's find the volume of 3581.25 mol water:

$$ \mathrm{3581.25 \, mol \, H_{2}O \times \frac{18 \, g}{mol} \times \frac{L}{1000 \, g} = 64.46 \, L \, H_{2}O}$$

So, instead of 100 liters of water as stated in the book, we can only make 64.46 liters!

Why such a large discrepancy? Besides going through the calculations, there is a more intuitive explanation. The oxygen atom in a water molecule makes up the vast majority (89%) of the molecule's mass, with the two hydrogen atoms making up the rest. Therefore, the mass of the liquid oxygen that our hero starts with is already very close to the mass of the water that he will end up with! In fact, the mass of the water is only 12.5% more than the mass of the original liquid oxygen. To compare their volumes, we must take the different densities into account:

$$ \mathrm{50 \, L \, O_{2} \times \frac{1000}{1146} \times \frac{18}{16} = 64.46 \, L} $$

The moral of this story is that you should not calculate reactions using volume! Remember that because the molecules are the ones taking part in the reaction, you must work in terms of molecules, not volume! If he wanted to make 100 liters of water, he should have started with 77.6 liters of liquid oxygen, not 50 liters.

But I'm nitpicking! Overall, it was a very good novel and I am looking forward to seeing the movie version when it is released later this year.

  [b0a5267e]: https://youtu.be/5SemyzKgaUU?t=2162 "Adam Savage Interviews 'The Martian' Author Andy Weir"
