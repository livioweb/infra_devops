# Devops 
## Bem vindo ao InfraJangoFett
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
Um pequeno projeto de infra utilizando maquinas virtuais, gerenciadas com o Vagrant.
Esta infra conta com uma VM com o jenkis, Gitlab. Sonakube e a do App, este ultimo sera onde a aplicação rodara. 

##### Links Uteis
* https://netdata.cloud
* https://learn.netdata.cloud/docs/
* https://learn.netdata.cloud/docs/agent/health/notifications/telegram
* https://www.vagrantup.com/docs/cli/snapshot
* https://grafana.com/grafana/dashboards/10922

Stressa maquina a 85%
````
$ stress-ng -c 0 -l 85
````


#### [gitlab]
172.17.177.40:9081 
* https://github.com/sameersbn/docker-gitlab
* 
###### netdata 
172.17.177.40:19999

#### [jenkis]
172.17.177.42:9080 

 * ansible jenkis -u vagrant --private-key  ssh-keys/vagrant_id_rsa -i hosts -m shell -a 'echo Hello, World'
 * ansible jenkis -u vagrant --private-key .vagrant/machines/jenkis/virtualbox/private_key  -i hosts -m shell -a 'echo Hello, World'
 * ssh-keygen -f "/home/anakin/.ssh/known_hosts" -R "172.17.177.42"
 * ssh-copy-id -i ssh-keys/vagrant_id_rsa.pub vagrant@172.17.177.42 -f 
 * echo "" > ~/.ssh/known_hosts
###### netdata 
172.17.177.42:19999

#### [sonarkube]
172.17.177.44:9082 
###### netdata 
172.17.177.44:19999

#### [app]
172.17.177.48:8080
###### netdata 
172.17.177.48:19999

#### [grafana]
172.17.177.50
* https://github.com/terorie/netdata-influx

###### netdata 
172.17.177.50:19999
