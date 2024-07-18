# Projeto-linux-#!/bin/bash

# Script Bash para automatização de tarefas criado por Eder Thomaz Lino
# Bootcamp Linux Experience - Professor Denilson Bonatti

echo "Criando os diretórios ..."
mkdir /adm
mkdir /ven 
mkdir /sec 
mkdir /publico

echo " Criando os grupos ..."
groupadd GRP_ADM
groupadd GRP_VEN
groupadd GRP_SEC

echo "Aplicando permissões - diretório adm ..."
chown root:GRP_ADM adm
chmod 770 adm

echo "Aplicando permissões - diretório ven ..."
chown root:GRP_VEN ven
chmod 770 ven

echo "Aplicando permissões - diretório sec ..."
chown root:GRP_SEC sec
chmod 770 sec

echo "Aplicando permissões - diretório publico ..."
chmod 777 publico

echo "Criando usuários do GRP_ADM ..."
useradd carlos -c "Carlos" -s /bin/bash -m -p $(openssl passwd -crypt Senha123) -G GRP_ADM
useradd maria -c "Maria" -s /bin/bash -m -p $(openssl passwd -crypt Senha123) -G GRP_ADM
useradd joao -c "João" -s /bin/bash -m -p $(openssl passwd -crypt Senha123) -G GRP_ADM

echo "Criando os usuários do GRP_VEN ..."
useradd debora -c "Débora" -s /bin/bash -m -p $(openssl passwd -crypt Senha123) -G GRP_VEN
useradd sebastiana -c "Sebastiana" -s /bin/bash -m -p $(openssl passwd -crypt Senha123) -G GRP_VEN
useradd roberto -c "Roberto" -s /bin/bash -m -p $(openssl passwd -crypt Senha123) -G GRP_VEN

echo "Criando os usuários do GRP_SEC ..."
useradd josefina -c "Josefina" -s /bin/bash -m -p $(openssl passwd -crypt Senha123) -G GRP_SEC
useradd amanda -c "Amanda" -s /bin/bash -m -p $(openssl passwd -crypt Senha123) -G GRP_SEC
useradd rogerio -c "Rogerio" -s /bin/bash -m -p $(openssl passwd -crypt Senha123) -G GRP_SEC



echo "Finalizado e concluido o scripts......."
