# Projeto de Trabalho de Conclusão

Provisionamento e criação de um Data Lake utilizando tecnologias Open Source.

## Requisitos Gerais
O provisionamento pode ser feito tantom em ambiente local como em Cloud. 
Para o Ambiente local ou em Cloud são necessários: <br>
* 7 VMs, cada uma com 1GB de RAM e um 1vCpu mínimo.


## Requisitos para instalação On Premise
* VirtualBox
* Vagrant
* Ansible

## Requisitos para instalação em Cloud
* Vagrant
* Ansible

## Passos para instalação local

1. Estando no diretório raiz do projeto rodar: <br>`ansible-playbook provisioning.yml -i hosts`
1. Após finalizada a instalação logar via ssh no Nodo principal com o usuário hadoop e executar:<br>`start-hdfs.sh` e `start-spark.sh`
1. Para acessar o HDFS e o YARN
   1. **HDFS http://{IP_NODO_RAIZ}:9870M
   1. **YARN http://{IP_NODO_RAIZ}:8088/cluster 
   
## Passos para instalação em Cloud

1. Editar o arquivo `aws_hosts` ajustando o IP e HOSTNAME conforme o criado na aws.
1. Ainda no arquivo `aws_hosts` colocar o caminho para sua chave ssh na AWS
1. Estando no diretório raiz do projeto rodar: <br>`ansible-playbook cloud_provisioning.yml -i aws_hosts`
1. Após finalizada a instalação logar via ssh no Nodo principal com o usuário hadoop e executar:<br>`start-hdfs.sh` e `start-spark.sh`
1. Para acessar o HDFS e o YARN
   1. **HDFS http://{IP_NODO_RAIZ}:9870M
   1. **YARN http://{IP_NODO_RAIZ}:8088/cluster 
