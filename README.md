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


