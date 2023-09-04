def branchname="feature334"
String randomString = org.apache.commons.lang.RandomStringUtils.random(32, true, true)
pipeline{
    agent any
    // }
    environment {
        ADITYA = "aditya"
        PD_INTEGRATION_KEY = "e742dd74641b4205c04e235904079307"
        PD_SELF_KEY = "${randomString}"
        PD_INCIDENT_SUMMARY = "summary- ${randomString}"
        PD_INCIDENT_SOURCE = "JenkinsCI"
        PD_INCIDENT_SEVERITY = "Critical"
        
    }
    
    stages {
        
        stage('1')
        {
            
                steps{
    //                 sh """
    //                 env.SOMETHING="aditya"
    //                 // ADITYA="xvxvxvx"
    //                 // pipelineStore.put("key",[name:"adbv",version:23])
		  //  """
		  script {
    		  if(branchname.substring(0,6)=="feature"){
                        // git branch: 'main', credentialsId: '02c515b6-f2d9-433b-914c-a18921a5dad1', url: 'https://github.com/AdityaNutulapati/test-s3-1'
                    echo "hehhee"  
                }
            
		  }  
        }
        }
        stage('2')
        {
            
                steps{
                    // sh """
                    // env.SOMETHING="done"
                    // echo ${env.SOMETHING}
                    script {
                    env.SOMETHING = "2"
                    echo "${PD_SELF_KEY}"
                    // env.SOMETHING = giveMeKey()
                    echo "$randomString"
                    echo "SOMETHING = ${env.SOMETHING}"// creates env.SOMETHING variable
                }
		  //  """
                    // git branch: 'main', credentialsId: '02c515b6-f2d9-433b-914c-a18921a5dad1', url: 'https://github.com/AdityaNutulapati/test-s3-1'
                    
                }
                
        }
        
    
    }
    // post{
    //     success{
    //         script{
    //             pagerduty(resolve:true,routingKey:"$PD_INTEGRATION_KEY",incidentSummary:"$PD_INCIDENT_SUMMARY",incidentSource:"$PD_INCIDENT_SOURCE",dedupKey:"$PD_SELF_KEY")
    //             echo "SUCCESS"
    //         }
    //     }
    //     failure {
    //         script{
    //             pagerduty(resolve:false,routingKey:"$PD_INTEGRATION_KEY",incidentSummary:"$PD_INCIDENT_SUMMARY",incidentSource:"$PD_INCIDENT_SOURCE",incidentSeverity:"$PD_INCIDENT_SEVERITY",dedupKey:"$PD_SELF_KEY")
    //             echo "PD SENT- STAGE FAILURE"
    //         }
    //     }
    //     aborted {
    //         script{
    //             pagerduty(resolve:false,routingKey:"$PD_INTEGRATION_KEY",incidentSummary:"$PD_INCIDENT_SUMMARY",incidentSource:"$PD_INCIDENT_SOURCE",incidentSeverity:"$PD_INCIDENT_SEVERITY",dedupKey:"$PD_SELF_KEY")
    //             echo "PD SENT- STAGE ABORTED"
    //         }
    //     }
    //     unstable {
    //         script{
    //             pagerduty(resolve:false,routingKey:"$PD_INTEGRATION_KEY",incidentSummary:"$PD_INCIDENT_SUMMARY",incidentSource:"$PD_INCIDENT_SOURCE",incidentSeverity:"$PD_INCIDENT_SEVERITY",dedupKey:"$PD_SELF_KEY")
    //             echo "PD SENT- STAGE UNSTABLE"
    //         }
    //     }
        
    // }
}
