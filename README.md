# Para Rodar o arquivo da avaliacao final siga os passos a seguir

## passo 0 - Clone do repositorio e entrar na pasta do projeto
> git clone https://github.com/Menosse/iaac-mba-clcdevops.git

> cd iaac-mba-clcdevops 

## passo 1 - Iniciar e configurar as maquinas virtuais 
### Iniciar as maquina virtuais
> vagrant up

### Rodar o script de instalacao do ansible e outras dependencias
#### Script de inicializacao Maquina iaac
Abra um novo terminal
> vagrant ssh iaac

> cd /vagrant

> sudo sh iaac.sh

### Exportar o ansible.cfg nas maquinas
> export ANSIBLE_CONFIG="./ansible.cfg"

#### Script de inicializacao Maquina server
Abra um novo terminal

> vagrant ssh server

> cd /vagrant

> sudo sh server.sh

### Criar chave ssh e permitir o acesso da maquina iaac na maquina server
Na maquina iaac e Seguir os passos para criar a chave
> ssh-keygen

Copiar a chave
> cat /home/vagrant/.ssh/id_rsa.pub

Entrar na maquina server e colar o conteúdo a chave arquivo no arquivo /home/vagrant/.ssh/authorized_keys
> sudo vi /home/vagrant/.ssh/authorized_keys

Conferir se a chave foi colada corretamente
> cat /home/vagrant/.ssh/authorized_keys

Abrir o arquivo "$ sudo vi /etc/ssh/sshd_config" e procurar pela linha "PasswordAuthentication no" e mudar para "yes" e salvar o arquivo.
> sudo vi /etc/ssh/sshd_config

Após salvar o arquivo reiniciar o serviço do sshd
> sudo systemctl restart ssh


## passo 2 - Rodar o playbook de instalacao da aplicacao
> cd ansible_slackio/

> ansible-playbook playbook.yml 


## passo 2 - 
## passo 3 - 
## passo 4 - 
## passo 6 - 
## passo 7 - 
## passo 8 - 
## passo 9 - 
## passo 10 - 
## passo 11 - 
## passo 12 - 