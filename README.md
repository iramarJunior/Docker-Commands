# Comandos Básicos do Docker

### Subir um container
```
$ docker run [nome do container]
```

### Listar containers ativos
```
$ docker ps
```

### Listar todos os containers
```
$ docker ps -a
```

### Acessar o sistema dentro do container
```
$ docker run -it [nome do container]
```

### Iniciar um container parado
```
$ docker start [container id]
```

### Parar um container rodando
```
$ docker stop [container id]
```

### Iniciar no terminal de um container
```
$ docker start -a -i [container id]
```

### Remover um container
```
$ docker rm [container id]
```

### Remover todos os containers
```
$ docker container prune
```

### Remover uma Imagem
```
$ docker rmi [nome da imagem]
```

### Rodar um container sem travar o terminal
```
$ docker run -d [nome do container]
```

### Parar um container imediatamente
```
$ docker stop -t 0 [container id]
```

### Ver portas ao iniciar um container
```
$ docker run -d -P [nome do container]
```

### Definir porta
```
$ docker run -p 8080:80 [nome do container]
```

### Ver porta do container
```
$ docker port [container id]
```

### Ver o IP da maquina virtual
```
$ docker-machine ip
```

### Dar um nome para o container
```
$ docker run --name [nome que deseja dar] [container id]
```

### Setar variável de ambiente
```
$ docker run -e [nome e valor da variavel XXXX='xxxx'] [nome do container]
```

### Listar ids dos containers que estão rodando
```
$ docker ps -q
```

### Parar containers com $()
```
$ docker stop -t 0 $(docker ps -q)
```

## Volumes Docker

### Criar um volume
```
$ docker run -v "/var/www" ubuntu
```
```
$ docker run -v [caminho do host "C:\\user\junior:/var/www"] [nome do container]
```

### Informações do container
```
$ docker inspect [container id]
```

### Iniciar um comando na maquina utilizando o volume (ambiente de desenvolvimento)
```
$ docker run -d -p 3000:80 -v ""caminho do host : caminho do container"] -w [caminho do container] [comando a ser executado]
```
