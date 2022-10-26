# Testing and Robotic Process Automation (RPA) on a Web Application
RPA is used to mimic human tasks in the same way that a person would execute the process.
In this project I used this web application [Connected Office: Device Management System](https://connectedoffice-devicemanagement.azurewebsites.net/)
to perform User acceptance testing (UAT) using an  UiPath Robot. 

### Task performed by the robot in the orchestrator
1. Get credential stored in the orchestrator (username and password) and store them to variables

### Task perform by the robot in the Excel file
1. Get data excel file 
2. Read the data from the file, and 
3. Store the data from the file in the dataTable - three sheets (Zone, Catagory, and Device) each in its on dataTable 

### Tasks performed by the robot in the web application
1. Log In using credential stored in the orchestrator assest
2. Click on the Zone tab 
3. Peform CRUD operation on the Zones tab
4. Click on the Category tab
5. Perform CRUD operations on the Category tab
6. Click on the Device tab
7. Perform CRUD operations on the Device tab

### Purpose
To ensure that the input entered int the web application generate the expected output

### How the use the Robot
To run the application ensure that Start button is clicked on the workflow, so the application flow can start from top to bottom and 
then simply click the Run button

### Table of Contents
1. [Login](#Login)
2. [Zone](#Zone)
3. [Category](#Category)
4. [Device](#Device)
5. [Delete](#Delete)

<a name="Login"></a>      
#### 1. Login <br>
* The Robot will get the credential from the orchestrator and use them to log in

<a name="Zone"></a>      
#### 2. Zones <br>
After logging In the Robot will:
* Click on the zone tab <br>
<img src="Img/{name}.png" width=200>

* Click the the add icon and add the data from the Zone dataTable ZoneName and Zonedescription column  and click Create button <br>
<img src="Img/{name}.png" width=200>

* Click the view icon to view the zone added <br>
<img src="Img/{name}.png" width=200>

* Click the the edit button to test edti Zone description and click Save button <br>
<img src="Img/{name}.png" width=200>

<a name="Category"></a>      
#### 3. Category <br>
Then after all the rows in the zone dataTable have been added the Category tab will be clicked and the Robot will:
* Click the the add icon and add the data from the Category dataTable CategoryName and Categorydescription column and click Create button <br>
<img src="Img/{name}.png" width=200>

* Click the view icon to view the category added <br>
<img src="Img/{name}.png" width=200>

* Click the the edit button to test edti category description and click Save button <br>
<img src="Img/{name}.png" width=200>


<a name="Device"></a>      
#### 4. Device <br>
Then after all the rows in the category dataTable have been added the Device tab will be clicked and the Robot will:
* Click the the add icon and add the data from the Device dataTable and click Create button <br>
<img src="Img/{name}.png" width=200>

* Click the view icon to view the device added <br>
<img src="Img/{name}.png" width=200>

* Click the the edit button to test edti device status and check/uncheck the box for isActive and click Save button <br>
  * For the device status a String array was used to store {"In Operation", "Broken", "Maintenance", "Stopped"}, so to test the device status
  an element in the array is returned randomly to the status textbox. And for the isActive the box is checked/unchecked. <br>
<img src="Img/{name}.png" width=200>

<a name="Delete"></a>      
#### 5. Delete <br>
Then after all the rows in the device dataTable have been added the Robot will:

* Delete all the devices <br>
* Then, Click the Zone tab and delete all the zones <br>
* Finally, Click the Category tab and delete all the categories <br>


