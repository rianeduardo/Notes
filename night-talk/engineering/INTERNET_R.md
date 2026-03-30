# Night Talk 34 — Como a internet decide pra onde seus dados vão

**29 de março de 2026**

Então bora lá

**Como que um pacote de dados sai do seu celular… e encontra um servidor do outro lado do planeta?**

Tipo  

você abre um site  

e em milissegundos  

a informação vai e volta.

Mas, quem que decidiu esse caminho né?

Quem escolheu por onde isso passou?  

Porque não existe uma estrada fixa  

Não existe um GPS da internet  

Então hoje eu vou explicar como a internet decide isso  

E por que isso é muito mais caótico do que parece  

---

## Primeiro, a internet não é uma coisa só

A gente fala “internet” como se fosse uma coisa única  

Mas na real ela é um monte de redes conectadas  

Cada uma controlada por alguém  

Tipo:

- Provedores  

- Empresas  

- Universidades  

- Governos  

---

## Sistemas Autônomos

Cada uma dessas redes é chamada de:

**Sistema Autônomo (AS)**

Basicamente  

uma rede com regras próprias  

controlada por uma entidade  

---

## Agora imagina isso

Milhares de redes  

cada uma com interesses próprios  

todas conectadas  

E mesmo assim  

os dados chegam no lugar certo  

---

## Então quem organiza isso?

Aqui entra um protocolo absurdo  

Chamado:

**BGP (Border Gateway Protocol)**

---

## O que o BGP faz

O BGP é tipo o “Waze da internet”  

Mas sem mapa central  

Cada rede fala pra outra:

“eu sei chegar nesses destinos aqui”

E as outras redes decidem se acreditam ou não  

---

## É tipo um sistema de confiança

Não existe uma autoridade central dizendo:

“esse é o caminho correto”

As redes simplesmente:

- anunciam rotas  

- confiam umas nas outras  

- e encaminham os dados  

---

## Agora pensa no problema

E se alguém mentir?

---

## BGP não verifica muita coisa

Esse é o ponto mais insano  

O BGP foi criado numa época onde todo mundo meio que confiava  

Então ele não tem validação forte  

Se uma rede anuncia:

“eu sei chegar no Google”

Outras redes podem acreditar, e vão kkkk

---

## E isso já deu problema

Já aconteceu de empresas anunciarem rotas erradas  

E do nada  

tráfego global inteiro ir pro lugar errado

Tipo:

- site cair  

- serviço parar  

- tráfego ser redirecionado  

---

## Isso se chama BGP hijack

É quando alguém:

- anuncia rota falsa  

- sequestra tráfego  

---

## Pode ser erro ou ataque

Às vezes é erro né

Mas também pode ser usado como ataque  

Tipo:

- interceptar dados  

- derrubar serviços  

- redirecionar tráfego  

---

## O caminho não é fixo

Outro detalhe interessante  

Seu dado não segue sempre o mesmo caminho  

Ele pode mudar  

dependendo de:

- congestionamento  

- falhas  

- decisões das redes  

---

## Ou seja

Dois pacotes enviados juntos  

podem chegar por caminhos completamente diferentes  

---

## A internet é meio improvisada

E esse é o ponto mais interessante  

A internet não foi projetada como um sistema perfeito  

Ela foi evoluindo  

crescendo  

se adaptando  

---

## E mesmo assim funciona

Mesmo com:

- milhares de redes  

- decisões descentralizadas  

- falhas  

- erros humanos  

Ela funciona  

---

## Conclusão

Então voltando pra pergunta do começo  

Quem decide o caminho dos seus dados?

Ninguém centralmente  

É uma negociação constante entre redes  

Baseada em confiança e anúncios de rotas.

E isso cria uma coisa meio bizarra  

A internet é ao mesmo tempo:

- Extremamente organizada  

e  

- Completamente caótica  

---

Então é isso  

Esse foi o **Night Talk 34**

E isso mostra uma coisa bem interessante  

A internet funciona não porque é perfeita  

Mas porque ela aguenta erro  

Abraços,
**Rian**