
pipeline{
    agent any
    stages{
        stage("Deploy portofolio  on AWS S3"){
            steps{
              withAWS(credentials: "AWS-ID", region: 'us-east-1'){
                s3Upload(file:'index.html', bucket:'aws-ug-conakry', path:'')
                s3Upload(file:'error.html', bucket:'aws-ug-conakry', path:'')
                s3Upload(file:'style.css', bucket:'aws-ug-conakry', path:'')
                s3Upload(file:'script.js', bucket:'aws-ug-conakry', path:'')
                s3Upload(file:'competition.png', bucket:'aws-ug-conakry', path:'')
                s3Upload(file:'conference.png', bucket:'aws-ug-conakry', path:'')
                s3Upload(file:'facebook.png', bucket:'aws-ug-conakry', path:'')
                s3Upload(file:'handshake.png', bucket:'aws-ug-conakry', path:'')
                s3Upload(file:'linkedin.png', bucket:'aws-ug-conakry', path:'')
                s3Upload(file:'meetup.png', bucket:'aws-ug-conakry', path:'')
                s3Upload(file:'nimba-2.png', bucket:'aws-ug-conakry', path:'')
                s3Upload(file:'ug-conakry.png', bucket:'aws-ug-conakry', path:'')
                s3Upload(file:'whatsapp.png', bucket:'aws-ug-conakry', path:'')
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

