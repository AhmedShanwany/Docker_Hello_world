 pipeline {

     agent any
	 
	 stages{
	 
		stage ('clone repo from hub'){
			steps{
				
				git branch: 'main', credentialsId: 'none', url: 'https://github.com/AhmedShanwany/Docker_Hello_world.git'
				
			}
		}
		
        stage ('List Directory and set jdkpath') {
            steps {
                script {
				bat 'dir'
				//bat 'set path=C:\\Program Files (x86)\\jdk-19_windows-x64_bin\\jdk-19.0.2\\bin'
				
                     }
            }
        }
      
        stage ('Compile code') {
            steps {
				script{
				bat 'javac Hello_world.java'
				}
			}
        }
		stage ('execute code') {
            steps {
				script{
                bat 'java Hello_world'
                
				}
			}
        }
		}
		}