<img align="left" src="https://user-images.githubusercontent.com/62319355/105784986-d6f40380-5fb4-11eb-95e9-2261360d0120.jpg" width="220" height="80" alt="Tableau Server">
<img align="right" src="https://user-images.githubusercontent.com/62319355/105791113-6eab1f00-5fc0-11eb-938c-58db40f72c20.png" width="150" height="80" alt="Cloudera logo">
:smile: :grinning: :sleepy: :relieved: :confused: :open_mouth: :astonished: :thumbsup:


# tableau_server_and_offline_excel_file_connection


```
Creator: Ray Kim Dong Hyun
Contact: rainmankim@gmail.com

* For easier understanding, I am going to call Tableau Server "Ray's Tableau Server".

In my other github repository, I have shown how you can connect Tableau Desktop with Cloudera Hadoop Server  for data source publishing & connection.
(https://github.com/rainmankim/tableau_server_cloudera_data_extraction)

<http://www.example.com>
In this reposito




This repository will show you the following in the following order:
- (1) Connect Tableau Desktop with Cloudera Hadoop Server
- (2) Extract necessary data (with custom SQL if necessary)
- (3) Publish data source onto "Ray's Tableau Server" with emedded authetification as LIVE data source
- (4) From "Ray's Tabealu Server", change the data from LIVE to EXTRACT  (takes a while)
- (5) Open a new Tableau Desktop instance and connect to the publisehd data source in "Ray's Tableau Server"
- (6-optional) Set refresch schedule for extracted data
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

#### You will receive an email upton extraction (at least that is how it is configured).
#### In addition, you can monitor the extraction process in real-time as shown.
<img align="center" src="https://user-images.githubusercontent.com/62319355/105821830-3fafa000-5ff6-11eb-897a-a0ceb4298d8e.png" alt="Live to extract">



### Step 5. Once data source has been extracted on the Tableau, let us connect to the data.
#### Now, you will experience much less loading of data as compared to live connection.
#### You may ask "Why not just extract from the very start?"  The biggest reason is that it can throw an error when you extract at the start.
<img align="center" src="https://user-images.githubusercontent.com/62319355/105823826-9918ce80-5ff8-11eb-8d7c-fcbd4e1f97ab.png" alt="Connect to ray DB">


### Step 6. (Optional) You can set refresh schedule on the Extract on "Ray's Tableau Server" easily.
<img align="center" src="https://user-images.githubusercontent.com/62319355/105824522-6e7b4580-5ff9-11eb-95fd-55e75066650d.png" alt="Refresh Extracts">



🎈🦾 😎 That's it from me.  Happy Data Stitching!!
--------------------------------------------------------------------------------------------------------------------------------------------------





## Credits
```
- Secular saints of Tableau Community
```


