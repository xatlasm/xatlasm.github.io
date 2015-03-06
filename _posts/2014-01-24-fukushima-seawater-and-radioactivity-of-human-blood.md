---
layout: post
title: Fukushima Seawater and the Radioactivity of Human Blood
---

You may have come across articles [like this one](http://www.naturalnews.com/043585_fukushima_radiation_pacific_ocean_marine_science_organization.html) across the web breathlessly heralding "alarming" predictions of seawater contamination from Fukushima of up to 30 becquerels per cubic meter (Bq/m^3) along the West Coast of North America. What do these numbers mean? Should you be worried?

<!--more-->

These predictions are sourced from a [scientific paper](http://www.sciencedirect.com/science/article/pii/S096706371300112X) published last year. The researchers used computer simulations to predict the dispersion patterns of cesium-137 released from Fukushima across the North Pacific Ocean over the next few decades. They concluded by predicting that the seawater along some areas along the West Coast of North America will experience cesium-137 concentrations between 10 and 30 Bq/m^3 between 2014 and 2020. But is that a lot of radioactivity?

Let's compare it to something that you are probably more familiar with: blood! Everyone knows that blood is essential to keep your body working properly. What you might not know is that your own blood is radioactive as well! Human blood, like the rest of your body, contains potassium, an ionic salt necessary for nerve function and maintaining the balance of water inside your cells. However, naturally-occurring potassium is slightly radioactive due to the presence of potassium-40 (0.0117% of all potassium), an isotope with a half-life of 1.2 billion years. Because of this, anything containing potassium emits a very small amount of radioactivity. For example, bananas are rich in potassium, and a typical banana has an activity of about 15 Bq because of it.

Knowing this, I decided to calculate the radioactivity of human blood due to potassium, so that we can compare it to the "alarming" contamination predicted in the Pacific Ocean.

The [normal range](http://www.nlm.nih.gov/medlineplus/ency/article/003484.htm) for potassium in human blood[^1] is 3.7~5.2 mEq/L. mEq stands for milliequivalent, and is a fancy unit for measuring ion concentrations in solution. We can easily convert this to a more standard milligrams per liter, by noting that 1 mEq = 1 mmol (millimole) for potassium ions, and that the atomic weight of potassium is 39.0983 milligrams per millimole. In other words, the normal concentration of potassium in human blood is 145~203 mg/L.

[^1]: These values refer to the potassium found only in the liquid part of blood, serum. Your blood cells also contain potassium, so the actual amount of potassium in your blood is **about 20 times** higher than the numbers we will use for our calculations!

$$3.7\sim 5.2\: \mathrm{\frac{mEq}{L}} \: \times 1\: \mathrm{\frac{mmol}{mEq}} \times 39.0983\: \mathrm{\frac{mg}{mmol}} =  145\sim 203\: \mathrm{\frac{mg}{L}}$$

Now for the radioactivity of potassium. As I mentioned before, potassium-40 comprises 0.0117% of natural potassium, and potassium-40's half life is 1.2 billion years. From this, we can calculate the specific activity (radioactivity per unit mass) of potassium, which comes out to 31.7 Bq/g.

$$0.0117\% \times \mathrm{\frac{6.022\times 10^{23}}{mole}}\times\frac{\ln {2}}{1.248\times10^{9}\: \mathrm{year}}\times \mathrm{\frac{1\: mole}{39.0983\: grams}} \times \mathrm{\frac{1\: year}{3.154\times10^{7}\: second}}= 31.7 \: \mathrm{\frac{Bq}{g}}$$

Finally, let's multiply this by the potassium concentration in blood to find its radioactivity from potassium.

$$31.7 \: \mathrm{\frac{Bq}{g}} \times 145\sim 203\: \mathrm{\frac{mg}{L}} = 4.60\sim 6.44\: \mathrm{\frac{Bq}{L}}$$

Scaled up to match the seawater volume quoted above, this comes out to 4,600~6,440 Bq/m^3, **over 150 times higher** than the predicted increase in seawater radioactivity along the West Coast of North America! Put another way, the predicted extra radioactivity in 1000 liters of seawater (~30 Bq) is the same amount that can be found in about 6 liters of human blood.

The [natural radioactivity of seawater](http://www.dailykos.com/story/2013/11/07/1253941/-Putting-Fukushima-in-Perspetive-A-primer-on-radioactivity-in-the-Ocean#) is about 13 Bq/L = 13,000 Bq/m^3, so a 30 Bq/m^3 increase would increase the water's natural radioactivity by only 0.23%. This is so small that it will be undetectable even by sensitive measuring equipment (the detection limit for cesium-137 in water is about 0.5 Bq/L, or 500 Bq/m^3).

In conclusion, the minuscule amount of extra radioactivity in the seawater far from Fukushima is predicted to reach a maximum concentration that is still more than 150 times **lower** than the radioactivity in your own blood! There will be so little that it will be undetectable by radiation detectors unless they first process the seawater to increase its dissolved solids concentration by a factor of about 15. In short, you should take these kinds of "alarming" reports of radioactive seawater with a grain of (sea) salt.
