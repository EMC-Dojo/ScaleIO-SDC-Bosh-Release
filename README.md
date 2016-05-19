###ScaleIO Bosh Release
ScaleIO contains 3 major components:
 - MDM - Management component
 - SDS - Storage component
 - SDC - Client

 This Bosh release only contains the SDC, which is required to be placed in the client VM in order to access volumes hosted in ScaleIO.

###Creating Bosh Release

 1. Obtain code from Github:
 2. Go into the directory:
 3. Create Bosh Release

 ```
 git clone https://github.com/EMC-CMD/ScaleIO-SDC-Bosh-Release.git
 cd ScaleIO-SDC-Bosh-Release
 bosh create release
 ```
###About CF-Persistence
In order to set up CF-Persistence, the SDC, RexRay, and Volman bosh releases need to colocate in Diego Cells VMs. More documentation coming soon.

###Deploying Scaleio SDC release
* Git clone this project into your working directory
```
cd ~/workspace
git clone https://github.com/EMC-CMD/ScaleIO-SDC-Bosh-Release
cd ~/workspace/ScaleIO-SDC-Bosh-Release
```
* Upload Bosh stemcell
```
bosh upload stemcell https://bosh.io/d/stemcells/bosh-aws-xen-hvm-ubuntu-trusty-go_agent?v=3215
```
* Use manifest from template folder

Please refer to examples directory to see manifest template and fill in the information you want.

* Create, upload, and deploy sdc release
```
bosh deployment {PATH_TO_YOUR_MANIFEST}
bosh -n create release --force &&
bosh -n upload release &&
bosh -n deploy
```

###Contact
- Email: [EMCDojo@emc.com](mailto:EMCDojo@emc.com) 
- Twitter: [@EMCDojo](https://twitter.com/hashtag/emcdojo)
- Blog: [EMC Dojo Blog](dojoblog.emc.com)
