# Analog_projects

# IHP INSTALLTION (UBUNTU)
Step 1: Clone/download this GitHub repository onto your laptop. 
```
mkdir github 
cd github  
git clone --depth=1 https://github.com/iic-jku/iic-osic-tools.git 
```
Step 2: Install Docker on your computer 

Set up Docker's apt repository.
```
sudo apt-get update 
sudo apt-get install ca-certificates curl 
sudo install -m 0755 -d /etc/apt/keyrings 
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc 
sudo chmod a+r /etc/apt/keyrings/docker.asc 
```

```
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
```
Install the Docker packages.
```
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
```

Verify the docker installation by running the above command

```
sudo docker run hello-world
```
Step 3:  Post installtion steps for   Docker engine
Create the docker group.
```
sudo groupadd docker
```
Add your user to the docker group.
```
sudo usermod -aG docker $USER
```
Log out and log back in so that your group membership is re-evaluated.
```
newgrp docker
```
Verify by running above command that we can now runn docker without sudo command.
```
docker run hello-world
```
Step 4: After succesfully installing Docker now we have  to run command ```./start_x.sh```  .On the first run it will download and exract all the files which will take time .
After succesfull installation we will see a new terminal like shown below.

![Screenshot from 2024-06-28 00-27-11](https://github.com/High-Performance-Analog-VLSI/Analog_projects/assets/141152904/bb169045-0c1e-4ab5-8b7a-30c1a467b0cd)

Step 5: Setup IHP PDK 
Now we need to  type  the following command to set up  our pdk to  IHP PDK.
```
PDK_ROOT=/foss/pdks
PDK=sg13g2
PDKPATH=/foss/pdks/sg13g2
export KLAYOUT_HOME=/foss/designs/.klayout

```
Step 6: Now to see schematic editor we need to type ``` xschem``` on the new teminal.
after doing so a schematic 
![Screenshot from 2024-06-28 00-29-44](https://github.com/High-Performance-Analog-VLSI/Analog_projects/assets/141152904/c37495c8-861b-4a09-a27d-da46dc032e77)
vien like shown below  will apear.


![Screenshot from 2024-06-28 02-30-51](https://github.com/High-Performance-Analog-VLSI/Analog_projects/assets/141152904/03848794-e655-4a8b-8574-a962c22df0d9)

Now going to the file we can open a new schematic and make  our own design like shown
![Screenshot from 2024-06-28 00-26-08](https://github.com/High-Performance-Analog-VLSI/Analog_projects/assets/141152904/7645a8ea-c528-4a31-8808-1468f24a8de7)
