+ create ssh key pair using `ssh-keygen` command
+ Make sure it is stored in ~/.ssh folder
+ Now `cat` the public key copy it.
+ login to remote server and add ssh public key according to their documentation
+ Now add private key to your local machine ssh agent
+ First start ssh agent `eval ssh-agent`
You will get output with a id
+ Now add the key `ssh-add <path-to-key>`
+ Now ssh into the remote server

+ Command to test the key `ssh -T git@github.com`
+ git remote set-url origin git@github.com:username/your-repository.git

