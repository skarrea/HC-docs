# On-boarding

## Overview

### Purpose

Describe the steps and responsibilities required to onboard new users to the Hunt Cloud environment.

### Scope

This guide covers initial introductions, account setup, cloud access, project organization.

### Audience

Supervisors, lab leaders, lab coordinators, and new users.

### Responsibilities

- **Supervisor / Lab leader:** ensure the new user is introduced to this document, and assign a mentor _(if the supervisor is not capable of being the mentor)_.

  > By default the mentor should be the supervisor.

- **Lab leader:** approve the new user data access.

- **Lab coordinator:** create node user accounts, configure group permissions, and enable required services (Docker, storage).

- **New user:** make sure that the checklist is completed, read this wiki documents, and request additional access or help with software installation when needed.

### Prerequisites For New User

- Send a new user request and sign the new user agreement.

- Active account in the home lab following HUNT Cloud Team instructions.

- SSH key and workbench access.

- Contact details for lab leader and lab coordinator.

## Checklist For Supervisors/Mentors

1. Provide the new user with this on-boarding document.

2. Explain the cloud concept, layers of protection, and the need for it.

3. Explain the hierarchy of the cloud: space, lab and nodes.

4. Explain the roles of space and lab administrators.

5. Introduce the HUNT Cloud official documentation and their sections.

6. Explain how to make an order on service desk.

7. Explain how to use workbench.

   > Clarify that the storage is differ on workbench from the main home lab.

   > Clarify that is the main way to access the cloud.

8. Introduce other cloud access options (eg. ssh terminal, VS Code, MobaXterm).

9. Explain the folders and storage organization within the lab (work, scratch, archive) and their established subfolders (e.g. `/mnt/work/common`; `/mnt/archive/datasets`).

10. Request node account if GPU or non-managed nodes are required.

11. Confirm storage and group permissions.

12. Introduce the basics linux commands.

    > Check https://www.geeksforgeeks.org/linux-unix/linux-commands-cheat-sheet/

13. Make sure to activate system-wise **Anaconda** on the Lab. Also any other already installed software (e.g., ITKSnap, MATLAB, 3D Slicer, elastix)

    > **[For Digital Life Lab]** Instructions are in the file `/mnt/work/software/SoftwareGuide.txt`

14. Explain the difference between lab level software and user specific software, and how to install user specific software.

15. Explain that software on the workbench is not the same as the software in the lab as the software in the workbench is run in a container.

16. Explain who can access which data on the cloud.

17. Explain data privacy and handling principles.

18. Point them to read and follow the steps of the following section [Procedure For New Users](#procedure-for-new-users).

## Procedure For New Users

1. Make sure that the above checklist [Checklist For Supervisors/Mentors](#checklist-for-supervisorsmentors) was done and you understood the explanation and all is clear for you.

2. Create a user folder  
   Path: `/mnt/work/users/username`

   - This is your user personal folder. You can organize it as you wish.

3. Project folder organization

   - Maintain this organization and don't change it.

   - Enforce good data practices.

   - Learn the difference between Linux symbolic links vs copies.

4. Cloud privacy

   - Know which data you can and can't access.

   - Learn how to restrict others from accessing your folders _if deemed necessary_.

5. Compute nodes and user accounts

   > **This should be guided and explained by the lab coordinator**

   - Use only if you will need to use GPUs or non-managed machines.

   - Ask the lab coordinator to create you a user on the node.

     > [NOTE] Your username at the node shall be the same of the home lab's.

   - Ask for explanation of the differences between GPU nodes and the home instance.

   - Ask for explanation of the data transfer between GPU nodes and home instance.

   - If there is a need for it, ask the lab coordinator to grant you **sudo** access.

     > [NOTE] You will not be grant sudo access automatically.

   - Setup your requirements on the node:

     - Install user-specific mamba.

     - Install any other software you may need (e.g. itk-snap, MATLAB,..etc) also user-specific.

   - Ask the lab coordinator if is Docker already installed on the node machine.

     > [NOTE] Docker shall be installed system-wide and users shall be added to the docker group.

6. Data transfer policy

   - You **MUST read** the Data Treatment section on this internal wiki.

   - Never download data without **explicit written permission from Lab leader**, except for material allowed for publications.
