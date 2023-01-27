# github_checkov

Lacework wrapped the soluble CLI in Docker a container and pushed it here https://hub.docker.com/r/ryansheldrakelw/soluble-scan. 

This container will scan the contents of a volume mount with the Soluble CLI. In order for the scan to be uploaded two environment variables must also be passed in.

# Invocation is as follows

docker run -it -v "local machine directory containing IaC code":/tmp/soluble-temp -e SOLUBLE_API_TOKEN="$SOLUBLE_API_TOKEN" -e LW_IAC_ORGANIZATION="$LW_IAC_ORGANIZATION" ryansheldrakelw/soluble-scan

In the above the variables are pulled in from local env variables and passed into the container as env variables to auth the scan to the Soluble user interface. Your Soluble Org ID which is numeric can be found in the Soluble UI > settings > Organizations.

