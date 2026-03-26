# Day-44-Secrets-Artifacts-Running-Real-Tests-in-CI

## Challenge Tasks

## Task 1: GitHub Secrets

   1. Go to your repo → Settings → Secrets and Variables → Actions
   2. Create a secret called MY_SECRET_MESSAGE
   3. Create a workflow that reads it and prints: The secret is set: true (never print the actual value)
   4. Try to print ${{ secrets.MY_SECRET_MESSAGE }} directly — what does GitHub show?

  <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/016c0166-62b9-434a-89ba-7055083693da" />

  ## Task 2: Use Secrets as Environment Variables
  
  1. Pass a secret to a step as an environment variable
  2. Use it in a shell command without ever hardcoding it
   3. Add DOCKER_USERNAME and DOCKER_TOKEN as secrets (you'll need these on Day 45)
      
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/a972747c-d705-47bd-9733-275dbbf6b46d" />

## Task 3: Upload Artifacts

  1. Create a step that generates a file — e.g., a test report or a log file
  2. Use actions/upload-artifact to save it
  3. After the workflow runs, download the artifact from the Actions tab

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/90d9341d-7ed5-43e5-b088-79213392a15b" />
<img width="856" height="444" alt="Image" src="https://github.com/user-attachments/assets/8371bf50-caeb-4cd4-92fc-4fdc1ac532ec" />

## Task 4: Download Artifacts Between Jobs

  1. Job 1: generate a file and upload it as an artifact
  2. Job 2: download the artifact from Job 1 and use it (print its contents)

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/64f47591-7012-49fa-81fa-3b71ef248eef" />

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/5077582a-aaf9-40a1-859b-7852741abf9e" />

## Task 5: Run Real Tests in CI

Take any script from your earlier days (Python or Shell) and run it in CI:

  1. Add your script to the github-actions-practice repo
  2. Write a workflow that:
      - Checks out the code
      - Installs any dependencies needed
       -  Runs the script
      - Fails the pipeline if the script exits with a non-zero code
 3. Intentionally break the script — verify the pipeline goes red
 4. Fix it — verify it goes green again

## Task 6: Caching

  1. Add actions/cache to a workflow that installs dependencies
  2. Run it twice — observe the time difference
  3. Write in your notes: What is being cached and where is it stored?


