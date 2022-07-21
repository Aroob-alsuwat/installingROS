# installingROS
1.. Installing VirtualBox
1.	Download VirtualBox for Windows Host 
 ![image](https://user-images.githubusercontent.com/109753912/180270472-85859d61-8a5a-4884-9a40-8c3d5d53d72b.png)

2.	Run the .exe file and install VirtualBox

2.. Download Ubuntu 
1.	Download Ubuntu 
 ![image](https://user-images.githubusercontent.com/109753912/180270730-e8eff033-8950-4df3-948a-10df1ca432a0.png)

Download may take a while as the file size for Ubuntu 20.04.2.0 LTS is 2.7GB.

3.. Create Virtual Machine
1.	Open VirtualBox.
2.	Create a new virtual machine by clicking on the New icon or going to Machine > New.
 ![image](https://user-images.githubusercontent.com/109753912/180270974-b9472f95-9c34-43fa-aa5b-a652d7afa915.png)

3.	Enter Ubuntu as the name. Type and Version should be automatically filled for you, if not, set Type to Linux and Version to Ubuntu (64-bit). Click Next.
 ![image](https://user-images.githubusercontent.com/109753912/180271009-027bbc31-719a-4dd5-a8d2-44a4620289f5.png)
4.	Increase the memory size to 6144MB (6GB). If 6144MB is within the orange or red zone, use a memory size of 4096MB instead. Click Next.
 ![image](https://user-images.githubusercontent.com/109753912/180271165-cb446ea7-fd9b-4da0-a0be-119f2b0af49f.png)
5.	Select Create a virtual hard disk now and click Create.
![image](https://user-images.githubusercontent.com/109753912/180271210-8b802be6-d69e-4f31-b53d-aa705fc4a33c.png)
6.	Select VDI (VirtualBox Disk Image) and click Next.
 ![image](https://user-images.githubusercontent.com/109753912/180271286-9ab14fbd-97b5-446b-9f22-50d3b4fd648d.png)
 ![image](https://user-images.githubusercontent.com/109753912/180271354-f6525e57-fb6a-4e35-b06c-4525edad2ee0.png)
i.	Select Dynamically allocated and click Next.
7.	Change the hard disk size to 35.00GB. You may change the location where the disk image is saved at but it is alright to leave it as the default. Click Create.
 ![image](https://user-images.githubusercontent.com/109753912/180271447-9cf6295d-78d1-4c23-9fe8-d241c45063b1.png)
8.	Right-click on the newly created virtual machine and click Settings. Alternatively single left-click the virtual machine and go to Machine > Settings.
 ![image](https://user-images.githubusercontent.com/109753912/180271501-b83a5652-7908-4cb8-9e02-d1ea4ecf0459.png)
9.	Navigate to Storage on the left-hand menu and select the Storage tab. Click on the line with the CD. On the right, under Optical Drive, click on the CD icon with the down arrow and select Choose a disk file.... Navigate to the earlier downloaded Ubuntu ISO.
 ![image](https://user-images.githubusercontent.com/109753912/180271566-a314dc0e-57d1-4e0f-a04c-0a5152447589.png)
10.	Navigate to System on the left-hand menu and select the Processor tab. Increase the slider until the end of the green zone, which may be different as compared to the diagram below.
![image](https://user-images.githubusercontent.com/109753912/180271617-2e16ed3a-8102-4c3d-bdb8-4325dc576257.png)

4.. Install Ubuntu
1.	Double click on the newly created virtual machine.
 ![image](https://user-images.githubusercontent.com/109753912/180272123-f64ae47b-f05b-43a9-b665-d206c752f4d2.png)
The virtual machine will start to boot
2.	Wait while the virtual machine to checks the disk.
 ![image](https://user-images.githubusercontent.com/109753912/180272179-151ba4ae-542c-4167-9631-0f5bf9511cdd.png)
3.	Select Install Ubuntu.
 ![image](https://user-images.githubusercontent.com/109753912/180272213-3b3cbedc-0b0e-4f00-b1aa-68279ae95870.png)
4.	Choose  keyboard layout as English (US). Click Continue.
 ![image](https://user-images.githubusercontent.com/109753912/180272254-e1fee089-47cf-44f0-926c-111c8184d0f5.png)
5.	Select Minimal installation, Download updates while installing Ubuntu and Install third-party software for graphics and Wi-Fi hardware and additional media formats. Click Continue.
 ![image](https://user-images.githubusercontent.com/109753912/180272294-252d3490-eaaf-463e-b83a-f0b65d3c1534.png)
6.	Select Erase disk and install Ubuntu. Click Install Now and click Continue if a warning pops out.
 ![image](https://user-images.githubusercontent.com/109753912/180272356-76a81d17-e06b-4715-8c05-3117589e5887.png)
7.	Select your country and click Continue.
8.	Enter your personal details and click Continue.
9.	Wait while Ubuntu installs. This may take a while.
10.	Restart the VM. If prompted to remove the installation medium, just press enter.
![image](https://user-images.githubusercontent.com/109753912/180272398-496acc29-f894-4cc8-9dd8-39f45ebfc77a.png) 

5.. Installing ROS on Ubuntu
1.	Open Software & Updates program by pressing the windows key and searching Software & Updates.
2.	Tick all boxes and click Close.
 ![image](https://user-images.githubusercontent.com/109753912/180272519-3b3f6494-09c5-4c19-9765-c8d457ea9977.png)
3.	Click Reload.
4.	Open a terminal window by pressing the windows key and searching Terminal or using the keyboard shortcut Ctrl+Alt+T.
5.	Run the following commands sequentially. 
6.	Set up ROS repo on Ubuntu 20.04
Run this command to add the ROS package repo: sudosh -c 'echo "deb http://packages.ros.org/ros/ubuntu bionic main" > /etc/apt/sources.list.d/ros-melodic.list'
 ![image](https://user-images.githubusercontent.com/109753912/180272703-ac772ef2-8823-4b1c-b7a1-e1208b723bfb.png)
7.	Add Official ROS repo keyring
To make sure we get authentic ROS Melodic package we will install, run sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654. 
![image](https://user-images.githubusercontent.com/109753912/180272760-3289cb0c-ab69-45ff-8371-9b5f94e74c86.png)
8.	Update ROS package index
Run sudo apt update to pull all the ROS Melodic packages in formation in Ubuntu 18.04. 
![image](https://user-images.githubusercontent.com/109753912/180272844-b98f41ff-f4ae-4994-8456-1758155a639f.png)
9.	Install ROS Melodic desktop package on Ubuntu 20.04
Here we will run sudo apt install ros-melodic-desktop-full to install all the ROS Melodic packages we will ever need.
 ![image](https://user-images.githubusercontent.com/109753912/180272895-880f9335-ce59-4483-838e-9455f175ba0f.png)




























