# SimpleCodeCommitRepo
- This Repository contains a buildspec.yml file and index.html file. You can modify the name in the files to give your name if you wish.
- The index.html file contains a name and the buildspec.yml file tests to look for this name, and if it is found, the build is succeeded.
- You can create a simple AWS CodeBuild project by following these steps:
- Add these files to your AWS CodeCommit repo or you can use GitHub repo as the source.
- Create a Build Project in AWS CodeBuild:
  - Give a name (eg. - CodeDeployDemo) and description to your project.
  - In Environment, choose managed image and select Amazon Linux 2 as the OS. Let CodeBuild create the service role for you.
  - You can do additional configuration as per your requirement (VPC, etc.)....**SKIP FOR NOw**
  - If you are using the same buildspec.yml file then you don't need to give name (By default, CodeBuild looks for a file          named buildspec.yml in the source code root directory). If you have the file by different name, then give the path to that buildspec file.
  - You can choose to add artifact if you want....**SKIP FOR NOW**
  - Add CloudWatch logs by giving some group name and stream name as "Logs".
  - Click Create Build Project.
- Click on Start Build when the project is created.
- You can check the status and Phase Details to see the Build status.
- Since the name is found in the index.html file, the build will succeed.
- You can then change the name in the index.html file in your CodeCommit or GitHub repo and commit the changes. This time when you Start the Build, it will eventualy fail because buildspec.yml file could not find the name in the index.html file.
# Your simple AWS CodeBuild project with CodeCommit Repo is Complete!
