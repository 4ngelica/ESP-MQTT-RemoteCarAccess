<p align="center">
  <img  src="https://user-images.githubusercontent.com/47900225/105637590-1a336280-5e4d-11eb-897f-cde0fb915437.png">
</p>

 <p align="center">
    <a href="#RemoteCarAccess_about">Sobre</a> • 
    <a href="#RemoteCarAccess_techs">Componentes</a> • 
    <a href="#RemoteCarAccess_draw">Desenhos esquemáticos</a> •
    <a href="#RemoteCarAccess_install">Instalação</a> • 
    <a href="#RemoteCarAccess_install">Demonstração</a> • 
    <a href="#RemoteCarAccess_ref">Referências</a> •
    <a href="#RemoteCarAccess_group">Integrantes do grupo</a>
    <h3 align="center">REMOTE CAR ACCESS</h3>

  <p align="center">
    Projeto de teleoperação robótica para controlar dois carros via Wifi a partir de qualquer localização do mundo.  
  </p>


## :pushpin: Sobre
<p align="justify" id="RemoteCarAccess_about">
   O projeto Remote Car Access é um sistema teleoperação robótica para controlar dois protótipos carros utilizando o protocolo MQTT e o módulo ESP8266. Esse projeto foi desenvolvido em grupo como requisito avaliativo da disciplina Projetos de Sistemas Mecatrônicos II da Escola de Engenharia de São Carlos - USP. O funcionamento do projeto é baseado em duas operações: um carro é o mestre e o outro é um replicador. O carro mestre se diferencia estruturalmente do replicador por possuir um sensor de proximidade ultrassônico. 
   Quando o carro mestre se movimenta, o carro replicador copia seus movimentos. Quando a distância até um obstáculo medida pelo sensor é menor do que 40 centímetros, o movimento do carro mestre é interrompido, e consequentemente, o carro replicador também pára. Ainda, o carro replicador pode se movimentar independentemente. 
</p>

## :pushpin: Componentes
<div id="RemoteCarAccess_techs">
 <p>Projeto mecânico:</p>
<ul>
    <li>2 chassis</li>
    <li>4 rodas de Borracha</li> 
    <li>2 rodas auxiliares </li> 
    <li>4 discos de Encoder </li> 
    <li>2 suportes para 4 Pilhas</li>
    <li>2 jogos de parafusos e espaçadores para roda auxiliar</li>
</ul> 
 <p>Projeto eletro-eletrônico:</p>
<ul>
    <li>4 motores DC (3~6v)</li>
    <li>2 chaves On/Off</li> 
    <li>1 sensor ultrassônico HC-SR04</li>
    <li>NodeMCU V3 - ESP8266</li>
    <li>Módulo Driver Ponte H - L298N</li>
    <li>Jumpers</li>
    <li>Protoboard 170 Pontos</li>
    <li>Powerbank ou Bateria 9V</li>
    <li>4 pilhas AA</li>
    <li>Jumpers</li>
</ul> 
</div>

## :pushpin: Desenhos esquemáticos
<p id="RemoteCarAccess_draw">Acesse os desenhos esquemáticos dos projetos eletro-eletrônico e mecânico na pasta <a href="https://github.com/4ngelica/ESP-MQTT-RemoteCarAccess/tree/master/Desenhos">Desenhos</a>.</p>
<p align="center">
  <img  src="https://user-images.githubusercontent.com/47900225/105635815-cbcd9600-5e43-11eb-9c04-d065868fb206.png">
</p>


## :pushpin: Instalação
<p id="RemoteCarAccess_install">

• Baixe os arquivos ou faça o clone desse repositório:

`git clone https://github.com/4ngelica/ESP-MQTT-RemoteCarAccess.git `

•  Essa pasta contém os arquivos dos scripts da Arduino IDE que devem ser carregados em cada uma das placas nodeMCU (<b>sketch-red-joycon.ino</b> e <b>sketch-blue-joycon.ino</b>, dos carros replicador e mestre, respectivamente). Além disso, para que o projeto funcione você deve baixar e instalar as bibliotecas <b>ESP8266WiFi</b> e <b>PubSubClient</b>, que também estão contidas nesse repositório.

• Depois de instalar as bibliotecas, abra os arquivos <b>sketch-red-joycon.ino</b> e <b>sketch-blue-joycon.ino</b> na IDE Arduino e altere as propriedades <i>#define ID_MQTT  "IdCarroReplicador"</i> e <i>#define ID_MQTT  "IdCarroMestre"</i> <b>(Esse passo é MUITO IMPORTANTE. Cada uma das IDs deve ser diferente e única, caso contrário, quando um carro se conectar ao servidor, o outro será desconectado).</b>

• Ainda no editor, altere as propriedades <i>SSID = "suaRedeWifi"</i> e <i>PASSWORD = "suaSenha"</i> para cada um dos carros, utilizando a rede wifi do local onde cada um dos carros vai ficar. <b>(Aqui você está definindo em qual rede wifi o nodeMCU deve se conectar, para então tentar a conexão com o servidor).</b>

• Carregue os sketches em cada um dos carros. Você pode verificar se a conexão ocorreu com sucesso abrindo a <b>porta serial 115200</b>.

• Nesse ponto, a configuração dos carros está finalizada. Para acessar a interface de controle, siga as instruções do repositório <a href="https://www.github.com/4ngelica/INTERFACE-RemoteCarAccess ">INTERFACE-RemoteCarAccess</a>.

• Se você já tem acesso a interface e a conectou com o servidor, já está pronto para enviar comandos aos carros. Os botões do Joycon Azul controlam o carro mestre e os botões do Joycon vermelho controlam o carro replicador.

## :pushpin: Demonstração
<p id="RemoteCarAccess_demo">Acesse o vídeo demonstrativo do projeto <a href="https://youtu.be/VFwJNbv6L60">aqui</a>.  </p>


## :pushpin: Referências
<p id="RemoteCarAccess_ref">
 • Artigo: <a href="https://www.filipeflop.com/blog/controle-monitoramento-iot-nodemcu-e-mqtt/">Controle e Monitoramento IoT com NodeMCU e MQTT</a> 
 • Repositório: <a href="https://github.com/filipeflop/Interface-Web-MQTT">Interface-Web-MQTT</a>.
</p>

## :pushpin: Integrantes do grupo
<ul id="RemoteCarAccess_group">
    <li>Alex José Arantes</li>
    <li>Alexsander dos Santos Sena</li>
    <li>Angélica Batassim Nunes</li> 
    <li>Ariel Alejandro Arce Maciel</li>
    <li>Bruno Moneda Alberto dos Santos</li>
    <li>Mayara Vivian dos Prazeres Cruz</li> 
    <li>Thais Mafra Navarro</li> 
</ul>  

<footer>
    <hr></hr>
<p align="center">
Made with :heart: by Angélica Batassim
</p>
</footer> 
