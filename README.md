# INTRODUCTION 

The foundation of insightful data analysis lies in working with clean data. Messy or disorganized data can potentially lead to inaccurate conclusions, resulting in significant financial losses for companies.

Aspiring data analysts must recognize the vital importance of mastering various methods and techniques for data cleaning. While data cleaning can be time-consuming, consistent practice is the path to achieving proficiency in this critical skill.

This article presents a step-by-step guide to cleaning untidy data extracted from a random Twitter account (X). The tool employed for this data cleaning process is the Power Query Editor within Power BI.

# THE DATASET

The dataset was received in the form of a CSV file and comprises 9 columns with a total of 42 rows. It consists of weightlifting records for three athletes, with their data listed one below the other, as illustrated in the image below.

![Screenshot (435)](https://github.com/dannieRope/DO-YOU-EVEN-LIFT---DATA-CLEANING-PROJECT/assets/132214828/f4585a52-792d-4b70-ac65-51c4a8b7dbb0)

At first glance, the data may appear acceptable, but upon closer examination, it becomes evident that it is not. Performing data analysis on this dataset could pose significant challenges.

We must restructure the dataset by stacking the records of the three athletes together. This restructuring should include their full names and the corresponding session and recording dates.

# THE CLEANING PROCESS

This process begins with the importation of the dataset into the Power Query Editor. To accomplish this, navigate to the Data tab, select "Get Data," click on "From File," and then opt for "From Excel Workbook".

Locate the dataset file at your chosen location.

The Navigator window will appear. Select the worksheet that contains the data, and then click "Transform" at the bottom to import the data into the Power Query Editor.

The image illustrates the appearance of the data when imported into Power Query.

![Screenshot (426)](https://github.com/dannieRope/DO-YOU-EVEN-LIFT---DATA-CLEANING-PROJECT/assets/132214828/086b768a-aea3-47a5-a6a1-0dc8c33eb9e0)

The next step involves splitting the first three columns. By using a colon (:)-based delimiter, we can extract both the first and last names of the athletes involved in the event by splitting the first and second columns.

Also, splitting the third column allows us to acquire the dates corresponding to each session recording.

To extract the first name, navigate to the first column labeled 'Column1.' In the Home tab, access the Split column feature in the transform ribbon. A drop-down menu will emerge; select 'delimiter' from the menu, opt for "colon" as the delimiter, and proceed by clicking 'OK.' 

![split column outcome](https://github.com/dannieRope/DO-YOU-EVEN-LIFT---DATA-CLEANING-PROJECT/assets/132214828/c65cf48e-5fc3-440e-97cf-396ef2e413c0)


Apply the same procedure to the second and third columns to extract the last name and date.

![Screenshot (431)](https://github.com/dannieRope/DO-YOU-EVEN-LIFT---DATA-CLEANING-PROJECT/assets/132214828/362e4401-206a-4028-8d8e-9187bdbb664e)


The next step involves populating the columns that hold the first name, last name, and date, utilizing the fill-down feature found in the transform tab. 

This action ensures that each row is filled with the corresponding name and date.

To do this, simultaneously select the three columns by holding down the 'Ctrl' key and clicking on each column.

Then, within the transform tab, click on the 'fill' option and select 'down' from the drop-down menu. This process ensures the dissemination of the name and date values throughout each row.

![Filldown](https://github.com/dannieRope/DO-YOU-EVEN-LIFT---DATA-CLEANING-PROJECT/assets/132214828/706df5f5-ea17-423d-b359-1c2624471b88)


![Fill down outcome](https://github.com/dannieRope/DO-YOU-EVEN-LIFT---DATA-CLEANING-PROJECT/assets/132214828/ed26ba36-ae61-4dfb-b476-46b9f93ff1b5)


Combine the columns containing the first and last names to obtain the full names of the participants. Select the two columns, then go to the transform tab and click on "merge column." Specify the separator; in this case, choose "space" as the separator.

![merge with space](https://github.com/dannieRope/DO-YOU-EVEN-LIFT---DATA-CLEANING-PROJECT/assets/132214828/ff6b184a-ab87-48c6-93c8-289cd3c21a9f)


![Screenshot (433)](https://github.com/dannieRope/DO-YOU-EVEN-LIFT---DATA-CLEANING-PROJECT/assets/132214828/c5023372-bba4-41f0-bb81-31440d9294b3)


Promote the first row as the header by clicking on "Use first Row as Headers" in the transform tab.

Finally, remove the first three rows, as they are not necessary for the analysis.

The next step involves filtering the session column to eliminate unnecessary rows. To accomplish this, click on the drop-down button on the session column, uncheck blank, first name, and session in the drop-down, and click 'OK'.

![Filter session column](https://github.com/dannieRope/DO-YOU-EVEN-LIFT---DATA-CLEANING-PROJECT/assets/132214828/58dc0428-f8c6-43a9-bebf-ddc2b22f2b1c)


After filtering, rename the column containing the names of the athletes as "Full Name" and the one containing the dates as "Date." Finally, remove the last two columns since they do not contain any values, thereby reducing redundancy.

![Screenshot (434)](https://github.com/dannieRope/DO-YOU-EVEN-LIFT---DATA-CLEANING-PROJECT/assets/132214828/8370bcf3-70be-4096-a01e-505dc3edaaf2)


There you have it, then. Now that the dataset has been cleaned, it is ready for further analysis.




