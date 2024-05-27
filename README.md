# Test_Repo
This is a new Test Repo for practice. Where multiple questions are asked and solution is provided.

Q1. Set up a repository called Test_Repo with the following files: 
1.	A powershell script called init.ps1.
2.	A README.md file with a project description.
3.	Yml scripts to run a CI/CD pipeline on Azure DevOps.

The script init.ps1 should implement 3 functions called: 
1.	Setup-Env that prints the message – “Running pre-build init” when invoked.
2.	Build-Proj that prints the message – “Building Project” when invoked.
3.	Release-Build that prints the message – “Deploying Artifacts” when invoked.

Definition of success: A user should be able to do the following:
1.	Clone the repository
2.	Checkout the development branch
3.	Open powershell in the repository folder and run the command `./init.ps1` that loads all functions.
4.	Once the ps1 script is loaded, Run the command Setup-Env to which the response will be “Running     pre-build init” .
5.	Run the command Build-Proj to which the response will be “Building Project”
6.	Run the command Release-Build to which the response will be ““Deploying Artifacts
