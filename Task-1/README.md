#  Task 1: Server Setup and SSH Configuration

         This task demonstrates how to securely connect to an AWS EC2 Ubuntu instance using:

# Step-1 :
         In our local machine Linux and Windows, Mac open terminal and create key-pair using command "ssh-keygen" created two key.

          id_ed25519        (Private Key)
          id_ed25519.pub    (Public Key)


          View the public key 
          "cat ~/.ssh/id_ed25519.pub"

          Copy this public key.  

# Step-2 :
         open AWS and create instance and key-pair for using secure loging " Server Setup and SSH Configuration"  Public Key stored in   ~/.ssh/authorized_keys past the key.
 
         Configure SSH Directory Permissions (On EC2)

         chmod 700 ~/.ssh
         chmod 600 ~/.ssh/authorized_keys


# Step-3 :
          now we test this for our local terminal "ssh ec2-13-235-18-50.ap-south-1.compute.amazonaws.com"  

          press Enter: Secure Passwordless SSH Login 



# Note :
     AWS using secure connection with the help of key value pair. 


