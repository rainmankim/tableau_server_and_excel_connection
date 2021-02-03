<img align="left" src="https://user-images.githubusercontent.com/62319355/105784986-d6f40380-5fb4-11eb-95e9-2261360d0120.jpg" width="220" height="80" alt="Tableau Server">
<img align="right" src="https://user-images.githubusercontent.com/62319355/106690730-48633000-660d-11eb-85b8-129753f1f931.png" width="150" alt="Excel logo">
:smile: :grinning: :sleepy: :relieved: :confused: :open_mouth: :astonished: :thumbsup:


## tableau_server_and_offline_excel_file_connection


```
Creator: Ray Kim Dong Hyun
Contact: rainmankim@gmail.com

* For easier understanding, I am going to call Tableau Server "Ray's Tableau Server".

In my other github repository, I have shown how you can connect Tableau Desktop with Cloudera Hadoop Server
for data source publishing & connection.

```
(https://github.com/rainmankim/tableau_server_cloudera_data_extraction)

```
Suppose you have main data source extract on Ray's Tableau Server which contains HR details about your colleagues.
Now, you come across a secret Excel file that containts list of your colleagues who happen to be aliens
You need to quickly match this Excel file with the data on Ray's Tableau Server to stop alien invasion.

Here are four data joining-blending options.  I am going to show Option 1 through Option 4 one by one.

- (Option 1) Directly JOIN  Main HR Data Extract on Ray's Tableau Server  &  Offline Excel File

- (Option 2) Directly blend Offline Excel File with HR Data Extract on Ray's Tableau Server

- (Option 3) First publish offline Excel File onto Ray's Tableau Server.   Then, blend main HR Data Extract on Ray's Tableau Server  & Alien Data on Ray's Tableau Server

- (Option 4)  First publish offline Excel File onto Ray's Tableau Server.   Then, join HR Data Extract on Ray's Tableau Server  & Alien Data on Ray's Tableau Server
```

### Option 1 Directly JOIN  Main HR Data Extract on Ray's Tableau Server  &  Offline Excel File
---> This is simply not allowed. You cannot join with a data table in Ray's Tableau SErver.

### Option 2 Directly blend Offline Excel File with HR Data Extract on Ray's Tableau Server
#### --> Connect to HR Data Extract on Ray's Tableau Server.    And  also connect to offline Excel file as a "NEW Data source"   
<img align="center" src="https://user-images.githubusercontent.com/62319355/106698186-456f3c00-661b-11eb-972d-10505f849150.png" alt="tableau_cloudera_connection image">

#### --> Next, go to "Edit Data Relationships" option as shown below                       
<img align="center" src="https://user-images.githubusercontent.com/62319355/106705361-c54fd300-6628-11eb-9bb3-1b7346f7e9a7.png" alt="tableau_cloudera_connection image">

#### --> Using custom matching, match necessary primary key(s)
<img align="center" src="https://user-images.githubusercontent.com/62319355/106706466-b5d18980-662a-11eb-81e0-e25e1a92ec05.png" alt="data blend">


### Option 3 First publish offline Excel File onto Ray's Tableau Server.   Then, blend main HR Data Extract on Ray's Tableau Server  & Alien Data on Ray's Tableau Server
<img align="center" src="https://user-images.githubusercontent.com/62319355/106709772-f384e100-662f-11eb-86fe-ff3da276fe68.png" alt="publish sample excel">


1111111111111111111
22222222222222222222222
333333333333


```
Option 1

JJCC Excel File  +  NTS Data on Server  (join)  ----> Fail

Option 2

JJCC Excel File  +  NTS Data on Server  (data blend)  ----> Works

Option 3

JJCC Excel file published on server    + NTS data on server   (then using data blend)

Benefit : Just need to update Excel data source onto Tableau Server (same file name &column name)  without touching Tableau workbook

Option 4??


```


### Step 1.  Let's open up Tableau Desktop and connect to Cloudera Hadoop with your credentials
<img align="center" src="https://user-images.githubusercontent.com/62319355/105792845-10337000-5fc3-11eb-9fd8-43d35e496f13.png" alt="tableau_cloudera_connection image">

### Step 2. Next, connect to Cloudera Table.  And I have written custom SQL query because the DB is too big(You can extract the DB as a whole)
<img align="center" src="https://user-images.githubusercontent.com/62319355/105798924-3d395000-5fce-11eb-99e2-7ab2811a9fd9.png" alt="tableau_cloudera_connection image">

### Step 3. Next, we shall now publish the databse onto "Ray's Tableau Server"
<img align="center" src="https://user-images.githubusercontent.com/62319355/105799297-29dab480-5fcf-11eb-878d-a751ae42211c.png" alt="tableau_cloudera_connection image">


### I recommend publishing this with "Embedded Password" setting with Live connection (because it often fails when you try to extract first)
#### If you choose "prompt user", it will ask for your password every single time. 
#### Alternatively, you can choose to publish as "prompt user" and you can still change to "Embedded Password" in "Ray's Tableau Server".
#### I will show you in step 4
<img align="center" src="https://user-images.githubusercontent.com/62319355/105804723-788e4b80-5fdb-11eb-89b2-135c378efbd0.png">


### Step 4A. Now let us go to "Ray's Tableau Server".  
#### Search for the published data soruce. 
#### If you had published as "Prompt User", you can change to "Embedded Password" authetification instead.
<img align="center" src="https://user-images.githubusercontent.com/62319355/105806935-e3418600-5fdf-11eb-9379-6b47a65da4e5.png" alt="tableau_edit_connection"


### Step 4B.  Change the data connection from LIVE to EXTRACT  (takes a while)
<img align="center" src="https://user-images.githubusercontent.com/62319355/105820676-d4b19980-5ff4-11eb-9b60-ce1b78c4d3dc.png" alt="Live to extract">

#### Once you click "Extract", "Ray's Tableau Server" will start to extract from Cloudera Database.
<img align="center" src="https://user-images.githubusercontent.com/62319355/105821234-910b5f80-5ff5-11eb-912c-8cfb388d7023.png" alt="Live to extract">




🎈🦾 😎 That's it from me. Try not to alienate people!
--------------------------------------------------------------------------------------------------------------------------------------------------



## Credits
```
- Credits: Mohammed Shameel  (insanely smart and resourceful)
- Secular saints of Tableau Community
```

