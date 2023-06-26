
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
  - [Segurança](#segurança)
    - [Modelo de responsabilidade compartilhada](#modelo-de-responsabilidade-compartilhada)
    - [AWS Identity and Access Management (IAM)](#aws-identity-and-access-management-iam)
    - [Usuário-raiz da conta AWS](#usuário-raiz-da-conta-aws)
    - [Usuários do IAM](#usuários-do-iam)
    - [Políticas do IAM](#políticas-do-iam)
    - [Grupos do IAM](#grupos-do-iam)
    - [Funções do IAM](#funções-do-iam)
    - [Autenticação multifator](#autenticação-multifator)
    - [AWS Organizations](#aws-organizations)
      - [Unidades Organizacionais](#unidades-organizacionais)
    - [Conformidade](#conformidade)
      - [AWS Artifact](#aws-artifact)
      - [Artifact Agreements](#artifact-agreements)
      - [Artifact Reports](#artifact-reports)
      - [Centro de conformidade para o cliente](#centro-de-conformidade-para-o-cliente)
    - [Ataques DDOs](#ataques-ddos)
      - [Ataques distribuídos de negação de serviço](#ataques-distribuídos-de-negação-de-serviço)
      - [AWS Shield](#aws-shield)
        - [AWS Shield Standard](#aws-shield-standard)
        - [AWS Shield Advanced](#aws-shield-advanced)
    - [Serviços de Segurança Adicionais](#serviços-de-segurança-adicionais)
      - [AWS Key Management Service (AWS KMS)](#aws-key-management-service-aws-kms)
      - [AWS WAF](#aws-waf)
      - [Amazon Inspector](#amazon-inspector)
      - [Amazon GuardDuty](#amazon-guardduty)
  - [Monitoramento e análise](#monitoramento-e-análise)
    - [Amazon CLoudWatch](#amazon-cloudwatch)
      - [Alarmes do CloudWatch](#alarmes-do-cloudwatch)
      - [Painel do CloudWatch](#painel-do-cloudwatch)
    - [AWS CloudTrail](#aws-cloudtrail)
    - [AWS Trusted Advisor](#aws-trusted-advisor)
      - [Painel do AWS Trusted Advisor](#painel-do-aws-trusted-advisor)
  - [Definição de preços e suporte](#definição-de-preços-e-suporte)
    - [Nível Gratuito da AWS](#nível-gratuito-da-aws)
      - [Sempre gratuito](#sempre-gratuito)
      - [12 meses gratuitos](#12-meses-gratuitos)
      - [Versão de teste](#versão-de-teste)
    - [Conceitos de definição de preço da AWS](#conceitos-de-definição-de-preço-da-aws)
      - [Pague somente pelo que usar](#pague-somente-pelo-que-usar)
      - [Pague menos ao fazer reserva](#pague-menos-ao-fazer-reserva)
      - [Pague menos com descontos baseados em volume, quando usar mais](#pague-menos-com-descontos-baseados-em-volume-quando-usar-mais)
      - [Calculadora de preços da AWS](#calculadora-de-preços-da-aws)
    - [Painel de cobrança](#painel-de-cobrança)
    - [Faturamento consolidado](#faturamento-consolidado)
    - [AWS Budgets](#aws-budgets)
    - [AWS Cost Explorer](#aws-cost-explorer)
    - [Planos do AWS Support](#planos-do-aws-support)
      - [Basic](#basic)
      - [Suporte Developer, Business e Enterprise](#suporte-developer-business-e-enterprise)
      - [Developer](#developer)
      - [Business](#business)
      - [Enterprise](#enterprise)
      - [Technical Account Manager (TAM)](#technical-account-manager-tam)
    - [AWS Marketplace](#aws-marketplace)
  - [Migração e inovação](#migração-e-inovação)
    - [AWS Cloud Adoption Framework (AWS CAF)](#aws-cloud-adoption-framework-aws-caf)
      - [Perspectiva de negócio](#perspectiva-de-negócio)
      - [Perspectiva de pessoas](#perspectiva-de-pessoas)
      - [Perspectiva de governança](#perspectiva-de-governança)
      - [Perspectiva de plataforma](#perspectiva-de-plataforma)
      - [Perspectiva de segurança](#perspectiva-de-segurança)
      - [Perspectiva de operações](#perspectiva-de-operações)
    - [Estratégia de migração para a nuvem](#estratégia-de-migração-para-a-nuvem)
      - [Redefinição de hospedagem](#redefinição-de-hospedagem)
      - [Redefinição de plataforma](#redefinição-de-plataforma)
      - [Refatoração/rearquitetura](#refatoraçãorearquitetura)
      - [Recompra](#recompra)
      - [Retenção](#retenção)
      - [Inativação](#inativação)
    - [AWS Snow Family](#aws-snow-family)
      - [AWS Snowcone](#aws-snowcone)
      - [AWS Snowball](#aws-snowball)
      - [AWS Snowmobile](#aws-snowmobile)
    - [Inovação com a AWS](#inovação-com-a-aws)
      - [Aplicativos sem servidor](#aplicativos-sem-servidor)
      - [Inteligencia Artificial](#inteligencia-artificial)
      - [Machine Learning](#machine-learning)

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

## Segurança

### Modelo de responsabilidade compartilhada

Ao longo deste curso, você aprendeu sobre diversos recursos que podem ser criados na nuvem AWS. Esses recursos são as instâncias do Amazon EC2, os buckets do Amazon S3 e os bancos de dados do Amazon RDS. Quem é responsável por manter esses recursos seguros: você (o cliente) ou AWS?

A resposta é ambos. Isso é porque você não trata seu ambiente AWS como um único objeto. Em vez disso, você trata o ambiente como uma coleção de partes que se combinam. A AWS é responsável por algumas partes do seu ambiente e você (o cliente) é responsável por outras. Esse conceito é conhecido como modelo de responsabilidade compartilhada.

O modelo de responsabilidade compartilhada divide-se em responsabilidades do cliente (comumente chamadas de "segurança na nuvem") e responsabilidades da AWS (comumente referidas como "segurança da nuvem").

Você pode pensar nesse modelo como sendo parecido com a divisão de responsabilidades entre um proprietário e uma construtora. A construtora (AWS) é responsável por edificar sua casa e garantir que ela seja construída com solidez. Como proprietário (o cliente), é sua responsabilidade proteger tudo na casa, garantindo que as portas estejam fechadas e trancadas.

### AWS Identity and Access Management (IAM)

O AWS Identity and Access Management (IAM) permite que você gerencie o acesso aos serviços e recursos AWS com segurança.
O IAM oferece a flexibilidade de configurar o acesso com base nas necessidades operacionais e de segurança específicas da sua empresa. Você pode fazer isso usando uma combinação dos recursos do IAM, explorados em detalhes nesta lição:

- Usuários, grupos e funções do IAM
- Políticas do IAM
- Autenticação multifator

Você também conhecerá as práticas recomendadas para cada um desses recursos.

### Usuário-raiz da conta AWS

Ao criar uma conta AWS pela primeira vez, você começa com uma identidade conhecida como usuário-raiz.

O usuário-raiz é acessado ao entrar com o endereço de e-mail e a senha usados para criar a conta AWS. Pense no usuário-raiz como sendo parecido com o proprietário da cafeteria: ele tem acesso completo a todos os serviços e recursos AWS na conta.

**Não use o usuário-raiz para tarefas cotidianas.**

Em vez disso, use o usuário-raiz para criar seu primeiro usuário do IAM e atribua a ele permissões para criar outros usuários.

Em seguida, continue a criar outros usuários do IAM e acesse essas identidades para executar tarefas comuns em toda a AWS. Use o usuário-raiz somente quando precisar executar um número limitado de tarefas disponíveis somente para o usuário-raiz. Exemplos dessas tarefas são a alteração do endereço de e-mail do usuário-raiz e a alteração do plano do AWS Support.

### Usuários do IAM

Um usuário do IAM é uma identidade que você cria na AWS. Ele representa a pessoa ou o aplicativo que interage com os serviços e recursos AWS. Consiste em um nome e credenciais.

Por padrão, ao criar um novo usuário do IAM na AWS, não há permissões associadas a ele. Para permitir que o usuário do IAM execute ações específicas na AWS, como iniciar uma instância do Amazon EC2 ou criar um bucket do Amazon S3, você deve conceder ao usuário do IAM as permissões necessárias.

**Recomendamos que crie usuários individuais do IAM para cada pessoa que precisa acessar a AWS.**

Mesmo que você tenha vários funcionários que precisem do mesmo nível de acesso, você deve criar usuários individuais do IAM para cada um deles. Isso fornece segurança adicional, permitindo que cada usuário do IAM tenha um conjunto exclusivo de credenciais de segurança.

### Políticas do IAM

Uma política do IAM é um documento que concede ou nega permissões para serviços e recursos AWS.  

As políticas do IAM permitem que você personalize os níveis de acesso dos usuários aos recursos. Por exemplo, você pode permitir que os usuários acessem todos os buckets do Amazon S3 em sua conta AWS ou apenas um bucket específico.

Siga o princípio de segurança de menor privilégio ao conceder permissões.

Seguindo esse princípio, você ajuda a impedir que usuários ou funções tenham mais permissões do que o necessário para executar as tarefas.

Por exemplo, se um funcionário precisar acessar apenas um bucket específico, especifique o bucket na política do IAM. Faça isso em vez de conceder ao funcionário acesso a todos os buckets em sua conta AWS.

### Grupos do IAM

Um grupo do IAM é um conjunto de usuários do IAM. Ao atribuir uma política do IAM a um grupo, todos os usuários do grupo recebem permissões especificadas pela política.

Eis um exemplo de como isso pode funcionar na cafeteria. Em vez de atribuir permissões aos operadores um de cada vez, o proprietário pode criar o grupo "operadores de caixa" do IAM. O proprietário pode, em seguida, adicionar usuários do IAM ao grupo e associar permissões no nível do grupo.

A atribuição de políticas do IAM no nível de grupo também facilita o ajuste de permissões quando um funcionário é transferido para um trabalho diferente. Por exemplo, se um operador de caixa se tornar um especialista em inventário, o proprietário da cafeteria o removerá do grupo "operadores de caixa" do IAM e o adicionará ao grupo "especialistas em inventário". Isso garante que os funcionários tenham apenas as permissões necessárias para a função atual.

E se um funcionário da cafeteria não tiver trocado de função permanentemente, mas, em vez disso, revezar em diferentes estações de trabalho ao longo do dia? Esse funcionário pode ter o acesso de que precisa pelas funções do IAM.

### Funções do IAM

Na cafeteria, um funcionário se reveza em diferentes estações de trabalho ao longo do dia. Dependendo do tamanho da equipe da cafeteria, esse funcionário pode desempenhar várias tarefas: trabalhar na caixa registradora, atualizar o sistema de inventário, processar pedidos on-line e assim por diante.

Quando o funcionário precisa alternar para uma tarefa diferente, ele desiste do acesso a uma estação de trabalho e obtém acesso à próxima estação de trabalho. O funcionário pode alternar facilmente entre estações de trabalho, mas, a qualquer momento, ele pode ter acesso a uma única estação de trabalho. Esse mesmo conceito existe na AWS com as funções do IAM.

Uma função do IAM é uma identidade que você pode assumir para obter acesso temporário a permissões.

Antes que um usuário, aplicativo ou serviço do IAM possa assumir uma função do IAM, ele deve receber permissões para alternar para a função. Quando alguém assume uma função do IAM, ele abandona todas as permissões anteriores que tinha em uma função anterior e assume as permissões da nova função.

**As funções do IAM são ideais para situações em que o acesso a serviços ou recursos precisa ser concedido temporariamente, em vez de a longo prazo.**

### Autenticação multifator

Você já entrou em um site que exigia várias informações para verificar sua identidade? Talvez tenha sido necessário digitar sua senha e, em seguida, uma segunda forma de autenticação, como um código aleatório enviado para o telefone. Esse é um exemplo de autenticação multifator.

No IAM, a autenticação multifator (MFA) fornece uma camada adicional de segurança para sua conta AWS.

### AWS Organizations

Suponha que sua empresa tenha múltiplas contas AWS. Você pode usar o AWS Organizationspara consolidar e gerenciar múltiplas contas AWS em um local central.

Ao criar uma organização, o AWS Organizations cria automaticamente uma raiz, que é o contêiner primário para todas as contas de sua organização.

No AWS Organizations, você pode controlar de forma centralizada as permissões para as contas em sua organização usando as políticas de controle de serviço (SCPs). As SCPs permitem que você coloque restrições nos serviços AWS, recursos e ações individuais de API que os usuários e funções em cada conta podem acessar.

**A cobrança consolidada é outro recurso do AWS Organizations. Você conhecerá melhor a cobrança consolidada em um módulo posterior.**

#### Unidades Organizacionais

No AWS Organizations, você pode agrupar contas em unidades organizacionais (UO) para facilitar o gerenciamento de contas com requisitos de negócios ou segurança semelhantes. Ao aplicar uma política a uma UO, todas as contas na UO herdam automaticamente as permissões especificadas na política.  

Ao organizar contas separadas em UO, você pode isolar mais facilmente cargas de trabalho ou aplicativos com requisitos de segurança específicos. Por exemplo, se sua empresa tiver contas que podem acessar apenas os serviços AWS que atendam a determinados requisitos normativos, você poderá colocar essas contas em uma UO. Em seguida, você pode associar uma política à UO que bloqueia o acesso a todos os outros serviços AWS que não atendam aos requisitos normativos.

### Conformidade

A AWS oferece uma ampla variedade de serviços e recursos para ajudar você a atender aos requisitos de conformidade e segurança para a AWS e seus aplicativos executados na AWS.

#### AWS Artifact

Dependendo do setor de sua empresa, talvez seja necessário manter padrões específicos. Uma auditoria ou inspeção assegurará que a empresa cumpriu esses padrões.

O AWS Artifact é um serviço que fornece acesso sob demanda a relatórios de segurança e conformidade da AWS e a contratos on-line selecionados. O AWS Artifact tem duas seções principais: AWS Artifact Agreements e o AWS Artifact Reports.

#### Artifact Agreements

Suponha que sua empresa precise assinar um contrato com a AWS em relação ao uso de determinados tipos de informações em todos os serviços AWS. Você pode fazer isso pelo AWS Artifact Agreements.

No AWS Artifact Agreements, você pode revisar, aceitar e gerenciar contratos para uma conta individual e para todas as suas contas no AWS Organizations. Diferentes tipos de acordos são oferecidos para atender às necessidades dos clientes sujeitos a regulamentações específicas, como a Lei de Portabilidade e Responsabilidade dos Provedores de Saúde dos EUA (HIPAA).

#### Artifact Reports

Suponha que um membro da equipe de desenvolvimento da sua empresa esteja criando um aplicativo e precise de mais informações sobre a responsabilidade em cumprir determinados padrões regulatórios. Você pode recomendar o acesso a essas informações em AWS Artifact Reports.

O AWS Artifact Reports fornece relatórios de conformidade por auditores terceirizados. Esses auditores testaram e verificaram se a AWS está em conformidade com diversas normas e regulamentações de segurança globais, regionais e específicas do setor. O AWS Artifact Reports se mantém atualizado com os relatórios publicados mais recentes. Você pode fornecer os artefatos de auditoria da AWS aos auditores ou reguladores como evidência dos controles de segurança da AWS.

#### Centro de conformidade para o cliente

O Centro de conformidade para o cliente contém recursos que ajudam você a saber mais sobre a conformidade da AWS.

No Centro de conformidade para o cliente, você pode ler histórias de conformidade dos clientes para descobrir como as empresas de setores regulamentados resolveram vários desafios de conformidade, governança e auditoria.

Você também pode acessar whitepapers e documentação de conformidade sobre tópicos como:

- Respostas da AWS aos principais problemas de conformidade
- Uma visão geral do risco e da conformidade da AWS
- Uma lista de verificação da segurança de auditoria

Além disso, o Centro de conformidade para o cliente inclui um plano de aprendizagem para auditores. Esse plano de aprendizagem foi elaborado para indivíduos em funções jurídicas, de auditoria e de conformidade que desejam saber mais sobre como suas operações internas podem demonstrar conformidade usando a nuvem AWS.

### Ataques DDOs

Os clientes podem telefonar para a cafeteria para fazer os pedidos. Depois de atender cada chamada, um operador de caixa anota o pedido e o entrega ao barista.

No entanto, suponha que uma pessoa esteja telefonando várias vezes para fazer pedidos, mas nunca retira suas bebidas. Isso faz com que o operador de caixa fique indisponível para atender chamadas de outros clientes. A cafeteria pode tentar parar os pedidos falsos bloqueando o número de telefone que a pessoa está usando.

Nesse cenário, as ações da pessoa passando o trote são semelhantes a um ataque de negação de serviço.

Um ataque de negação de serviço (DoS) é uma tentativa deliberada de tornar um site ou aplicativo indisponível para os usuários.
Por exemplo, um invasor pode inundar um site ou aplicativo com tráfego excessivo de rede até que o site ou o aplicativo de destino se sobrecarregue e não seja mais capaz de responder. Se o site ou aplicativo ficar indisponível, o serviço será negado aos usuários tentando fazer solicitações legítimas.

#### Ataques distribuídos de negação de serviço

Agora, suponha que a pessoa passando o trote tenha recrutado a ajuda de amigos.

Essa pessoa e seus amigos telefonam repetidamente para a cafeteria para fazer pedidos, mesmo que não pretendam retirá-los. Esses pedidos são provenientes de números de telefone diferentes e é impossível que a cafeteria bloqueie todos eles. Além disso, o influxo de chamadas dificultou cada vez mais o atendimento aos clientes. Isso se parece com um ataque distribuído de negação de serviço.

Em um ataque distribuído de negação de serviço (DDoS), várias fontes são usadas para iniciar um ataque que visa tornar um site ou aplicativo indisponível. O ataque pode ser feito por um grupo de invasores, ou até mesmo um único invasor. O único invasor pode usar vários computadores infectados (também conhecidos como “bots”) para enviar tráfego excessivo a um site ou aplicativo.

Para ajudar a minimizar o efeito de ataques DoS e DDoS em seus aplicativos, você pode usar o AWS Shield.

#### AWS Shield

O AWS Shield é um serviço que protege aplicativos contra ataques DDoS. O AWS Shield oferece dois níveis de proteção: Standard e Advanced.

##### AWS Shield Standard

O AWS Shield Standard protege automaticamente todos os clientes AWS sem nenhum custo. Ele protege seus recursos AWS contra os tipos de ataques DDoS mais comuns e frequentes.

À medida que o tráfego de rede ingressa em seus aplicativos, o AWS Shield Standard usa diversas técnicas de análise para detectar tráfego mal-intencionado em tempo real e mitigá-lo automaticamente. O AWS Shield Standard também monitora continuamente o tráfego de rede para detectar novos ataques e reagir rapidamente para proteger seus aplicativos.

##### AWS Shield Advanced

O AWS Shield Advanced é um serviço pago que fornece diagnósticos detalhados de ataques e a capacidade de detectar e mitigar ataques elaborados de DDoS.

Ele também se integra a outros serviços, como o Amazon CloudFront, o Amazon Route 53 e o Elastic Load Balancing. Além disso, você pode integrar o AWS Shield ao AWS WAF escrevendo regras personalizadas para mitigar ataques complexos de DDoS.

### Serviços de Segurança Adicionais

#### AWS Key Management Service (AWS KMS)

A cafeteria tem muitos itens, como máquinas de café, confeitaria, dinheiro nas caixas registradoras e assim por diante. Você pode pensar nesses itens como dados. Os proprietários da cafeteria querem garantir que todos esses itens estejam protegidos, independentemente de estarem dispostos na sala de armazenamento ou em transporte.

Da mesma forma, você deve garantir que os dados de seus aplicativos estejam protegidos durante o armazenamento (criptografia em repouso) e sendo transmitidos (criptografia em trânsito).

O AWS Key Management Service (AWS KMS) permite que você execute operações de criptografia pelo uso de chaves de criptografia. Uma chave de criptografia é uma cadeia aleatória de dígitos usada para bloquear (criptografar) e desbloquear (descriptografar) dados. Você pode usar o AWS KMS para criar, gerenciar e usar chaves de criptografia. Você também pode controlar o uso de chaves em uma ampla gama de serviços e em seus aplicativos.

Com o AWS KMS, você pode escolher os níveis específicos de controle de acesso necessários para suas chaves. Por exemplo, você pode especificar quais usuários e funções do IAM podem gerenciar chaves. Do mesmo modo, você pode desativar temporariamente as chaves para que não sejam mais usadas. Suas chaves nunca saem do AWS KMS e você está sempre no controle delas.

#### AWS WAF

O AWS WAF é um firewall de aplicativo web que permite monitorar solicitações de rede que entram em seus aplicativos web.

O AWS WAF trabalha em conjunto com o Amazon CloudFront e um balanceador de carga de aplicativo. Lembre-se das listas de controle de acesso de rede que você aprendeu em um módulo anterior. O AWS WAF funciona de forma semelhante para bloquear ou permitir o tráfego. No entanto, ele faz isso usando uma lista de controle de acesso (ACL) da web para proteger seus recursos AWS.

Suponha que o aplicativo tenha recebido solicitações de rede mal-intencionadas de vários endereços IP. Você quer impedir que essas solicitações continuem a acessar seu aplicativo, mas também deseja garantir que usuários legítimos ainda possam acessá-lo. Você configura a ACL da web para permitir todas as solicitações, exceto aquelas dos endereços IP que você especificou.

Quando uma solicitação entra no AWS WAF, ele confere a lista de regras configurada na ACL da web. Se uma solicitação não for proveniente de um dos endereços IP bloqueados, o AWS WAF permite o acesso ao aplicativo.

No entanto, se uma solicitação for proveniente de um dos endereços IP bloqueados que você especificou na ACL da web, o acesso é negado.

#### Amazon Inspector

Suponha que os desenvolvedores da cafeteria estão desenvolvendo e testando um novo aplicativo para pedidos. Eles querem se certificar de que estão projetando o aplicativo de acordo com as práticas recomendadas de segurança. Contudo, eles têm vários outros aplicativos para desenvolver, por isso, não podem passar tempo demais fazendo avaliações manuais. Para fazer avaliações de segurança automatizadas, eles decidem usar o Amazon Inspector.

O Amazon Inspector ajuda a melhorar a segurança e a conformidade dos aplicativos executando avaliações de segurança automatizadas. Ele verifica os aplicativos quanto a vulnerabilidades de segurança e desvios das práticas recomendadas de segurança, como acesso aberto a instâncias do Amazon EC2 e instalações de versões de software vulneráveis.

Depois que o Amazon Inspector faz uma avaliação, ele fornece uma lista de descobertas de segurança. A lista prioriza por nível de gravidade, com uma descrição detalhada de cada problema de segurança e uma recomendação sobre como corrigi-lo. Contudo, a AWS não garante que seguir as recomendações feitas resolverá todos os possíveis problemas de segurança. Sob o modelo de responsabilidade compartilhada, os clientes são responsáveis pela segurança de ferramentas, aplicativos e processos executados nos serviços AWS.

#### Amazon GuardDuty

O Amazon GuardDuty é um serviço que fornece detecção inteligente de ameaças para sua infraestrutura e seus recursos AWS. Ele identifica ameaças monitorando continuamente a atividade da rede e o comportamento da conta no seu ambiente AWS.

Depois de habilitar o GuardDuty para sua conta AWS, ele começa a monitorar sua atividade de rede e conta. Você não precisa implantar ou gerenciar nenhum outro software de segurança. O GuardDuty analisa continuamente dados de várias fontes da AWS, incluindo logs de fluxo de VPC e logs de DNS.

Se ele detectar ameaças, você poderá revisar as descobertas detalhadas no AWS Management Console. As descobertas incluem etapas recomendadas para a correção. Você também pode configurar as funções do AWS Lambda para executar as etapas de correção automaticamente em resposta às descobertas de segurança do GuardDuty.

## Monitoramento e análise

Neste módulo, você aprenderá a:

- Resumir abordagens para monitorar seu ambiente AWS.
- Descrever os benefícios do Amazon CloudWatch.
- Descrever os benefícios do AWS CloudTrail.
- Descrever os benefícios do AWS Trusted Advisor.

### Amazon CLoudWatch

O Amazon CloudWatch é um serviço web que permite monitorar e gerenciar várias métricas e configurar ações de alarme de acordo com os dados dessas métricas.

O CloudWatch usa métricas para representar os pontos de dados para seus recursos. Os serviços AWS enviam as métricas ao CloudWatch. Em seguida, o CloudWatch usa essas métricas para criar automaticamente gráficos que mostram como o desempenho mudou ao longo do tempo.

#### Alarmes do CloudWatch

Com o CloudWatch, você pode criar alarmes que executam ações automaticamente se o valor da métrica ultrapassar ou for inferior a um limite predefinido.

Por exemplo, suponha que os desenvolvedores da sua empresa usem instâncias do Amazon EC2 para fins de desenvolvimento ou teste de aplicativos. Se os desenvolvedores ocasionalmente se esquecerem de interromper as instâncias, as instâncias continuarão a ser executadas e incorrerão em cobranças.

Nesse cenário, você pode criar um alarme do CloudWatch que interrompe automaticamente uma instância do Amazon EC2 quando a porcentagem de utilização da CPU permanecer abaixo de um determinado limite por um período específico. Ao configurar o alarme, você pode especificar se deseja receber uma notificação sempre que esse alarme for acionado.

#### Painel do CloudWatch

O recurso de painel do CloudWatch permite que você acesse todas as métricas de seus recursos em um único local. Por exemplo, você pode usar um painel do CloudWatch para monitorar a utilização da CPU de uma instância do Amazon EC2, o número total de solicitações feitas para um bucket do Amazon S3 e muito mais. Você pode até personalizar painéis separados para diferentes fins comerciais, aplicativos ou recursos.

### AWS CloudTrail

O AWS CloudTrail registra as chamadas de API realizadas na sua conta. As informações gravadas são identidade do chamador da API, hora da chamada da API, endereço IP de origem do chamador da API e muito mais. Você pode pensar no CloudTrail como uma “trilha” de migalhas de pão (ou um log de ações) que alguém deixou para trás.

Lembre-se de que você pode usar chamadas de API para provisionar, gerenciar e configurar seus recursos AWS. Com o CloudTrail, você pode visualizar um histórico completo de atividades do usuário e chamadas de API de seus aplicativos e recursos.

Normalmente, os eventos são atualizados no CloudTrail dentro de 15 minutos após uma chamada de API. Você pode filtrar eventos especificando a hora e a data em que uma chamada de API ocorreu, o usuário que solicitou a ação, o tipo de recurso envolvido na chamada de API e muito mais.

### AWS Trusted Advisor

O AWS Trusted Advisor é um serviço web que inspeciona seu ambiente AWS e faz recomendações em tempo real de acordo com as práticas recomendadas da AWS.

O Trusted Advisor compara suas descobertas com as práticas recomendadas da AWS em cinco categorias: otimização de custos, desempenho, segurança, tolerância a falhas e limites de serviço. Para as verificações em cada categoria, o Trusted Advisor oferece uma lista de ações recomendadas e recursos adicionais para saber mais sobre as práticas recomendadas da AWS.

As orientações feitas pelo AWS Trusted Advisor podem beneficiar sua empresa em todos os estágios da implantação. Por exemplo, você pode usar o AWS Trusted Advisor para ajudar enquanto cria novos fluxos de trabalho e desenvolve novos aplicativos. Ou você pode usá-lo enquanto faz melhorias contínuas em aplicativos e recursos existentes.

#### Painel do AWS Trusted Advisor

Ao acessar o painel do Trusted Advisor no AWS Management Console, você pode revisar verificações concluídas para otimização de custos, desempenho, segurança, tolerância a falhas e limites de serviço.

Para cada categoria:

- A marca de verificação verde indica o número de itens para os quais não foram detectados problemas.
- O triângulo laranja representa o número de investigações recomendadas.
- O círculo vermelho representa o número de ações recomendadas.

## Definição de preços e suporte

Objetivos de aprendizado

Neste módulo, você aprenderá a:

- Descrever os modelos de definição de preço e suporte AWS.
- Descrever o nível gratuito da AWS.
- Descrever os principais benefícios do AWS Organizations e da cobrança consolidada.
- Explicar os benefícios do AWS Budgets.
- Explicar os benefícios do AWS Cost Explorer.
- Explicar os principais benefícios da Calculadora de preços AWS.
- Distinguir entre os vários planos do AWS Support.
- Descrever os benefícios do AWS Marketplace.

### Nível Gratuito da AWS

Com o nível gratuito da AWS, você começa a usar determinados serviços sem ter que se preocupar em incorrer em custos durante o período especificado.

Três tipos de ofertas estão disponíveis:

- Sempre gratuito
- 12 meses gratuitos
- Versão de teste

Para cada oferta de nível gratuito, revise o detalhes sobre exatamente quais recursos estão incluídos.

#### Sempre gratuito

Essas ofertas não expiram e estão disponíveis para todos os clientes AWS.

Por exemplo, o AWS Lambda permite um milhão de solicitações gratuitas e até 3,2 milhões de segundos de tempo de computação por mês. O Amazon DynamoDB libera 25 GB de armazenamento gratuito por mês.

#### 12 meses gratuitos

Essas ofertas são gratuitas por 12 meses após sua data de inscrição inicial na AWS.

Quantidades específicas de armazenamento comum do Amazon S3, limites para horas mensais de tempo de computação do Amazon EC2 e quantidades de transferência de dados do Amazon CloudFront para fora são alguns exemplos.

#### Versão de teste

As versões de teste gratuitas de curto prazo começam na data em que você ativa determinado serviço. A duração de cada teste pode variar de acordo com o número de dias ou a quantidade de uso do serviço.

Por exemplo, o Amazon Inspector oferece uma versão gratuita de 90 dias. O Amazon Lightsail (um serviço que permite que você execute servidores virtuais privados) oferece 750 horas de uso gratuitas em um período de 30 dias.

### Conceitos de definição de preço da AWS

A AWS oferece diversos serviços de computação em nuvem com modelos de pagamento conforme o uso.

#### Pague somente pelo que usar

Para cada serviço, você paga exatamente a quantidade de recursos que realmente usa, sem exigir contratos de longo prazo ou licenciamento complexo.

#### Pague menos ao fazer reserva

Alguns serviços oferecem opções de reserva com desconto significativo em comparação com as definições de preços da instância sob demanda.

Por exemplo, suponha que sua empresa use instâncias do Amazon EC2 para uma carga de trabalho que precisa ser executada continuamente. Você pode optar por executar essa carga de trabalho no Amazon EC2 Instance Savings Plans, pois o plano permite uma economia de até 72% em relação à capacidade equivalente da instância sob demanda.

#### Pague menos com descontos baseados em volume, quando usar mais

Alguns serviços oferecem definição de preço em camadas, portanto, o custo por unidade é incrementalmente menor com o aumento do uso.
Por exemplo, quanto mais espaço de armazenamento do Amazon S3 você usar, menos pagará por GB.

#### Calculadora de preços da AWS

A calculadora de preços AWS permite explorar os serviços AWS e gerar uma estimativa de custo de seus casos de uso na AWS. Você pode organizar as suas estimativas da AWS por grupos que definir. Um grupo pode refletir como sua empresa está organizada, por exemplo, fornecer estimativas por centro de custo.
Depois de criar uma estimativa, você pode salvá-la e gerar um link para compartilhá-la com outras pessoas.

Suponha que sua empresa esteja interessada em usar o Amazon EC2. No entanto, você ainda não tem certeza de qual Região AWS ou tipo de instância seria o mais econômico para seu caso de uso. Na calculadora de preços AWS, você pode inserir detalhes como o tipo de sistema operacional necessário, requisitos de memória e requisitos de entrada/saída (E/S). Usando a calculadora de preços AWS, você pode revisar uma comparação estimada de diferentes tipos de instância do EC2 nas Regiões AWS.

### Painel de cobrança

Use o painel de gerenciamento de faturamento e custos da AWS para pagar sua fatura da AWS, monitorar seu uso e analisar e controlar seus custos.

- Compare o saldo atual do mês acumulado com o mês anterior e obtenha uma previsão do próximo mês com base no uso atual.
- Visualize os gastos do mês acumulado por serviço.
- Visualize o uso do nível gratuito por serviço.
- Acesse o Cost Explorer e crie orçamentos.
- Adquira e gerencie o Savings Plans.
- Publique relatórios de custos e uso da AWS.

### Faturamento consolidado

Em um módulo anterior, você aprendeu sobre o AWS Organizations, um serviço que permite gerenciar múltiplas contas AWS em um local central. O AWS Organizations também oferece a opção de cobrança consolidada.

O recurso de cobrança consolidada do AWS Organizations permite que você receba uma única fatura para todas as contas AWS de sua organização. Ao consolidar, você pode rastrear facilmente os custos combinados de todas as contas vinculadas em sua organização. O número máximo de contas permitido para uma organização é quatro, mas você pode entrar em contato com o AWS Support para aumentar sua cota, se necessário.

Na sua fatura mensal, você pode revisar os encargos discriminados incorridos por cada conta. Isso permite que você tenha maior transparência nas contas da sua organização, mantendo a conveniência de receber uma única fatura mensal.

Outro benefício da cobrança consolidada é a capacidade de compartilhar preços de desconto por volume, Savings Plans e instâncias reservadas nas contas da sua organização. Por exemplo, uma conta pode não ter uso mensal suficiente para se qualificar para preços com desconto. No entanto, quando várias contas são combinadas, o uso agregado pode resultar em um benefício que se aplica a todas as contas na organização.

### AWS Budgets

No AWS Budgets, você pode criar orçamentos para planejar o uso do serviço, os custos de serviço e as reservas de instâncias.

As informações do AWS Budgets são atualizadas três vezes por dia. Isso ajuda você a definir com precisão a proximidade entre seu uso e os valores orçados ou limites de nível gratuito da AWS.

No AWS Budgets, você também pode definir alertas personalizados para quando seu uso exceder (ou estiver prestes a exceder) o valor orçado.

### AWS Cost Explorer

O AWS Cost Explorer é uma ferramenta que permite visualizar, interpretar e gerenciar seus custos e uso da AWS ao longo do tempo.

O AWS Cost Explorer inclui um relatório básico dos custos e do uso dos cinco principais serviços da AWS de acúmulo de custos. Você pode aplicar filtros e grupos personalizados para analisar seus dados. Por exemplo, você pode exibir o uso de recursos no nível por hora.

### Planos do AWS Support

A AWS oferece quatro planos de suporte diferentes para ajudar você a solucionar problemas, reduzir custos e usar os serviços AWS de forma eficiente.

Você pode escolher entre os seguintes planos de suporte para atender às necessidades de sua empresa:

- Basic
- Developer
- Business
- Enterprise

#### Basic

O suporte Basic é gratuito para todos os clientes AWS. Inclui acesso a whitepapers, documentação e comunidades de suporte. Com o suporte Basic, você também pode entrar em contato com a AWS para tratar de questões de cobrança e aumento do limite de serviço

Com ele, você tem acesso a uma seleção limitada de verificações do AWS Trusted Advisor. Além disso, você pode usar o AWS Personal Health Dashboard, uma ferramenta com alertas e orientações de correção quando a AWS enfrenta eventos que podem afetar você.

Se a sua empresa precisar de suporte além do nível Basic, é possível adquirir os suportes Developer, Business ou Enterprise.

#### Suporte Developer, Business e Enterprise

Os planos de suporte Developer, Business e Enterprise têm todos os benefícios do suporte Basic, além de poder abrir um número irrestrito de casos de suporte técnico. Esses três planos de suporte têm pagamento mensal e não exigem contratos de longo prazo.

As informações deste curso destacam apenas uma alguns detalhes para cada plano de suporte. Uma visão geral completa do que faz parte de cada plano de suporte, incluindo a definição de preço de cada plano, está disponível no site do AWS Support.

Em geral, para definição de preço, o plano Developer tem o menor custo, o plano Business é intermediário e o plano Enterprise tem o custo mais alto.

Para saber mais, clique no símbolo + ao lado de cada categoria

#### Developer

Os clientes com um plano de suporte Developer têm acesso a recursos como:

- Orientação de práticas recomendadas
- Ferramentas de diagnóstico do lado do cliente
- Suporte à arquitetura de componentes fundamentais, que consiste em orientações sobre como usar as ofertas, recursos e serviços AWS combinados

Por exemplo, suponha que sua empresa esteja explorando os serviços AWS. Você já ouviu falar sobre alguns serviços diferentes da AWS. No entanto, você não tem certeza de como usá-los combinados para criar aplicativos que possam atender às necessidades de sua empresa. Nesse cenário, o suporte à arquitetura de componentes fundamentais incluído no plano de suporte Developer pode ajudar você a identificar oportunidades para combinar serviços e recursos específicos.

#### Business

Os clientes com um plano de suporte Business têm acesso a recursos adicionais, incluindo:

- Orientação de caso de uso para identificar ofertas, recursos e serviços AWS que podem atender melhor às suas necessidades específicas
- Todas as verificações do AWS Trusted Advisor
- Suporte limitado para software de terceiros, como sistemas operacionais comuns e componentes de pilha de aplicativos

Suponha que sua empresa tenha o plano de suporte Business e queira instalar um sistema operacional de terceiros comum em suas instâncias do Amazon EC2. Você pode entrar em contato com o AWS Support para obter assistência com a instalação, configuração e solução de problemas do sistema operacional. Para tópicos avançados, como otimizar o desempenho, usar scripts personalizados ou resolver problemas de segurança, pode ser necessário entrar em contato diretamente com o provedor de software de terceiros.

#### Enterprise

Além de todos os recursos incluídos nos planos de suporte Basic, Developer e Business, os clientes com um plano de suporte Enterprise têm acesso a recursos como:

- Orientação de arquitetura de aplicativos, que é um relacionamento consultivo para apoiar casos de uso e aplicativos específicos da sua empresa
- Gerenciamento de eventos de infraestrutura: engajamento de curto prazo com o AWS Support que ajuda sua empresa a compreender melhor seus casos de uso. Também fornece à sua empresa orientação de arquitetura e scaling.
- Um technical account manager

#### Technical Account Manager (TAM)

O plano de suporte Enterprise inclui acesso a um technical account manager (TAM).

Se a sua empresa tiver um plano de suporte Enterprise, o TAM será seu principal ponto de contato com a AWS. Ele oferece orientação, revisões de arquitetura e comunicação contínua com sua empresa enquanto você planeja, implanta e otimiza seus aplicativos.

Seu TAM oferece o conhecimento especializado em toda a gama de serviços AWS. Ele ajuda você a projetar soluções que usam vários serviços combinados de forma eficiente por uma abordagem integrada.

Por exemplo, suponha que você tenha interesse em desenvolver um aplicativo que use vários serviços AWS combinados. O TAM pode fornecer informações sobre como usar melhor os serviços em conjunto. Ele consegue isso ao mesmo tempo em que se alinha com as necessidades específicas que sua empresa espera atender com o novo aplicativo.

### AWS Marketplace

O AWS Marketplace é um catálogo digital com milhares de ofertas de fornecedores independentes de software. Você pode usar o AWS Marketplace para encontrar, testar e comprar software que pode ser executado na AWS.

Para cada oferta no AWS Marketplace, você pode acessar informações detalhadas sobre opções de definição de preço, suporte disponível e avaliações de outros clientes AWS.

Você também pode explorar soluções de software por setor e caso de uso. Por exemplo, suponha que sua empresa atue no setor de saúde. No AWS Marketplace, você pode analisar casos de uso que o software ajuda a resolver, como implementar soluções para proteger prontuários de pacientes, ou usar modelos de machine learning para analisar o histórico médico de um paciente e prever possíveis riscos para a saúde.

O AWS Marketplace oferece produtos em várias categorias, como produtos de infraestrutura, aplicativos de negócios, produtos de dados e DevOps.

Em cada categoria, você pode restringir sua pesquisa navegando pelas ofertas de produtos em subcategorias. Por exemplo, as subcategorias na categoria DevOps incluem áreas como Desenvolvimento de aplicativos, Monitoramento e Teste.

## Migração e inovação

Neste módulo, você aprenderá a:

- Compreender a migração e a inovação na nuvem AWS.
- Resumir o AWS Cloud Adoption Framework (AWS CAF).
- Resumir os seis principais fatores de uma estratégia de migração para a nuvem.
- Descrever os benefícios das soluções de migração de dados da AWS, como o AWS Snowcone, o AWS Snowball e o AWS Snowmobile.
- Resumir o amplo escopo de soluções inovadoras que a AWS oferece.

### AWS Cloud Adoption Framework (AWS CAF)

No nível mais alto, o AWS Cloud Adoption Framework (AWS CAF) organiza orientações em seis áreas de foco chamadas perspectivas. Cada perspectiva aborda responsabilidades distintas. O processo de planejamento ajuda as pessoas certas em toda a organização a se prepararem para as mudanças futuras.

Em geral, as perspectivas de negócio, pessoas e governança se concentram nas capacidades comerciais, enquanto as perspectivas de plataforma, segurança e operações se concentram em capacidades técnicas.

#### Perspectiva de negócio

A perspectiva de negócio garante que a TI esteja alinhada às necessidades de negócio e que os investimentos em TI estejam vinculados aos principais resultados dos negócios.

Use a perspectiva de negócio para criar um caso de negócio sólido para adoção da nuvem e priorizar as iniciativas de adoção da nuvem. Garanta que suas estratégias e metas de negócios estejam alinhadas com suas estratégias e metas de TI.

As funções comuns a perspectiva de negócio são:

- Gerentes de negócios
- Gerentes financeiros
- Proprietários de orçamento
- Stakeholders de estratégia

#### Perspectiva de pessoas

A perspectiva de pessoas promove o desenvolvimento de uma estratégia de gerenciamento de alterações em toda a organização para a adoção bem-sucedida da nuvem.

Use a perspectiva de pessoas para avaliar estruturas e funções organizacionais, novos requisitos de habilidades e processos e identificar lacunas. Isso ajuda a priorizar treinamento, pessoal e mudanças organizacionais.

As funções comuns da perspectiva de pessoas são:

- Recursos humanos
- Equipe
- Gerentes de pessoas

#### Perspectiva de governança

A perspectiva de governança concentra-se nas habilidades e nos processos para alinhar as estratégias de TI e de negócios. Isso garante que você maximize o valor comercial e minimize os riscos.

Use a perspectiva de governança para entender como atualizar as habilidades e os processos da equipe necessários para garantir a governança de negócios na nuvem. Gerencie e mensure os investimentos em nuvem para avaliar os resultados de negócios.

As funções comuns na perspectiva de governança são:

- Diretor de informações (CIO)
- Gerentes do programa
- Arquitetos empresariais
- Analistas de negócios
- Gerentes de portfólio

#### Perspectiva de plataforma

A perspectiva de plataforma inclui princípios e padrões para implementação de novas soluções na nuvem e migração de cargas de trabalho locais para a nuvem.

Use uma variedade de modelos arquitetônicos para entender e comunicar a estrutura dos sistemas de TI e suas relações. Descreva a arquitetura do ambiente de destino em detalhes.

As funções comuns da perspectiva de plataforma são:

- Diretor de tecnologia (CTO)
- Gerentes de TI
- Arquitetos de soluções

#### Perspectiva de segurança

A perspectiva de segurança garante que a organização atenda aos objetivos de segurança de visibilidade, auditoria, controle e agilidade.

Use o AWS CAF para estruturar a seleção e a implementação de controles de segurança que atendam às necessidades da organização.

As funções comuns da perspectiva de segurança são:

Diretor de segurança da informação (CISO)
Gerentes de segurança de TI
Analistas de segurança de TI

#### Perspectiva de operações

A perspectiva de operações ajuda você a habilitar, executar, usar, operar e recuperar cargas de trabalho de TI para o nível definido com os stakeholders da empresa.

Defina como os negócios diários, trimestrais e anuais são conduzidos. Alinhe e dê suporte às operações do negócio. O AWS CAF ajuda os stakeholders a definir os procedimentos operacionais atuais e identificar mudanças de processo e treinamento necessários para implementar a nuvem com sucesso.

As funções comuns da perspectiva de operações são:

- Gerentes de operações de TI
- Gerentes de suporte de TI

### Estratégia de migração para a nuvem

Ao migrar aplicativos para a nuvem, seis das estratégias de migração mais comuns que você pode implementar são:

- Redefinição de hospedagem
- Redefinição de plataforma
- Refatoração/rearquitetura
- Recompra
- Retenção
- Inativação

#### Redefinição de hospedagem

Redefinir hospedagem, também conhecida como “lift-and-shift”, envolve a movimentação de aplicativos sem alterações.

No cenário de uma grande migração legada, em que a empresa busca implementar sua migração e dimensionar rapidamente para atender a um caso de negócio, a hospedagem da maioria dos aplicativos é redefinida.

#### Redefinição de plataforma

Realocação de plataforma, também conhecida como “lift, tinker and shift”, envolve fazer algumas otimizações na nuvem para obter um benefício tangível. A otimização é alcançada sem alterar a arquitetura central do aplicativo.

#### Refatoração/rearquitetura

Refatoração (também conhecida como rearquitetura) envolve reimaginar como um aplicativo é arquitetado e desenvolvido usando recursos nativos da nuvem. A refatoração costuma ser orientada pela forte necessidade que a empresa tem de adicionar recursos, scaling ou desempenho que, de outra forma, seriam difíceis de obter no ambiente atual do palicativo.

#### Recompra

Recompra envolve a mudança de uma licença tradicional para um modelo de software como serviço.

Por exemplo, uma empresa pode optar por implementar a estratégia de recompra migrando de um sistema de gerenciamento de relacionamento com o cliente (CRM) para o Salesforce.com.

#### Retenção

Retenção consiste em manter os aplicativos essenciais para a empresa no ambiente de origem. Isso pode incluir aplicativos que exigem refatoração importante antes de serem migrados ou trabalhos que podem ser adiados.

#### Inativação

Inativação é o processo de remoção de aplicativos que não são mais necessários.

### AWS Snow Family

O AWS Snow Family é uma coleção de dispositivos físicos que ajudam a migrar dados para a AWS de maneira rápida, fácil e segura. Os dispositivos Snow são enviados para você e podem ser usados para transferir dados para a AWS diretamente de seu datacenter. Os dispositivos Snow são robustos, seguros e projetados para operar em ambientes com condições adversas, incluindo locais com poeira, umidade e variações de temperatura.

Esses dispositivos oferecem diferentes pontos de capacidade e a maioria inclui recursos de computação integrados. A AWS é a proprietária e responsável pelo gerenciamento da Snow Family, que integra recursos de segurança, monitoramento, gerenciamento de armazenamento e computação da AWS.  

#### AWS Snowcone

O AWS Snowcone é um dispositivo pequeno, robusto e seguro para transferência de dados e computação de borda.

Ele tem 2 CPUs, 4 GB de memória e 8 TB de armazenamento utilizável.

#### AWS Snowball

O AWS Snowball oferece dois tipos de dispositivos: os dispositivos

- Snowball Edge otimizados para armazenamento são ideais para migrações de dados de grande escala e fluxos de trabalho de transferência recorrentes, em além da computação local com necessidades maiores de capacidade.
  - Armazenamento: 80 TB de capacidade de disco rígido (HDD) para volumes de blocos e armazenamento de objeto compatível com o Amazon S3, além de unidade de estado sólido (SSD) de 1 TB para volumes de blocos.
  - Computação: 40 vCPUs e 80 GiB de memória para dar suporte a instâncias sbe1 do Amazon EC2 (equivalente a C5).
- O Snowball Edge otimizado para computação fornece recursos de computação poderosos para casos de uso, como machine learning, análise de vídeo em movimento completo, análise e pilhas de computação locais.
  - Armazenamento: capacidade de HDD utilizável de 42 TB para armazenamento de objeto compatível com o Amazon S3 ou volumes de blocos compatíveis com o Amazon EBS e também 7,68 TB de capacidade de SSD NVMe utilizável para volumes de blocos compatíveis com o Amazon EBS.
  - Computação: 52 vCPUs, 208 GiB de memória e uma GPU NVIDIA Tesla V100 opcional. Os dispositivos executam as instâncias sbe-c e sbe-g do Amazon EC2, que são equivalentes às instâncias C5, M5a, G3 e P3.

#### AWS Snowmobile

O AWS Snowmobile é um serviço de transferência dados na escala de exabytes usado para mover grandes quantidades de dados para a nuvem AWS.

Você pode transferir até 100 petabytes por Snowmobile, um contêiner de transporte reforçado com 13,71 metros de comprimento puxado por um caminhão semirreboque.

### Inovação com a AWS

Ao examinar como usar os serviços da AWS, é importante focar nos resultados desejados. Você fica devidamente preparado para impulsionar a inovação na nuvem se conseguir articular claramente as seguintes condições:

- O estado atual
- O estado desejado
- Os problemas que você está tentando resolver

Considerar alguns dos caminhos que poderá explorar no futuro, enquanto continuar em sua jornada para a nuvem.

#### Aplicativos sem servidor

Com a AWS, sem servidor significa que você não precisa administrar, fazer manutenção ou administrar servidores de aplicativos. Você não precisa se preocupar com tolerância a falhas ou disponibilidade. A AWS lida com esses recursos para você.

O AWS Lambda é um exemplo de um serviço que você pode usar para executar aplicativos sem servidor. Se projetar sua arquitetura para acionar funções do Lambda para executar seu código, você poderá ignorar a necessidade de gerenciar uma frota de servidores.

Criar sua arquitetura com aplicativos sem servidor permite que seus desenvolvedores se concentrem no produto principal em vez de gerenciar e operar servidores.

#### Inteligencia Artificial

A AWS oferece uma variedade de serviços com tecnologia de inteligência artificial (IA).

Por exemplo, você pode executar as seguintes tarefas:

- Converter fala em texto com o Amazon Transcribe.
- Descobrir padrões em texto com o Amazon Comprehend.
- Identificar atividades on-line potencialmente fraudulentas com o Amazon Fraud Detector.
- Criar chatbots de voz e texto com o Amazon Lex.

#### Machine Learning

O desenvolvimento tradicional de machine learning (ML) é complexo, caro, demorado e propenso a erros. A AWS oferece o Amazon SageMaker, que remove o trabalho difícil do processo e ajuda você a criar, treinar e implantar modelos de ML rapidamente.

Você pode usar ML para analisar dados, resolver problemas complexos e prever resultados antes que eles aconteçam.
