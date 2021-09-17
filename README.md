# Machine_Learnng_Project-DataDrivenCompitition


Pump it Up: Data Mining the Water Table


**Introduction: -**

There are 4 data sets such as submission format, training set, test set training label set . Training set has 59400 data with 40 features. Target variable has three possible outcomes.
*Functional
*Non-functional
*Functional but it needs to repair.

**Data Preprocessing: -**

The features which are similar with other features were dropped.
*management_group
*scheme_management
*quantity_group
*source_class
*source_type
*quality_group
*payment_type
*extraction_type_class
*extraction_type
*waterpoint_type_group

When considering the construction_year feature, there were many different values. Because of that, these values were arranged according to the decade. Before did that replace 0 with 1986 which was the median value. Since all the records were recorded by the same person that column was dropped

In installer column filled the missing values with “unknown” and corrected the spelling errors in the installer column. That means because of spelling errors the same installer was identified as the different installers. After that created a new column(installer_cat) considering the highest count of installers. The First 16 highest count installers were used as the same and others replaced as the “other”.
In funder column fill the missing values with “unknown” After that created a new column(funder_cat) considering the highest count of the funder. The first 19 highest count funders were used as the same and others were replace as the “other”.

Drop the colums which has the many difference values. So, dropped these columns.
*wpt_name
*scheme_name
*region_code
*amount_tsh
*num_private
*subvillage
*id

Filled the missing values in population column with its mean value (180) and also filled the missing values in permit and public_meeting columns.

When considering the recorded date column, calculated the number of dates from the recorded date to the final date and added a new column to the date set with these

Dropped the columns which are called funder, installer, construction_year , lga and ward. Finally used 20 columns to model training.
*days_since_recorded    
*gps_height             
*longitude              
*latitude               
*basin                  
*region                 
*district_code            
*population             
*public_meeting         
*permit                 
*extraction_type_group  
*management             
*payment                
*water_quality          
*quantity               
*source                 
*waterpoint_type        
*decade                 
*installer_cat          
*funder_cat  



I applied one hot encoding for these categorical features.
*funder_cat
*basin
*installer_cat
*public_meeting
*scheme_management
*permit
*extraction_type
*extraction_type_class
*management
*payment_type
*quality_group
*quantity
*source
*source_class
*waterpoint_type

**Accuracy: -**

	By dividing training data set into two parts calculate the accuracy of the used model.


**Modeling: -**

	I have been tried with different models like RandomForest , XGBoot, KNeighbors, DecisionTree.  RandomForest gave the best score.

**Highest score: -** 0.8166

**Rank: -** 1663






           



