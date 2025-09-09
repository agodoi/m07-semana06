## O que é um Load Balancer?

* O Load Balancer (Balanceador de Carga) é como um porteiro inteligente que recebe todas as requisições que chegam à sua aplicação e decide para qual servidor (EC2, container, etc.) cada requisição deve ser enviada.
* Ele distribui o tráfego entre várias instâncias, evitando que apenas uma fique sobrecarregada.
* Ele trabalha junto com o grupo de destino: o grupo diz quais servidores estão disponíveis, e o Load Balancer escolhe para qual mandar a próxima requisição.
* Pode funcionar em diferentes camadas:
  - Application Load Balancer (ALB): olha o conteúdo da requisição (URL, cabeçalhos, etc.) e decide para onde mandar.
  - Network Load Balancer (NLB): trabalha mais “rápido e bruto”, lidando diretamente com conexões TCP/UDP.


## Exemplo simples, fião!

Pensa em uma fila de caixas de supermercado:

* O balcão principal com a fila de clientes é o Load Balancer.
* Os caixas do supermercado são as instâncias EC2.
* O grupo de destino é a lista de caixas que estão abertos e funcionando.
* O Load Balancer observa:
  - Se o caixa 3 está fechado, ele não manda cliente para lá.
  - Se a fila no caixa 1 está muito grande, ele manda o próximo cliente para o caixa 2.
  - Assim, todos os clientes são atendidos mais rápido, sem sobrecarregar apenas um caixa.

## Nesse exercício, você:

1) Criou um Application Load Balancer (LabELB).
2) Ele recebe todas as requisições HTTP dos usuários.
3) Consulta o grupo de destino (LabGroup) para saber quais instâncias estão íntegras.
4) Encaminha cada requisição para uma dessas instâncias de forma equilibrada e que esteja saudável
