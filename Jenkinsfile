node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image'){

sh "docker build -t lornanyokabi:latest ."
}

stage('Docker login to hub and push the image'){
sh "docker login -u 'lornanyokabi' -p 'Muranga1234' "
sh "docker tag lornanyokabi:latest lornanyokabi/wangeshilorna:latest"
sh "docker push lornanyokabi/wangeshilorna"
}

stage('Apply changes to the environment') {
sh "ls -l"
sh "php -S localhost:5000"
}


}
