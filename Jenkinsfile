pipeline {
  agent {
    node {
      label 'Unity-Windows'
    }

  }
  stages {
    stage('Build StandaloneWindows64') {
      environment {
        BUILD_TARGET = 'StandaloneWindows64'
      }
      steps {
        bat 'bash -c CI/build.sh'
      }
    }

    stage('Archive') {
      steps {
        bat '$BASH -c CI/archivebuild.sh'
      }
    }

  }
  environment {
    UNITY_EXECUTABLE = '/mnt/d/Program\\ Files/Unity\\ Editors/2020.1.4f1/Editor/Unity.exe'
    PROJECT_PATH = 'E:/My Code/PersonalProjects/Unity/Unity3D-Jenkins'
    BUILD_NAME = 'Unity3D-Jenkins'
    ARTIFACTS = '_artifacts'
    BASH = 'C:\Windows\System32\bash.exe'
  }
}