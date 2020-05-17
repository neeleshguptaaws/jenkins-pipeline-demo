node()
{
    stage "Checkout Code"
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/nvn17git/nvnshoppingcart']]])
    
    stage "Build Code"
        sh "mvn clean package"
        
    stage "Deploy" 
        sh "echo 'Hello world'"
        sh 'sudo cp /var/lib/jenkins/workspace/pipeline-1/target/nvnshoppingcart.war /opt/war_files/'
        
    
}