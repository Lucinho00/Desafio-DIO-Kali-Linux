# Desafio-DIO-Kali-Linux

1. Preparando o Kali Linux
Antes de iniciar, certifique-se de que o Kali Linux esteja instalado em sua máquina. Caso ainda não tenha, você pode baixar e instalar o Kali Linux a partir do site oficial. O Kali Linux é uma distribuição focada em segurança e pentesting, já vem com o SET instalado.

2. Obter acesso root
Abra o terminal do Kali Linux.
Digite o comando para obter permissões de root (superusuário) e pressione Enter
sudo su
Você será solicitado a digitar a senha do usuário. Faça isso e pressione Enter.

3. Iniciar o Social-Engineer Toolkit (SET)
Com o terminal aberto e em modo root, digite o comando para iniciar o SET:
setoolkit
E pressione Enter.
O SET vai carregar e mostrar um menu interativo com várias opções. Você verá algo como isso:

Welcome to the Social-Engineer Toolkit (SET)!
Please select from the following menu:

1) Social-Engineering Attacks
2) Penetration Testing (exploits)
3) Third Party Modules
4) Update the Social-Engineer Toolkit
5) Exit


4. Escolher o tipo de ataque - Social-Engineering Attacks
Digite 1 e pressione Enter para selecionar Social-Engineering Attacks.

1) Social-Engineering Attacks
2) Penetration Testing (exploits)
3) Third Party Modules
4) Update the Social-Engineer Toolkit
5) Exit

5. Escolher o vetor de ataque - Website Attack Vectors
Agora, você verá um novo menu com várias opções. Digite 2 e pressione Enter para escolher Website Attack Vectors:

1) Spear-Phishing Attack Vectors
2) Website Attack Vectors
3) Infectious Media Generator
4) Create a Payload and Listener
5) Mass Mailer Attack


6. Escolher o método de ataque - Credential Harvester
Em seguida, você verá uma nova lista. Digite 3 e pressione Enter para escolher o Credential Harvester Attack Method.

1) Credential Harvester Attack Method
2) Web Jacking Attack Method
3) Tabnabbing Attack Method
4) Multi-Attack Web Method
5) Return to main menu


7. Escolher o método - Site Cloner
Agora, selecione a opção 2 para Site Cloner. O Site Cloner vai criar uma cópia do site de sua escolha e capturar as credenciais inseridas pelos usuários na página falsa.

1) Site Cloner
2) Custom HTML Page
3) Return to main menu


8. Obter o endereço IP da sua máquina (máquina atacante)
Para garantir que os visitantes acessem o seu servidor local, você precisa saber o endereço IP da sua máquina.

Abra o terminal e digite o comando abaixo para descobrir seu IP local:

ifconfig

Na saída, procure pela interface de rede conectada, como eth0 (para conexões com fio) ou wlan0 (para conexões sem fio). O endereço IP será algo como 192.168.x.x.

Inserir o URL para clonar (Facebook)
Agora, o SET vai pedir para você inserir o URL do site que deseja clonar. Como exemplo, insira o URL do Facebook:

http://www.facebook.com

Pressione Enter.

10. Definir o IP e iniciar o servidor
O SET vai pedir para você inserir o IP da máquina para servir a página clonada. Coloque o endereço IP da sua máquina que você obteve com o comando ifconfig.

O SET vai configurar o servidor web e exibir uma mensagem como:

Starting the credential harvester at IP: 192.168.x.x

Isso significa que o servidor foi configurado e o site clonado está disponível em seu IP local.

A página de phishing (Facebook clonado)
Agora, quando você acessar o IP da sua máquina em um navegador, ele exibirá a página clonada do Facebook. Se um usuário acessar esse link e inserir suas credenciais (nome de usuário e senha), os dados serão capturados pelo SET.

Visualizar as credenciais capturadas
O SET irá capturar e exibir as credenciais inseridas na página clonada. Você pode visualizar as informações acessando o terminal onde o SET foi executado.

As credenciais capturadas serão exibidas em tempo real, com informações como usuário e senha.

Esse procedimento só deve ser realizado em um ambiente controlado e com permissão explícita, como mencionado anteriormente. Realizar phishing em ambientes reais sem autorização é ilegal e antiético. Use este conhecimento para aprender e proteger sistemas, não para causar danos.
