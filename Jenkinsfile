pipeline{
     	agent any
     	stages{
     		stage('version'){
     			steps{
     				checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'GitHUB-CREDENTIALS', url: 'https://github.com/ralphizuike/parallel_pipeline.git']]])
     			}
     		}
     		stage('parallel-job'){
     			parallel{
     				stage('sub-job1'){
     					steps{
     						echo 'action1'
     					}
     				}
     				stage('sub-job2'){
     					steps{
     						echo 'action2'
     					}
     				}
     				stage('sub-job3'){
     					steps{
     						echo 'action3'

     					}
     				}
     				stage('sub-job4'){
     					steps{
     						echo 'Dr Eng Ike'
     					}
     					
     				}
     			}

     		}
     		stage('codebuild'){
     			steps{
     				sh 'cat /etc/passwd'
     			}
     		}
     	}
     }
