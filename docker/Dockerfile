FROM mysql
ENV MYSQL_ROOT_PASSWORD=root 
EXPOSE 3306
COPY ./database.sql /docker-entrypoint-initdb.d/

# https://www.youtube.com/watch?v=FrKccQUeaUE&t=300s
# docker build -t mysql_db .
# docker exec -it 25b719de221b /bin/bash

# Executando o MySQL no modo daemon, permitindo acessar por DBeaver. 
# (Necessário configurar em propriedades da conexão: "" e "allowPublicKeyRetrieval=true")
# $ docker run -d -p 3306:3306 -e MYSQL_ROOT_PASSWORD=root mysql_db --lower_case_table_names=1


#por Otávio Prado | 3951.7k xp | 7150 posts  Moderador
#22/12/2020
#Na string de conexão você pode incluir a opção "allowPublicKeyRetrieval=true", exemplo:
#jdbc:mysql://localhost:3306/db?allowPublicKeyRetrieval=true&useSSL=false 
# COPIAR CÓDIGO

#Para usuários do DBeaver:
#Clique com o botão direito na sua conexão, escolha "Editar Conexão"
#Na tela "Configurações de conexão" (tela principal), clique em "Editar configurações do driver"
#Clique em "Propriedades da conexão"
#Clique com o botão direito na área "propriedades do usuário" e escolha "Adicionar nova propriedade"
#Adicione duas propriedades: "useSSL" e "allowPublicKeyRetrieval"
#Defina seus valores como "false" e "true" clicando duas vezes na coluna "value"

# Mostrando a versão do MySQL
#SHOW VARIABLES LIKE "%version%";

# Mostrando outros parâmetros
#SHOW VARIABLES LIKE "%slow%";
#SHOW VARIABLES LIKE "%log%";
#SHOW VARIABLES LIKE "%lower%";