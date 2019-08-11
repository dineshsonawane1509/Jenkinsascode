node()
{
    stage "Checkout Code"
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/dineshsonawane1509/Jenkinsascode.git']]])
    
    stage "Build Code"
        sh "mvn clean package"
        
    stage "Deploy Application"
        //sh 'rm /var/lib/tomcat/webapps/nvnshoppingcart*'
        sh 'sudo cp **/*.war /opt'
}

