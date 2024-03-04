# Steps to configure your IDE to work with GitHub via SSH:

Generate an SSH key pair on your local machine if you haven't already.
Copy the public key (id_rsa.pub) to your GitHub account settings.

Create .ssh folder in your home directory. 
    If you don't have an .ssh folder, you can create one and place the key pair files in it.
create config file [with out any extension] in .ssh folder with the following content
    Host github.com
        HostName github.com
        User git
        IdentityFile ~/.ssh/id_rsa

    Replace ~/.ssh/id_rsa with the path to your private key file.
    
    This configuration tells the SSH client to use the specified private key when connecting to GitHub.
    
    

# Set your username and email in the Git configuration:
    git config --global user.name "Satish-Kalari"
    git config --global user.email "sarvag@gmail.com"

# Set the URL for the Git repository:
    git remote set-url origin <repository-url>
    
    Replace <repository-url> with the URL of your Git repository.


    
