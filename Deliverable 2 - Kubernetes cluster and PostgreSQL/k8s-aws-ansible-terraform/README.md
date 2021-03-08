# k8s-aws-ansible-terraform

## Pontos a serem comentados
Não consegui finalizar os testes, está criando a instâncias, instalando o que precisa, porém não consegui finalizar a validação da inserção dos nós no cluster

## Pré-Requisitos

O usuário (Chave IAM) que executar, precisará de permissão para criar VPC, SecurityGroup e EC2

## Ajustar variáveis conforme ambiente na AWS

Pontos importante é a utilização de AMI que já tenha feito a assinatura, caso contrário ocorrerá erro
Certifique-se que a variável key_pair_name, está igual a que for criada na AWS
As demais informações, fica a critério de uso da AWS

```sh
vi aws-terraform/variables.tf 
```

## Como utilizar?

É necessário criar um par de chaves na aws, e o arquivo deve ser utilizado no commando ssh-add

```sh
ssh-agent zsh
ssh-add your_key_pair.pem
ansible-playbook -i hosts main.yml
```

## Como Destruir o que foi criado

```sh
cd aws-terraform
terraform destroy --auto-approve
```
