Created maven.yml file 
name: Java CI with Maven
on:
  push:
    branches: [ "main" ]

jobs:
 compile:
    name: Compile Project 
    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v4
    - name: Set up JDK 17
      uses: actions/setup-java@v4
      with:
        java-version: '17'
        distribution: 'temurin'
        cache: maven
    - name: Build with Maven
      run: |
       mvn compile
       echo "Complie done"
 test:
    name: Execute unit test project
    runs-on: ubuntu-latest
    needs: compile

    steps:
    - uses: actions/checkout@v4
    - name: Set up JDK 17
      uses: actions/setup-java@v4
      with:
        java-version: '17'
        distribution: 'temurin'
        cache: maven
    - name: Build with Maven
      run: mvn -B test --file pom.xml
 build:
    name: build project
    runs-on: ubuntu-latest
    needs: test

    steps:
    - uses: actions/checkout@v4
    - name: Set up JDK 17
      uses: actions/setup-java@v4
      with:
        java-version: '17'
        distribution: 'temurin'
        cache: maven
    - name: Build with Maven
      run: mvn -B package --file pom.xml
      
    - uses: actions/upload-artifact@v7
      with:
        name: boardgame
        path: target/*.jar
*******************************************************************************************************************************************
     <img width="1898" height="977" alt="image" src="https://github.com/user-attachments/assets/a2f48cfd-8055-493b-8e02-5124fcbb627b" />  
     <img width="1917" height="935" alt="image" src="https://github.com/user-attachments/assets/4b3e91c3-e3b9-46e3-8411-e91c4a01f36a" />

   
