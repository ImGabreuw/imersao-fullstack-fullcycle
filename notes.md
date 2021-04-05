# Imersão Full Stack && Full Cycle 2.0

### Desenvolvedor FullStack VS Desenvolvedor FullCycle

* Desenvolvedor FullStack = domina as linguagens para programar back-end / front-end
* Desenvolvedor FullCycle = programar + arquitetura + entregar aplicação testada + deploada + monitorada

### WebSocket

* Uma forma de você fazer uma conexão TCP entre o browser e o servidor (**conexão persistente**)
* Requisições no mesmo canal

---

## Apache Kafka

### O que é?
* **event-driven** (eventos)
  * Exemplos: carros, E-commerce, alarmes, monitoramento, microsserviços
* Tempo real (**pouca latência**)
* Histórico dos dados

### Características
* Plataforma
* Trabalha de forma distribuída  
* Bancos de dados - onde armazena os dados do histórico
* Extremamente rápido e com baixa latência
* Utiliza o disco ao invés de memória para processar os dados

### **OBS**: **NÃO** é apenas um sistema tradicional de filas como **RabbitMQ**

### Conceitos básicos

* O que é um "Topic"?

  * Stream de dados que atual como um banco de dados
  * Todos os dados ficam armazenados, ou seja, cada **Topic** tem seu "local" para armazenar seus dados
  * **Topic** possui várias partições (**distribuição dos dados nessas partições**)
    * Cada partição é definido por números. Ex: 0, 1, 2, etc
    * Você é obrigado a definir a quantidade de partições quando for criar um **Topic**   

* O que é um Kafka Cluster

  * Conjunto de **Brokers**
  * Cada **Broker** é um servidor
  * Cada **Broker** é resposnsável por armazenar os dados de uma partição
  * Cada partição de um **Topic** está distruibuído em diferentes **Brokers**
  
  <br>
  
  * **Representação**
    ![kafka-cluster](https://github.com/ImGabreuw/imersao-fullstack-fullcycle/blob/master/.github/kafka_cluster.PNG)
  
* O que é um Kafka Cluster: Replication Factor
  * Apache ZooKeeper - serviço para gerenciar as máquinas com base na "saúde" dela,

  * **Representação**
    ![kafka-cluster-replication-factor](https://github.com/ImGabreuw/imersao-fullstack-fullcycle/blob/master/.github/kafka_cluster_replication_factor.PNG)

* Ecossistema
  * Kafka Connect (**Connectors**)
  * Confluent Schema Registry
  * Rest Proxy
  * ksqlDB
  * Kafka Streams (Baixo nível)
