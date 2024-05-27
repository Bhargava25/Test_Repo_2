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

   Below is the image results the above task that has been completed successfully.

   ![image](https://github.com/Bhargava25/Test_Repo/assets/28252364/71955cdd-a3a4-463f-8b8d-844879d44f4e)


Q2. In the same repo, set up 2 pipelines, 
1.	A Test-Repo-CI pipeline, that runs whenever a PR is raised to main. This pipeline will have only the build stage. The build stage will have 2 tasks:
a.	A setup task – this will call `./init.ps1` and then call the Setup-Env command
b.	A build task - this will call `./init.ps1` and then call the Build-Proj command
2.	A Test-Repo-Release pipeline that needs to be triggered manually. This pipeline will have a build stage and a deploy stage. The build stage will be the same as above. The deploy stage will have one task, which will call `./init.ps1` and then call the Release-Build command. 
Set up, on ADO, these two pipelines under the pipelines tab so that they can be run as needed. 

On the same repo, set up your local laptop as an agent inside an agent pool named “Test-Repo-Agent-Pool” and make the necessary settings so that both the Test-Repo-CI and Test-Repo-Release pipelines use that agent to run the pipeline.

Definition of success: A user should be able to do the following:
1.	A developer, when he/she raises a PR, should automatically trigger a Test-Repo-CI pipeline.
2.	A developer can manually trigger a Test-Repo-Release Pipeline on ADO.
3.	Both of them run on the agent created in the laptop.

The above task is completed successfully

Q3. (Bonus Question) In the same repository, set up a basic CMake infrastructure. This should be linked to the  Build-Proj command so that, when it is called:
1.	CMake is invoked, and 
2.	The top level CMakelists.txt file prints the output “Building Project” instead of the powershell script printing it.




