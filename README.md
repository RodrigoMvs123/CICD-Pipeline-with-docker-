# CICD-Pipeline-with-docker-

https://raw.githubusercontent.com/RodrigoMvs123/CICD-Pipeline-with-docker-/main/README.md


https://github.com/RodrigoMvs123/CICD-Pipeline-with-docker-/blame/main/README.md


GitHub Actions and CICD

GitHub Actions Tutorial - Basic Concepts and CI/CD Pipeline with Docker


Java App with Gradle ( Build Artifact ) 
Docker Image ( Build Image ) 
Private Repository ( Docker Hub ) / push docker repository

 
Commit code
Test 
Build 
Push 
Deploy 

Nodejs App
Build Docker Image 
Push to Nexus Repo 
Deploy to DigitalOcean Server

Java App with Maven 
Integration Tests Linux and Windows 
Build Docker Image 
Push to AWS Repo 
Deploy to AWS EKS


Java App with Gradle ( Build Artifact ) 
Docker Image ( Build Image ) 
Private Repository ( Docker Hub ) / push docker repository

git push 
set up this workflow ( Template ) 
Deploy your code with these popular services ( Java with Gradle ) 

<> Code 
gradle.yml 
create a new branch 
create a pull request 


name: Java CI with Gradle









on:


 push:


   branches: [ "main" ]


 pull_request:


   branches: [ "main" ]







permissions:


 contents: read







jobs:


 build:







   runs-on: ${{matrix.os}}


strategy:
   matrix:
    os:[ubuntu-latest, windows-latest, macOS-latest]




   steps:


   - uses: actions/checkout@v3


   - name: Set up JDK 11


     uses: actions/setup-java@v3


     with:


       java-version: '11'


       distribution: 'temurin'


   - name: Build with Gradle


     uses: gradle/gradle-build-action@67421db6bd0bf253fb4bd25b31ebb98943c375e1


     with:


       arguments: build

actions 
build ( ubuntu-latest ) 
build ( windows-latest ) 
build ( macOS-latest
docker hub 



name: Java CI with Gradle









on:


 push:


   branches: [ "main" ]


 pull_request:


   branches: [ "main" ]







permissions:


 contents: read







jobs:


 build:







   runs-on: ${{matrix.os}}


strategy:
   matrix:
    os:[ubuntu-latest, windows-latest, macOS-latest]




   steps:


   - uses: actions/checkout@v3


   - name: Set up JDK 11


     uses: actions/setup-java@v3


     with:


       java-version: '11'


       distribution: 'temurin'


   - name: Build with Gradle
-name: Build and Push Docker Image 
run: 
name: Login to DockerHub
        uses: docker/login-action@v2
        with:
image: nanajanashia/demo-app
registry: docker.io 
          username: ${{ secrets.DOCKERHUB_USERNAME }}
          password: ${{ secrets.DOCKERHUB_TOKEN }}






     uses: gradle/gradle-build-action@67421db6bd0bf253fb4bd25b31ebb98943c375e1


     with:


       arguments: build


Build and push Docker images · Actions · GitHub Marketplace



