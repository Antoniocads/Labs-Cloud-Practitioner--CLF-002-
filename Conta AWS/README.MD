## CRIANDO A CONTA, OBSERVANDO FREE TIER E CRIANDO ALERTA PARA EVITAR COBRANÇAS DENESCENESSÁRIAS

Ao começar a utilizar os serviços AWS, seguiremos sempre pela primeira etapa de criar a conta ou realizar o login nela.

Nesta conta, o intuito é utilizar sempre que possível o free tier da AWS. Caso seja necessário utilizar algum serviço com configuração fora do free tier, iremos implementar um alerta de faturamento para sempre nos enviar um aviso caso chegue perto ou atinga 10 doláres.

# Habilitando métrica de Billing no Cloudwatch

Para habilitar as métricas de Billing no Cloudwatch, devemos realizar a seguinte ação:
1. Clicar no nome do seu usuário, no canto superior direito;
2. Clicar em Conta;
3. No menu lateral, na esquerda, terá que descer a barra de rolamento até encontrar a opção "Preferências de faturamento";
4. Em "Preferências de faturamento", deverá clicar em "Editar" no grupo de configurações "Preferências de alerta";
5. Habilite as duas opções para seguirmos com a criação do alerta.

Alertas AWS Free Tier: Irá enviar um e-mail de alerta sempre que estivermos perto ou ultrapassando os benefícios do Free Tier.

Alertas Cloudwatch Faturamento: Irá habilitar métricas na qual será possível gerar alertas sobre o faturamento da conta. Uma vez habilitado, não será possível desabilitar.

## Criando alerta

Para criarmos o alerta, iremos utilizar o serviço de alertas e logs chamado CloudWatch (será abordado mais a frente). Porém, será necessário habiltar uma opção na conta para termos a opção de Billing lá no sistema de alertas do Cloudwatch.