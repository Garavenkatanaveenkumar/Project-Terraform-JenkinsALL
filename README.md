node {
    stage('checkout') { 
        git branch: 'main', credentialsId: 'cd366127-54ec-4215-b962-902cedf32f97', url: 'https://github.com/Garavenkatanaveenkumar/Project-Terraform-JenkinsALL.git'
    }
    stage('init') {
        sh "terraform init -reconfigure"
        
        }
    stage('action') {
        sh "terraform ${action} --auto-approve"
        
        }
}


The project parametrized ->choice parameter
 action
 apply
 destroy
 
