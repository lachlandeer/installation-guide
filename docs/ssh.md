# Setting Up SSH Keys

SSH Keys make logging into servers and the like simpler since we don't need passwords.
Let's create a new one for the machine

## Creating a SSH Key

In the terminal type:

```{bash}
ssh-keygen
```

Usually I don't create a passphrase or give the file a custom name, so it ends up as `id_rsa`

## Copying the SSH Key to Servers

Now we want the copy the public part of our SSH key to the servers one logs into.
Do this as follows:

```{bash}
ssh-copy-id -i ~/.ssh/id_rsa.pub user@host
```

You will be prompted for the passcode to log into the server when you do this.

Once this works, we want to check that you can now log in using the ssh key:

```{out}
ssh user@host
```

which should take you to the terminal of the server you logged in to.

## Automated Login to Server with Terminal Profiles

One can create 'Profiles' on their own terminal so automate the login to a server to a simple point-and-click.
Here's how:

* Open a terminal window
* Go to the menu bar and click 'Preferences' to open up a menu window
* Click the `+` Next to the Profiles menu
* Name your profile something useful
* In that profile go to 'Command'
* Select the 'Run command as login shell' and 'Run custom command instead of my shell'
* In the custom command box add the ssh command `ssh user@host`
* Close the Preferences menus

Now when you click the down-arrow you should get a choice of which terminal you want to open. 
If you click on the profile you just created you should be able to ssh into your server (provided any required VPN is on). 

## Add to GitHub

We also want to add the new ssh key to our github account so we can clone, push and pull using the SSH key rather than entering our username and password each time.
Proceed as follows:

* Log in to your GitHub profile
* Go to Settings
* Go to 'SSH and GPG Keys'
* Click 'New SSH Key'
* Give the new key a name and copy across the contents of the public part of your key created above.