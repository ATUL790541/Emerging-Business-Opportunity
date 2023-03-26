# Emerging-Business-Opportunity

The client (Manufacturer A) is a leading Food & Beverage manufacturer. Client wants to understand the growth patterns of consumer preferences (themes) and evaluate positioning of their brand across different themes. Client also wants to know the sales drivers of their products.

# Table of Content
  * [Abstract](#abstract)
  * [Data Description](#data-description)
  * [Project Outline](#project-outline)
    -  [Data Preparation](#data-wrangling)
    -  [Data exploration](#standardization)
    -  [Hypothesis Validation](#eda)
    -  [Build Sales Model](#text-pre-processing)
    -  [Identify Driver Of Sales](#encoding-categorical-values)
    -  [ Recommend levers for business growth](#feature-selection)
  
  * [Conclusion](#run)
  * [Reference](#reference)

# Abstract

Company will also provide a clear and detailed description of the dataset including all the fields present. Company will make available knowledgeable personnel to provide any necessary background on data and business context. These personnel will also help in working with the end consumers of our models and identifying which features could be actionable. They would also help in corroborating findings from the models and can help provide an insider’s business perspective.

# Data Description

Client will provide the following data for the project:
    
    ● Sales Data – At UPC level for both Client and Competitors
    ● Social Media Data– Mentions of theme across all Social       
    ● Google Search Data – Search volume of the Theme
    ● Theme_Product_List – Product to theme Mapping
    ● Product_Manufacturer_List – Product to Manufacturer Mapping
    ● Theme List – Theme Names

# Data Preparation
   ● Total unique themes available across all data sources
 
   ![Screenshot (412)](https://user-images.githubusercontent.com/75777816/227100184-cad93f9e-b103-434c-850c-050f04cccd2b.png)
   
   ● Understands consumer preference(themes) available in each data source
   
   |  GOOGLE SEARCH | SALES DATA  | SOCIAL MEDIA |
   |----|----|----|
   |![Picture1](https://user-images.githubusercontent.com/75777816/227101045-5a158e9a-376a-4e03-98d3-6d2244eca464.png)|![Picture2](https://user-images.githubusercontent.com/75777816/227101053-32772dee-da3f-4010-9a6c-74f9b8167321.png)|![Picture3](https://user-images.githubusercontent.com/75777816/227101068-03320015-0eaa-4426-8f68-03899ad662c7.png)|
  
  ● Provide a report for data sufficiency, sparsity and anomalies in each data source
  
  ![Screenshot (413)](https://user-images.githubusercontent.com/75777816/227102264-130e3f65-39cd-4f65-b827-2a86440262c9.png)

  ● Recommend the time granularity (Daily/Weekly/Monthly/Quarterly/Yearly) for the analysis
 |  2014 | 2015 | 2016 |
 |----|----|----|
 |![2014](https://user-images.githubusercontent.com/75777816/227103117-9d57fcc1-6e01-48e9-bbaa-7cdc9b7ca8e4.png)|![2015](https://user-images.githubusercontent.com/75777816/227103120-a5ef6895-4be5-4d5c-8818-2dcee0562570.png)|![2016](https://user-images.githubusercontent.com/75777816/227103122-7171f0dd-eed6-4417-aeca-ec2ce343f5ab.png)|
| 2017 | 2018 | 2019 |
|![2017](https://user-images.githubusercontent.com/75777816/227103126-6d38538d-9ff2-4d89-9c2e-c61bad5c0a6b.png)|![2018](https://user-images.githubusercontent.com/75777816/227103129-badee43f-7cc8-4fcf-ac18-217232509661.png)|![2019](https://user-images.githubusercontent.com/75777816/227103132-5e897435-74dd-444a-8cf7-0c3de54f58c4.png)|

# Data exploration
  ● Anamolies In Dataset 
   |  Google_search_data | Product_manufacturer_list | Sales_data |
   |----|----|----|
   |![google](https://user-images.githubusercontent.com/75777816/227104853-dfbf4b60-9aba-4919-9847-ed607f3c1b29.png)|![prod](https://user-images.githubusercontent.com/75777816/227104858-66f67a57-d13a-42d6-9ff9-bdd30159bac5.png)|![sales](https://user-images.githubusercontent.com/75777816/227104861-83dc7529-7cca-47be-ad13-da56e8ae0cda.png)|
   |  Social_media_data |  Theme_list | Theme_product_list |
   |![socail](https://user-images.githubusercontent.com/75777816/227105349-b08d6614-f1fa-45d0-847f-4ffbd762cfae.png)|![Theme](https://user-images.githubusercontent.com/75777816/227105351-967492df-e169-487e-968b-1e7bfa969314.png)|![theme_pdct](https://user-images.githubusercontent.com/75777816/227105356-1723acc5-9600-411c-a1bc-e870b7a849e8.png)|
   
  ● Understand the overall market share of our client

  ![m1](https://user-images.githubusercontent.com/75777816/227755081-2db3fecb-32b2-4adb-bd45-3f2f85a2cd62.png)
  ![m2](https://user-images.githubusercontent.com/75777816/227755085-793bd66c-f505-4430-ad7a-1c67ebfba81b.png)
  
  ● Find the potential competitors for our client in each theme
  |  American Gumbo | Low Carb | Ethical Packaging | Ginger Bread |
  |------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
  |![american](https://user-images.githubusercontent.com/75777816/227755600-739e779f-7017-45e3-966c-44336d79255f.png)|![anony](https://user-images.githubusercontent.com/75777816/227755603-5f0c6161-fc4d-4dc1-9b8b-acee703aa522.png)|![ethical](https://user-images.githubusercontent.com/75777816/227756191-37335726-21a8-4426-9a86-c75822ceb0ad.png)|![ginger](https://user-images.githubusercontent.com/75777816/227756192-87216b38-d17b-48b1-8ac7-ea018a4b925f.png)|
  
  ● What are the themes which are emerging in social media, Google Search & Sales
    ![emerge](https://user-images.githubusercontent.com/75777816/227756651-2175cc4a-3ab8-43ef-a687-bb7ede2b09e4.png)
  
  ● Hypothesis Validation and Latency Calculation
  |  Hypothesis Validation | Latency Calculation | 
  |--------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
  |![Screenshot (415)](https://user-images.githubusercontent.com/75777816/227757012-bf15b421-31c0-448f-a120-900bbd1f90f5.png)|![Screenshot (414)](https://user-images.githubusercontent.com/75777816/227757010-b88b39c5-acad-4d22-9973-178f7bc45105.png)|

# Build Sales Model
  ● Identify the right  model technique and select the suitable variables
  
  ![Screenshot (416)](https://user-images.githubusercontent.com/75777816/227760596-89017d75-c9c1-42a2-b5fe-aab10ec1e11d.png)
  
  ● Estimate the impact on sales due to social trends, search trends, own price and competitor effects
  
  ![Screenshot (417)](https://user-images.githubusercontent.com/75777816/227760597-b71bee18-b3e5-40a6-bc9b-34087ee438de.png)
  
# Identify Driver Of Sales
  
  ![Screenshot (418)](https://user-images.githubusercontent.com/75777816/227760761-8eb674eb-9359-4d2b-974f-02d807aebb6e.png)
 
# Recommend levers for business growth
 
  ![Screenshot (419)](https://user-images.githubusercontent.com/75777816/227760764-bd9956ef-a1ad-44e8-8433-adfba98c5967.png)


  
  

