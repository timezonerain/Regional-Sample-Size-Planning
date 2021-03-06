# Introduction to the Rshiny regional sample size planning tool
Licensed under the MPL-2.0 license.

### Multivation
In MRCTs we often face the need to plan sample size for different regions/countries.

With certain number of patients for a region, if there's reasonable probability (e.g.80%) that the desired proportion (e.g.50%) of overall treatment effect can be retained, and the treatment effect is positive, we can demonstrate that the sample size for that region is plausible from a statistical perspective. With desired criteria, we can in turn decide how many sample size we want to allocate to that region.

Note that the desired consistency probability and proportion to retain effect varie across regions/countries, studies, endpoints etc. The final decision should be based on not only statistical characteristics, but also regulatory requirements, operational feasibility etc. Please refer to ICH E5& E17 for other important factors to consider.

Note that changing the sample size of a region will not impact MRCT sample size, only the fraction of sample size allocating to that region changes.

<br/>

### Table of contents
- [Layout of the app](#layout)
- [Tutorial](#tutorial1)
  - [Step 1: Identify the endpoint of interest](#identify) 
  - [Step 2: Fill in required information](#fill-in1) 
  - [Step 3: Submit!](#submit)
  - [Step 4: View the output section](#output1) 
  - [Step 5: Download csv file](#download-csv) 
- [Tutorial (Time to event)](#tutorial2) 
  - [Fill in required information](#fill-in2) 
  - [Optional: Event and sample size calculation](#optional1) 
  - [Output table](#output2) 
- [Tutorial (Negative Binomial)](#tutorial3) 
  - [Fill in required information](#fill-in3) 
  - [Optional: Sample size calculation](#optional2) 
  - [Output table](#output3)  
- [Reference](#reference) 

<br/>

<h3 id="layout">Layout of the app</h3> 

- **Entering the tool**: 

![](image/layout1.PNG)


- **The "Normal Endpoints" tab**: Consists with a side pannel on the left which inputs are required and results section on the right.

![](image/layout2.PNG)

- **Layout of "Time-to-Event Endpoints" and "Negative Binomial Endpoints" are similar**

<br/>

<h3 id="tutorial1">Tutorial</h3> 

<h4 id="identify">Step 1: Identify the endpoint of interest</h4> 

- If you are planning the sample size based on difference of means endpoint, select the "Normal Endpoints" tab.

- For time-to-event endpoints such as survival, PFS, EFS etc. the "Time-to-Event Endpoints" tab should be selected.

- For negative binomial endpoints, e.g. the number of new lesions seen during a 6-month period, the "Negative Binomial Endpoints" tab should be selected.

The below steps will use normal endpoint for illustration.  

<h4 id="fill-in1">Step 2: Fill in required information</h4> 

- "Type 1 error", "Power" and "MRCT sample size" are needed for calculating the corresponding probabilities

<img src="image/tutnormal1.PNG" width="430">

- MRCT sample size calculation (optional): Input other parameters (in addition to type 1 error and power), which allows you to calculate the sample size if it's not ready by hand. The calculated sample size will be updated automatically in the "Trial Information" section.

<img src="image/tutnormal2.PNG" width="430">

- Check consistency critieria: Specify desired consistency probability with the proportion of global effect to be retained

<img src="image/tutnormal3.PNG" width="430">

<h4 id="submit">Step 3: Submit! </h4>

- After clicking the "Submit" button, it takes about 1-10 seconds for the table to appear.

![](image/tutnormal4.PNG)

<h4 id="output1">Step 4: View the output section</h4>

<img src="image/outnormal1.PNG">

- The sentence on top states the corresponding regional sample size when there's 80% chance 50% of the MRCT effect is retained.

![](image/outnormal2.PNG)

- The output table allows you to search specific ranges of interest for each column.

![](image/outnormal3.PNG)

- You can also sort colunmns ascendingly/descendingly, change the number of entries you want to display on one page etc.

![](image/outnormal4.PNG)

<h4 id="download-csv">Step 5: Download the csv</h4>

- The download section allows you to enter 6 regional sample size fractions (out of MRCT sample size) to download, the default fractions are 5%, 10%, 15%, 20%, 25% and the calculated fraction where 80% probability 50% of MRCT effect is retained.

<img src="image/outnormal5.PNG" width="700">

- The csv file will be downloaded directly to the default folder (normally download folder)

![](image/outnormal6.PNG)

- The table layout will be the same as the one in output section, with fractions of interest

<img src="image/outnormal7.PNG" width="700">


<br/>

<h3 id="tutorial2">Tutorial (Time-to-Event)</h3> 

<h4 id="fill-in2">Fill in required information</h4>

- Fill in 'Hazard ratio', 'Treatment:Control' (ratio), 'MRCT event size' and 'MRCT sample size' (optional: if empty, the output will only have regional event size information)

<img src="image/tutsurv1.PNG" width="430">

<h4 id="optional1">Optional: Event and sample size calculation</h4>

- If event size is not ready by hand, fill in type 1 error and power in addition to calculate
- Sample size can be calculated further by specifying the maturity of events at analysis
- Results will be automatically updated in the "Trial Information" section

<img src="image/tutsurv2.PNG" width="430">

- Check the consistency criteria

<img src="image/tutnormal4.PNG" width="430">

<h4 id="output2">Output section</h4>

- The output section is slightly different, including an additional column 'Regional event size' 

<img src="image/outsurv1.PNG">

The rest of the steps are the same.

<br/>

<h3 id="tutorial3">Tutorial (Negative Binomial)</h3> 

<h4 id="fill-in3">Fill in required information</h4>

<img src="image/tutnegbin1.PNG" width="430">

- Treatment group rate can also be calculated with Reference group rate and Rate ratio.

<img src="image/tutnegbin2.PNG" width="430">

<h4 id="optional1">Optional: Event and sample size calculation</h4>

- If sample size is not ready by hand, in addition to information in "Trial Information", fill in type 1 error, power, and choose the method to estimate variance under null hypothesis

- The sample size calculation reference is provided

- Results will be automatically updated in the "Trial Information" section

<img src="image/tutnegbin3.PNG" width="430">

- Check the consistency criteria

<img src="image/tutnormal4.PNG" width="430">

<h4 id="output3">Output section</h4>
<img src="image/outnegbin1.PNG">

The rest of the steps are the same.






<br/>
<h3 id="reference">References</h3> 

- Quan, H., Zhao, P. L., Zhang, J., Roessner, M., & Aizawa, K. (2010). Sample size considerations for Japanese patients in a multi‐regional trial based on MHLW guidance. Pharmaceutical Statistics, 9(2), 100-112.
- Hayashi, Nobuya & Itoh, Yohji. (2018). A Re-examination of Japanese Sample Size Calculation for Multi-regional Clinical Trial Evaluating Survival Endpoint. Japanese Journal of Biometrics. 38. 10.5691/jjb.38.79. 
- Zhu, H. and Lakkis, H. (2014), Sample size calculation for comparing two negative binomial rates. Statist. Med., 33: 376-387. doi:10.1002/sim.5947
- Packages used for building the app: 
  - httpuv
  - shiny
  - shinydashboard
  - shinyjs
  - DT
  - shinycssloaders

### End
Features including overall consistency probability, plotting and other common endpoints will be added in the future

 
