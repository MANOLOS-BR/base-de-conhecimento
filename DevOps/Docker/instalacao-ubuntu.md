# Instalação Docker no Ubuntu 64 bits. 

Para iniciar o Docker Engine no Ubuntu, verifique se você atende aos pré-requisitos e instale o Docker.

## Pré-requisitos
### Requisitos do Sistema Operacional

Para instalar o Docker Engine, você precisa da versão de 64 bits de uma destas versões do Ubuntu:

- Ubuntu Eoan 19.10
- Ubuntu Bionic 18.04 (LTS)
- Ubuntu Xenial 16.04 (LTS)

O Docker Engine é suportado nas arquiteturas x86_64 (ou amd64), armhf, arm64, s390x (IBM Z) e ppc64le (IBM Power).

> Todos os comandos listados devem ser executados no seu terminal `(ctrl + t)`.


### Desinstalar versões antigas

Antes de mais nada, remova possíveis versões antigas do Docker:

```console
sudo apt-get remove docker docker-engine docker.io containerd runc
```

Depois, atualize o banco de dados de pacotes:

```
sudo apt-get update
```

Agora, adicione ao sistema a chave GPG oficial do repositório do Docker:

```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

Adicione o repositório do Docker às fontes do APT:

```
sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"
```

Atualize o banco de dados de pacotes, pare ter acesso aos pacotes do Docker a partir do novo repositório adicionado:

```
sudo apt-get update
```

Por fim, instale o pacote docker-ce:

```
sudo apt-get install docker-ce
```

Caso você queira, você pode verificar se o Docker foi instalado corretamente verificando a sua versão:

```
sudo docker version
```

E para executar o Docker sem precisar de sudo, adicione o seu usuário ao grupo docker:

```
sudo usermod -aG docker $(whoami)
```

Para mais informações consultar [Install Docker Engine on Ubuntu](https://docs.docker.com/engine/install/ubuntu/)
