# MyProjectPython
# must be unique in a given SonarQube instance
sonar.projectKey=my:project

# --- optional properties ---

# defaults to project key
#sonar.projectName=My project
# defaults to 'not provided'
#sonar.projectVersion=1.0
 
# Path is relative to the sonar-project.properties file. Defaults to .
#sonar.sources=.
 
# Encoding of the source code. Default is default system encoding
#sonar.sourceEncoding=UTF-8
docker run \
    --rm \
    -e SONAR_HOST_URL="http://${SONARQUBE_URL}"  \
    -v "${YOUR_REPO}:/usr/src" \
    sonarsource/sonar-scanner-cli
