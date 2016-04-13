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

###Contact
- Slack Channel:
  - Organization: <http://codecommunity.slack.com>
  - Channel: `#project-rexray`
- Contact: [Victor Fong](mailto:victor.fong@emc.com) [@EMCDojo](https://twitter.com/hashtag/emcdojo)
- Blog: [EMC Dojo Blog](dojoblog.emc.com)
 
 
 
 

 
