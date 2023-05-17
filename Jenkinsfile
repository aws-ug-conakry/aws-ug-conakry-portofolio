
pipeline{
    agent any
    stages{
        stage("Deploy portofolio  on AWS S3"){
            steps{
              withAWS(credentials: "AWS-ID", region: 'us-east-1'){
                s3Upload(file:'index.html', bucket:'aws-ug-conakry', path:'')
                s3Upload(file:'error.html', bucket:'aws-ug-conakry', path:'')
                s3Upload(file:'css/style.css', bucket:'aws-ug-conakry', path:'css/')
                s3Upload(file:'js/script.js', bucket:'aws-ug-conakry', path:'js/')
                s3Upload(file:'images/*', bucket:'aws-ug-conakry', path:'images/')
             
              }
            }
            post{
                always{
                     echo "Ce bloc s'affiche dans tous les cas"
                }
                success{
                    echo "Ce bloc s'affiche quand c'est tout est success"
                    // notification par mail, slack
                }
                failure{
                     echo "Ce bloc s'affiche quand y'a une erreur"
                    // notification par mail, slack
                }
            }
        }
    }
    post{
        always{
            echo "Ce bloc s'affiche dans tous les cas"
        }
        success{
            echo "Ce bloc s'affiche quand c'est tout est success"
            // notification par mail, slack
        }
        failure{
           echo "Ce bloc s'affiche quand y'a une erreur"
           // notification par mail, slack
        }
    }
}

