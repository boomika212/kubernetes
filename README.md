# Kubernetes
KUBERNETES CONFIGURATION AND CONTEXTS:-
kubectl config view 
kubectl config get-contexts
kubectl config set-credentials name --username=.....  --password=....
----------------------------------------------------------------------------------------------------------------
TO CREATE A DEPLOY.YAML FILE AND THE POD IS CREATED NOW 
cat <<EOF | kubectl apply -f -
apiVersion: v1
kind: Pod
metadata:
  name: busybox-sleep
spec:
  containers:
  - name: busybox
    image: busybox
    args:         
    - sleep
    - "1000000"
---
apiVersion: v1
kind: Pod
metadata:
  name: busybox-sleep-less
spec:
  containers:
  - name: busybox
    image: busybox           
    args:
    - sleep
    - "1000"
EOF
----------------------------------------------------------------------------------------------------------------
PROERTIES THAT ARE SET FOR THE CONTAINER IN YAML FILE 

name
image
command
args
workingDir
ports
env
resources
volumeMounts
livenessProbe
readinessProbe
lifecycle
terminationMessagePath
imagePullPolicy
securityContext
stdin
stdinOnce
tty
