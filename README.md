Participant-A
=============
Tools to combine the Asc and Desc measurement to extract the EW and Up component of Displacement.

### Quick link

* [Installation](#installation)
* [Submitting the workflow](#submit)
* [Test the application](#test)

### <a name="installation"></a>Installation

Log on the Developer Cloud Sandbox and run these commands in a shell:

* Install **IDL**

```bash
sudo yum install -y idl
```

* Install the application from github

```bash
cd
git clone git@github.com:ew-up-displacement-challenge/Participant-A.git
cd Participant-A
mvn install
```

* Install the application from rpm

```bash
curl -L -O https://github.com/ew-up-displacement-challenge/Participant-A/releases/download/v0.35/Participant-A-0.35-ciop.noarch.rpm
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
| Parameter 1   | 680 |
| Parameter 2   | 220 |

| Data |
|------|
| file:///application/data/asc_T408.zip |
| file:///application/data/desc_T472.zip | 
| file:///application/data/asc_T365.zip |
| file:///application/data/desc_T200.zip |

* Outputs specification

| Output                                                             | Size |
|--------------------------------------------------------------------|------|

TBW

* Test pass/fail criteria

All products listed in test outputs specification are generated

##### Test Participant-A-02

* Test Procedure

Invoke the application via the Dashboard with the parameters listed in the test inputs specification

* Inputs specification 

| Parameter   | Value |
|-------------|---------------------------------------------------------------------------------------------------------|
| Parameter 1   | 680 |
| Parameter 2   | 220 |

* Outputs specification

| Output                                                             | Size |
|--------------------------------------------------------------------|------|

TBW

* Test pass/fail criteria

All products listed in test outputs specification are generated
