# gitHub
>>github saves an initial version of code and we change 
it again and again as the work progress.
It saves all the progress so that it can track down all the changes wo made to our code 
and track down error as well.  

git track down all the changes we made meanwhile the github provides a plateform to save your projects 
and also helps people to work together

## git commands

>> git clone :- clone a repo or code from github to your local machine

>> git add :- to add the changes made in your local machine to github

>> git commit:- commit your changes with a message like what changes are made, which code is changed etc

>> git push :- push your changes to the git hub after gitadd, git commit to a given repository by https or shell

>> git status :- check status of our changes if it is added commited etc

# ssh(secure shell)

we generate a key to let the github know we are the real user who using the repository

>>ssh-keygen -t rsa -b 4096 -c 'your git hub email address'

-t is the type of key 
-b bits of key
-c additional comment

>>ls | grep testkey:- list all the files in present directory

>>cat testkey.pub:- print testkey.pub in cli or gitbash

>>pbcopy < direction:- copy file in the directed folder or just select the text of public key adnd aadd to github
>> git push origin master :- push all the file from the local machine to github

## Adding ssh key to ssh agent 
>> adding our privet key which is our identity as owner of the code to the local machine is known as adding to ssh agent

>> eval "$(ssh-agent -s)":- which starts our ssh agent and gives a agent pid num 

>> Agent Pid :- The ssh-agent is a helper program that keeps track of user's identity keys and their passphrases. 
		The agent can then use the keys to log into other servers 
		without having the user type in a password or passphrase again.

>> ssh-add [direction to privet key] :- key will b added to ssh-agent in local machine

## Creating repository local machine and push to the git hub

>> git init :- initiate the git repository 

>> git add . :- add all the file in the repository to git or staged to git
 
>> git commit -m :- commit all files -m = message

>> git remote add origin [ssh or https address]:- asking git to upload the changes to provided address

>> git push -u origin master :- -u = an upsteam after intializing it
			 you only need to use git push for further changes


# branches

>> git checkout -b [branchname] :- create a branch

>> git checkout [branchname]:- switch between branches

>> git diff [branchname] :- compare branch to another

>> git push {to main branchaddress} => will give a message to create a pull request

>> git merge [branchname] :- merge the branche to mainbranch

>> git branch -d [branchname] :- to delete the merged branch

## types of branches

1. Main branch :- it is the main code  or body of the repository or project which is going to be deployed

2. feature branch :- we can work on a code seperatily in feature branch without changing the main branch
			 until the code is good to go

3. hotfixbranch :- mainly used to fix bugs. to fix a bug create a hot fix branch and 
			fix the bug,and add the code to main branch


>> pull request :- they are made to pull the changes to one branch to another and 
	also for pull the changes made in github to local macahine or vice versa

 # git undoing

>> git reset [file name] :- reset the last staging

>> git reset HEAD~1:- reset staging and commit of last one commit if ~2 then two commits

>> git log :- gives log of all commits that are made in a reverse cronological order

>> git reset [hash id of commit from git log]:- reset the commits or remove commits after the hash id

>> git reset --hard [hashid]:- delete all the changes made after the hash id


>>github fork :- using git hub fork we can completly copy another code which gives full access to the code


` 
usage: ssh-keygen [-q] [-a rounds] [-b bits] [-C comment] [-f output_keyfile]
                  [-m format] [-N new_passphrase] [-O option]
                  [-t dsa | ecdsa | ecdsa-sk | ed25519 | ed25519-sk | rsa]
                  [-w provider] [-Z cipher]
       ssh-keygen -p [-a rounds] [-f keyfile] [-m format] [-N new_passphrase]
                   [-P old_passphrase] [-Z cipher]
       ssh-keygen -i [-f input_keyfile] [-m key_format]     
       ssh-keygen -e [-f input_keyfile] [-m key_format]     
       ssh-keygen -y [-f input_keyfile]
       ssh-keygen -c [-a rounds] [-C comment] [-f keyfile] [-P passphrase]
       ssh-keygen -l [-v] [-E fingerprint_hash] [-f input_keyfile]
       ssh-keygen -B [-f input_keyfile]
       ssh-keygen -D pkcs11
       ssh-keygen -F hostname [-lv] [-f known_hosts_file]   
       ssh-keygen -H [-f known_hosts_file]
       ssh-keygen -K [-a rounds] [-w provider]
       ssh-keygen -R hostname [-f known_hosts_file]
       ssh-keygen -r hostname [-g] [-f input_keyfile]       
       ssh-keygen -M generate [-O option] output_file       
       ssh-keygen -M screen [-f input_file] [-O option] output_file
       ssh-keygen -I certificate_identity -s ca_key [-hU] [-D pkcs11_provider]
                  [-n principals] [-O option] [-V validity_interval]
                  [-z serial_number] file ...
       ssh-keygen -L [-f input_keyfile]
       ssh-keygen -A [-a rounds] [-f prefix_path]
       ssh-keygen -k -f krl_file [-u] [-s ca_public] [-z version_number]
                  file ...
       ssh-keygen -Q [-l] -f krl_file [file ...]
       ssh-keygen -Y find-principals -s signature_file -f allowed_signers_file
       ssh-keygen -Y check-novalidate -n namespace -s signature_file
       ssh-keygen -Y sign -f key_file -n namespace file ... 
       ssh-keygen -Y verify -f allowed_signers_file -I signer_identity
                  -n namespace -s signature_file [-r revocation_file]
`

>> git pull :- pull the changes that are made buy your team mate 
