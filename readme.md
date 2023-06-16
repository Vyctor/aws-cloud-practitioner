
# AWS

- [AWS](#aws)
  - [Computação na nuvem](#computação-na-nuvem)
    - [Amazon EC2](#amazon-ec2)
    - [Tipos de Instâncias do Amazon EC2](#tipos-de-instâncias-do-amazon-ec2)
      - [Uso Geral](#uso-geral)
      - [Otimizadas para computação](#otimizadas-para-computação)
      - [Otimizadas para memória](#otimizadas-para-memória)
      - [Otimizadas para Computação acelerada](#otimizadas-para-computação-acelerada)
      - [Otimizadas para armazenamento](#otimizadas-para-armazenamento)
    - [Definição de preços do Amazon EC2](#definição-de-preços-do-amazon-ec2)
      - [Instâncias sob demanda](#instâncias-sob-demanda)
      - [Saving plans](#saving-plans)
      - [Instâncias reservadas](#instâncias-reservadas)
      - [Instâncias spot](#instâncias-spot)
      - [Instâncias dedicadas](#instâncias-dedicadas)
    - [Escalabilidade do Amazon EC2](#escalabilidade-do-amazon-ec2)
      - [Amazon EC2 Auto Scaling](#amazon-ec2-auto-scaling)
      - [Exemplo Auto Scaling](#exemplo-auto-scaling)
    - [Direcionamento de tráfego com o Elastic Load Balancing](#direcionamento-de-tráfego-com-o-elastic-load-balancing)
      - [Exemplo Elastic Load Balancing](#exemplo-elastic-load-balancing)
        - [Período de baixa demanda](#período-de-baixa-demanda)
        - [Período de alta demanda](#período-de-alta-demanda)
    - [Sistema de mensagens e enfileiramento](#sistema-de-mensagens-e-enfileiramento)
      - [Amazon Simple Notification Service (Amazon SNS)](#amazon-simple-notification-service-amazon-sns)
      - [Amazon Simple Queue Service (Amazon SQS)](#amazon-simple-queue-service-amazon-sqs)
    - [Outros serviços de computação](#outros-serviços-de-computação)
      - [Computação sem servidor - serverless](#computação-sem-servidor---serverless)
      - [AWS Lambda](#aws-lambda)
      - [Contêineres](#contêineres)
      - [Amazon Elastic Container Service (Amazon ECS)](#amazon-elastic-container-service-amazon-ecs)
      - [Amazon Elastic Kubernetes Service (Amazon EKS)](#amazon-elastic-kubernetes-service-amazon-eks)
      - [Amazon Fargate](#amazon-fargate)
  - [Infraestrutura Global e Confiabilidade](#infraestrutura-global-e-confiabilidade)
    - [Seleção de região](#seleção-de-região)
      - [Conformidade com governança de dados e requisitos legais](#conformidade-com-governança-de-dados-e-requisitos-legais)
      - [Proximidade dos usuários finais](#proximidade-dos-usuários-finais)
      - [Serviços disponíveis na Região](#serviços-disponíveis-na-região)
      - [Preços](#preços)
    - [Zonas de disponibilidade](#zonas-de-disponibilidade)
    - [Pontos de presença](#pontos-de-presença)
    - [AWS Elastic Beanstalk](#aws-elastic-beanstalk)
    - [AWS CloudFormation](#aws-cloudformation)
  - [Redes](#redes)
  - [Armazenamento e banco de dados](#armazenamento-e-banco-de-dados)
  - [Segurança](#segurança)
  - [Monitoramento e análise](#monitoramento-e-análise)
  - [Definição de preços e suporte](#definição-de-preços-e-suporte)
  - [Migração e inovação](#migração-e-inovação)
  - [A jornada para a nuvem](#a-jornada-para-a-nuvem)
  - [Noções básicas do AWS Certified Cloud Practitioner](#noções-básicas-do-aws-certified-cloud-practitioner)

A AWS é uma plataforma de serviços em nuvem que oferece poder computacional, armazenamento de banco de dados, entrega de conteúdo e outras funcionalidades para ajudar as empresas a expandir e crescer.

## Computação na nuvem

### Amazon EC2

O Amazon Elastic Compute Cloud (Amazon EC2) fornece capacidade computacional segura e redimensionável na nuvem como instâncias do Amazon EC2.

Imagine que você é responsável pela arquitetura dos recursos de sua empresa e precisa ser compatível com novos sites. Com recursos locais tradicionais, você precisa fazer o seguinte:

- Gastar dinheiro adiantadamente para comprar hardware.
- Aguardar até que os servidores sejam entregues.
- Instalar os servidores em seu data center físico.
- Fazer todas as configurações necessárias.

Em comparação, com uma instância do Amazon EC2, você pode usar um servidor virtual para executar aplicativos na nuvem AWS.

- Você pode provisionar e executar uma instância do Amazon EC2 em minutos.
- Você pode parar de usar a instância quando terminar de executar uma carga de trabalho.
- Você paga apenas pelo tempo de computação em que uma instância estiver em execução, não quando ela é interrompida ou encerrada.
- Você pode economizar custos pagando apenas pela capacidade do servidor necessária ou desejada.

### Tipos de Instâncias do Amazon EC2

Os tipos de instâncias do Amazon EC2 são otimizados para tarefas diferentes. Ao selecionar um tipo de instância, considere as necessidades específicas de suas cargas de trabalho e seus aplicativos. Isso pode incluir requisitos para recursos de computação, memória ou armazenamento.

#### Uso Geral

Instâncias de uso geral equilibram os recursos de computação, memória e rede. Você pode usá-las para diversas cargas de trabalho, como:

- servidores de aplicativos
- servidores de jogos
- servidores de back-end para aplicativos empresariais
- bancos de dados pequenos e médios

Suponha que você tenha um aplicativo no qual as necessidades de recursos para computação, memória e rede sejam praticamente equivalentes. Você pode executar esse aplicativo em uma instância de uso geral porque ele não precisa de otimização em nenhuma área de recurso único.

#### Otimizadas para computação

Instâncias otimizadas para computação são ideais para aplicativos vinculados à computação que se beneficiam de processadores de alto desempenho. Assim como instâncias de uso geral, você pode usar instâncias otimizadas para computação para cargas de trabalho, como servidores web, de aplicativos e de jogos.

No entanto, a diferença é que aplicativos otimizados para computação são ideais para servidores web de alto desempenho, servidores de aplicativos de computação intensiva e servidores de jogos dedicados. Você também pode usar instâncias otimizadas para computação para cargas de trabalho de processamento em lote, com o processamento de muitas transações em um único grupo.

#### Otimizadas para memória

Instâncias otimizadas para memória são projetadas para fornecer desempenho rápido para cargas de trabalho que processam grandes conjuntos de dados na memória. Na computação, a memória é uma área de armazenamento temporário. Ela contém todos os dados e instruções de que uma unidade central de processamento (CPU) precisa para conseguir realizar ações. Antes que um programa de computador ou aplicativo possa ser executado, ele é carregado do armazenamento para a memória. Esse processo de pré-carregamento dá à CPU acesso direto ao programa de computador.

Suponha que você tenha uma carga de trabalho que precise que grandes quantidades de dados sejam pré-carregados antes de executar um aplicativo. Esse cenário pode ser de um banco de dados de alto desempenho ou uma carga de trabalho que envolva a execução de processamento em tempo real de uma grande quantidade de dados não estruturados. Nesses tipos de casos de uso, considere usar uma instância otimizada para memória. As instâncias otimizadas para memória permitem que você execute cargas de trabalho com altas necessidades de memória e tenha um ótimo desempenho.

#### Otimizadas para Computação acelerada

Instâncias de computação acelerada usam aceleradores de hardware, ou coprocessadores, para executar algumas funções de forma mais eficiente do que é possível em um software executado em CPUs. Exemplos dessas funções são cálculos de números com vírgula flutuante, processamento de gráficos e correspondência de padrões de dados.

Na computação, um acelerador de hardware é um componente que pode agilizar o processamento de dados. As instâncias de computação acelerada são ideais para cargas de trabalho, como aplicativos gráficos e streaming de jogos e de aplicativos.

#### Otimizadas para armazenamento

As instâncias otimizadas para armazenamento são projetadas para cargas de trabalho que exigem alto acesso sequencial de leitura e gravação a grandes conjuntos de dados no armazenamento local. Exemplos de cargas de trabalho adequadas para instâncias otimizadas para armazenamento são sistemas de arquivos distribuídos, aplicativos de data warehouse e sistemas de processamento de transações on-line de alta frequência (OLTP).

Na computação, o termo operações de entrada/saída por segundo (IOPS) é uma métrica que mensura o desempenho de um dispositivo de armazenamento. Ela indica quantas operações diferentes de entrada ou saída um dispositivo pode executar em um segundo. As instâncias otimizadas para armazenamento foram projetadas para fornecer dezenas de milhares de IOPS aleatórias e de baixa latência para aplicativos.

Imagine as operações de entrada como dados colocados em um sistema, como registros inseridos em um banco de dados. Uma operação de saída são dados gerados por um servidor. Um exemplo de saída pode ser a análise realizada nos registros em um banco de dados. Se você tiver um aplicativo com alto requisito de IOPS, uma instância otimizada para armazenamento poderá fornecer melhor desempenho em relação a outros tipos de instâncias não otimizados para esse tipo de caso de uso.

### Definição de preços do Amazon EC2

Com o Amazon EC2, você paga apenas pelo tempo de computação que usar. O Amazon EC2 oferece diversas opções de preço para diferentes casos de uso. Por exemplo, se o seu caso de uso tolerar interrupções, você poderá economizar com instâncias spot. Você também pode economizar assumindo um compromisso antecipadamente e bloqueando um nível mínimo de uso com instâncias reservadas.

#### Instâncias sob demanda

Instâncias sob demanda são ideais para cargas de trabalho irregulares de curto prazo que não podem ser interrompidas. Custos antecipados ou contratos mínimos não se aplicam. As instâncias são executadas continuamente até que sejam interrompidas e você paga apenas pelo tempo de computação que usar.

Exemplos de casos de uso para instâncias sob demanda são desenvolvimento e teste de aplicativos e execução de aplicativos com padrões de uso imprevisíveis. As instâncias sob demanda não são recomendadas para cargas de trabalho que duram um ano ou mais, porque essas cargas de trabalho podem ser mais econômicas usando instâncias reservadas.

#### Saving plans

A AWS oferece Savings Plans para vários serviços computacionais, incluindo o Amazon EC2. O Savings Plans do Amazon EC2 permite reduzir os custos de computação ao haver o compromisso com uma quantidade consistente de uso de computação por um período de um ou três anos. Esse compromisso resulta em economias de até 72% em relação aos custos de instâncias sob demanda.

Qualquer uso até o compromisso é cobrado de acordo com o preço de Savings Plan com desconto (por exemplo, USD 10 por hora). Qualquer uso além do compromisso é cobrado de acordo com os preços normais de instâncias sob demanda.

Mais adiante neste curso, você analisará o AWS Cost Explorer, uma ferramenta que permite visualizar, interpretar e gerenciar o uso e os custos da AWS ao longo do tempo. Se você estiver considerando o modelo Savings Plans, o AWS Cost Explorer poderá analisar seu uso do Amazon EC2 nos últimos 7, 30 ou 60 dias. O AWS Cost Explorer também dá recomendações personalizadas para Savings Plans. Essas recomendações calculam o quanto você pode economizar mensalmente com o Amazon EC2, com base no uso anterior do Amazon EC2 e no valor do compromisso por hora em um Savings Plan de um ou três anos.

#### Instâncias reservadas

Instâncias reservadas são um desconto de cobrança aplicado ao uso de instâncias sob demanda em sua conta. Você pode adquirir instâncias reservadas comuns e instâncias reservadas conversíveis por um período de um ou três anos, e instâncias reservadas agendadas por um período de um ano. Você tem mais economia com a opção de três anos.

Ao final do período da instância reservada, você pode continuar usando a instância do Amazon EC2 sem interrupção. No entanto, são cobrados os preços de instâncias sob demanda até que um dos procedimentos a seguir seja feito:

- Encerrar a instância.
- Adquirir uma nova instância reservada que corresponda aos atributos da instância (tipo de instância, Região, locação e plataforma).

#### Instâncias spot

As instâncias spot são ideais para cargas de trabalho com horários de início e término flexíveis ou que toleram interrupções. As instâncias spot usam a capacidade de computação não utilizada do Amazon EC2 e têm uma economia de até 90% de desconto em relação aos preços das instâncias sob demanda.

Suponha que você tenha um trabalho de processamento em segundo plano que pode ser iniciado e interrompido conforme for necessário (como o trabalho de processamento de dados para uma pesquisa de cliente). Você deseja iniciar e interromper o trabalho de processamento sem afetar as operações gerais de seus negócios. Se você fizer uma solicitação spot e a capacidade do Amazon EC2 estiver disponível, a instância spot será iniciada. No entanto, se você fizer uma solicitação spot e a capacidade do Amazon EC2 estiver indisponível, a solicitação não terá sucesso até que a capacidade seja disponibilizada. A capacidade indisponível pode atrasar a execução do trabalho de processamento em segundo plano.

Depois de executar uma instância spot, se a capacidade não estiver mais disponível ou a demanda por instâncias spot aumentar, sua instância poderá ser interrompida. Isso pode não representar problemas para o trabalho de processamento em segundo plano. No entanto, no exemplo anterior de desenvolvimento e teste de aplicativos, é provável que você queira evitar interrupções inesperadas. Portanto, escolha um tipo de instância do EC2 diferente que seja ideal para essas tarefas.

#### Instâncias dedicadas

Hosts dedicados são servidores físicos com capacidade de instância do Amazon EC2 totalmente dedicada ao uso do cliente.

Você pode usar suas licenças de software por soquete, por núcleo ou por VM existentes para manter a conformidade da licença. Você pode adquirir hosts dedicados sob demanda e reservas de hosts dedicados. De todas as opções do Amazon EC2 que foram abordadas, os hosts dedicados são os mais caros.

### Escalabilidade do Amazon EC2

A escalabilidade envolve começar apenas com os recursos de que você precisa e projetar sua arquitetura para responder automaticamente às alterações de demanda, fazendo aumentos ou reduções. Como resultado, você paga apenas pelos recursos que usa. Você não precisa se preocupar com a falta de capacidade de computação para atender às necessidades de seus clientes.

Se você quisesse que o processo de scaling acontecesse automaticamente, qual serviço AWS você usaria? O serviço AWS que fornece essa funcionalidade para instâncias do Amazon EC2 é o Amazon EC2 Auto Scaling.

#### Amazon EC2 Auto Scaling

Se você já tentou acessar um site que não carregava e atingiu o tempo limite algumas vezes, ele pode ter recebido mais solicitações do que conseguia atender. Essa situação é semelhante a esperar em uma longa fila em uma cafeteria quando há apenas um barista disponível para registrar os pedidos dos clientes.

O Amazon EC2 Auto Scaling permite que você adicione ou remova automaticamente instâncias do Amazon EC2 em resposta à alteração da demanda do aplicativo. Ao fazer auto scaling de suas instâncias, aumentando ou reduzindo conforme a necessidade, você consegue manter uma sensação maior de disponibilidade de aplicativos.

No Amazon EC2 Auto Scaling, há duas abordagens disponíveis: scaling dinâmico e scaling preditivo.

- O scaling dinâmico responde às alterações na demanda.
- O scaling preditivo programa automaticamente o número correto de instância do Amazon EC2 com base na demanda prevista.

#### Exemplo Auto Scaling

Já que na nuvem a capacidade computacional é um recurso programático, você pode adotar uma abordagem mais flexível para o problema de scaling. Ao adicionar o Amazon EC2 Auto Scaling a um aplicativo, você pode adicionar novas instâncias ao aplicativo quando for necessário e encerrá-las quando não forem mais necessárias.

Suponha que você esteja se preparando para executar um aplicativo em instâncias do Amazon EC2. Ao configurar o tamanho do seu grupo do Auto Scaling, você pode definir o número mínimo de instâncias do Amazon EC2 como sendo um. Isso significa que, em qualquer momento, deve haver pelo menos uma instância do Amazon EC2 em execução.

Ao criar um grupo do Auto Scaling, você pode definir o número mínimo de instâncias do Amazon EC2. A capacidade mínima é o número de instâncias do Amazon EC2 que são executadas imediatamente após a criação do grupo do Auto Scaling. Neste exemplo, o grupo do Auto Scaling tem uma capacidade mínima de uma instância do Amazon EC2.

Em seguida, você pode definir a capacidade desejada como duas instâncias do Amazon EC2, mesmo que o aplicativo precise de um mínimo de uma única instância do Amazon EC2 para que seja executado.

**Se você não especificar o número desejado de instâncias do Amazon EC2 em um grupo do Auto Scaling, a capacidade desejada se tornará a capacidade mínima regular.**

A terceira configuração que você pode definir em um grupo do Auto Scaling é a capacidade máxima. Por exemplo, você pode configurar o grupo do Auto Scaling para aumentar em resposta à demanda elevada, mas apenas para um máximo de quatro instâncias do Amazon EC2.

Como o Amazon EC2 Auto Scaling usa instâncias do Amazon EC2, você paga apenas pelas instâncias que usar, e somente quando elas forem usadas. Você agora tem uma arquitetura econômica que fornece a melhor experiência do cliente e ao mesmo tempo reduz custos.

### Direcionamento de tráfego com o Elastic Load Balancing

O Elastic Load Balancing é o serviço AWS que distribui automaticamente o tráfego de entrada de aplicativos entre vários recursos, como instâncias do Amazon EC2.

Um balanceador de carga atua como um ponto único de contato para todo o tráfego da web de entrada no seu grupo do Auto Scaling. Isso significa que, à medida que você adiciona ou remove instâncias do Amazon EC2 em resposta à quantidade de tráfego de entrada, essas solicitações são direcionadas para o balanceador de carga primeiro. Em seguida, as solicitações se espalham por vários recursos que lidarão com elas. Por exemplo, se você tiver várias instâncias do Amazon EC2, o Elastic Load Balancing distribuirá a carga de trabalho entre elas para que nenhuma instância tenha que carregar a maior parte.

Embora o Elastic Load Balancing e o Amazon EC2 Auto Scaling sejam serviços separados, eles trabalham juntos para que os aplicativos executados no Amazon EC2 possam fornecer alto desempenho e disponibilidade.

#### Exemplo Elastic Load Balancing

##### Período de baixa demanda

Aqui está um exemplo de como o Elastic Load Balancing funciona. Suponha que alguns clientes vieram à cafeteria e estão prontos para fazer seus pedidos.

Se apenas algumas caixas registradoras estiverem abertas, isso corresponde à demanda dos clientes que precisam do serviço. A cafeteria tem menos probabilidade de ter caixas registradoras abertas sem clientes. Nesse exemplo, você pode pensar nas caixas registradoras como instâncias do Amazon EC2.

##### Período de alta demanda

Ao longo do dia, à medida que o número de clientes aumenta, a cafeteria abre mais caixas registradoras para acomodá-los. No diagrama, o grupo do Auto Scaling representa isso.

Além disso, um funcionário da cafeteria direciona os clientes para a caixa registradora mais adequada para que o número de solicitações possa ser distribuído uniformemente entre as caixas abertas. Você pode pensar nesse funcionário da cafeteria como um balanceador de carga.

### Sistema de mensagens e enfileiramento

Os aplicativos são formados por vários componentes. Os componentes se comunicam entre si para transmitir dados, atender solicitações e manter o aplicativo em execução.

Suponha que você tenha um aplicativo com componentes com acoplamento forte. Esses componentes podem ser bancos de dados, servidores, interface do usuário, lógica de negócios e assim por diante. Esse tipo de arquitetura pode ser considerado um aplicativo monolítico.

Nessa abordagem à arquitetura do aplicativo, se um único componente falhar, outros componentes falharão e possivelmente todo o aplicativo.

**Para ajudar a manter a disponibilidade do aplicativo quando um único componente falha, você pode projetar esse aplicativo por uma abordagem de microsserviços.**

Em uma abordagem de microsserviços, os componentes do aplicativo têm um acoplamento fraco. Neste caso, se um único componente falhar, os outros componentes continuarão funcionando porque estarão em comunicação uns com os outros. O acoplamento fraco evita a falha completa do aplicativo.

Ao projetar aplicativos na AWS, você pode adotar uma abordagem de microsserviços com serviços e componentes que cumprem funções diferentes. Dois serviços facilitam a integração de aplicativos: Amazon Simple Notification Service (Amazon SNS) e Amazon Simple Queue Service (Amazon SQS).

#### Amazon Simple Notification Service (Amazon SNS)

O Amazon Simple Notification Service (Amazon SNS) é um serviço de publicação/assinatura. Usando tópicos do Amazon SNS, um editor publica mensagens para assinantes. Isso se parece com a cafeteria: o operador de caixa entrega os pedidos ao barista que, por sua vez, prepara as bebidas.

No Amazon SNS, os assinantes podem ser servidores web, endereços de e-mail, funções do AWS Lambda ou várias outras opções.

#### Amazon Simple Queue Service (Amazon SQS)

O Amazon Simple Queue Service (Amazon SQS) é um serviço de enfileiramento de mensagens.

Use o Amazon SQS para enviar, armazenar e receber mensagens entre componentes de software, sem perder mensagens ou precisar que outros serviços estejam disponíveis. No Amazon SQS, um aplicativo envia mensagens para uma fila. Um usuário ou serviço recupera uma mensagem da fila, processa-a e a exclui da fila.

### Outros serviços de computação

#### Computação sem servidor - serverless

No início deste módulo, você conheceu o Amazon EC2, um serviço que permite executar servidores virtuais na nuvem. Se você quiser executar aplicativos no Amazon EC2, faça o seguinte:

1. Provisione as instâncias (servidores virtuais).
2. Faça upload do código
3. Continue gerenciando as instâncias enquanto o aplicativo está em execução.

O termo “sem servidor”, ou serverless, significa que o código é executado em servidores, sem que você precise provisionar ou gerenciar esses servidores. Com a computação sem servidor, você pode se concentrar na inovação de novos produtos e recursos em vez de manter servidores.

Outro benefício da computação sem servidor é a flexibilidade de dimensionar aplicativos sem servidor automaticamente. A computação sem servidor pode ajustar a capacidade de aplicativos modificando as unidades de consumo, como taxa de transferência e memória.

Um serviço AWS para computação sem servidor é o AWS Lambda.

#### AWS Lambda

O AWS Lambda é um serviço que permite a execução de códigos sem a necessidade de provisionar ou gerenciar servidores.

Ao usar o AWS Lambda, você paga apenas pelo tempo de computação que consumir. As cobranças se aplicam ao tempo em que o código fica em execução. Você pode executar códigos para praticamente qualquer tipo de aplicativo ou serviço de back-end sem a necessidade de qualquer gerenciamento.

Por exemplo, uma função simples do Lambda é o redimensionamento automático de imagens com o upload feito na nuvem AWS. Nesse caso, a função é acionada ao fazer upload de uma nova imagem.

#### Contêineres

Os contêineres são uma maneira comum de empacotar códigos, configurações e dependências do aplicativo em um único objeto. Você também pode usar contêineres para processos e fluxos de trabalho nos quais há requisitos essenciais de segurança, confiabilidade e escalabilidade.

#### Amazon Elastic Container Service (Amazon ECS)

O Amazon Elastic Container Service (Amazon ECS) é um sistema de gerenciamento de contêineres altamente dimensionável e de alto desempenho que permite executar e dimensionar aplicativos em contêineres na AWS.

O Amazon ECS é compatível com contêineres Docker. O Docker é uma plataforma de software que permite criar, testar e implantar aplicativos rapidamente. A AWS é compatível com c Docker Community Edition de código aberto e do Docker Enterprise Edition baseado em assinatura. Com o Amazon ECS, você pode usar chamadas de API para iniciar e interromper aplicativos ativados pelo Docke

#### Amazon Elastic Kubernetes Service (Amazon EKS)

O Amazon Elastic Kubernetes Service (Amazon EKS) é um serviço totalmente gerenciado que você pode usar para executar o Kubernetes na AWS.

O Kubernetes é um software de código aberto que permite implantar e gerenciar aplicativos em contêineres em grande escala. Uma grande comunidade de voluntários mantém o Kubernetes, e a AWS trabalha ativamente em conjunto com essa comunidade Kubernetes. Conforme novos recursos e funcionalidades são lançados para aplicativos Kubernetes, você pode facilmente aplicar essas atualizações aos aplicativos gerenciados pelo Amazon EKS.

#### Amazon Fargate

O AWS Fargate é um mecanismo de computação sem servidor para contêineres. Ele funciona com o Amazon ECS e o Amazon EKS.

Com o AWS Fargate, você não precisa provisionar ou gerenciar servidores. O AWS Fargate gerencia sua infraestrutura de servidor para você. Você pode se concentrar em inovar e desenvolver seus aplicativos, pagando apenas pelos recursos necessários para executar os contêineres.

## Infraestrutura Global e Confiabilidade

Neste módulo, você aprenderá a:

- Resumir os benefícios da infraestrutura global da AWS.
- Descrever o conceito básico de Zonas de Disponibilidade.
- Descrever os benefícios do Amazon CloudFront e dos locais de borda.
- Comparar métodos diferentes de provisionamento de serviços AWS.

### Seleção de região

Ao determinar a Região certa para seus serviços, dados e aplicativos, considere os quatro fatores de negócios a seguir.

#### Conformidade com governança de dados e requisitos legais

Dependendo da sua empresa e localização, talvez seja necessário executar seus dados em áreas específicas. Por exemplo, se sua empresa exige que todos os dados residam dentro dos limites do Reino Unido, você deve escolher a Região Londres.

Nem todas as empresas têm regulamentações de dados específicas para a localização, portanto, você pode precisar se concentrar nos outros três fatores.

#### Proximidade dos usuários finais

A seleção de uma Região próxima de seus clientes ajudará você a obter o conteúdo com mais rapidez. Por exemplo, sua empresa está sediada em Washington, DC, e muitos de seus clientes residem em Singapura. Você pode considerar executar sua infraestrutura na Região Norte da Virgínia por estar perto da sede da empresa e executar os aplicativos a partir da Região Singapura.

#### Serviços disponíveis na Região

Às vezes, a Região mais próxima pode não ter todos os recursos que você deseja oferecer aos clientes. A AWS inova frequentemente ao criar novos serviços e expandir recursos em serviços existentes. No entanto, disponibilizar novos serviços em todo o mundo às vezes exige que a AWS desenvolva o hardware físico de cada Região por vez.

Suponha que seus desenvolvedores queiram criar um aplicativo que use o Amazon Braket (plataforma de computação quântica da AWS). Neste curso, o Amazon Braket ainda não está disponível em todas as Regiões AWS em todo o mundo, por isso, os desenvolvedores precisariam executá-lo em uma das Regiões que já o oferece.

#### Preços

Suponha que você pretenda executar aplicativos nos Estados Unidos e no Brasil. Com a estrutura tributária do Brasil, pode custar 50% mais caro executar a mesma carga de trabalho na Região São Paulo em comparação com a Região Oregon. Você aprenderá com detalhes que vários fatores determinam o preço, mas, por enquanto, saiba que o custo dos serviços pode variar entre as regiões.

### Zonas de disponibilidade

Uma Zona de Disponibilidade é um único data center ou um grupo de data centers em uma Região. As Zonas de Disponibilidade estão localizadas a dezenas de quilômetros de distância umas das outras. A proximidade é suficiente para haver baixa latência (tempo entre o momento em que o conteúdo foi solicitado e recebido) entre as Zonas de Disponibilidade. No entanto, se ocorrer um desastre em uma parte da Região, há distância suficiente para reduzir a chance de que várias Zonas de Disponibilidade sejam afetadas.

### Pontos de presença

Os pontos de presença são locais físicos onde a AWS tem infraestrutura para fornecer serviços de rede de baixa latência. Os pontos de presença são usados pelo Amazon CloudFront para fornecer conteúdo aos usuários finais com mais rapidez.

### AWS Elastic Beanstalk

O AWS Elastic Beanstalk é um serviço que gerencia a infraestrutura para você. Ele provisiona os recursos necessários para executar seu aplicativo e dimensiona automaticamente esses recursos para atender à demanda. Você carrega seu código e o Elastic Beanstalk cuida do resto.

Com o AWS Elastic Beanstalk, você fornece definições de código e configuração, e o Elastic Beanstalk implanta os recursos necessários para executar as seguintes tarefas:

- Ajustar capacidade
- Balancear carga
- Dimensionar de forma automática
- Monitorar a integridade do aplicativo

### AWS CloudFormation

O AWS CloudFormation é um serviço que permite provisionar recursos da AWS usando modelos. Os modelos são arquivos de texto simples que descrevem os recursos e suas dependências. Você pode usar o AWS CloudFormation para criar, atualizar e excluir recursos da AWS em uma única operação, conhecida como pilha.

Com o AWS CloudFormation, você pode considerar sua infraestrutura como código. Isso significa que você pode criar um ambiente escrevendo linhas de código em vez de usar o AWS Management Console para provisionar recursos individualmente.

O AWS CloudFormation provisiona os recursos de maneira segura e repetível, permitindo que você crie frequentemente a infraestrutura e os aplicativos sem precisar executar ações manuais ou criar scripts personalizados. Ele determina quais são as operações mais adequadas para gerenciar sua pilha e reverte as alterações automaticamente se detectar erros.

## Redes

## Armazenamento e banco de dados

## Segurança

## Monitoramento e análise

## Definição de preços e suporte

## Migração e inovação

## A jornada para a nuvem

## Noções básicas do AWS Certified Cloud Practitioner
