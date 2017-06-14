#!/usr/bin/groovy

node {
  stage('scm'){
    checkout scm
  }
  stage('test'){
    sh 'mvn test'
  }
  stage('install'){
    sh 'mvn install'
}
