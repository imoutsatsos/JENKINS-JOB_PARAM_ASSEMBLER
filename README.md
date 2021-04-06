# JOB_PARAM_ASSEMBLER README #
JOB_PARAM_ASSEMBLER:A utility job to jumpstart job assembly from ready made components. Select parameters from one or more freestyle projects

### What is this repository for? ###

The repository provides an archive of the key artifacts required to setup (or update) the job on a Jenkins server. Artifacts include:

* Job configuration, and job-specific properties and scripts
* Shared Groovy Scriptlets
* Shared External scripts

### Job Dependencies ###

### Deployment Instructions ###

* Clone the repository ```git clone https://github.com/imoutsatsos/JENKINS-JOB_PARAM_ASSEMBLER.git```
* Deploy artifacts with [gradle](https://gradle.org/)
	* Open console in repository folder and execute command ```gradle deploy```
	* Deployment creates a **backup of all original files** (if they exist) in **qmic-JOB_PARAM_ASSEMBLER/backup** folder
	* Project configuration, scripts and properties are deployed to **$JENKINS_HOME/jobs/JOB_PARAM_ASSEMBLER** folder
	* Scriptlets are deployed to **$JENKINS_HOME/scriptlet/scripts** folder

* Review project plugins (shown below with latest version tested) and install as needed
 	* scriptler@3.1
  	* uno-choice@2.3
  	* htmlpublisher@1.23
  	* summary_report@1.15
  	* ws-cleanup@0.38
  	* build-name-setter@2.1.0
 

### How do I build this job? ###

1. Select a free-style Jenkins job
2. Select one or more job parameters to copy
3. Add selected parameters to the list of parameters to be copied to target job
4. Repeat steps 1,2,3 as needed
5. Manage and re-order the parameter list as needed with the appropriate buttons
6. Check whether to append to or overwrite existing target project parameters
7. Build it!

