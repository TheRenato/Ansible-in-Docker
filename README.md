# Ansible-in-Docker

Based on the article

https://duffney.io/containers-for-ansible-development

## How to use

Again, this information is from the link above.


docker run --rm --volume "$(pwd)":/ansible -w /ansible renato81/ansible-in-docker <thePlaybookFile> <theHost>


Let's go! What is happening above?

'--rm' This will remove the container after it has exited. Why? beacuse after it has run the ansible playbook it will exited. And the container will just hang on. This wey we can remove it after the job is done.

'"$(pwd)":/ansible' We will set current folder we execute the command in a volume at "/ansible" in the container.

'-w /ansible' We have set that folder as the working folder.

'renato81/ansible-in-docker' the docker image. You are free to use mine. But you are free to forke this repo and push up your own image. But be then you change this part.
