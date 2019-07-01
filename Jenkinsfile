node {
    
docker.image('node:6-alpine').inside('-p 3000:3000') {
    
   stage('Preparation') { 
      git 'https://github.com/JamesMellors/simple-node-js-react-npm-app.git'
    
   }
   stage('Build') {
      sh 'npm install'
   }

   stage('Deliver'){
       sh './jenkins/scripts/deliver.sh'
       input message: 'Finished using the web site ? (Click "Proceed" to continue)'
       sh './jenkins/scripts/kill.sh'
   }
}
}