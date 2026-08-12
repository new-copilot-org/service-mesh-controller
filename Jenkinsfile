<![CDATA[
// Source: https://github.com/uchennaofodile/movie-land (No explicit license, educational use)
// Test case: React app deployment to Netlify
pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
        sh 'npm run build'
      }
    }
    stage('Deploy') {
      environment {
        NETLIFY_SITE_ID = 'classy-paletas-f45a67'
        NETLIFY_AUTH_TOKEN = credentials('netlify-token')
      }
      steps {
        sh 'npm install -g netlify-cli'
        sh 'netlify deploy --prod --dir=build --site=$NETLIFY_SITE_ID --auth=$NETLIFY_AUTH_TOKEN'
      }
    }
  }
}
    ]]>