# *what is gitlab runner*
gitlab runners are services that run on one or more nodes and clones the projects repository  
on the runners node and reads the contents of the pipelines and executes them in the environment  
that we defined, it could be shell, docker, ssh ,kubernetes or etc. and then send the results back to gitlab.

---
* gitlab-runner configuration file is in `/etc/gitlab-runner/config.toml`

---
* You can click on this [link](https://docs.gitlab.com/runner/configuration/advanced-configuration.html) to see the configuration documents.
