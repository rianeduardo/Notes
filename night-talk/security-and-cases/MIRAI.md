#Night Talk 60 — Botnets: O fantasma da Mirai e o exército de torradeiras

26 de maio de 2026

Fala galera, chegamos no talk 60, né.

Pra fechar essa sequência que a gente começou com Engenharia Reversa, passou por OSINT e Shodan, hoje a gente vai falar do "Big Boss" das consequências de deixar dispositivo mal configurado na rede

**Botnets e a icônica Mirai**

Se você acha que seu roteador de casa ou sua lâmpada inteligente são inofensivos

Hoje tu vai descobrir que eles podem ser usados pra derrubar países inteiros se caírem nas mãos certas (ou erradas, né)

---

## O que é uma Botnet real oficial

Se eu não me engano já falei um pouco aqui, mas bora lá

Imagina um exército de zumbis, mas em vez de bom, zumbis, são dispositivos eletrônicos

Uma botnet é basicamente uma rede de computadores (ou qualquer coisa com IP) que foi infectada por um malware e agora obedece a um único mestre: o Botmaster

OUUU o famoso C2 (Command & Control)

---

O bizarro é que o dono do dispositivo não faz a menor ideia de que a torradeira dele tá, nesse exato momento, ajudando a derrubar o site de um banco na Europa

Pro usuário, o Wi-Fi só tá "um pouco lento hoje", né kkkk

Provavelmente algo da tua casa mesmo já serviu de botnet

Ou ainda serve, até hoje...

---

## A lenda da Mirai: Como tudo começou

Curiosidade foda: Esse nome, pra quem manja de japonês vêm de futuro né

Eu mesmo achei que o nome era pra ser isso saca, futuro, pq revolucionou e tudo mais

Mas não, o nome vem de um fucking anime, chamado Mirai Nikki, uns nerdão fizeram esse malware aí

Enfim...

---

A Mirai não foi só "mais um malware". Ela mudou as regras do jogo em 2016

E sabe o que é o mais irônico?

**Ela não foi criada por um grupo de espionagem estatal ou por hackers russos de elite** 

Foi criada por uns moleques que queriam ganhar vantagem em servidores de Minecraft, derrubando a conexão dos rivais com ataques de DDoS, ou seja, mais nerdão ainda

Só que o código era tão eficiente que a parada saiu do controle e virou um monstro que quase quebrou a espinha da internet

---

## Como a Mirai se espalhava (O link com o Shodan)

Lembra que no talk passado a gente falou que o Shodan acha tudo que tem senha padrão?

Pois é, a Mirai era tipo um Shodan automatizado e malicioso.

---

_O código dela funcionava assim:_

Ela escaneava a internet inteira atrás de dispositivos IoT (câmeras, roteadores, DVRs) que tivessem a porta Telnet (23) aberta

Quando achava, ela tentava um ataque de força bruta, mas não era um ataque qualquer.

Ela tinha uma lista interna de apenas 64 combinações de usuário e senha padrão (tipo admin/admin, root/12345, guest/12345).

Parece pouco, né? Mas como o mundo é preguiçoso e ninguém troca a senha dessas paradas, ela conseguiu infectar centenas de milhares de dispositivos em tempo recorde.

Uma vez infectado, o dispositivo virava um sordadinho pronto pra obedecer ordens do C2

---

## O ataque que parou o mundo

Em outubro de 2016, a Mirai mostrou do que era capaz

Ela focou o poder de fogo dela na Dyn, que é um provedor de DNS gigante.

Se tu derruba o DNS, você derruba a tradução de nomes da internet

É como se você apagasse todas as placas de sinalização de uma rodovia.

---

Resultado?

- Twitter (atual X) caiu.

- Spotify caiu.

- Netflix caiu.

- Reddit caiu.

- GitHub caiu.

Metade da internet dos EUA e da Europa ficou no escuro por horas

Tudo por causa de câmeras de segurança chinesas e roteadores domésticos com a senha admin kkkkk

O poder de processamento de uma câmera é lixo, mas o poder de 500 mil câmeras juntas é uma bomba atômica digital

---

## Por que a Mirai ainda é um problema hoje?

>"Ah Rian, mas isso foi em 2016, já corrigiram né?"

Aí que tu se engana colega

---

Os criadores da Mirai, quando sentiram o cerco da polícia fechar, fizeram a parada mais caótica possível: liberaram o código-fonte no fórum HackFonts

SIM. Mirai é fucking open-source

Isso significa que qualquer skid ou curioso hoje em dia pode baixar o código, modificar, adicionar novas senhas, novas vulnerabilidades e criar sua própria versão

É por isso que vira e mexe a gente vê variantes como a "Mozi" ou a "Okiru".

O "DNA" da Mirai tá espalhado por toda a internet das coisas até hoje

---

## A anatomia de um ataque de DDoS (Denial of Service)

Só pra tu entender como seu roteador vira uma arma:

Existem vários tipos de ataque que uma botnet faz, mas os mais comuns são:

- **UDP Flood:** O botmaster manda os 500 mil dispositivos mandarem pacotes UDP pro alvo ao mesmo tempo, o servidor do alvo fica tão ocupado tentando processar aquele lixo que não sobra espaço pra atender os usuários reais.

- **HTTP Flood:** É como se 1 milhão de pessoas dessem F5 num site ao mesmo tempo. O servidor web abre o bico e cai.

É força bruta pura. Não tem firewall que segure se o volume de dados for maior que a largura de banda da empresa, né

---

## Como se proteger (ou não ser um zumbi)

Se tu não quer que sua rede seja usada pra atacar os outros (e de quebra ficar com a internet uma carroça), o básico que a gente sempre fala aqui:

- Mude a senha padrão: Vô nem falar nada disso aqui

- Desative o UPnP: Aquela parada que abre portas no roteador automaticamente? É um convite pra malware. Desativa essa bosta

- Atualize o Firmware: Eu sei que dá preguiça, mas os fabricantes lançam patches de segurança. Se tu não atualiza, você é um alvo fácil pro próximo scanner que passar

- Isole o IoT: Se tu manja mais, cria uma VLAN ou uma rede Wi-Fi só pras suas "coisas inteligentes", se a sua lâmpada for infectada, o hacker não consegue pular pro seu PC onde tá seu banco e seu código.

---

## O Insight de hoje

A segurança da internet não depende só dos grandes servidores do Google ou da Amazon

Ela depende do seu roteador de 100 reais e daquela câmera barata que você comprou no site chinês.

No mundo hiperconectado, a sua falta de cuidado com a sua rede doméstica é o que alimenta o arsenal dos maiores ataques cibernéticos da história.

A gente não tá mais na era onde o hacker precisa de um supercomputador enquanto tem 160 de QI. Ele só precisa que tu seja preguiçoso 

---

## Resumo rápido pra fixar

```
Botnet = Rede de dispositivos zumbis controlada por um C2.

Mirai = A botnet que usou senhas padrão de IoT pra derrubar o DNS da internet.

Legado = O código é open source hoje, gerando dezenas de variantes novas todo ano.

DDoS = O principal uso dessas redes: sufocar alvos com excesso de tráfego.

Prevenção = Trocar senhas padrão e isolar dispositivos IoT da sua rede principal.
```

---

##Fechamento

Então tipo assim

A próxima vez que seu Wi-Fi der aquela engasgada sem motivo, ou seu roteador começar a esquentar do nada...

Dá uma olhada nos logs

Vai que tu é um soldado raso e nem sabe que tá acontecendo, né kkkk

---

Porque no fim

Na internet das coisas, se você não protege a sua "coisa", ela vira a "coisa" de outra pessoa

Eu sabo muito

---

Esse foi o Night Talk 60

---

Abraços,
**Rian**
