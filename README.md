## This is How to Connect the  GitHub ssh to my pc

#### The following steps use to generate and use SSH in the github, using commands for git bash use to connect the RSA to the github
1. First generate the ssh key:
   - Run the following command 
     ```
     $ ssh-keygen
     ``` 

   - Save it in the root ~ directory saved as "ssh_key_name" by passphrase, you can choose one and dont forget it.

2. Second, got to https://github.com/settings/ssh/new and :
    - add a title to your key.
    - copy the ssh_key_name.pub content.
    - paste it in the Key field and click "Add SSH Key".

3. Third, Using the private Key:
   - every time you start a new terminal you need to initiatize the ssh-agent 
   - You can use the Private key by using this commands
       ```
       $ eval `ssh-agent`
       $ ssh-add ~/ssh_key_name
       ```
   - Now, mutching with SSH url :
       ```
       $ git clone git@github.com:aissamyekhlef/ssh-test.git
       ```

Congratulations, Now you can use the SSH on the GitHub.