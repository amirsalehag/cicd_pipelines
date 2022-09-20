# To install GitLab Runner
* Add the official GitLab repository:  

For Debian/Ubuntu/Mint:
```
curl -L "https://packages.gitlab.com/install/repositories/runner/gitlab-runner/script.deb.sh" | sudo bash
```
(Debian users can use APT pinning.)  
```
cat <<EOF | sudo tee /etc/apt/preferences.d/pin-gitlab-runner.pref
Explanation: Prefer GitLab provided packages over the Debian native ones
Package: gitlab-runner
Pin: origin packages.gitlab.com
Pin-Priority: 1001
EOF
```

For RHEL/CentOS/Fedora:
```
curl -L "https://packages.gitlab.com/install/repositories/runner/gitlab-runner/script.rpm.sh" | sudo bash
```
* Install the latest version of GitLab Runner

For Debian/Ubuntu/Mint:
```
sudo apt-get install gitlab-runner
```
For RHEL/CentOS/Fedora:
```
sudo yum install gitlab-runner
```
* Running and reginstering the runner for gitlab instance
```
sudo gitlab-runner register --url http://{url or the ip address of the gitlab instance} \
--registration-token {REGISTRATION_TOKEN from cicd option}
```
and then we select the runner executer.etc,SHELL if you want to be run on the shell itself ,or DOCKER if wanted to be run on docker container and...
