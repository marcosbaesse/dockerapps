# dockerizing-examples
Um repositório com exemplos de aplicações docker usando o docker-compose

# Instalando Docker
## Ubuntu, Mint

Desinstala versões antigas:

```sudo apt-get remove docker docker-engine docker.io containerd runc```

Atualiza o Index do pacote

```sudo apt-get update```

Instala pacotes para permitir o apt a usar um repositório fora do HTTPS:

```
sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common
```

Adiciona a chave GPG oficial do Docker:

```curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -```

Configura o repositório estável **para o seu sistema**:
- Ubuntu 18.04/Mint 19, 19.1 and 19.2

```
sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   bionic \
   stable"
```

Atualiza o index do pacote:

```
sudo apt-get update
```

Instala a última versão da Engine do Docker:

```
sudo apt-get install docker-ce docker-ce-cli containerd.io
```

Verifica esta Engine do Docker:

```
sudo docker run hello-world
```

Cria o grupo para o docker:

```
sudo groupadd docker
```

Adiciona o seu usuário ao grupo do docker:

```
sudo usermod -aG docker $USER
```

Agora deslogue, ou, no linux, ative as mudanças:

```
newgrp docker
```

Verifica se você consegue rodar comandos docker sem utilizar sudo:

```
docker run hello-world
```

Pega a versão estável do composer:

```
sudo curl -L "https://github.com/docker/compose/releases/download/1.24.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
```

Aplica permissões de execução:

```
sudo chmod +x /usr/local/bin/docker-compose
```

Testa a instalação:

```
docker-compose --version
```