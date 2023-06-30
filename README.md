# Breakage analysis
## Table of contents

1. [Background](#background)
2. [Size and focus](#size-and-focus)
3. [Tools used](#tools-used)
4. [Findings](#findings)
5. [Usage](#usage)

### Background
This **exploratory data analysis** is about product loss or 'breakages' in an ophthalmic laboratory (my current place of work). It aims to investigate the major causes of breakages and their origins in 2022. The data used comes from a dataset located in the main server of the laboratory, which is updated daily with new information about breakage occurrences in the laboratory.


### Size and focus
This dataset contains 40 columns and 17658 rows.
The focus of this exploratory analysis is the origin and the causes of breakages  
and its attribute count is as follows:
- 21 types of breakage origin (Machine_Name)
- 190 types of breakage causes (Reas_Name)

### Tools used
- **Programming language :** Python
- **Libraries:** Numpy, Pandas, Seaborn, Plotly
- **Platforms:** Jupyter Notebooks

### Findings

**Summary Statistics**

![image](https://github.com/ojimenez24/Breakage2022/assets/123837381/7a423ed8-8549-417b-887b-952dc5a3605b)

As we can see, 'finished edgers' is where most breakages occurred in 2022. 
This breakage origin is closely followed by 'DC' (distribution center)

Now let's take a look at the count of breakages per reason.

*since many of the reasons are redundant and displaying all 190 reasons would be impractical, I decided to set a threshold to show only reasons with a reason count higher than 10% of the highest reason count (around 200)

![image](https://github.com/ojimenez24/Breakage2022/assets/123837381/375c7038-0bdf-40fc-a63a-1dfb7ad284f3)

Now, let's look at each of the top breakage origins by categorizing them and digging more into the type of breakage they produce.



**Categorical Statistics**

![image](https://github.com/ojimenez24/Breakage2022/assets/123837381/dc0644f8-8e94-40a3-808f-7b11ea3c0800)

In first place with over 5000 overall breakages, we have 'finished edgers'.It is not surprising to find that in 'finished edgers' the second biggest breakage reason "Scratch edging w/oAR" (over 2000) is found. Also, this reason is by far the highest compared to the other breakage reasons in 'finished edgers'.

![image](https://github.com/ojimenez24/Breakage2022/assets/123837381/c382a31b-fb3c-4857-b382-bf948e351f24)


The second breakage origin with a little less than 5000 breakage occurrences is 'DC'. Just as 'finished edgers' it also contains the highest reason overall 'defective lens front'. Furthermore, similar to 'finished edgers' this is by far the highest reason (close to 2500) compared to the other reasons for breakages coming from 'DC' 

![image](https://github.com/ojimenez24/Breakage2022/assets/123837381/4e488c53-1784-483e-b67c-111ca6387ef8)

In third place with just under 2000 breakage occurrences, we have 'poly coater' and the highest reason by far is 'pits'. Interestingly enough this is the 3rd biggest breakage reason overall.

![image](https://github.com/ojimenez24/Breakage2022/assets/123837381/6dd6cf30-d5f5-4e19-98fa-771ded5fd6f7)

In fourth place, closely following 'poly coater' we have 'ORBIT GEN' with less than 2000 breakage occurrences. The biggest breakage reason here is 'file hole wrong dir' with around 550 occurrences

![image](https://github.com/ojimenez24/Breakage2022/assets/123837381/1fa172c9-0a23-496c-9de5-4aa31bd22eae)

In fifth place, we have an 'A/R lab' with a breakage count of around 1500. The biggest breakage reason here is the 'poor coating issue'

**Time Statistics**

After analyzing every significant breakage origin closely, we can move into the time and frequency the breakages happen to have a broader view and look for clues or patterns regarding the time of the year and monthly and daily breakage volume.

![image](https://github.com/ojimenez24/Breakage2022/assets/123837381/187d17c4-ee01-43d1-9a44-e3969f32b9ad)

Looking at the graph above, we can see how breakage occurrences are the highest in August with over 1750 breakages and are closely followed by March with a breakage count of over 1750 as well.

Now, let's examine the same data in a linear way to see the changes more clearly.

![image](https://github.com/ojimenez24/Breakage2022/assets/123837381/24aa7fb3-4952-4ed0-bf7a-2e88c88363c0)

By observing the graph above, we can tell that there seems to be a downward trend meaning that the volume of breakages is decreasing in general, if we use a line plot we can confirm this.

![image](https://github.com/ojimenez24/Breakage2022/assets/123837381/46860aa6-3be9-401e-9dd0-94730e699930)


The plot above clearly shows a downward trend and also the outliers throughout the year.

Now let's take a look at the top breakage origin and the 3 biggest breakage reasons and their occurrences throughout the year

![image](https://github.com/ojimenez24/Breakage2022/assets/123837381/8fcdf915-0bde-44db-adad-5707c361b813)


![image](https://github.com/ojimenez24/Breakage2022/assets/123837381/89b00309-d8cb-4408-9dc2-b082d82db885)


![image](https://github.com/ojimenez24/Breakage2022/assets/123837381/63dbf4a4-f4ac-4bba-aeb8-8d68f69aab4b)


![image](https://github.com/ojimenez24/Breakage2022/assets/123837381/7502ad95-a381-475e-be26-a2d7dfd50dc2)

As we can see, the occurrences differ from reason to reason and there is not a specific time of the year when breakage occurrences happen the most.

Finally, as a bonus let's plot the volume of breakages from each weekday for each month using a heatmap.

![image](https://github.com/ojimenez24/Breakage2022/assets/123837381/900b7eaa-79a9-4537-aa59-1027a0e53d48)

It's interesting to see that the highest amount of breakages per day per month happened on Wednesdays in August. However, it is not very surprising to see this because as we saw earlier, the month with the most breakages is August.

### Usage
For the entire process and a detailed description of each step, use [nbviewer](https://nbviewer.org/github/ojimenez24/Breakage2022/blob/main/Data%20Science%20Project%20-%20Breakages%20EA.ipynb)

Anybody can use this project as they see fit as long as it is liked to this repository; there is no need to ask for permission.

[Back to top](#breakage-analysis)
