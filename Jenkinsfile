
pipeline {
  agent any 
  //ENVIRONMENT BLOCK

  //This block is used to define environment variables that can be used throughout the pipeline.
  //These variables can be used in any stage of the pipeline.
  //They are useful for defining constants or configuration values that are needed in multiple stages.
  //For example, you might want to define the name of the application, the version number, or the build number.
  //In this case, we are defining three environment variables: APP_NAME, APP_VERSION, and APP_BUILD_NUMBER.
  //APP_NAME is set to 'DSOC3 Web-APP', APP_VERSION is set to '1.0.0', and APP_BUILD_NUMBER is set to the current build number.
  //These variables can be used in any stage of the pipeline by referencing them with the env prefix.
  //For example, you could use ${env.APP_NAME} to reference the APP_NAME variable in a stage.
  //This is useful for keeping your pipeline code clean and organized, and for avoiding hardcoding values in multiple places.
  //The environment block is optional, but it can be very useful for defining variables that are used in multiple stages.
  //In this case, we are defining three environment variables: APP_NAME, APP_VERSION, and APP_BUILD_NUMBER.
  environment {
    //ENVIRONMENT VARIABLES
    ENV_VAR1 = 'env var-1 Value'
    ENV_VAR2 = 'env var-2 Value'
    ENV_VAR3 = 'env var-3 Value'
  } 
  stages{
    stage('Build') {
      steps {
        echo 'Building DSOC3 Web-APP..'
        echo "Value of ENV_VAR1: ${env.ENV_VAR1}"
        
        
      }
    } //EO Stage Build
      stage('Test') {
        steps {
          echo 'Testing DSOC3 Web-APP..'
          echo "Value of ENV_VAR2: ${env.ENV_VAR2}"
      } 
       } //EO Stage Test
     stage('Deploy') {
        steps {
          echo 'Deploying DSOC3 Web-APP..'
          echo "Value of ENV_VAR3: ${env.ENV_VAR3}"
        }
      } //EO Stage Deploy
    } //EO stages
    //POST BLOCK
    post{
      always {
        echo 'This will always run'
      }
      success {
        echo 'This will run only if the build is successful'
      }
      failure {
        echo 'This will run only if the build fails'
      }
      unstable {
        echo 'This will run only if the build is unstable'
      }
    }
  }   //EO pipeline
