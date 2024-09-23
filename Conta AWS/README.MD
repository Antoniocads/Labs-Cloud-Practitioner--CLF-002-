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

# Criando alerta

Para criarmos o alerta, iremos utilizar o serviço de alertas e logs chamado CloudWatch (será abordado mais a frente). Porém, será necessário habiltar uma opção na conta para termos a opção de Billing lá no sistema de alertas do Cloudwatch.

No serviço Cloudwatch, na barra lateral na esquerda, iremos expandir a opção de "Alarme" e clicar em "Todos os alarmes":

1. Ao carregar, iremos clicar na opção chamada "Criar Alarme";
2. Vamos clicar em "Selecionar Métrica";
3. Terá algumas opção na aba de "Navegador", iremos clicar inicialmente na opção "Billing" ou "Faturamento";
4. Iremos clicar na opção "Carga total estimada";
5. Vamos selecionar a opção que aparece ao lado do valor da moeda e seguir;
6. Iremos manter o "Tipo de Limite" por Estático;
7. Já na etapa de "Sempre que...", iremos alocar o valor de "Maior/Igual" e definir o valor limite como 10 doláres.
8. Na segunda parte, vamos alocar o estado como "Alarme";
9. Vamos selecionar a opção "Criar novo tópico";
10. Será necessário alocar um nome (caso queira algo diferente), alocar o e-mail que irá receber este alerta e clicar em "Criar tópico";
11. Na terceira etapa, será necessário alocar um nome para o alarme;
12. Na quarta e última etapa será apenas uma validação das configurações alocadas.

Ao criar o alarme pela primeira vez, utilizando o SNS, devemos nos alertas a mensagem no topo mencionando "Assinaturas SNS". Será necessário clicar no botão para corrigirmos isso.

# Configurando SNS

Na página do SNS, devemos selecionar a subscrição que está pendente a ser confirmada e clicar em "Requisitar confirmação".
Após clicar, chegará uma mensagem no e-mail que você cadastrou para receber os disparos SNS, basta clicar em "Confirmar subscrição" e atualiar a página da AWS.