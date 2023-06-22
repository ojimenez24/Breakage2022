# Breakage analysis
## Table of contents

1. [Background](#background)
2. [Size and focus](#size-and-focus)
3. [Tools used](#tools-used)
4. [Findings](#findings)
5. [Usage](#usage)

### Background
This **exploratory data analysis** is about product loss or 'breakages' in a ophthalmic laboratory (my current place of work). It aims to investigate the major causes of breakages and their origins in 2022. The data used comes from a dataset located in the main server of the laboratory, which is updated daily with new information about breakage occurrences in the laboratory.


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

As we can see, 'finished edgers' is where most breakages have ocurred in 2022. 
This breakage origin is closely followed by 'DC' (distribution center)

Now let's take a look at the count of breakages per reason.

*since many of the reasons are redundant and displaying all 190 reasons would be impractical, I decided to set a threshold to show only reasons with a reason count higher than 10% of the highest reason count (around 200)

![image](https://github.com/ojimenez24/Breakage2022/assets/123837381/375c7038-0bdf-40fc-a63a-1dfb7ad284f3)

Now, let's look at each of the top breakage origins by categorizing them and digging more into the type of breakage they produce.



**Categorical Statistics**

![image](https://github.com/ojimenez24/Breakage2022/assets/123837381/dc0644f8-8e94-40a3-808f-7b11ea3c0800)

In first place with over 5000 overall breakages we have 'finished edgers'.It is not surprising to find that in 'finished edgers' the second biggest breakage reason "Scratch edging w/oAR" (over 2000) is found. Also this reason is by far the highest compared to the other breakage reasons in 'finished edgers'.

![image](https://github.com/ojimenez24/Breakage2022/assets/123837381/c382a31b-fb3c-4857-b382-bf948e351f24)


The second breakage origin with a little less than 5000 breakage ocurrences is 'DC'. Just as 'finished edgers' it also  contains the highest reason overall 'defective lens front'. Furthermore, similar to 'finished edgers' this is by far the highest reason (close to 2500) compared to the other reasons for breakages coming from 'DC' 

![image](https://github.com/ojimenez24/Breakage2022/assets/123837381/4e488c53-1784-483e-b67c-111ca6387ef8)

In third place with just under 2000 breakage ocurrences we have 'poly coater' and the highest reason by far is 'pits'. Interestngly enought this is the 3rd biggest breakage reason overall.

![image](https://github.com/ojimenez24/Breakage2022/assets/123837381/6dd6cf30-d5f5-4e19-98fa-771ded5fd6f7)

In fourth place, closely following 'poly coater' we have 'ORBIT GEN' with less than 2000 breakage ocurrences. The biggest breakage reason here is 'file hole wrong dir' with around 550 ocurrences

![image](https://user-images.githubusercontent.com/123837381/229902540-98222a81-d66f-4754-8b02-58661a551c45.png)

We have 'ORBIT GEN' (Generator) in the last category. Unlike all other machines, this machine is almost entirely automated and requires minimal human intervention (when functioning as it should). However, the way we troubleshoot problems in the machine is by configuring its settings or replacing external components (more intrusive troubleshooting would require a specialist due to the complexity of the machine). The top reasons are 'No Engraving' and 'GEN power off.' As mentioned, we can configure the setting to solve these problems or change the engraving tool. However, **setting up bimonthly or trimonthly specialist visits or getting personnel certified to troubleshoot the machine correctly** could reduce the number of breakages here.

**Time Statistics**

After analyzing every significant breakage origin closely, we can move into the time and frequency the breakages happen to have a broader view and look for clues or patterns regarding the time of the year and monthly and daily breakage volume.

![image](https://user-images.githubusercontent.com/123837381/230182980-01c58655-cb77-4248-9e00-dc1ee0c71006.png)

Looking at the graph above, we can see how breakage occurrences are the highest in January and part of February, which makes sense since these months are some of our busiest in the year. After this period, there was a dramatic drop in breakages, which reached its lowest point in May (2020 was when we halted almost all of our operations for two entire months, so it is unsurprising to see such a dramatic change).


![image](https://user-images.githubusercontent.com/123837381/230186500-7d70e827-cf38-4837-83f6-f372179fac46.png)

This linear plot shows that there are some outliers there.

Let's take a look at each significant breakage reason thorough the year.

![image](https://user-images.githubusercontent.com/123837381/230193999-f6dff9c4-6652-4c95-ad2e-1e9d086f5907.png)

![image](https://user-images.githubusercontent.com/123837381/230194077-58877012-f030-41d1-912d-c79c817a5726.png)

![image](https://user-images.githubusercontent.com/123837381/230194188-ff3fd37e-b766-473a-bf72-c4630eaa83d2.png)

![image](https://user-images.githubusercontent.com/123837381/230194253-07f04c00-a36a-4c4c-825d-eba4ebf2e83e.png)

As we can see, the quarantine period from the middle of March to the end of May is present in every plot above.

Now, let's downscale a bit, look at the day level, and see which days of the week generally have the most breakages.

![image](https://user-images.githubusercontent.com/123837381/230658279-21287987-dc55-4d2b-aadc-b2c65e76c57f.png)

While I do not know any specific reason for these daily results, this information is good to reference for future operations.

Finally, let's plot the volume of breakages from each weekday for each month using a heatmap.

![image](https://user-images.githubusercontent.com/123837381/230659394-5552add2-dc0b-4dab-8796-27bd6d7216f9.png)

It's interesting to see that the highest amount of breakages per day per month happened on Thursday, Friday, and Tuesday of January and February. However, it does for the busyness at the beginning of the year.





### Usage
For the entire process and a detailed description of each step, use [nbviewer](https://nbviewer.org/github/ojimenez24/Breakage-Analysis/blob/main/Data%20Science%20Project%20-%20Breakages%20EA.ipynb)

Anybody can use this project as they see fit as long as it is liked to this repository; there is no need to ask for permission.

[Back to top](#breakage-analysis)
