node(){
    stage ("cloning the code"){
        checkout([$class: 'GitSCM', branche: [[name: '*/develop']], doGenerateSubmoduleConfigurations: false, extensions: [], gitTool: 'Default', submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/csenapati12/maven-samples.git']]])

    }
    stage ("Compile"){
        bat '''set JAVA_HOME=C:\\Program Files\\Java\\jdk1.8.0_144
mvn package'''
    }
   
   
    stage ("Deploy the code"){
        bat '''cd C:\\chaitanya\\devops\\training\\july-batch
cmd /k deploy.bat'''

    }
}
