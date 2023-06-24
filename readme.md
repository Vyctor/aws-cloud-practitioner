
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
    - [Amazon Virtual Private Cloud (Amazon VPC)](#amazon-virtual-private-cloud-amazon-vpc)
    - [Gateway da internet](#gateway-da-internet)
    - [E se você tiver uma VPC apenas com recursos privados?](#e-se-você-tiver-uma-vpc-apenas-com-recursos-privados)
    - [AWS Direct Connect](#aws-direct-connect)
    - [Sub-redes e listas de controle de acesso à rede](#sub-redes-e-listas-de-controle-de-acesso-à-rede)
    - [Sub-redes](#sub-redes)
    - [Tráfego de rede em uma VPC](#tráfego-de-rede-em-uma-vpc)
    - [Lista de controle de acesso (ACL) de rede](#lista-de-controle-de-acesso-acl-de-rede)
    - [Filtragem de pacotes stateless](#filtragem-de-pacotes-stateless)
    - [Grupos de segurança](#grupos-de-segurança)
    - [Filtragem de pacotes stateful](#filtragem-de-pacotes-stateful)
    - [Domain Name System (DNS)](#domain-name-system-dns)
    - [Amazon Route 53](#amazon-route-53)
  - [Armazenamento e banco de dados](#armazenamento-e-banco-de-dados)
    - [Armazenamentos de instâncias](#armazenamentos-de-instâncias)
    - [Amazon Elastic Block Store (Amazon EBS)](#amazon-elastic-block-store-amazon-ebs)
    - [Snapshots do Amazon EBS](#snapshots-do-amazon-ebs)
    - [Armazenamento de objetos](#armazenamento-de-objetos)
    - [Amazon Simple Storage Service (Amazon S3)](#amazon-simple-storage-service-amazon-s3)
    - [Classes de armazenamento do Amazon S3](#classes-de-armazenamento-do-amazon-s3)
      - [S3 Standard](#s3-standard)
      - [S3 Standard Infraquent Access (S3 Standard IA)](#s3-standard-infraquent-access-s3-standard-ia)
      - [S3 Standard Infraquent Access (S3 Standard IA - One Zone)](#s3-standard-infraquent-access-s3-standard-ia---one-zone)
      - [S3 Intelligent Tiering](#s3-intelligent-tiering)
      - [S3 Glacier](#s3-glacier)
      - [S3 Glacier Deep Archive](#s3-glacier-deep-archive)
    - [Elastic File System (Amazon EFS)](#elastic-file-system-amazon-efs)
    - [Amazon RDS](#amazon-rds)
    - [Mecanismos de banco de dados do Amazon RDS](#mecanismos-de-banco-de-dados-do-amazon-rds)
    - [Amazon Aurora](#amazon-aurora)
    - [Amazon DynamoDB](#amazon-dynamodb)
    - [Amazon Redshift](#amazon-redshift)
    - [AWS Database Migration Service](#aws-database-migration-service)
      - [Outros casos de uso do AWS DMS](#outros-casos-de-uso-do-aws-dms)
    - [Outros serviços de banco de dados](#outros-serviços-de-banco-de-dados)

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

O termo "sem servidor", ou serverless, significa que o código é executado em servidores, sem que você precise provisionar ou gerenciar esses servidores. Com a computação sem servidor, você pode se concentrar na inovação de novos produtos e recursos em vez de manter servidores.

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

Neste módulo, você aprenderá a:

- Descrever os conceitos básicos de redes.
- Descrever a diferença entre recursos de redes públicas e privadas.
- Explicar como um gateway privado virtual funciona usando um cenário real.
- Explicar como uma rede privada virtual (VPN) funciona usando um cenário real.
- Descrever o benefício do AWS Direct Connect.
- Descrever o benefício das implantações híbridas.
- Descrever as camadas de segurança usadas em uma estratégia de TI.
- Descrever os serviços que os clientes usam para interagir com a rede global da AWS.

### Amazon Virtual Private Cloud (Amazon VPC)

Imagine os milhões de clientes que usam os serviços AWS. Imagine também os milhões de recursos que esses clientes criaram, como as instâncias do Amazon EC2. Sem limites para todos esses recursos, o tráfego de rede fluiria entre eles sem restrições.

Um serviço de rede que você pode usar para definir limites para seus recursos AWS é o Amazon Virtual Private Cloud (Amazon VPC).

O Amazon VPC permite que você provisione uma seção isolada da nuvem AWS. Nessa seção isolada, você pode executar os recursos em uma rede virtual que definir. Em uma Virtual Private Cloud (VPC), você pode organizar seus recursos em sub-redes. Uma sub-rede é uma seção de uma VPC que pode conter recursos como instâncias do Amazon EC2.

### Gateway da internet

Para permitir que o tráfego público da internet acesse sua VPC, é preciso anexar um gateway da internet à VPC.
Um gateway da internet é uma conexão entre uma VPC e a internet. Você pode pensar em um gateway da internet como sendo semelhante a uma porta que os clientes usam para entrar na cafeteria. Sem um gateway da internet, ninguém pode acessar os recursos em sua VPC.

### E se você tiver uma VPC apenas com recursos privados?

Para acessar recursos privados em uma VPC, você pode usar um gateway privado virtual.

Veja um exemplo de como um gateway privado virtual funciona. Você pode pensar na internet como o caminho entre sua casa e a cafeteria. Suponha que você está viajando com um guarda-costas para proteção. Você ainda usa o mesmo caminho que outros clientes, mas com uma camada extra de proteção.

O guarda-costas é como uma conexão de rede privada virtual (VPN) que criptografa (ou protege) seu tráfego de internet de todas as outras solicitações ao redor.

O gateway privado virtual é o componente que permite que o tráfego protegido da internet ingresse na VPC. Mesmo que sua conexão com a cafeteria tenha proteção extra, os engarrafamentos são possíveis porque você usa o mesmo caminho que outros clientes.

Um gateway privado virtual permite estabelecer uma conexão VPN (rede virtual privada) entre a VPC e uma rede privada, como um data center local ou uma rede corporativa interna. Um gateway privado virtual permitirá o tráfego na VPC somente se ele for proveniente de uma rede aprovada.

### AWS Direct Connect

O AWS Direct Connect é um serviço que permite estabelecer uma conexão privada dedicada entre seu data center e uma VPC.

Suponha que haja um prédio com um corredor que liga o prédio diretamente à cafeteria. Somente os moradores do prédio podem passar por esse corredor.

Esse corredor privado fornece o mesmo tipo de conexão dedicada que o AWS Direct Connect. Os moradores conseguem entrar na cafeteria sem precisarem usar a estrada pública compartilhada com outros clientes.

A conexão privada que o AWS Direct Connect fornece ajuda você a reduzir os custos de rede e a aumentar a quantidade de largura de banda que pode trafegar pela sua rede.

### Sub-redes e listas de controle de acesso à rede

Para saber mais sobre a função das sub-redes em uma VPC, revise o exemplo da cafeteria a seguir.

Primeiro, os clientes fazem os pedidos ao operador de caixa. O operador de caixa, em seguida, passa os pedidos para o barista. Esse processo permite que a fila prossiga sem problemas à medida que mais clientes entram.

Suponha que alguns clientes tentem pular a fila do caixa e fazer seus pedidos diretamente ao barista. Isso interrompe o fluxo de tráfego e faz com que os clientes acessem uma parte da cafeteria que é restrita a eles.

Para corrigir isso, os proprietários da cafeteria dividem a área do balcão colocando o operador de caixa e o barista em estações de trabalho separadas. A estação de trabalho do operador de caixa é voltada para o público e projetada para receber clientes. A área do barista é privada. O barista ainda pode receber pedidos do operador de caixa, mas não diretamente dos clientes.

Isso se parece à forma como você pode usar os serviços de redes da AWS para isolar recursos e determinar exatamente como o tráfego de rede flui.

Na cafeteria, você pode pensar na área do balcão como uma VPC. A área do balcão divide-se em duas áreas separadas para a estação de trabalho do operador de caixa e para a estação de trabalho do barista. Em uma VPC, sub-redes são áreas separadas usadas para agrupar recursos.

### Sub-redes

Uma sub-rede é uma seção de uma VPC na qual você pode agrupar recursos com base em necessidades operacionais ou de segurança. As sub-redes podem ser públicas ou privadas.

**Sub-redes públicas** contêm recursos que precisam ser acessíveis ao público, como o site de uma loja on-line.

As **sub-redes privadas** contêm recursos que devem ser acessíveis apenas pela sua rede privada, como um banco de dados contendo informações pessoais dos clientes e históricos de pedidos.

Em uma VPC, as sub-redes podem se comunicar entre si. Por exemplo, um aplicativo que envolve instâncias do Amazon EC2 em uma sub-rede pública que se comunicam com bancos de dados localizados em uma sub-rede privada.

### Tráfego de rede em uma VPC

Quando um cliente solicita dados de um aplicativo hospedado na nuvem AWS, essa solicitação é enviada como um pacote. Um pacote é uma unidade de dados enviada pela internet ou por uma rede.

Ele entra em uma VPC por um gateway da internet. Antes de um pacote poder entrar em uma sub-rede ou sair de uma sub-rede, ele verifica se há permissões. Essas permissões indicam quem enviou o pacote e como ele tenta se comunicar com os recursos em uma sub-rede.

O componente da VPC que verifica as permissões de pacotes para sub-redes é uma lista de controle de acesso (ACL) de rede.

### Lista de controle de acesso (ACL) de rede

Uma lista de controle de acesso (ACL) de rede é um firewall virtual que controla o tráfego de entrada e saída no nível de sub-rede.

Por exemplo, saia da cafeteria e imagine que você está em um aeroporto. No aeroporto, os viajantes estão tentando entrar em um país diferente. Você pode pensar nos viajantes como pacotes e no oficial de controle de passaportes como uma ACL de rede. O oficial de controle de passaportes verifica as credenciais dos viajantes quando entram e saem do país. Se um viajante estiver em uma lista aprovada, ele poderá passar. No entanto, se ele não estiver na lista aprovada ou estiver explicitamente em uma lista de viajantes proibidos, ele não poderá entrar.

Cada conta AWS tem uma ACL de rede regular. Ao configurar sua VPC, você pode usar a ACL de rede comum da sua conta ou criar ACLs de rede personalizadas.

Por padrão, a ACL de rede comum da conta permite todo o tráfego de entrada e saída, mas você pode modificá-la adicionando suas próprias regras. Para ACLs de rede personalizadas, todo o tráfego de entrada e saída é negado até que você adicione regras para especificar qual tráfego permitir. Além disso, todas as ACLs de rede têm uma regra de negação explícita. Essa regra garante que, se um pacote não corresponder a nenhuma das outras regras na lista, ele será negado.

### Filtragem de pacotes stateless

As ACLs de rede executam a filtragem de pacotes stateless. Elas não se lembram de nada e verificam os pacotes que atravessam a fronteira da sub-rede em todos os sentidos: entrada e saída.

Lembre-se do exemplo anterior de um viajante que quer entrar em um país diferente. Isso se parece com o envio de uma solicitação de uma instância do Amazon EC2 e para a internet.

Quando uma resposta de pacote para essa solicitação volta para a sub-rede, a ACL de rede não se lembra da solicitação anterior. A ACL de rede verifica a resposta do pacote em relação à lista de regras para determinar se deseja permitir ou negar.

Depois que um pacote entra em uma sub-rede, ele deve ter as permissões avaliadas para recursos dentro da sub-rede, como as instâncias do Amazon EC2.

O componente da VPC que verifica as permissões de pacote para uma instância do Amazon EC2 é um grupo de segurança.

### Grupos de segurança

Um grupo de segurança é um firewall virtual que controla o tráfego de entrada e saída de uma instância do Amazon EC2.

Por padrão, um grupo de segurança nega todo o tráfego de entrada e permite todo o tráfego de saída. Você pode adicionar regras personalizadas para configurar o tráfego a ser permitido ou negado.

Para este exemplo, suponha que você esteja em um prédio com um porteiro que cumprimenta os visitantes no lobby. Você pode pensar nos visitantes como pacotes e no porteiro como um grupo de segurança. À medida que os visitantes chegam, o porteiro verifica uma lista para garantir que eles podem entrar no edifício. No entanto, o porteiro não verifica a lista novamente quando os visitantes saem do edifício

Se você tiver várias instâncias do Amazon EC2 em uma sub-rede, poderá associá-las ao mesmo grupo de segurança ou usar grupos de segurança diferentes para cada instância.

### Filtragem de pacotes stateful

Os grupos de segurança fazem a filtragem de pacotes stateful. Eles se lembram de decisões anteriores tomadas para pacotes recebidos.

Considere o mesmo exemplo de envio de uma solicitação de uma instância do Amazon EC2 para a internet.

Quando uma resposta de pacote para essa solicitação retorna para a instância, o grupo de segurança lembra da solicitação anterior. O grupo de segurança permite que a resposta prossiga, independentemente das regras do grupo de segurança de entrada.

As ACLs de rede e os grupos de segurança permitem que você configure regras personalizadas para o tráfego em sua VPC. Conforme você aprende mais sobre a segurança e a rede da AWS, verifique se entendeu as diferenças entre ACLs de rede e grupos de segurança.

### Domain Name System (DNS)

Suponha que a AnyCompany tenha um site hospedado na nuvem AWS. Os clientes digitam o endereço da web no navegador e podem acessar o site. Isso acontece devido à resolução Domain Name System (DNS). A resolução de DNS envolve um servidor DNS que se comunica com um servidor web.

Você pode pensar no DNS como sendo a lista telefônica da internet. A resolução de DNS é o processo de conversão de um nome de domínio para um endereço IP.

Por exemplo, suponha que você deseja acessar o site da AnyCompany.

1. Quando você insere o nome de domínio no navegador, essa solicitação é enviada para um resolvedor de DNS do cliente.
2. O resolvedor de DNS do cliente solicita ao servidor DNS da empresa o endereço IP que corresponde ao site da AnyCompany.
3. O servidor DNS responde com o endereço IP para o site da AnyCompany, 192.0.2.0.

### Amazon Route 53

O Amazon Route 53 é um serviço web de DNS. Oferece aos desenvolvedores e empresas uma maneira confiável de rotear os usuários finais para aplicativos da internet hospedados na AWS.

O Amazon Route 53 conecta solicitações de usuários à infraestrutura em execução na AWS (como instâncias do Amazon EC2 e balanceadores de carga). Ele pode direcionar os usuários para a infraestrutura fora da AWS.

Outro recurso do Route 53 é a capacidade de gerenciar os registros DNS para nomes de domínio. Você pode registrar novos nomes de domínio diretamente no Route 53. Você também pode transferir registros DNS para nomes de domínio existentes gerenciados por outras empresas de registro de domínio. Isso permite que você gerencie todos os seus nomes de domínio em um único local.

No módulo anterior, você conheceu o Amazon CloudFront, um serviço de entrega de conteúdo. O exemplo a seguir descreve como o Route 53 e o Amazon CloudFront trabalham juntos para entregar conteúdo aos clientes.

## Armazenamento e banco de dados

Neste módulo, você aprenderá a:

- Resumir o conceito básico de armazenamento e bancos de dados.
- Descrever os benefícios do Amazon Elastic Block Store (Amazon EBS).
- Descrever os benefícios do Amazon Simple Storage Solution (Amazon S3).
- Descrever os benefícios do Amazon Elastic File System (Amazon EFS).
- Resumir várias soluções de armazenamento.
- Descrever os benefícios do Amazon Relational Database Service (RDS).
- Descrever os benefícios do Amazon DynamoDB.
- Resumir vários serviços de banco de dados.

### Armazenamentos de instâncias

Os volumes de armazenamento a nível de bloco se comportam como discos rígidos físicos.

Um armazenamento de instâncias fornece armazenamento temporário a nível de bloco para uma instância do Amazon EC2. Um armazenamento de instância é o armazenamento em disco fisicamente anexo ao computador host para uma instância do EC2 e, portanto, tem a mesma vida útil da instância. Quando a instância é encerrada, todos os dados no armazenamento de instâncias são perdidos.

### Amazon Elastic Block Store (Amazon EBS)

O Amazon Elastic Block Store (Amazon EBS) é um serviço que fornece volumes de armazenamento a nível de bloco que você pode usar com instâncias do Amazon EC2. Se você interromper ou encerrar uma instância do Amazon EC2, todos os dados no volume do EBS anexo permanecerão disponíveis.

Para criar um volume do EBS, defina a configuração (como tamanho e tipo do volume) e a provisão. Depois de criar um volume do EBS, ele pode ser anexado a uma instância do Amazon EC2.

Como os volumes do EBS são para dados que precisam perdurar, é importante fazer backup dos dados. Você pode fazer backups complementares de volumes do EBS criando snapshots do Amazon EBS.

Um volume do Amazon EBS armazena dados em uma única Zona de Disponibilidade.

Para anexar uma instância do Amazon EC2 a um volume do EBS, tanto a instância do Amazon EC2 quanto o volume do EBS devem residir na mesma Zona de Disponibilidade.

### Snapshots do Amazon EBS

Um snapshot do EBS é um backup incremental. Isso significa que o primeiro backup de um volume copia todos os dados. Nos backups subsequentes, somente os blocos de dados que foram alterados desde o snapshot mais recente são salvos.

Os backups complementares são diferentes dos backups completos, nos quais todos os dados em um volume de armazenamento são copiados cada vez que ocorre um backup. O backup completo inclui dados que não foram alterados desde o backup mais recente.

### Armazenamento de objetos

No armazenamento de objetos, cada objeto consiste em dados, metadados e uma chave.

Os dados podem ser uma imagem, vídeo, documento de texto ou qualquer outro tipo de arquivo. Os metadados contêm informações sobre o que são os dados, como eles são usados, o tamanho do objeto e assim por diante. A chave de um objeto é seu identificador exclusivo.

**Lembre-se de que, quando modificar um arquivo no armazenamento de blocos, somente as partes alteradas são atualizadas. Quando um arquivo no armazenamento de objetos é modificado, todo o objeto é atualizado.**

### Amazon Simple Storage Service (Amazon S3)

O Amazon Simple Storage Service (Amazon S3) é um serviço que fornece armazenamento a nível do objeto. O Amazon S3 armazena dados como objetos em buckets.

É possível fazer upload de qualquer tipo de arquivo para o Amazon S3, como imagens, vídeos, arquivos de texto e assim por diante. Por exemplo, você pode usar o Amazon S3 para armazenar arquivos de backup, arquivos de mídia para um site ou documentos arquivados. O Amazon S3 oferece espaço de armazenamento ilimitado. O tamanho máximo de arquivo para um objeto no Amazon S3 é de 5 TB.

Ao fazer upload de um arquivo para o Amazon S3, é possível definir permissões para controlar a visibilidade e o acesso a ele. Você também pode usar o recurso de versionamento do Amazon S3 para rastrear alterações em seus objetos ao longo do tempo.

### Classes de armazenamento do Amazon S3

Com o Amazon S3, você paga somente pelo que usar. Você pode escolher dentre diversas categorias de armazenamento aquela que melhor se ajusta às suas necessidades de negócios e de custo. Ao selecionar uma categoria de armazenamento do Amazon S3, considere esses dois fatores:

- Com que frequência você planeja recuperar seus dados
- Seus dados precisam estar muito ou pouco disponíveis

#### S3 Standard

- Projetado para dados acessados com frequência
- Armazena dados em um mínimo de três Zonas de Disponibilidade

O S3 Standard fornece alta disponibilidade para objetos. Isso o torna uma boa escolha para diversos casos de uso, como sites, distribuição de conteúdo e análise de dados. O S3 Standard tem um custo mais alto do que outras categorias de armazenamento para dados acessados com pouca frequência e armazenamento de arquivamento.

#### S3 Standard Infraquent Access (S3 Standard IA)

- Ideal para dados com pouca frequência de acesso
- Semelhante ao S3 Standard, mas com um preço de armazenamento mais baixo e um preço de recuperação mais alto
-

O S3 Standard-IA é ideal para dados acessados com pouca frequência, mas que precisam ter alta disponibilidade para quando necessário. O S3 Standard e o S3 Standard - IA armazenam dados em um mínimo de três Zonas de Disponibilidade. O S3 Standard - IA fornece o mesmo nível de disponibilidade do S3 Standard, mas com um preço de armazenamento mais baixo e um preço de recuperação mais alto.

#### S3 Standard Infraquent Access (S3 Standard IA - One Zone)

- Armazena dados em uma única Zona de Disponibilidade
- Tem um preço de armazenamento menor do que o S3 Standard - IA
  
Comparado com o S3 Standard e o S3 Standard - IA, que armazenam dados em um mínimo de três Zonas de Disponibilidade, o S3 One Zone - IA armazena em uma única Zona de Disponibilidade. Isso o torna uma boa categoria de armazenamento nas seguintes condições:

- Você quer economizar custos com armazenamento.
- Você pode reproduzir facilmente seus dados em caso de falha na Zona de Disponibilidade.

#### S3 Intelligent Tiering

- Ideal para dados com padrões de acesso desconhecidos ou em alteração
- Requer uma pequena taxa mensal de monitoramento e automação por objeto
  
Na categoria de armazenamento S3 Intelligent-Tiering, o Amazon S3 monitora os padrões de acesso dos objetos. Se você não acessou um objeto por 30 dias consecutivos, o Amazon S3 o move automaticamente para o nível de acesso pouco frequente S3 Standard - IA. Se você acessar um objeto no nível de acesso pouco frequente, o Amazon S3 o move automaticamente para o nível de acesso frequente S3 Standard.

#### S3 Glacier

- Armazenamento de baixo custo projetado para arquivamento de dados
- Capaz de recuperar objetos em poucos minutos a horas

O S3 Glacier é uma categoria de armazenamento de baixo custo, ideal para o arquivamento de dados. Por exemplo, você pode usar essa categoria para armazenar registros de clientes arquivados ou arquivos de fotos e vídeos mais antigos.

#### S3 Glacier Deep Archive

- Categoria de armazenamento de objetos com menor custo, ideal para arquivamento
- Capaz de recuperar objetos em 12 horas

Ao decidir entre o Amazon S3 Glacier e o Amazon S3 Glacier Deep Archive, considere a prontidão com que você precisa recuperar objetos arquivados. É possível recuperar objetos armazenados na categoria de armazenamento S3 Glacier de alguns minutos a algumas horas. Em comparação, é possível recuperar objetos armazenados na categoria de armazenamento S3 Glacier Deep Archive em até 12 horas.

### Elastic File System (Amazon EFS)

No armazenamento de arquivos, vários clientes (como usuários, aplicativos, servidores e assim por diante) podem acessar dados armazenados em pastas de arquivos compartilhadas. Nessa abordagem, um servidor de armazenamento usa armazenamento em bloco com um sistema de arquivos local para organizar os arquivos. Os clientes acessam dados através de caminhos de arquivo.

Comparado ao armazenamento em blocos e ao armazenamento de objetos, o armazenamento de arquivos é ideal para casos de uso em que um grande número de serviços e recursos precisam acessar os mesmos dados ao mesmo tempo.

O Amazon Elastic File System (Amazon EFS) é um sistema de arquivos escalável usado com os serviços de nuvem AWS e recursos locais. À medida que você adiciona e remove arquivos, o Amazon EFS expande e retrai automaticamente. Ele pode dimensionar sob demanda para petabytes sem interromper os aplicativos.

O Amazon EFS é um serviço regional. Ele armazena dados em várias Zonas de Disponibilidade e entre elas.

O armazenamento duplicado permite que você acesse dados simultaneamente de todas as Zonas de Disponibilidade na Região em que um sistema de arquivos está localizado. Além disso, os servidores locais podem acessar o Amazon EFS usando o AWS Direct Connect.

### Amazon RDS

O Amazon Relational Database Service (Amazon RDS) é um serviço que permite executar bancos de dados relacionais na nuvem AWS.

O Amazon RDS é um serviço gerenciado que automatiza tarefas como provisionamento de hardware, configuração de banco de dados, patch e backups. Com esses recursos, você pode passar menos tempo concluindo tarefas administrativas e mais tempo usando dados para inovar seus aplicativos. Você pode integrar o Amazon RDS a outros serviços para atender às suas necessidades de negócios e operacionais, como usar o AWS Lambda para consultar seu banco de dados a partir de um aplicativo sem servidor.

O Amazon RDS fornece inúmeras opções de segurança diferentes. Muitos mecanismos de banco de dados do Amazon RDS oferecem criptografia em repouso (protegendo os dados enquanto estão armazenados) e criptografia em trânsito (protegendo os dados enquanto estão sendo enviados e recebidos).

### Mecanismos de banco de dados do Amazon RDS

O Amazon RDS está disponível em seis mecanismos de banco de dados, que otimizam memória, desempenho ou entrada/saída (E/S). Os mecanismos de banco de dados compatíveis são:

- Amazon Aurora
- PostgreSQL
- MySQL
- MariaDB
- Oracle Database
- Microsoft SQL Server

### Amazon Aurora

Amazon Aurora

O Amazon Aurora é um banco de dados relacional de nível empresarial. É compatível com os bancos de dados relacionais MySQL e PostgreSQL. É até cinco vezes mais rápido do que os bancos de dados MySQL comuns e até três vezes mais rápido do que os bancos de dados PostgreSQL comuns.

O Amazon Aurora ajuda a reduzir os custos do banco de dados reduzindo operações desnecessárias de entrada/saída (E/S), garantindo que os recursos do banco de dados permaneçam confiáveis e disponíveis.

Considere o Amazon Aurora se suas cargas de trabalho exigem alta disponibilidade. Ele replica seis cópias de seus dados em três Zonas de Disponibilidade e faz backup contínuo de seus dados para o Amazon S3.

### Amazon DynamoDB

O Amazon DynamoDB é um serviço de banco de dados de chave-valor. Ele oferece um desempenho de um dígito de milissegundo em qualquer scaling.

O DynamoDB é sem servidor, o que significa que você não precisa provisionar, aplicar patches ou gerenciar servidores.

Você também não precisa instalar, manter ou operar o software.

À medida que o tamanho do banco de dados expande ou retrai, o DynamoDB é dimensionado automaticamente para ajustar as alterações na capacidade e, ao mesmo tempo, manter o desempenho consistente.

Isso o torna uma escolha adequada para casos de uso que exigem alto desempenho durante o scaling.

### Amazon Redshift

O Amazon Redshift é serviço de data warehouse que você pode usar para análise de big data. Ele oferece a capacidade de coletar dados de muitas fontes além de ajudar a entender relações e tendências em todos os seus dados.

### AWS Database Migration Service

O AWS Database Migration Service (AWS DMS) permite migrar bancos de dados relacionais e não relacionais e outros tipos de armazenamentos de dados.

Com o AWS DMS, você move dados entre bancos de dados de origem e de destino. Os bancos de dados de origem e de destino podem ser do mesmo tipo ou de tipos diferentes. Durante a migração, o banco de dados de origem permanece operacional, reduzindo o tempo de inatividade em qualquer aplicativo que dependa do banco de dados.

Por exemplo, suponha que você tenha um banco de dados MySQL armazenado localmente em uma instância do Amazon EC2 ou no Amazon RDS. Pense no banco de dados MySQL como seu banco de dados de origem. Usando o AWS DMS, você pode migrar seus dados para um banco de dados de destino, por exemplo, um banco de dados do Amazon Aurora.

#### Outros casos de uso do AWS DMS

- Os desenvolvedores conseguem testar os aplicativos com os dados de produção sem afetar os usuários de produção
- Combinação de vários bancos de dados em um único banco de dados
- Envio de cópias contínuas de seus dados para outras fontes de destino em vez de fazer uma migração única

### Outros serviços de banco de dados

- O Amazon DocumentDB é um serviço de banco de dados de documentos compatível com cargas de trabalho do MongoDB. (MongoDB é um programa de banco de dados de documentos.
- O Amazon Neptune é um serviço de banco de dados de grafo. Você pode usar o Amazon Neptune para criar e executar aplicativos que funcionam com conjuntos de dados altamente conectados, como mecanismos de recomendação, detecção de fraudes e gráficos de conhecimento.
- O Amazon Quantum Ledger Database (Amazon QLDB) é um serviço de banco de dados ledger. Você pode usar o Amazon QLDB para revisar um histórico completo de todas as alterações feitas nos dados do aplicativo.
- O Amazon Managed Blockchain é um serviço para criar e gerenciar redes de blockchain com estruturas de código aberto. O Blockchain é um sistema de registro distribuído que permite que várias partes executem transações e compartilhem dados sem uma autoridade central.
- O Amazon ElastiCache é um serviço que adiciona camadas de cache sobre seus bancos de dados para ajudar a melhorar os tempos de leitura de solicitações comuns. Ele é compatível com dois tipos de armazenamentos de dados: Redis e Memcached.
- O Amazon DynamoDB Accelerator (DAX) é um cache em memória para o DynamoDB. Ele ajuda a melhorar os tempos de resposta de milissegundos para microssegundos.
