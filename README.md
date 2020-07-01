# Portable-Local-Network-Server-Final-Year-Project

Hundreds and thousands of web application &amp; web sites are being created every single day. In order to run or process these kinds of web-based application huge chunks of server are required, and to power these servers 24/7 huge amount of electricity is consumed. It might be possible to buy/rent certain amount of server space, but it is very expensive to buy the entire server. So, the main objective of this project is to make even more highly efficient, completely inexpensive and portable pocket size web server. 

# Portable local network server
Setting up Raspberry Pi 4 to serve a Django project using Apache2.
.

### Software Required for setting up the Raspberry-pi: 

##### Raspberry pi Operating system-- https://www.raspberrypi.org/downloads/raspberry-pi-os/

##### SD card formatter -- https://www.sdcard.org/downloads/formatter/

##### Flash Rapios os in Sd card -- https://www.balena.io/etcher/


### Setting up raspberry pi

1. Total wipeout of the SD Card:

    1. Download SDFormatter.

    2. Install it

    3. Plugin MicroSD card.

    4. Open SDFormatter

    5. Select that specific card

    6. Select "Quick Format".

    7. Click "Format"

2. Download [Raspberry-pi os](https://www.raspberrypi.org/downloads/raspbian/) .

    1. Once downloaded, extract/unzip downloaded contents.

    2. The file is about 3 Giga bytes.

3. Download and open [Etcher](https://www.balena.io/etcher/)

4. Run it and select the operating system image file.

5. Select the formatted SD card.

6. Click **Burn** to transfer Raspbian to the microSD card. Once complete, you can safely pull the card out 

7. Insert the microSD card into Raspberry Pi 

8. Power on Raspberry Pi



### Getting IP Address of the Pi

1. Turn Raspberry Pi on and ensure microSD card is inserted that contains the Raspbian Jessie Linux Operating System 

2. Connect USB Keyboard, USB Mouse, and Monitor (through HDMI)

3. Connect Raspberry Pi to the Internet on your local network :
  
4. Open up `Terminal` and type `ifconfig`. You should see the following result:

    You'll need to find this line `inet addr:`

5. SSH into your Pi with `ssh pi@<ip>`:

    Mac/Linux Users (non-Pi linux):
    
    1. Open Open Terminal
    2. type `ssh pi@<IP>`
    3. Accept the warning about fingerprint authenticity (if any)
    4. The default password is `raspberry`
    
    
    Windows Users:
    
    1. Download & Install [PuTTY](http://www.putty.org/)
    2. Open PuTTY
    3. type `ssh pi@<IP>` 
    4. Accept the warning about fingerprint authenticity 
    5. The default password is `raspberry`



### Apache2 and Django installation inside Raspberry pi

Install Apache2 on raspberry-pi:

```
sudo apt-get install apache2 -y
sudo apt-get install libapache2-mod-wsgi-py3
```

Install Pip & Django:

```
sudo apt-get install python-setuptools python-dev build-essential

sudo easy_install pip 

sudo pip install django==X.Y.Z #where X.Y.Z is the version number

sudo pip install django==1.10.3

sudo pip install virtualenv 

```
Enabling module wsgi
```
sudo a2enmod wsgi
```

Restart Apache service:

```
# Restart in two ways:
sudo apachectl restart
sudo service apache2 restart
```
Start Apache service : 
```
# Start the Apache:
sudo apachectl start
sudo service apache2 start
```
Stop Apcahe Service : 
```
# Stop Apache in two ways:
sudo apachectl stop
sudo service apache2 stop
```

# Required Python libraries
#### For Bulk installation copy it and paste it inside requirements.txt file and install it as ```pip3 install -r requirements.txt```

```urllib3==1.23
Pillow==5.2.0
chardet==3.0.4
Django==2.1
django-crispy-forms==1.7.2
idna==2.7
requests==2.19.1
pytz==2018.5
certifi==2018.10.15
```



# Slides

.                                |  Table of Content:
:-------------------------------------------------:|:-------------------------------------------------:
![](https://user-images.githubusercontent.com/37651620/86200106-94338f80-bb7b-11ea-8f6e-053b16d9de38.png)           |  ![](https://user-images.githubusercontent.com/37651620/86200105-9269cc00-bb7b-11ea-8715-d6cd6e094ddb.png)

Aim of Project                                |  Project Objectives
:-------------------------------------------------:|:-------------------------------------------------:
![](https://user-images.githubusercontent.com/37651620/86200103-91d13580-bb7b-11ea-89c4-188535e7cce9.png)           |  ![](https://user-images.githubusercontent.com/37651620/86200101-91389f00-bb7b-11ea-8ff6-2ba9761ea20d.png)

Meeting Record                                |  ER Diagram
:-------------------------------------------------:|:-------------------------------------------------:
![](https://user-images.githubusercontent.com/37651620/86200099-90077200-bb7b-11ea-9604-a680c793acb9.png)          |  ![Screenshot (53)](https://user-images.githubusercontent.com/37651620/86200098-8ed64500-bb7b-11ea-9e7a-586cc6f6fa86.png)

Structure Chart                                |  USe Case Diagram
:-------------------------------------------------:|:-------------------------------------------------:
![Screenshot (54)](https://user-images.githubusercontent.com/37651620/86200094-8e3dae80-bb7b-11ea-9b42-b77ef11a0a2d.png)          |  ![Screenshot (55)](https://user-images.githubusercontent.com/37651620/86200092-8d0c8180-bb7b-11ea-9e09-6ad4176c3a44.png)

Task Sheet                                |  Gantt Chart
:-------------------------------------------------:|:-------------------------------------------------:
![Screenshot (56)](https://user-images.githubusercontent.com/37651620/86200091-8bdb5480-bb7b-11ea-9d49-ad9041ef7f7a.png)           |  ![Screenshot (57)](https://user-images.githubusercontent.com/37651620/86200090-8aaa2780-bb7b-11ea-9ffe-6176aa039026.png)


calendar                                |  Timeline
:-------------------------------------------------:|:-------------------------------------------------:
![Screenshot (58)](https://user-images.githubusercontent.com/37651620/86200087-8a119100-bb7b-11ea-9787-69a778d1f046.png)          |  ![Screenshot (59)](https://user-images.githubusercontent.com/37651620/86200086-88e06400-bb7b-11ea-9600-9d15e63e422e.png)

Network Diagram                                |  Network Diagram  
:-------------------------------------------------:|:-------------------------------------------------:
![Screenshot (60)](https://user-images.githubusercontent.com/37651620/86200080-867e0a00-bb7b-11ea-8cda-783a4cce4604.png)  |  ![Screenshot (61)](https://user-images.githubusercontent.com/37651620/86200168-b0cfc780-bb7b-11ea-8a1d-897678b4f6da.png)

Network Diagram                                  |  Network Diagram  
:-------------------------------------------------:|:-------------------------------------------------:
![Screenshot (62)](https://user-images.githubusercontent.com/37651620/86200167-af9e9a80-bb7b-11ea-97e6-3c5b5d3ee723.png)           |  ![Screenshot (63)](https://user-images.githubusercontent.com/37651620/86200166-add4d700-bb7b-11ea-8f62-3ccf70965377.png)

Network Diagram                                  |  Resources Used  
:-------------------------------------------------:|:-------------------------------------------------:
![Screenshot (64)](https://user-images.githubusercontent.com/37651620/86200161-aca3aa00-bb7b-11ea-9ef6-8349bb028893.png) |  ![Screenshot (65)](https://user-images.githubusercontent.com/37651620/86200155-aad9e680-bb7b-11ea-9656-414730da3fc2.png)

 Requirement Catalogue "Overview"                               |  Requirement Catalogue "Functional Requirement" 
:-------------------------------------------------:|:-------------------------------------------------:
![Screenshot (66)](https://user-images.githubusercontent.com/37651620/86200153-a9a8b980-bb7b-11ea-8bfe-ae91e4fd3c80.png) |  ![Screenshot (67)](https://user-images.githubusercontent.com/37651620/86200150-a9102300-bb7b-11ea-99c2-a399ab063bb2.png)

  Requirement Catalogue "Non-Functional Requirement"                  |  website Mockups 
:-------------------------------------------------:|:-------------------------------------------------:
![Screenshot (68)](https://user-images.githubusercontent.com/37651620/86200148-a7def600-bb7b-11ea-83b1-5bdc055c8ac6.png)           |  ![Screenshot (69)](https://user-images.githubusercontent.com/37651620/86200144-a6153280-bb7b-11ea-8d6d-787fdbfc6870.png)

website Mockups                    |  Raspberry pi server mockups  
:-------------------------------------------------:|:-------------------------------------------------:
![Screenshot (70)](https://user-images.githubusercontent.com/37651620/86200142-a4e40580-bb7b-11ea-9d16-c0e16b61be82.png)          |  ![Screenshot (71)](https://user-images.githubusercontent.com/37651620/86200136-a31a4200-bb7b-11ea-9a20-1c1666abdf09.png)

Arduino circuit diagram mockups                           | Arduino circuit diagram mockups 
:-------------------------------------------------:|:-------------------------------------------------:
![Screenshot (72)](https://user-images.githubusercontent.com/37651620/86200133-a1e91500-bb7b-11ea-9856-d82481120a6b.png)   |  ![Screenshot (73)](https://user-images.githubusercontent.com/37651620/86200130-a1507e80-bb7b-11ea-964f-de97a35fe741.png)

Product Development:Front-End ”Login-page”                             | Register   
:-------------------------------------------------:|:-------------------------------------------------:
![Screenshot (74)](https://user-images.githubusercontent.com/37651620/86200123-9f86bb00-bb7b-11ea-8895-f825582cc908.png) |  ![Screenshot (75)](https://user-images.githubusercontent.com/37651620/86200120-9dbcf780-bb7b-11ea-80c1-56f4eeea9e60.png)

Home-Page                              |  Back End 
:-------------------------------------------------:|:-------------------------------------------------:
![Screenshot (76)](https://user-images.githubusercontent.com/37651620/86200119-9bf33400-bb7b-11ea-8d87-1d578ff21c3c.png)   |  ![Screenshot (77)](https://user-images.githubusercontent.com/37651620/86200118-9b5a9d80-bb7b-11ea-9471-0e99f87372c2.png)


Product Development:“Users” Database Tables on db.Sqlite3  | Product Development: “Posts” Database Tables on db.Sqlite3                       
-----------------------------------------------------------:|:-------------------------------------------------:
   ![Screenshot (78)](https://user-images.githubusercontent.com/37651620/86200116-9ac20700-bb7b-11ea-9a72-9594eaae5630.png) |  ![Screenshot (79)](https://user-images.githubusercontent.com/37651620/86200114-9990da00-bb7b-11ea-8bea-21c1d7e87240.png)     
 
 Final Product | Final Product                        
:--------|:-------------------------------------------------:
 ![Screenshot (80)](https://user-images.githubusercontent.com/37651620/86200110-95fd5300-bb7b-11ea-9216-4edde45555aa.png)  | ![Screenshot (81)](https://user-images.githubusercontent.com/37651620/86200112-97c71680-bb7b-11ea-8a9a-5c1c728eee33.png) 
      
