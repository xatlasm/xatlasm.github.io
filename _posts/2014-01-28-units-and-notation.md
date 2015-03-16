---
layout: post
title: Units and notation
tags: science units nuclear
date: 2014-01-28 15:00:04 +0000
---

Up until this point, I have mostly avoided using numbers, units, and
equations but in future articles this will not be possible. So now would
be a good time to ensure that you are acquainted with these concepts
before things get too complex.

<!--more-->

Scientific Notation
-------------------

Scientists often work with very large and very small numbers and also
need to keep track of the precision of measurements. For this purpose,
scientific notation is used. Numbers in scientific notation take the
form:

$$a \times 10^{b}$$

where *a* is a number (often a decimal) between 1 and 10 (negatives are
ok too), and *b* is an integer (no decimals allowed). It is also
acceptable to abbreviate $$  \times 10^{b}$$ by replacing it with: E
*b*.

While this may seem like a funny way to write a number, it is very
convenient for very large or very small numbers because it saves you
from having to count up the zeros or decimal places. This also
simplifies a lot of arithmetic and allows you to quickly make rough
estimates.

To convert a number into scientific notation, place a decimal point
after the most significant non-zero digit (that is, the first non-zero
digit when counting from the left) to form *a*. Then, the number of
times that you just moved the decimal becomes *b*. If you moved the
decimal to the left, *b* is a positive number, and *vice versa*. For
example:

$$ 8675309$$

would be written as

$$ 8.675309\times10^{6} $$

or

8.675309E6

in scientific notation. Notice how *a* (8.675309) is a number between 1
and 10, and *b* (6) is the number of places that you had to move the
decimal from the original number (8675309) to change it into *a*
(8.675309).

Element notation
----------------

Elements are referred to in chemical equations by their symbols, as
listed in the periodic table. Isotopes of elements are written by
writing the symbol for the element (for example, gold's symbol is Au),
followed by a dash (-) and then the atomic mass of the isotope. So, gold
197 would be written as: Au-197. In equations, this is often stylized
as:

$$ \mathrm{~^{197}_{79}Au} $$

with the atomic mass written in superscript in the upper-left of the
element's symbol. Sometimes (like in this example) you will see the
atomic number written in subscript in the lower-right of the element's
symbol. The atomic number isn't strictly necessary because the element's
symbol already specifies the atomic number, but when working with
equations it can save you the trouble of looking up an element's atomic
number if you don't have it memorized.

Units of measurement
--------------------

A unit is a fixed amount that describes a physical quantity, such as
length or time, that is used for measurement. You are already familiar
with many of these, such as kilograms, meters, liters, and so on.

In science, the SI unit system is used as a worldwide standard of
measurement. This means that the average American is handicapped when it
comes to science since the USA uses its own system of units. In this
guide, I will be using the SI system for all measurements and
calculations, so I will leave it as an exercise for my American readers
to either convert all quantities into American units or to simply learn
the metric system like the rest of the world!

Because of the very small size of nuclei, nuclear scientists use units
which may be unfamiliar to the average person, but are convenient when
working with quantities seen in nuclear science. I will introduce a few
of them to you now and more of them as they become relevant to the
topics of discussion.

### Energy

Although the SI fundamental unit of energy is the joule (J), a joule is
too large when speaking about the energy of individual atoms. Instead,
we use a unit called the electronvolt (eV).

$$ 1~\mathrm{eV} = 1.602\times10^{-19}~\mathrm{J} $$

As with all metric units, prefixes (k for 1000, M for 1000000, etc.) are
used to easily indicate magnitudes. For example, the energy of the gamma
ray released by the decay of a Ba-137m atom has an energy of 662 keV.

### Mass

Because atoms are so small, it would be silly to measure their masses in
kilograms! Instead, we use a unit called the atomic mass unit (u).

$$ 1~\mathrm{u} = 1.661\times10^{-27}~\mathrm{kg} $$

1 u is approximately equal to the mass of a proton or a neutron, and for
ordinary chemistry, this is good enough for most calculations. However,
in the nuclear sciences, we must use the exact masses for particles for
calculations:

mass of proton = 1.007276466812 u mass of neutron = 1.00866491600 u

Because of Einstein's famous $$ E=mc^2 $$ equation, mass can also be
expressed using units of energy.

$$ 1~\mathrm{u} = 931.494061~\mathrm{\frac{MeV}{c^2}} $$

The $$c^2$$ in $$ \mathrm{\frac{MeV}{c^2}} $$ is often removed, leaving
$$ \mathrm{MeV} $$ for convenience. Since this is the same unit to
denote energy, context determines whether mass or energy is meant.

### Amount of matter

Because atoms are so small, when we want to scale up our calculations to
human-sized units, we need a way to easily count how many atoms are in a
quantity of matter. Fortunately, the mole[^1] (mol) allows us to do just
that.

$$ 1~\mathrm{mol} = 6.022\times10^{23} $$

You may notice that the mol itself does not have any physical units
attached to it. This is not a mistake. A mole is simply a shorthand for
that very, very large number, much like how "one dozen" in English means
"12 of something". This may seem to be a very strange choice for a
number, but its utility is that it is a conversion factor between atomic
mass and grams! For example, the molecular mass (sum of the atomic
masses of the atoms in a molecule) of water is 18.015, so one mole of
water has a mass of 18.015 grams, but contains $$ 6.022\times10^{23} $$
atoms. In mathematical equations, the number of atoms is often indicated
by the letter N.

* * * * *

Summary
-------

-   You can easily write very big or very small numbers using scientific
    notation. It looks like $$ a \times 10^{b} $$ or *a* E *b*.
-   Elements are referred to by their symbols from the periodic table.
    When referring to a specific isotope, write the isotope's mass after
    the symbol: Au-197.
-   Energy is often measured in electronvolts
    (eV). $$ 1~\mathrm{eV} = 1.602\times10^{-19}~\mathrm{J} $$
-   Mass is measured in atomic mass units
    (u). $$ 1~\mathrm{u} = 1.661\times10^{-27}~\mathrm{kg} $$ Thanks to
    it $$ E=mc^2 $$, can also be measured using eV, just like
    energy! $$ 1~\mathrm{u} = 931.494061~\mathrm{MeV} $$
-   The unit for amount of matter is the mole
    (mol). $$ 1~\mathrm{mol} = 6.022\times10^{23} $$ Think of it as a
    scientist's version of a dozen.

Further resources
-----------------

<a href="https://www.youtube.com/watch?v=hQpQ0hxVNTg" target="_blank">Crash
Course Chemistry: Unit Conversion & Significant Figures</a>

<a href="http://hyperphysics.phy-astr.gsu.edu/hbase/nuclear/nucuni.html" target="_blank">The
Hyperphysics Page on Nuclear Units</a>

<a href="http://chemwiki.ucdavis.edu/Analytical_Chemistry/Quantifying_Nature/Units_of_Measure/SI_Units" target="_blank">Chemwiki:
SI Units</a>

* * * * *

[^1]: Yes, it's got a funny name!
