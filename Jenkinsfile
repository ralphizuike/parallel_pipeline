pipeline{
     	agent any
     	stages{
     		stage('version'){
     			steps{
     				git checkout
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