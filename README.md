# Ansible-Jenkins integration and auto build jenkins functionality
# Install ansible on Jenkins master instance 
apt-add-repository ppa:ansible/ansible
apt-get update
apt-get install ansible
# Create a new repository in github named 'ansible-jenkins'
# Back to terminal and create a directory named as 'ansible-jenkins'
mkdir jenkins-ansible
cd jenkins-ansible
# Create a file named docker.yml and modify the login and image details accordingly
# Once done, save the file and push to Git repository
git init
git add *
git commit -m "Initial commit"
git remote add origin https://github.com/<username>/jenkins-ansible.git
git push -u origin master
# Login to jenkins UI and install ansible plugin
# Add the root user credentials to Jenkins
# Create a new Freestyle project and provide repository url under source code management "https://github.com/<username>/jenkins-ansible.git"
# Update Build Triggers 
H/5 * * * *
# Invoke ansible ad hoc command to install python-pip package
# Invoke ansible ad hoc command to install docker-py python module
# Invoke Ansible playbook to execute the docker playbook from repository
# Save, Build and test the job
# Update the port in docker.yml file, push it again to github and verify the auto build happening in Jenkins
