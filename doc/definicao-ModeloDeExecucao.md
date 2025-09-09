## O que é um Modelo de Execução?

* É como um **“receituário pronto”** que a AWS usa para criar novas instâncias EC2 de forma padronizada.
* Nele você define todos os ingredientes necessários:
  - **Qual imagem (AMI)** será usada → o sistema operacional e aplicativos já instalados.
  - **Tipo de instância** → o “tamanho do computador” (ex: t2.micro, t3.medium).
  - **Chave SSH** → para você poder acessar.
  - **Security Groups** → para definir quem pode se conectar.
  - **Configurações extras** → como tags, scripts de inicialização e monitoramento no CloudWatch.

Depois, esse modelo pode ser usado pelo **Auto Scaling** para subir várias instâncias iguais, automaticamente.

## Exemplo simples

Pensa em uma **receita de bolo**:

* O **modelo de execução** é a receita escrita com todos os detalhes (ingredientes, medidas e modo de preparo).
* Cada vez que você segue essa receita, você faz um **bolo idêntico**.
* Se a demanda aumentar (muitos convidados chegando), você consegue assar vários bolos iguais de forma rápida, porque já tem a receita pronta.

Da mesma forma, o **Launch Template** garante que toda nova instância EC2 criada seja **padronizada**, sem precisar configurar tudo do zero.

## Relação com esse lab

1. Você criou ou vai criar um **Modelo de Execução chamado LabConfig**.
2. Nesse modelo você definiu:
   * A **AMI** do Web Server já configurado.
   * O **tipo de instância t2.micro** (free tier).
   * O **Security Group Web** para proteger o tráfego.
3. Esse modelo foi usado depois para o **Auto Scaling Group**, que criou novas instâncias automaticamente, todas iguais.
Quer que eu prepare também um **fluxo visual simples (Launch Template → Auto Scaling Group → Instâncias idênticas)** para você usar em slide?

