<h1>Monitorando Criptomoedas</h1>

  <p> Foi usada a API do MercadoBitcoin para monitorar os Criptoativos, toda documentação referente a API:  https://www.mercadobitcoin.com.br/api-doc/ </p>

  <h2>CriptoMoeadas Selecionadas</h2>
    
   <div style="display: inline;">
    <ul>
    <li> Bitcoin </li>
    <li> Ethereum</li>
    <li> PaxGold</li>
    <li> USD Coin</li>
    <li> XRP</li>
    <li> Cardano</li>
    <li> DogeCoin</li>
    <li> Solana</li>  
    <li> LiteCoin</li>
    <li> ShibaInu</li>
    <li> Polkadot</li>
    <li> FileCoin</li>
    <li> Cosmos</li>
    <li> Internet Computer</li>
    <li> Avalanche </li>
    <li> Algorand </li>
    <li> Tezos</li>
    <li> WrappedLuna</li>
    <li> Stellar</li>
    <li> Coti</li>
    <li> Mina</li>
    <li> Stacks</li>  
    <li> Oasis Network</li>
    <li> Axie Infinity</li>
    <li> Polygon</li>
    <li> FileCoin</li>
    <li> Cosmos</li>
    <li> Internet Computer</li>
    
  <h2>Método De Requisição</h2>
    <p> A API tem vários metodos de requisição, para esse projeto usei o método Ticker, exemplo: <br>

            https://www.mercadobitcoin.net/api/<coin>/<method>/

   <ul>
   <li>
        coin = Símbolo da Criptomoeda
   </li>
   <li>
          method = Método de Requisição    
   </li>
   </ul>
                  
   </p>

   <h2>Fazendo um Requisição</h2>

   <p>
    Usando seu terminal de preferência vamos fazer uma requisição de exemplo: <br>

          https://www.mercadobitcoin.net/api/BTC/ticker/

   <h2>Resposta</h2>
      <p>As respostas são retornadas no formato JSON da seguinte forma: <br><br>
         <img src="https://user-images.githubusercontent.com/98768795/183086821-f442cc29-7f1a-4c92-96c4-4ad2e87b1086.png"> </img> <br>

   <ul >
   Dentro do Método Ticker temos os seguintes parâmetros: <br><br>
   <li>High  = Maior Preço do Dia </li>
   <li>Low   = Menor Preço do Dia</li>
   <li>Vol   = Volume de Negociações</li>
   <li>Last  = Ultimo Preço Registrado | valor atual da Criptomoeda</li>
   <li>Buy   = Maior preço de oferta de compra das últimas 24 horas.</li>
   <li>Sell  = Menor preço de oferta de venda das últimas 24 horas.</li>
   <li>Date  = Data e hora da informação</li>
   <li>Open  = Valor de Abertura</li>
   <br>
    Todos os valores são retornados em forma de números decimais exceto o Date que retorna um número inteiro 
   </ul>
   </p>
   </p>

  <h2>No Zabbix<h2>
    <p>No zabbix para cada criptomoeda foram criados 5 itens: <br><br>
      <img src="https://user-images.githubusercontent.com/98768795/183090000-802db082-038d-4f8e-b40c-c7bf83a0f3f1.png"> </img>

   <ul>
    <li>Algorand      = Me traz o valor atual da criptomoeda</li>
    <li>Algorand Max  = Traz o maior valor da Criptomoeda no dia</li>
    <li>Algoand Min   = Traz o menor valor da Criptomoeda no dia</li>
    <li>Algorand open = Traz o valor de abertura da Criptomoeda</li>
    <li>Algorand vol  = Traz o volume de negociações da Criptomoeda</li>
   </ul>
   </p>

   <h2>Exemplo de Dados Coletados: </h2>
   <p>A coleta é atualizada a cada minuto</p> 
    <img src="https://user-images.githubusercontent.com/98768795/183091306-841040c3-a333-4764-97b5-8383c89c8ddb.png"> </img>

  <h2>Configurações do Item e Pré-Processamento</h2>
    <img src="https://user-images.githubusercontent.com/98768795/183092337-6baefa1f-c70a-4fac-ba00-b64757f9d131.png"> </img>
    <img src="https://user-images.githubusercontent.com/98768795/183092393-e494d140-7062-4162-9029-9c5ce4baaa54.png"> </img>

   <p>OBS: Cada Item usará um Parâmetro diferente para o pré-processamento, escolha a chave de acordo com a informação desejada, o template está disponível para download.</p>
   </div> 

   
 

  




