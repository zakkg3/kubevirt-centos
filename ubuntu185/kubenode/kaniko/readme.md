# create docker secretName

        kubectl create secret docker-registry regcred --docker-server=<your-registry-server> --docker-username=<your-name> --docker-password=<your-pword> --docker-email=<your-email>
        
        
# Create the Dockerfile


        kubectl create configmap dockerfile --from-file=./Dockerfile
