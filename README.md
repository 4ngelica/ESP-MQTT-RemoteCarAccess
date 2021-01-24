 <h3 align="center">REMOTE CAR ACCESS</h3>

  <p align="center">
   :man_technologist: :wrench: EM CONSTRUÇÃO :wrench: :woman_technologist: 
  </p>


<p align="center">
  <img  src="">
</p>

 <p align="center">
    <a href="#RemoteCarAccess_about">Sobre</a> • 
    <a href="#RemoteCarAccess_techs">Componentes</a> • 
    <a href="#RemoteCarAccess_install">Instalação</a> • 
    <a href="#RemoteCarAccess_ref">Referências</a> •
    <a href="#RemoteCarAccess_group">Integrantes do grupo</a> •
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
 Projeto mecânico:
<ul>
    <li>2 chassis</li>
    <li>4 rodas de Borracha</li> 
    <li>2 rodas auxiliares </li> 
    <li>4 discos de Encoder </li> 
    <li>2 suportes para 4 Pilhas</li>
    <li>2 jogos de parafusos e espaçadores para roda auxiliar</li>
</ul> 
 Projeto eletro-eletrônico:
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

## :pushpin: Instalação
<p id="RemoteCarAccess_install">

• Para utilizar as funcionalidades dessa interface é necessário baixar os arquivos ou clonar esse repositório:

`git clone https://github.com/4ngelica/INTERFACE-RemoteCarAccess.git `

• Certifique-se de que os arquivos permaneçam dentro da mesma pasta.

• Abra o arquivo <b>index.html</b> em qualquer editor para alterar as propriedades <i>value="mqttInterfaceEnvia"</i> e <i>value="mqttNodeMCURecebe"</i> <b>(Esse passo é MUITO IMPORTANTE. Caso não altere essas propriedades, a chance de acessar a nodeMCU de outra pessoa é grande).</b>

Se você deseja reproduzir o projeto completo, acesse a seção de instalação do repositório <a href="https://github.com/4ngelica/ESP-MQTT-RemoteCarAccess">ESP-MQTT-RemoteCarAccess</a>, que fornece detalhadamente os componentes necessários, desenhos esquemáticos, projetos mecânicos, eletrônicos, bibliotecas necessárias e demais arquivos.</p>

## :pushpin: Referências
<p id="RemoteCarAccess_ref">
 • Artigo: <a href="https://www.filipeflop.com/blog/controle-monitoramento-iot-nodemcu-e-mqtt/ ">Controle e Monitoramento IoT com NodeMCU e MQTT</a> 
 • Repositório: <a href="https://github.com/filipeflop/Interface-Web-MQTT">Interface-Web-MQTT</a>

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
