# Projeto de Trabalho de Conclusão

Provisionamento e criação de um Data Lake utilizando tecnologias Open Source.


## Requisitos para instalação On Premise

- VirtualBox
- Ansible

## Requisitos para instalação em Cloud

- Ansible

## Passos para instalação

    1 - Estando o diretório raiz rodar:
         
         ansible-playbook provisioning.yml -i hosts
    
    2 - Após finalizado:
    
        Logar via ssh no Nodo principal com o usuário hadoop. Estando no /home/hadoop executar start-hdfs.sh
    
        HDFS
        http://{IP_NODO_RAIZ}:9870
        
        YARN
        http://{IP_NODO_RAIZ}:8088/cluster
