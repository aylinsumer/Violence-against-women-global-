Violence Against Women (Global)
========================================================
author: Gemittarius
date: 21.06.2021
autosize: true
font-family: 'Adobe Hebrew Bold Italic' 
transition: zoom

Team Members
========================================================



- Aylin Sumer 090160324

- Tugrulgazi Avat 090160344


Violence...
========================================================

  Violence against women is a problem that should be perceived not only locally but also globally. 
 
  The UN describes violence against women and girls (VAWG) as: 
 
  "One of the most widespread, persistent, and devastating human rights violations in our world today. It remains largely unreported due to the impunity, silence, stigma, and shame surrounding it."
 
 
Our Data
========================================================

  The data was taken from a survey of men and women in African, Asian, and South American countries, exploring the attitudes and perceived justifications given for committing acts of violence against women.
 
What will be done?
========================================================

  In this research both subjects and the objects of the violence are included. 
  
  The data also explores different sociodemographic groups that the respondents belong to, including: Education Level, Marital status, Employment, and Age group. 
  
  The data reveals insights into some of the attitudes and assumptions that prevent progress in the global campaign to end violence against women and girls, based on a representative sample of each country.
  
Goals
========================================================
   
  Our main purpose is to show that violence against women and girls is never acceptable or justifiable by demonstrating both numerical and categorical variables. 
  
  We will be analyzing the percentages of people surveyed in the relevant group who agree with the question.


Let's Get Started!
======================================================== 

  

First of all, We need to see our data. Let us see our main columns:


```
[1] "RecordID"              "Country"               "Gender"               
[4] "Demographics.Question" "Demographics.Response" "Question"             
[7] "Survey.Year"           "Value"                
```


Continue 1 
======================================================== 
title: False

  Our data has a column named as Demographics.Question which gives us the 5 cases that we are going to analyze in the future. 
  Look at the Demographics.Question "Age".


```
  RecordID     Country Gender Demographics.Question Demographics.Response
1        1 Afghanistan      F                   Age                 15-24
2        1 Afghanistan      F                   Age                 25-34
3        1 Afghanistan      F                   Age                 35-49
4        1 Afghanistan      M                   Age                 25-34
5        1 Afghanistan      M                   Age                 35-49
6        1 Afghanistan      M                   Age                 15-24
7      351 Afghanistan      F                   Age                 15-24
8      351 Afghanistan      F                   Age                 25-34
                              Question Survey.Year Value
1            ... if she burns the food  01/01/2015  17.3
2            ... if she burns the food  01/01/2015  18.2
3            ... if she burns the food  01/01/2015  18.8
4            ... if she burns the food  01/01/2015   8.2
5            ... if she burns the food  01/01/2015   8.6
6            ... if she burns the food  01/01/2015   9.4
7 ... for at least one specific reason  01/01/2015  80.1
8 ... for at least one specific reason  01/01/2015  81.5
```


Continue 2 
======================================================== 
title: False


  We can see that age is repeating itself by the change in the response of our basic question.
  
  Our Age interval is below.
  
  

```
  Demographics.Response   n
1                 15-24 840
2                 25-34 840
3                 35-49 840
```


Continue 3 
======================================================== 
title: False

  And our Questions are;


```
                                 Question    n
1    ... for at least one specific reason 2100
2              ... if she argues with him 2100
3               ... if she burns the food 2100
4 ... if she goes out without telling him 2100
5        ... if she neglects the children 2100
6 ... if she refuses to have sex with him 2100
```


Continue 4 
======================================================== 
title: False

  So, we see that we have exactly 6 different answer, and 3 different age group.
  
  Let us see how many different demographics question we have.


```
  Demographics.Question    n
1                   Age 2520
2             Education 3360
3            Employment 2520
4        Marital status 2520
5             Residence 1680
```

Countries We are Working With
======================================================== 


```
 [1] "Afghanistan"               "Albania"                  
 [3] "Angola"                    "Armenia"                  
 [5] "Azerbaijan"                "Bangladesh"               
 [7] "Benin"                     "Bolivia"                  
 [9] "Burkina Faso"              "Burundi"                  
[11] "Cambodia"                  "Cameroon"                 
[13] "Chad"                      "Colombia"                 
[15] "Comoros"                   "Congo"                    
[17] "Congo Democratic Republic" "Cote d'Ivoire"            
[19] "Dominican Republic"        "Egypt"                    
[21] "Eritrea"                   "Eswatini"                 
[23] "Ethiopia"                  "Gabon"                    
[25] "Gambia"                    "Ghana"                    
[27] "Guatemala"                 "Guinea"                   
[29] "Guyana"                    "Haiti"                    
[31] "Honduras"                  "India"                    
[33] "Indonesia"                
```
 
Countries We are Working With
======================================================== 


```
 [1] "Liberia"               "Madagascar"            "Malawi"               
 [4] "Maldives"              "Mali"                  "Moldova"              
 [7] "Morocco"               "Mozambique"            "Myanmar"              
[10] "Namibia"               "Nepal"                 "Nicaragua"            
[13] "Niger"                 "Nigeria"               "Pakistan"             
[16] "Peru"                  "Philippines"           "Rwanda"               
[19] "Sao Tome and Principe" "Senegal"               "Sierra Leone"         
[22] "South Africa"          "Tajikistan"            "Tanzania"             
[25] "Timor-Leste"           "Togo"                  "Turkey"               
[28] "Turkmenistan"          "Uganda"                "Ukraine"              
[31] "Yemen"                 "Zambia"                "Zimbabwe"             
```


Split Data 
======================================================== 

  First and most important thing is that we need to make a gender study upon this data. So, We need to split our data into 2, such as the person who answered is female nor male.

  Female data;
  

```
  RecordID     Country Gender Demographics.Question
1        1 Afghanistan      F        Marital status
2        1 Afghanistan      F             Education
3        1 Afghanistan      F             Education
4        1 Afghanistan      F             Education
5        1 Afghanistan      F        Marital status
6        1 Afghanistan      F            Employment
         Demographics.Response                  Question Survey.Year Value
1                Never married ... if she burns the food  01/01/2015    NA
2                       Higher ... if she burns the food  01/01/2015  10.1
3                    Secondary ... if she burns the food  01/01/2015  13.7
4                      Primary ... if she burns the food  01/01/2015  13.8
5 Widowed, divorced, separated ... if she burns the food  01/01/2015  13.8
6            Employed for kind ... if she burns the food  01/01/2015  17.0
```

Split Data 
======================================================== 
  
  Male data;
  

```
  RecordID     Country Gender Demographics.Question
1        1 Afghanistan      M        Marital status
2        1 Afghanistan      M             Education
3        1 Afghanistan      M             Residence
4        1 Afghanistan      M            Employment
5        1 Afghanistan      M             Education
6        1 Afghanistan      M        Marital status
         Demographics.Response                  Question Survey.Year Value
1                Never married ... if she burns the food  01/01/2015    NA
2                       Higher ... if she burns the food  01/01/2015   4.5
3                        Urban ... if she burns the food  01/01/2015   4.6
4                   Unemployed ... if she burns the food  01/01/2015   5.2
5                      Primary ... if she burns the food  01/01/2015   6.3
6 Widowed, divorced, separated ... if she burns the food  01/01/2015   6.3
```

  We have 5 different case, so we may actually divide our data through demographics questions.
  
  
For  Male and Female Participants
======================================================== 
    
      
      
Female | Age            
Female | Education      
Female | Employment     
Female | Marital Status  
Female | Residence     
    
  ***  
  
Male | Age  
Male | Education  
Male | Employment  
Male | Marital Status  
Male | Residence  




















  
What Does the Value Column Mean?
======================================================== 
  
  Value column make us understand  that the % of people surveyed in the relevant group who agree with the question. 
  
  (e.g. the percentage of women aged 15-24 in Afghanistan who agree that a husband is justified in hitting or beating his wife if she burns the food)
  
  We know about our data that Congo Democratic Republic, Chad, Afghanistan are the three of the most valued countries.  

  And also Dominican Republic, Colombia, Peru are the three of the least valued countries. 
  
  Now on, we will discuss about the three most, the three least and Turkey graphs.
  
Female Participants - Age
======================================================== 
![plot of chunk unnamed-chunk-21](project_presentation_Gemittarius-figure/unnamed-chunk-21-1.png)
***
![plot of chunk unnamed-chunk-22](project_presentation_Gemittarius-figure/unnamed-chunk-22-1.png)
Female Participants - Age 2
======================================================== 
title: False
![plot of chunk unnamed-chunk-23](project_presentation_Gemittarius-figure/unnamed-chunk-23-1.png)
***
![plot of chunk unnamed-chunk-24](project_presentation_Gemittarius-figure/unnamed-chunk-24-1.png)
Female Participants - Age 3
======================================================== 
title: False
![plot of chunk unnamed-chunk-25](project_presentation_Gemittarius-figure/unnamed-chunk-25-1.png)
***
![plot of chunk unnamed-chunk-26](project_presentation_Gemittarius-figure/unnamed-chunk-26-1.png)
Female Participants - Age 4
======================================================== 
title: False

  First of all, there are really great number of women that justify the violence, for at least one specific reason in those countries...

  You may think that 15-24 ages are the one, valued the least, but some countries that is not the case, for example Uganda, Zimbabwe, in female participants.

Female Participants - Education
======================================================== 

![plot of chunk unnamed-chunk-27](project_presentation_Gemittarius-figure/unnamed-chunk-27-1.png)
***
![plot of chunk unnamed-chunk-28](project_presentation_Gemittarius-figure/unnamed-chunk-28-1.png)
Female Participants - Education 2
======================================================== 
title: False
![plot of chunk unnamed-chunk-29](project_presentation_Gemittarius-figure/unnamed-chunk-29-1.png)
***
![plot of chunk unnamed-chunk-30](project_presentation_Gemittarius-figure/unnamed-chunk-30-1.png)

Female Participants - Education 3
======================================================== 
title: False
![plot of chunk unnamed-chunk-31](project_presentation_Gemittarius-figure/unnamed-chunk-31-1.png)
***
![plot of chunk unnamed-chunk-32](project_presentation_Gemittarius-figure/unnamed-chunk-32-1.png)

Female Participants - Education 4
======================================================== 
title: False
  For Female participants, higher education makes the lowest violence fans. 
  
  But still, some countries have the smallest different at the values such as Timor-Leste and Chad. 
  
  Even they have higher education, still they think about justifying the violence. 
  
  For some countries education make almost no difference in the acceptability of violence.


Female Participants - Employment
======================================================== 
![plot of chunk unnamed-chunk-33](project_presentation_Gemittarius-figure/unnamed-chunk-33-1.png)
***
![plot of chunk unnamed-chunk-34](project_presentation_Gemittarius-figure/unnamed-chunk-34-1.png)
Female Participants - Employment 2
======================================================== 
title: False
![plot of chunk unnamed-chunk-35](project_presentation_Gemittarius-figure/unnamed-chunk-35-1.png)
***
![plot of chunk unnamed-chunk-36](project_presentation_Gemittarius-figure/unnamed-chunk-36-1.png)

Female Participants - Employment 3
======================================================== 
title: False
![plot of chunk unnamed-chunk-37](project_presentation_Gemittarius-figure/unnamed-chunk-37-1.png)
***
![plot of chunk unnamed-chunk-38](project_presentation_Gemittarius-figure/unnamed-chunk-38-1.png)

Female Participants - Employment 4
======================================================== 
title: False

  Employed for kind and unemployed participants mostly have close opinion about the violence, but mostly participants that employed for kind are the most violent sympathizers. 


Female Participants - Marital Status
======================================================== 

![plot of chunk unnamed-chunk-39](project_presentation_Gemittarius-figure/unnamed-chunk-39-1.png)
***
![plot of chunk unnamed-chunk-40](project_presentation_Gemittarius-figure/unnamed-chunk-40-1.png)

Female Participants - Marital Status 2
======================================================== 
title: False
![plot of chunk unnamed-chunk-41](project_presentation_Gemittarius-figure/unnamed-chunk-41-1.png)
***
![plot of chunk unnamed-chunk-42](project_presentation_Gemittarius-figure/unnamed-chunk-42-1.png)


Female Participants - Marital Status 3
======================================================== 
title: False
![plot of chunk unnamed-chunk-43](project_presentation_Gemittarius-figure/unnamed-chunk-43-1.png)
***
![plot of chunk unnamed-chunk-44](project_presentation_Gemittarius-figure/unnamed-chunk-44-1.png)

Female Participants - Marital Status 4
======================================================== 
title: False

  For female participants, Malawi, Maldives, Madagaskar, Lesotho, Eswatini, Comoros have the most violence fans in the never been married women. Doesn't it crazy? 
  
  Afghanistan and Pakistan have no information about the never married participants' thoughts. 

  Also that, Burundi, Nabia, Rwanda, Philiphines have the most violent divorced/widow women population. And Turkey has a tie with married/living together part of the women vs. divorced/widow women. It sounds about right.

Female Participants - Residence
======================================================== 
![plot of chunk unnamed-chunk-45](project_presentation_Gemittarius-figure/unnamed-chunk-45-1.png)
***
![plot of chunk unnamed-chunk-46](project_presentation_Gemittarius-figure/unnamed-chunk-46-1.png)

Female Participants - Residence 2
======================================================== 
title:False
![plot of chunk unnamed-chunk-47](project_presentation_Gemittarius-figure/unnamed-chunk-47-1.png)
***
![plot of chunk unnamed-chunk-48](project_presentation_Gemittarius-figure/unnamed-chunk-48-1.png)


Female Participants - Residence 3
======================================================== 
title: False
![plot of chunk unnamed-chunk-49](project_presentation_Gemittarius-figure/unnamed-chunk-49-1.png)
***
![plot of chunk unnamed-chunk-50](project_presentation_Gemittarius-figure/unnamed-chunk-50-1.png)
  
Female Participants - Residence 4
======================================================== 
title: False

  For female participants, always urban residences have the least violence thoughts than the rural residences.

  Well, it looks more normal than our other split data. 
  
Male Participants
======================================================== 
  We see in our data that Turkey, Turkmenistan, Yemen, Tajikistan,Peru, Philippines, Nicaragua, Morocco, Eritrea, Egypt and Bolivia has no information(NA values).
  
  There is no specific information in the data dictionary, whether male participants were not asked those questions or they did not answer.
  
  Because of that, We can not use the male participants in Turkey. We will continue in Turkey with female participants.

  Congo Democratic Republic, Chad, Afghanistan are still the three of the most valued countries.

  And also Dominican Republic, , Colombia, Guatemala (In female data there was Peru) are the three of the least valued countries.

  Now on, we will discuss about the three most, the three least and Turkey graphs.

Male Participants - Age
======================================================== 

![plot of chunk unnamed-chunk-51](project_presentation_Gemittarius-figure/unnamed-chunk-51-1.png)
***
![plot of chunk unnamed-chunk-52](project_presentation_Gemittarius-figure/unnamed-chunk-52-1.png)

Male Participants - Age 2
======================================================== 
title:False
![plot of chunk unnamed-chunk-53](project_presentation_Gemittarius-figure/unnamed-chunk-53-1.png)
***
![plot of chunk unnamed-chunk-54](project_presentation_Gemittarius-figure/unnamed-chunk-54-1.png)


Male Participants - Age 3
======================================================== 
title: False
![plot of chunk unnamed-chunk-55](project_presentation_Gemittarius-figure/unnamed-chunk-55-1.png)
***
![plot of chunk unnamed-chunk-56](project_presentation_Gemittarius-figure/unnamed-chunk-56-1.png)

Male Participants - Age 4
======================================================== 
title: False

  If you look at the male participants, you will see that most of the countries have higher violence value in the age 15-24, so  here, we can say the exceptions; Ukraine, Albania and Kyrgyz Republic. 

  Doesn't it sound so wrong?

Male Participants - Education
======================================================== 

![plot of chunk unnamed-chunk-57](project_presentation_Gemittarius-figure/unnamed-chunk-57-1.png)
![plot of chunk unnamed-chunk-58](project_presentation_Gemittarius-figure/unnamed-chunk-58-1.png)

Male Participants - Education 2
======================================================== 
title:False
![plot of chunk unnamed-chunk-59](project_presentation_Gemittarius-figure/unnamed-chunk-59-1.png)
***
![plot of chunk unnamed-chunk-60](project_presentation_Gemittarius-figure/unnamed-chunk-60-1.png)


Male Participants - Education 3
======================================================== 
title:False
![plot of chunk unnamed-chunk-61](project_presentation_Gemittarius-figure/unnamed-chunk-61-1.png)
***
![plot of chunk unnamed-chunk-62](project_presentation_Gemittarius-figure/unnamed-chunk-62-1.png)


Male Participants - Education 4
======================================================== 
title:False

  For Male participants, for Azerbaijan, Kyrgyz Republic, Ukraine and Moldova, there exist only the participants with higher and secondary educations. 
  
  We may see that participants from Timor-Leste and Kyrgyz Republic are more violent in higher education. Also Ukraine and Azerbaijan have the smallest difference between higher educated participants and non educated ones. 
  
  Did your brain just blow up? Well, education has no impact of some people...

Male Participants - Employment
======================================================== 
![plot of chunk unnamed-chunk-63](project_presentation_Gemittarius-figure/unnamed-chunk-63-1.png)
***
![plot of chunk unnamed-chunk-64](project_presentation_Gemittarius-figure/unnamed-chunk-64-1.png)

Male Participants - Employment 2
======================================================== 
title: False
![plot of chunk unnamed-chunk-65](project_presentation_Gemittarius-figure/unnamed-chunk-65-1.png)
***
![plot of chunk unnamed-chunk-66](project_presentation_Gemittarius-figure/unnamed-chunk-66-1.png)


Male Participants - Employment 3
======================================================== 
title:False
![plot of chunk unnamed-chunk-67](project_presentation_Gemittarius-figure/unnamed-chunk-67-1.png)
***
![plot of chunk unnamed-chunk-68](project_presentation_Gemittarius-figure/unnamed-chunk-68-1.png)


Male Participants - Employment 4
======================================================== 
title:False

  For male participants,except for Kyrgyz Republic, Timor-Leste and Azerbaijan participants who employed for kind justify violence the most. 

  But in Kyrgyz Republic, Timor-Leste and Azerbaijan, employed for cash participants justify the most. Also for Dominican Republic, there is no data for employed people.

  What should we understand from here? 

  Something like, even though they are employed they found a reason to show violence,and the unemployed ones think that they already have a reason to be violent. 

Male Participants - Marital Status
======================================================== 
![plot of chunk unnamed-chunk-69](project_presentation_Gemittarius-figure/unnamed-chunk-69-1.png)
***
![plot of chunk unnamed-chunk-70](project_presentation_Gemittarius-figure/unnamed-chunk-70-1.png)

Male Participants - Marital Status 2
======================================================== 
title:False
![plot of chunk unnamed-chunk-71](project_presentation_Gemittarius-figure/unnamed-chunk-71-1.png)
***
![plot of chunk unnamed-chunk-72](project_presentation_Gemittarius-figure/unnamed-chunk-72-1.png)

Male Participants - Marital Status 3
======================================================== 
title: False
![plot of chunk unnamed-chunk-73](project_presentation_Gemittarius-figure/unnamed-chunk-73-1.png)
***
![plot of chunk unnamed-chunk-74](project_presentation_Gemittarius-figure/unnamed-chunk-74-1.png)

Male Participants - Marital Status 4
======================================================== 
title: False

  For male participants, Comoros, Azerbaijan, Benin, Eswatini, Zambia, Zimbabwe  have the most violent thoughts in the never married men...

  Even though Dominican Republic has the lowest values in the survey, never married men in this country justify violence more then married and divorced/widow men.
  
  Have you ever noticied that the thoughts of women and men in the same countries have almost the same graphs with close values?
  
  Just think about that...



Male Participants - Residence
======================================================== 

![plot of chunk unnamed-chunk-75](project_presentation_Gemittarius-figure/unnamed-chunk-75-1.png)
***
![plot of chunk unnamed-chunk-76](project_presentation_Gemittarius-figure/unnamed-chunk-76-1.png)

Male Participants - Residence 2
======================================================== 
title:False
![plot of chunk unnamed-chunk-77](project_presentation_Gemittarius-figure/unnamed-chunk-77-1.png)
***
![plot of chunk unnamed-chunk-78](project_presentation_Gemittarius-figure/unnamed-chunk-78-1.png)


Male Participants - Residence 3
======================================================== 
title:False
![plot of chunk unnamed-chunk-79](project_presentation_Gemittarius-figure/unnamed-chunk-79-1.png)
***
![plot of chunk unnamed-chunk-80](project_presentation_Gemittarius-figure/unnamed-chunk-80-1.png)

Take A Deep Breath Now.
======================================================== 

  If you look close enough, you can see that all informations are connected, in urban, there are more people with education, more employments, age intervals mostly around 20-40 and so on. 
  
  If you look at one country at a time, you may see the relationships better. So let's try with Turkey.

  Lets look at our Turkey data.


Female Participants - Turkey -Age/Education
======================================================== 
![plot of chunk unnamed-chunk-81](project_presentation_Gemittarius-figure/unnamed-chunk-81-1.png)
***
![plot of chunk unnamed-chunk-82](project_presentation_Gemittarius-figure/unnamed-chunk-82-1.png)

Female Participants - Turkey - Age/Education 2
======================================================== 
title:False
If we examine the Turkey data, some deductions may be done (Even though male datas are lacking).

Ages:

- In 2013, over 15% of women between the ages of 35 and 49 and over 10% of women between the ages of 15 and 24 justifies the violence for at least one specific reason.
- In every question, elder women have the highest values.

Education:

- Let's only focus on "no education" and "primary" to see the importance of having an education. In every category, values of females who have no education doubles the values of females who have at least primary education.
- Also it is obvious that the higher education status a women have, the less her probability of justifying the action of violence.


Female Participants - Turkey -Employement/Marital Status
======================================================== 
![plot of chunk unnamed-chunk-83](project_presentation_Gemittarius-figure/unnamed-chunk-83-1.png)
***
![plot of chunk unnamed-chunk-84](project_presentation_Gemittarius-figure/unnamed-chunk-84-1.png)


Female Participants - Turkey -Employment/Marital Status 2
======================================================== 
title:False 

Marital Status:

- It is interesting to see that women married or living together and women widowed/divorced/separated have the similar percentages in most of the questions. However, women who never married are less tolerated when it comes to violence against them. Whether it is love or hate, it is a FAMILY which is easy to mess up but hard to form.(?)

Female Participants - Turkey - Residence
======================================================== 
![plot of chunk unnamed-chunk-85](project_presentation_Gemittarius-figure/unnamed-chunk-85-1.png)

Female Participants - Turkey - Residence 2
======================================================== 
title:False

Residence:

- Similar to the education part, women living in rural areas are two times more likely to accept the violence comparing to the women living in urban areas.

Those were concluded from datas of females. Since we have no male datas, we would want you to imagine the missing values of males by looking at those;


Turkey
======================================================== 
title: False

- Femicides, which mean the gender-based murder of a woman by a man, had increased by 1400 percent from 2002 to 2009 and that while 66 women were killed in 2002, this number reached 953 in the first 7 months of 2009. [See link](https://www.ntv.com.tr/yasam/kadin-cinayetleri-yuzde-1400-artis-gosterdi,8aPXnckeN0aWmKBDjlezJw)

Turkey 2
======================================================== 
title: False

- If we consider the year 2018, it is worse than 2020. 440 women were killed and 317 women were subjected to sexual violence.

![plot of chunk unnamed-chunk-86](project_presentation_Gemittarius-figure/unnamed-chunk-86-1.png)
***
![plot of chunk unnamed-chunk-87](project_presentation_Gemittarius-figure/unnamed-chunk-87-1.png)

Turkey 2
======================================================== 
title: False

![plot of chunk unnamed-chunk-88](project_presentation_Gemittarius-figure/unnamed-chunk-88-1.png)
***
There is a very serious increase in the number of suspicious female deaths presented as suicide or natural death and the number of women who are found dead suspiciously with the pandemic process. It is necessary to reveal whether women were killed, whether they were killed by accident, whether women were killed on the basis of gender (whether it was femicide), whether they committed suicide or were driven to suicide.


References
======================================================== 

[Survey](https://data.world/login?next=%2Fmakeovermonday%2F2020w10%2Fworkspace%2Ffile%3Ffilename%3D20200306%2BData%2BInternational%2BWomen%2527s%2BDay%2BViz5%2BLaunch.csv)

[NTV Yaşam - Kadın Cinayetleri](https://www.ntv.com.tr/yasam/kadin-cinayetleri-yuzde-1400-artis-gosterdi,8aPXnckeN0aWmKBDjlezJw)

[Kadın Cinayetlerini Durduracağız Platformu](http://kadincinayetlerinidurduracagiz.net/veriler/2947/kadin-cinayetlerini-durduracagiz-platformu-2020-raporu)
