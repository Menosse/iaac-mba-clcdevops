# Para Rodar o arquivo da avaliacao final siga os passos a seguir

## passo 0 - Clone do repositorio e entrar na pasta do projeto
> git clone https://github.com/Menosse/iaac-mba-clcdevops.git
> cd iaac-mba-clcdevops 
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

## Criar chave ssh e permitir o acesso da maquina iaac na maquina server
Na maquina iaac
> ssh-keygen
> cat /home/vagrant/.ssh/id_rsa.pub
Copiar a chave
Entrar na maquina server e colar o conteúdo a chave arquivo no arquivo /home/vagrant/.ssh/authorized_keys
> nano /home/vagrant/.ssh/authorized_keys
Conferir se a chave foi colada corretamente
> cat /home/vagrant/.ssh/authorized_keys


## passo 
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