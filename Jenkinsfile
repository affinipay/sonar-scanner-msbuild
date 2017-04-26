pipeline {
    agent {
        node {
            label 'msbuild'
        }
    }

    stages {
        stage('Checkout') {
            steps {
		        checkout scm
            }
        }
        stage('Build'){
            steps {
                bat 'nuget restore SonarQube.Scanner.MSBuild.sln'
                bat "\"${tool 'MSBuild'}\" SonarQube.Scanner.MSBuild.sln /p:Configuration=Release /p:Platform=\"Any CPU\" /m /p:ProductVersion=1.0.0.${env.BUILD_NUMBER} /p:FrameworkPathOverride=\"C:\\Program Files (x86)\\Reference Assemblies\\Microsoft\\Framework\\.NETFramework\\v4.6.1\""
            }
        }
        stage('Archive') {
            steps {
		        archive 'bin/Release/**'
            }
        }
    }
}
