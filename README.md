# UdemyRSA_automationCICD

1. Download Jenkins from https://www.jenkins.io/download/
2. Run Jenkins with the following command:
`java -jar jenkins.war --httpPort=9090`
3. Open a browser and navigate to http://localhost:9090
4. Copy the password from the console and paste it in the Jenkins UI
5. Install the suggested plugins
6. Create an admin user
7. Start using Jenkins
8. Create a new job
9. Configure the job work with WebHooks between GitHub and Jenkins
10. Configure test and build steps, such as
`mvn test -PRgression`
11. Configure the job to run on a push event
12. (Optional) Use [ngrok]("https://ngrok.com/") to expose the Jenkins server to the internet, instead of using the localhost one
13. Do push to the repository and see the Jenkins job running
