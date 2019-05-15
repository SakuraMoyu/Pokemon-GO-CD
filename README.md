# Pokemon-GO-CD
Generate a candidate CP list for a set of combinations of IVs of a pokemon at different level in Pokemon GO

How it works:
1. download the files to your local computer
2. open CD Calculator.html via web browser
3. in the browser, select the "stats.csv" file in this folder

At this point a form shall pop up

4. Fill the form and click "Start Calculation!" button at the bottom

Accuracy means the chance that these information will lead to a pokemon with target IV (P(target IV|Informations from CP, etc.)). 

Note that even though the minimum accuracy is set as 0% the calculator will still ignore cases with none of the IV combination meeting the target(thus the accuacy is 0%), the calculator will only shown cases that comprise with at least 1 target IV combination.

The calculator can now accept an arbitary combination of base stats of your own choice.

The calculation result will shown at the bottom, you can copy the table to excel and do what you want with the data.

You may also click the "Show Compact List" button to get the summarized information of the data.

Predicted appraisal result is also shown in summarized information.

Search string for the target IV range is now added at the bottom of the Compact List. Note that since only information about CP and HP can be used on search string its accuracy will be at the middle between "CP known" and "CP, HP and power up dust cost known".

Search string will split if the criteron overlap to each other which will generate more unwanted false positive.

Try not to set loose constrain on IV or it may not have enough memory to work with......

Result from a sample run of calculator was added as "Torchic Sample Run.xlsx", the configuation is (Atk IV >= 14, Def IV >= 11, Sta IV >= 11 and overall IV >= 40) with all accuracy set as 0%

Result of search string from sample run with same settings as above is added as "Torchic Sample Run.txt" as reference.

How to interpret the data generated:


Expected value: 

Show number of action you needed in order to get one of the IV combination you wanted, gives you an insight of how much candidate pokemon you will end up with after the spawn and trade so that you could set more realistic target.

Table with CP only:

If you don't care about candy, looking on this table gives you an idea to catch the pokemon or not, while it seems to be listing every single CP and such that it is not so useful, it's not true. If you set a sufficiently tight constrain(with around 200 combbinations only), even though the table shown a lot of candidate CP, but if you actually add up the column of number of possible combination you will find around 50% of combination is shut out from this list. 

Table with Summary page information:

If you will just catch everything this table will be more useful as you will need these extra information right after you spot out one candidate pokemon in your box by looking at its CP. With information about dust cost only pokemon within 2 levels will be grouped together, and HP is actually a decent extra information to further filter out some false positive. 

Table with Appraisal:

If you have some app that can immediately shown IV range after you finished appraisal inside the pokemon go app, you may not need this one, this is basically a IV calculator that try to calculate IVs of pokemon you will want to check beforehand so you can check the result by just matching the informations you gain. CP value within 2 power up is also shown as refrence so you can quickly check if the pokemon are actually holding the target IVs.

Table with level:

After all, the most significant ambiguity of the true IV combination of a usual CD pokemon after appraisal comes from level, so with this last pieces of information known in general you can yield 100% accuracy on identifying the pokemon is a target or not given that its level is not too low.


Max CP is given as this table is expected to be used with trading feature. In trading feature, after you have selected a pokemon, a range of CP after trading will be shown, checking the upper bound of this range can immediately tell which level your pokemon is. Note that if your friend is too low on trainer level you may not be able to get the correct max cp as the level of your pokemons will be trimmed to match your friend's trainer level. The range of CP has to be white color, instead of orange, in order to show the correct max CP.



If there is a calculation mistake(bug) please notify me as soon as possible, thank you for your cooperation.
