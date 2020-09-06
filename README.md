# Projeto de Trabalho de Conclusão

Provisionamento e criação de um Data Lake utilizando tecnologias Open Source.

## Requisitos Gerais
O provisionamento pode ser feito tantom em ambiente local como em Cloud. 
Para o Ambiente local ou em Cloud são necessários 7 VMs, cada uma com 1GB de RAM e um 1vCpu mínimo.


## Requisitos para instalação On Premise
* VirtualBox
* Vagrant
* Ansible

## Requisitos para instalação em Cloud
* Vagrant
* Ansible

## Passos para instalação Local
<br>
1. Estando no diretório raiz do projeto rodar:<br> 'ansible-playbook provisioning.yml -i hosts' <br>
2. Após finalizada a instalação logar via ssh no Nodo principal com o usuário hadoop e executar: <br> 'start-hdfs.sh' e 'start-spark.sh'<br>
     **HDFS http://{IP_NODO_RAIZ}:9870M <br>
     **YARN http://{IP_NODO_RAIZ}:8088/cluster <br>
