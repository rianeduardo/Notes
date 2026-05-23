# Night Talk 59 — Shodan: o Google que te deixa sem dormir

23 de maio de 2026

Ontem a gente falou de OSINT e de como as pessoas entregam o ouro no Linkedin, né, mas hoje o papo é sobre as máquinas que entregam o ouro sozinhas e ninguém nem percebe

_Shodan_

Se o Google indexa o que as pessoas escrevem pra outras pessoas lerem, o Shodan indexa o que as máquinas respondem quando alguém "bate na porta" delas

E o que elas respondem muitas vezes é bizarro e assustador ao mesmo tempo

Então bora lá

---

## O que é essa ferramenta afinal

O Shodan é, essencialmente, um buscador de dispositivos conectados.

_Mas esquece site bonitinho e SEO_

Diferente do Google, que manda robôs pra ler textos e imagens

O Shodan manda "pings" e tenta ler o banner de qualquer coisa que tenha um IP público e uma porta aberta

O banner é tipo o cartão de visitas da máquina, né

Ela fala: "Oi, eu sou um servidor Apache na versão tal" ou "Oi, eu sou uma câmera IP da marca tal"

_E nessa brincadeira, o Shodan acha de tudo:_

- Servidores de banco de dados (que deveriam estar escondidos)

- Câmeras de segurança de pet shop, escritório e até quarto de criança (tenso, né)

- Sistemas de controle industrial (SCADA) de usinas e fábricas

- Geladeiras, TVs e até lâmpadas inteligentes

- Semáforos e radares de velocidade

Sim, tudo isso de verdade

---

## A anatomia do vacilo: O perigo do "Default"

O grande problema que o Shodan revela não é nem uma falha zero-day super complexaque só a NSA conhece né

É a pura e simples negligência combinada com a pressa

Imagina que o dono de uma padaria quer colocar uma câmera pra ver o caixa de casa

_(Isso é SUPER comum)_

Ele compra a câmera, espeta no wifi, abre uma porta no roteador pra conseguir acessar pelo celular e...

Pronto!! Funciona, né?

Só que ele esqueceu de trocar a _senha de fábrica_

A grande e segura "admin" kkkkk

O Shodan passa por ali em minutos, vê que a porta tá aberta, identifica o modelo "ChinêsGenérico-3000" e indexa aquilo

-> Aí o hacker não precisa de exploit nenhum. Ele só digita no Shodan: product:"ChinêsGenérico-3000"

Aparece uma lista, ele tenta admin/admin ou admin/12345 e pronto.

**Ele tá dentro da rede do cara**

Isso não é hacking de cinema, é só saber onde a porta tá encostada

O que por sinal é extremamente fácil dependendo do caso

---

## Onde o buraco fica mais fundo (SCADA e Bancos)

Se fosse só câmera de padaria, beleza, né

(Todo respeito as padarias mas vocês não são tão importantes)

Mas o Shodan mostra coisas que fazem a gente questionar quem tá cuidando da infraestrutura do mundo

Você consegue achar painéis de controle de prédios inteiros. Ar-condicionado, elevador, iluminação...

TUDO ali, num painel web que, às vezes, nem senha tem.

Ou pior: bancos de dados tipo MongoDB ou Elasticsearch expostos

O cara sobe o banco na nuvem, esquece de configurar a whitelist de IPs, e o banco fica aberto pra internet toda

Aí não precisa de SQL Injection, né

É só conectar no IP e dar uma dumpada boua

---

É assim que acontece 90% desses vazamentos gigantes de dados que a gente vê na TV.

O cara nem precisou invadir, o dado tava ali, gritando pra ser levado

---

## Por que isso é importante pra você?

Se tu quer ser um hacker de verdade, ou um profissional de segurança sério, o Shodan é o seu melhor amigo e seu pior pesadelo

No pentest, é a primeira coisa que você olha

>"O que meu cliente tem exposto que ele nem sabe?"

Às vezes a empresa investe milhões em firewall...

Mas o estagiário de marketing subiu um servidor de teste "só pra ver um negócinho" e esqueceu ele ligado com uma versão do Linux de 2014

O Shodan vai sim te mostrar esse servidor

E esse servidor vai ser sim sua porta de entrada pra rede interna!

Sinal de coisas boas :))

---

## O Insight de hoje

A gente vive num mundo de Internet das Coisas (IoT)

Mas a galera esquece que cada "coisa" dessa é um computadorzinho com sistema operacional e falhas

Milhares de falhas talvez, algumas que nínguem descobriu ainda até hoje

Zero-days, que já falamos aqui diversas vezes

Quase TUDO no mundo hoje em dia tem potencial de ter uma zero-day

Segurança não é só o firewall do seu servidor principal, né

É a visão periférica

É aquele sensor de temperatura que o RH comprou e espetou no Wi-Fi da empresa sem avisar a TI.

Se tem um IP e uma porta, o Shodan vai achar, e se o Shodan achar, qualquer pessoa no mundo pode tentar a sorte

>"Privacidade e segurança dão trabalho. E a maioria das pessoas prefere a conveniência"

---

## Resumão rápido pra não esquecer 30s

- **Shodan = O buscador de hardware. Ele indexa o que tá "vivo" na rede**

- **Banners = A identidade do dispositivo que o Shodan lê**

- **Negligência = O combustível do Shodan (senhas padrão e falta de patch)**

- **Alcance = Vai de uma lâmpada até uma turbina de usina**

- **Uso técnico = Essencial pra Recon (reconhecimento) em qualquer teste de invasão**

---

##Fechamento

Então tipo assim

Dá uma olhada no que tu tem pendurado no seu roteador hoje

Se você abriu porta pra jogar ou pra acessar algo de fora, você tá no radar

Porque no fim das contas

Não adianta trancar a porta da frente com 10 cadeados se a janela do banheiro tá aberta e o Shodan já tirou foto de quem tá lá dentro

---

Esse foi o Night Talk 59

Nota: No próximo talk, acho que vou falar sobre como a gente se defende disso, ou talvez sobre como os caras usam essas falhas de IoT pra criar botnets gigantes, tipo a Mirai, então vão checar o talk 60!

---

Abraços,
**Rian**
