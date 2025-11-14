# On-boarding
Supervisors should introduce new hires to the on-boarding and off-boarding documents. Understand the hierarchy of the cloud: space, lab and nodes. Understand the roles lab leader and lab coordinator is most important. 

Show how to do orders from the service desk. Introduce people to the work-bench and understand how storage is different from the main home lab. 

Introduce people to the various ways of accessing hunt cloud; work-bench, ssh terminal, moba and VSCode. Main way of accessing the cloud for new hires will be work-bench.

Explain storage organization. How should new projects be organized. Oraganization is standard enough to be summarized in a single document. 

Introduce to the basic functions and commands on linux. 

How to use software: what is user specific and what exists on a lab/node level. Anaconda is installed on a lab level. Software on the workbench is not the same as the software in the lab as the software in the workbench is run in a container.

**Who is responsible for introducing all of these concepts?**

**Procedure for new users:**
1. Creare a user folder in /mnt/work/users/username 
2. Explain how to organize new folder projects. Enforce good data practices. Explain linux links vs copies.
3. Explain cloud privacy - who can access which data? Who can access your data?
4. Compute nodes - the lab coordinator should create a user for each new user. How are the gpu nodes different from the home instance. We have sudo access on these nodes - we might not give everyone sudo access.  **Can we make docker not need sudo and rely on devcontainers from environments?** We have limited resources on gpus - coordinate with other people on the gpus space. Make an install script to install user specific mamba and install docker system wide. Make sure to set up the usergroup for users to use docker. **Ask if docker is already installed on the spot/gpu machines?**
5. Never download data - if you need that you should have explicit written permission from Tone. Even if working with the data locally is easier. However, anything you can put in a publication can be downloaded. 
6. **Recommendations:** use git, but be careful what you upload. Keep data outside git repo in a separate repo to prevent fuck-ups. 