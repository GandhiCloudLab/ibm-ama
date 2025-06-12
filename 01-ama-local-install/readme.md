# IBM Application Modernization Accelerator (AMA) Installation

This documentation gives step by step instructions to install IBM Application Modernization Accelerator in Linux/MacOS.


## 1. Download AMA

1. Download the AMA binary from the URL https://www.ibm.com/support/pages/ibm-application-modernization-accelerator-downloads

<img src="images/img-11.png">

2. Unzip the downloaded file `application-modernization-accelerator-local-4.2.0.zip`

3. Goto the unziped folder.

```
cd /Users/xxxxx/application-modernization-accelerator-local-4.2.0
```

## 2. Install

1. Run the below command to launch the installation

```
./launch.sh
```

2. Accept the license by entering `1`

<img src="images/img-12.png">

3. Accept the Terms by entering `1`

<img src="images/img-13.png">

4. Choose the  `1) Installing Application Modernization Accelerator`

<img src="images/img-14.png">

It starts installing. At the end you will have URL to access the AMA.

<img src="images/img-15.png">
<img src="images/img-16.png">
<img src="images/img-17.png">
<img src="images/img-18.png">
<img src="images/img-19.png">

## 3. Create Workspace 

1. Open the AMA console https://x.x.x.x:443

2. Click on `Create Workspace` 

<img src="images/img-40.png">

3. Enter the workspace name

4. Click on  `Create`

<img src="images/img-41.png">

Workspace get created as like this.

<img src="images/img-42.png">

## 4. Download Discovery Tool

1. Open the workspace, by clicking on WS1 tile in the above screen.

You will get the below screen.  

2. Click on `Open discovery tool`

<img src="images/img-43.png">

3. Select the `Source operating system`

4. Click on `Open discovery tool`

<img src="images/img-44.png">

It will download the file `transformationadvisor-Linux_WS1.tgz` based on your selection.

## 5. Run Discovery in your source environment

To install the discovery tool, log on to your application server with the application owner’s user credentials and complete the following steps:

1. Copy the above `xxxx.tgz` file to to your application server

2. Untar the file

```
tar xvfz transformationadvisor-Linux_WS1.tgz
```

3. Goto the untarred folder.

```
cd /Users/xxxxx/transformationadvisorxxxxx
```

4. Run the below command in the websphere for the discovery.

```
 ./bin/transformationadvisor -w /opt/IBM/WebSphere/AppServer -p Profile01 --ignore-missing-binary --ignore-missing-shared-library --no-upload
```
Here 
- -w is WEBSPHERE_HOME_DIR
- -p is PROFILE_NAME

<img src="images/img-20.png">

5. Accept the license

<img src="images/img-21.png">

6. Note the file name `/root/install1/ama/transformationadvisor-4.2.0/Profile01.zip` listed at the end of the discovery.

<img src="images/img-22.png">
<img src="images/img-23.png">

## 6. Upload the discovery results to the AMA

<img src="images/img-24.png">
<img src="images/img-45.png">
<img src="images/img-25.png">

## 7. See the results.

<img src="images/img-26.png">
<img src="images/img-27.png">
<img src="images/img-28.png">
<img src="images/img-29.png">
<img src="images/img-30.png">
<img src="images/img-31.png">
<img src="images/img-32.png">

## Reference

Install
https://www.ibm.com/docs/en/ama?topic=install

Data Collector
https://www.ibm.com/docs/en/ama?topic=accelerator-using-data-collector
