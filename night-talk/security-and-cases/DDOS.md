# Night Talk 33 — Como funciona um ataque DDoS (de verdade)

**27 de março de 2026**

Então bora lá né pessoal  

Hoje eu quero começar com uma pergunta bem simples  

**Como que um site gigantão cai do nada?**

Tipo  

Um site com milhões de usuários,

infraestrutura robusta  

CDN,

cloud,

tudo certinho.

E mesmo assim, do nada  

Fica fora do ar?

---

## O que é um DDoS

DDoS significa:

**Distributed Denial of Service**

Ou seja  

Negação de serviço distribuída  

A ideia é simples  

Você não quebra o sistema  

Tu **sufoca ele**

---

## A analogia mais fácil

Imagina uma loja  

Ela atende 100 pessoas por minuto  

Agora imagina que chegam:

**100 mil pessoas ao mesmo tempo**

A loja não aguenta  

Não importa o quão organizada ela seja  

Ela trava  

---

## Agora leva isso pra internet

Um servidor tem limite  

Ele consegue lidar com:

- X requisições por segundo  

Se você manda muito mais que isso  

Ele vai eventualmente:

- Atrasar  

- Travar  

- Cair  

Isso é tipo, inevitável basicamente 

---

## Por que “Distributed”

Agora vem o ponto mais importante  

Se fosse só uma máquina atacando, seria fácil bloquear  

Mas no DDoS não  

O ataque vem de milhares, milhões de dispositivos diferentes  

---

## Botnets

Esses dispositivos formam o que chamamos de **botnet** (Já falei disso aqui!)

São computadores infectados  

Sem o dono saber  

Podem ser:

- PCs  

- Celulares  

- Servidores  

- Até geladeira, câmera, IoT  

Sim, qualquer coisa conectada pode virar parte disso 

Por mais bizarro que seja, se tu tiver sei lá, uma cafeteira conectada na internet, ela vira parte

---

## Como isso acontece

O atacante controla essa rede  

E manda todos os dispositivos fazerem requisições ao mesmo tempo  

Tipo:

>"todo mundo acessa esse site agora”

E pronto  

o site morre  

---

## Tipos de DDoS

Existem vários tipos  

Mas vou te dar os principais aqui

---

## Flood

O mais simples  

Só manda requisição sem parar  

Tipo:

- HTTP flood  

- UDP flood  

---

## Amplificação

Aqui fica mais interessante  

O atacante manda uma requisição pequena  

Mas o servidor responde com uma resposta muito maior  

Ou seja, multiplica o ataque  

---

## Ataque de camada 7

Esse é mais sofisticado  

Ele imita comportamento humano  

Tipo:

- Navegar  

- Clicar  

- Carregar páginas  

Mais difícil de detectar, e mais destrutivo consequentemente

---

## Por que isso ainda funciona

Agora vem a pergunta  

Se isso é tão conhecido por que ainda funciona?

---

## Escala

Porque hoje a internet tem bilhões de dispositivos  

É fácil criar botnets gigantes  

---

## Custo baixo

Ataques são baratos  

Defesa é cara  

---

## Assimetria

O atacante só precisa acertar uma coisa  

O defensor precisa proteger tudo  

---

## Cloud e DDoS

Hoje serviços como:

- AWS  

- Cloudflare  

- Google Cloud  

Tentam dar ali uma mitigada nisso tudo né

Usando:

- Rate limit  

- Distribuição  

- Filtragem  

Mas mesmo assim ataques gigantes ainda acontecem

---

## O detalhe mais interessante

DDoS não explora bug  

Não quebra criptografia  

Não invade sistema  

Ele só usa uma coisa né

**Escala**

---

## Conclusão

Então respondendo a pergunta do começo  

Como um site gigante cai do nada?

Ele não foi hackeado  

Ele foi sufocado.

DDoS é basicamente isso  

Não é sobre quebrar né 

É sobre **sobrecarregar até parar**

---

Então é isso  

Esse foi o **Night Talk 33**

E isso mostra uma coisa bem importante  

Nem todo ataque é sofisticado  

Às vezes, força bruta ainda vence  

Abraços,
**Rian**