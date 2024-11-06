pipeline{ 
agent any 
stages{ 
stage('checkout the code from github'){ 
steps{ 
git url: 'https://https://github.com/Surya182002/BankingApp.git/' 
echo 'github url checkout' 
} 
} 
stage('codecompile with surya'){ 
steps{ 
echo 'starting compiling' 
sh 'mvn compile' 
} 
} 
stage('codetesting with surya'){ 
steps{ 
sh 'mvn test' 
} 
} 
stage('qa with surya'){ 
            steps{ 
                sh 'mvn checkstyle:checkstyle' 
            } 
        } 
        stage('package with surya'){ 
            steps{ 
                sh 'mvn package' 
            } 
        } 
        stage('run dockerfile'){ 
          steps{ 
               sh 'docker build -t myimg .' 
           } 
         } 
         
    } 
}
