# Ponderada - Semana 9

Antonio Nassar - Eng. Software - T06

### Introdução:

Esta é uma ativade sobre como podemos provisionar uma instância EC2 na AWS utilizando Terraform, uma uma ferramenta de Infrastructure as Code (IaC) desenvolvida pela HashiCorp, em um exemplo de código baseado no tutorial da atividade ponderada.

---

#### Objetivo

Nessa atividade vamos demonstrar como foi feita a criação da infraestrutura na nuvem utilizando IaC com o Terraform, e os passos para realização.

---

## Setup do Ambiente

1. Terraform CLI (versão 1.2.0 ou superior).
2. AWS CLI definido com as devidas credenciais do desenvolvedor: AWS Access Key, Secret Access Key e um Session Token (em casos da utilização de AWS ACADEMY LABS) AWS_SECRET_ACCESS_KEY e
3. Conta AWS configurada com permissões para provisionar recursos.

---

## Passo a Passo da Atividade

#### 1. Criação de um diretório para execução da atividade.

Criamos um diretório específico para esta atividade.
![img](/imgs/aws-p1.png)

#### 2. Crie o arquivo main.tf:

Adicione o seguinte código (sujeito à alterações dependendo do usuário).

![img](/imgs/aws-p7.png)

#### 3. Configuração de credenciais da AWS:

Configuramos as credenciais obtidas na AWS (CLI), seguindo os protocolos de segurança em cloud.

## ![img](/imgs/aws-p3.png)

#### 4. Inicializar o Terraform na aplicação

Inicialize o diretório com o comando:

![img](/imgs/aws-p4.png)

#### 5. Validação do Código na Aplicação:

Formatamos e validamos as configurações para garantir que tudo está adequado.

![img](/imgs/aws-p5.png)

#### 6. Criação da Infraestrutura (IAC)

Deve-se executar o comando 'terraform apply' para provisionar a instância EC2, neste caso, e confirme a execução digitando 'yes', respectivamente.

![img](/imgs/aws-p6.png)

#### 7. Verificar os Recursos Provisionados

Deve-se verificar se os recursos foram provisionados no AWS Console usando:

```bash
terraform show
```

---

## Recursos Provisionados

Os seguintes recursos foram provisionados na AWS:

```bash
resource "aws_instance" "app_server" {
  ami           = "ami-830c94e3"
  instance_type = "t2.micro"

  tags = {
    Name = "ExampleAppServerInstance"
  }
}
```

---

## Conclusão

Com isso, este projeto demonstra como podemos utilizar o Terraform para provisionar uma infraestrutura básica (IAC) na AWS, e serve como modelo base para que possamos ampliar suas áreas de aplicação em cloud com outros tipos de aplicações, respectivamente.
