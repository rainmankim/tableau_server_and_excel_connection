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
#### --> First publish offline Excel File onto Ray's Tableau Server. 
<img align="center" src="https://user-images.githubusercontent.com/62319355/106709772-f384e100-662f-11eb-86fe-ff3da276fe68.png" alt="publish sample excel">

#### --> Using custom matching, match necessary primary key(s). This time you notice both connections are on Ray's Tableau Server
<img align="center" src="https://user-images.githubusercontent.com/62319355/106712541-10231800-6634-11eb-842f-b9ff7665699f.png" alt="data blend">


1111111111111111111
22222222222222222222222
333333333333 444444444444 55555555555


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




🎈🦾 😎 That's it from me. Try not to alienate people!
--------------------------------------------------------------------------------------------------------------------------------------------------



## Credits
```
- Credits: Mohammed Shameel  (insanely smart and resourceful)
- Secular saints of Tableau Community
```

