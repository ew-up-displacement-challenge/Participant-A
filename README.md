Participant-A
=============
Tools to combine the Asc and Desc measurement to extract the EW and Up component of Displacement.

### Quick link

* [Installation](#installation)
* [Submitting the workflow](#submit)
* [Test the application](#test)

### <a name="installation"></a>Installation

Log on the Developer Cloud Sandbox and run these commands in a shell:

* Install **Java 7**

```bash
sudo yum install -y idl
```

* Select Java 7

```bash
sudo /usr/sbin/alternatives --config java
```
This will show on the terminal window:

```
There are 3 programs which provide 'java'.

  Selection    Command
-----------------------------------------------
 + 1           /usr/java/jdk1.6.0_35/jre/bin/java
   2           /usr/lib/jvm/jre-1.5.0-gcj/bin/java
*  3           /usr/lib/jvm/jre-1.7.0-openjdk.x86_64/bin/java

Enter to keep the current selection[+], or type selection number:
```

Select java 1.7 out of the menu options by typing the correct number (here it's *3*).

* Install the application from github

```bash
cd
git clone git@github.com:ocean-color-ac-challenge/Participant-A.git
cd Participant-A
mvn install
```

* Install the application from rpm

```bash
curl -L -O https://github.com/ocean-color-ac-challenge/Participant-A/releases/download/v0.35/Participant-A-0.35-ciop.noarch.rpm
sudo yum -y install Participant-A-0.35-ciop.noarch.rpm
```

### <a name="submit"></a>Submitting the workflow

* Via the Sandbox shell 

Run this command in a shell:

```bash
ciop-run
```

* Via the Web Processing Service dashboard tab

Use your browser to go to the Sandbox dashboard tab at the address http://<sandbox ip>/dashboard

Click on the _Invoke_ tab

Below the "Process List" click on _Participant A_

Fill the parameters and click submit. 

### <a name="test"></a>Test the application

##### Test Participant-A-01

* Test Procedure

Invoke the application via the Dashboard with the parameters listed in the test inputs specification

* Inputs specification 

| Parameter   | Value |
|-------------|---------------------------------------------------------------------------------------------------------|
| Catalogue      | https://challenges.esa.int/eceo/datapackage/RRPAR/description?key=9d79148d-3e17-414b-9983-e4cef9e88ec6 |
| Start date   | 2002-03-01T00:00:00Z |
| End date     | 2012-05-09T23:59:59Z |
| aerosolType | CONTINENTAL |
| Aerosol Optical Depth  | 0.1 |
| Use ECMWF data in the MERIS ADS | true |
| List of POI for reflectance extraction |BOUS,43.367,7.9\|AAOT,45.314,12.508\|MOBY,20.828,-157.193 |
| Flag to trigger the publishing of Level 2 products generated | true |
| Flag to extract POI reflectances | false |

* Outputs specification

| Output                                                             | Size |
|--------------------------------------------------------------------|------|
MER_RR__1PNACR20060730_093546_000021432049_00480_23079_0000.N1.png|10.01 MB|
MER_RR__1PNACR20060730_093546_000021432049_00480_23079_0000.N1.tgz|193.73 MB|
MER_RR__1PRACR20030306_201313_000026082014_00243_05307_0000.N1.png|21.35 MB|
MER_RR__1PRACR20030306_201313_000026082014_00243_05307_0000.N1.tgz|367.81 MB|
MER_RR__1PRACR20040903_201756_000026282030_00057_13137_0000.N1.png|21.87 MB|
MER_RR__1PRACR20040903_201756_000026282030_00057_13137_0000.N1.tgz|367.88 MB|
MER_RR__1PRACR20050504_093419_000026382037_00022_16609_0000.N1.png|14.73 MB|
MER_RR__1PRACR20050504_093419_000026382037_00022_16609_0000.N1.tgz|265.6 MB|
MER_RR__1PRACR20070920_092716_000026302061_00437_29048_0000.N1.png|14.86 MB|
MER_RR__1PRACR20070920_092716_000026302061_00437_29048_0000.N1.tgz|266 MB|
MER_RR__1PRACR20080816_092020_000026302071_00165_33786_0000.N1.png|16.58 MB|
MER_RR__1PRACR20080816_092020_000026302071_00165_33786_0000.N1.tgz|267.37 MB|

* Test pass/fail criteria

All products listed in test outputs specification are generated

##### Test Participant-A-02

* Test Procedure

Invoke the application via the Dashboard with the parameters listed in the test inputs specification

* Inputs specification 

| Parameter   | Value |
|-------------|---------------------------------------------------------------------------------------------------------|
| Catalogue      | https://challenges.esa.int/eceo/datapackage/FRSPAR/description?key=495f181f-47d3-4668-b717-d36d4a560837 |
| Start date   | 2002-03-01T00:00:00Z |
| End date     | 2012-05-09T23:59:59Z |
| aerosolType | CONTINENTAL |
| Aerosol Optical Depth  | 0.1 |
| Use ECMWF data in the MERIS ADS | true |
| List of POI for reflectance extraction |BOUS,43.367,7.9\|AAOT,45.314,12.508\|MOBY,20.828,-157.193 |
| Flag to trigger the publishing of Level 2 products generated | true |
| Flag to extract POI reflectances | false |

* Outputs specification

| Output                                                             | Size |
|--------------------------------------------------------------------|------|
MER_FRS_1PPEPA20040711_020449_000002422028_00275_12353_1787.N1.png|21.16 MB|
MER_FRS_1PPEPA20040711_020449_000002422028_00275_12353_1787.N1.tgz|466.86 MB|
MER_FRS_1PPEPA20040717_021529_000002642028_00361_12439_1968.N1.png|18.27 MB|
MER_FRS_1PPEPA20040717_021529_000002642028_00361_12439_1968.N1.tgz|371.85 MB|

* Test pass/fail criteria

All products listed in test outputs specification are generated

##### Test Participant-A-03

* Test Procedure

Invoke the application via the Dashboard with the parameters listed in the test inputs specification

* Inputs specification 

| Parameter   | Value |
|-------------|---------------------------------------------------------------------------------------------------------|
| Catalogue      | https://challenges.esa.int/eceo/datapackage/RRPAR/description?key=9d79148d-3e17-414b-9983-e4cef9e88ec6 |
| Start date   | 2002-03-01T00:00:00Z |
| End date     | 2012-05-09T23:59:59Z |
| aerosolType | CONTINENTAL |
| Aerosol Optical Depth  | 0.1 |
| Use ECMWF data in the MERIS ADS | true |
| List of POI for reflectance extraction |BOUS,43.367,7.9\|AAOT,45.314,12.508\|MOBY,20.828,-157.193 |
| Flag to trigger the publishing of Level 2 products generated | false |
| Flag to extract POI reflectances | true |

* Outputs specification

| Output                                                             | Size |
|--------------------------------------------------------------------|------|
MER_RR__1PNACR20060730_093546_000021432049_00480_23079_0000.N1.txt|1.08 KB|
MER_RR__1PRACR20030306_201313_000026082014_00243_05307_0000.N1.txt|0.78 KB|
MER_RR__1PRACR20040903_201756_000026282030_00057_13137_0000.N1.txt|0.78 KB|
MER_RR__1PRACR20050504_093419_000026382037_00022_16609_0000.N1.txt|1.06 KB|
MER_RR__1PRACR20070920_092716_000026302061_00437_29048_0000.N1.txt|1.06 KB|
MER_RR__1PRACR20080816_092020_000026302071_00165_33786_0000.N1.txt|1.05 KB|

* Test pass/fail criteria

All products listed in test outputs specification are generated


##### Test Participant-A-04

* Test Procedure

Invoke the application via the Dashboard with the parameters listed in the test inputs specification

* Inputs specification 

| Parameter   | Value |
|-------------|---------------------------------------------------------------------------------------------------------|
| Catalogue      | https://challenges.esa.int/eceo/datapackage/FRSPAR/description?key=495f181f-47d3-4668-b717-d36d4a560837 |
| Start date   | 2002-03-01T00:00:00Z |
| End date     | 2012-05-09T23:59:59Z |
| aerosolType | CONTINENTAL |
| Aerosol Optical Depth  | 0.1 |
| Use ECMWF data in the MERIS ADS | true |
| List of POI for reflectance extraction |CHINA,27,122\|CHINA2,30,124\|CHINA3,22,126|
| Flag to trigger the publishing of Level 2 products generated | false |
| Flag to extract POI reflectances | true |

* Outputs specification

| Output                                                             | Size |
|--------------------------------------------------------------------|------|
MER_FRS_1PPEPA20040711_020449_000002422028_00275_12353_1787.N1.txt|0.77 KB|     
MER_FRS_1PPEPA20040717_021529_000002642028_00361_12439_1968.N1.txt|0.77 KB|

* Test pass/fail criteria

All products listed in test outputs specification are generated
