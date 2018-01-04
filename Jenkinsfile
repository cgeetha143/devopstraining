node {
   stage('Build docker container') {
       checkout([$class: 'GitSCM', ...])
       sh "docker build -t webapp ."
   }
   stage('test build') {
       sh "mkdir -p rspec screenshots"
       sh "docker run -v /var/jenkins_home/workspace/webapp/rspec/junit.xml:/myapp/junit.xml -v /var/jenkins_home/workspace/webapp/screenshots:/myapp/tmp/capybara -v webapp bundle exec rspec"
   }
   stage('Results') {
      junit 'rspec/junit*.xml'
      archive 'screenshots/*'
   }
