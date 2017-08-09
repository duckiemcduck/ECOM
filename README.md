# Servidor Wordpress + MariaDB com Docker 
Este repositório contêm scripts e configurações para executar um servidor apache com Wordpress utilizando serviços _Docker_
>Para mais informações sobre docker, consulte: https://aws.amazon.com/pt/docker/

## Instalação Linux (Ubuntu 16.04.3 Xenial)
### Comandos no terminal
1- Baixe ou clone este repositório para sua máquina local.
```
git clone https://github.com/duckiemcduck/ecom/
```
2- Entre no diretório do projeto.
```
cd ecom
```
3- Certifique-se que docker está instalado através deste comando:
```
docker
```

>Se não estiver, execute o script de instalação. Requer permissão de super-usuário.
```
./install-docker.sh
```

4- Certifique-se que docker-compose está instalado através deste comando:
```
docker-compose
```

>Se não estiver, execute o script de instalação. Requer permissão de super-usuário.
```
./install-docker-compose.sh
```

5- Execute o serviço

```
sudo docker-compose up
```

6- Identifique o endereço alocado pelo servidor.

*Os processos do banco de dados e do servidor serão iniciados.*

O processo do servidor esperará o processo do banco de dados inicializar antes de alocar um endereço.

>Espere o retorno da seguinte mensagem do processo do wordpress, informando o endereço do servidor:
![http://i.imgur.com/etxmjAj.png](http://i.imgur.com/etxmjAj.png)

7- Acesse o endereço pelo navegador e configure Wordpress como desejar.
![http://i.imgur.com/8lDLo9h.png](http://i.imgur.com/8lDLo9h.png)
 --
 
 ##Entrando no Banco de Dados
 1- Para entrar no container do banco de dados, digite:
 ```
 sudo docker exec -i -t ecom_mariadb_1 /bin/bash
 ```
 2- Entre no banco. A senha e o nome do banco de dados são fornecidos no arquivo docker-compose.yml.
 ```
 mysql -u root -p wordpress
 senha admin
 ```
 
 
