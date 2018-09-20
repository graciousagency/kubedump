# kubedump
Your one-stop command to dump kubernetes configs to files. We use this to add our configs to git for safe-keeping.

## Installation
Check it out, move it to /usr/local/bin/kubedump and chmod +x it
```
git clone https://github.com/graciousagency/kubernetes-dump.git
cd kubernetes-dump
mv kubedump /usr/local/bin/
chmod +x /usr/local/bin/kubedump
```

## Usage
Now if you run it when you have a cluster configured it will dump the following resources. They are placed in subdirectories matching the resource type.
* configmap
* cronjob
* deployments
* horizontalpodautoscalers
* ingresses
* limitranges
* persistentvolumeclaims
* persistentvolumes
* services
* statefulset

## Notes
* Ingresses are exported in a seperate loop WITHOUT --export to preserve the ip they are currently using
* You must have kubectl installed
* I highly recommend using [kubectx](https://github.com/ahmetb/kubectx) to switch between projects easily
