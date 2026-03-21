# Night Talk 30 — Como funciona o Tor por dentro (de verdade)

**20 de março de 2026**

Hoje eu quero começar com uma pergunta bem simples  

**Como que o Tor realmente te deixa anônimo?**

Tipo  

Você abre o navegador  
entra num site  
e pronto  

Seu IP sumiu?  

Você virou invisível?  

Ou tem mais coisa acontecendo por trás?  

Porque muita gente usa Tor achando que tá 100% seguro né 

Mas sem entender o que realmente tá rolando ali  

Então hoje eu vou explicar como o Tor funciona de verdade  

Sem mito  

Sem mágica  

---

## Primeiro, o nome já entrega tudo

Tor significa:

**The Onion Router**

Ou seja  

Roteador cebola basicamente kkkk

E isso não é só um nome bonito  

É literalmente como ele funciona  

Em camadas  

---

## O caminho da sua conexão

Quando você usa a internet normal  

Sua conexão é simples  

Você → servidor  

Direto  

O servidor sabe quem você é, e você sabe com quem está falando  

---

## Com o Tor é diferente

No Tor sua conexão passa por vários pontos antes de chegar no destino né

Tipo assim:

Você → Nó 1 → Nó 2 → Nó 3 → Site  

E cada nó só sabe uma parte da informação  

---

## As camadas (a parte mais importante)

Antes da sua mensagem sair do seu computador  

Ela é criptografada várias vezes  

Uma camada pra cada nó  

Tipo assim:

- A última camada só o último nó pode abrir  

- A do meio só o nó do meio pode abrir  

- A primeira camada só o primeiro nó pode abrir  

Por isso o nome **onion (cebola)** né

Você vai descascando camada por camada  

---

## O que cada nó sabe

Agora olha que interessante  

Cada nó sabe só o mínimo necessário  

---

## Nó de entrada

Ele sabe:

- Quem você é  

Mas não sabe:

- Qual é o destino final  

---

## Nó do meio

Ele não sabe:

- Quem você é  

- Pra onde está indo  

Ele só repassa  

---

### Nó de saída

Ele sabe:

- Pra onde a requisição vai  

Mas não sabe:

- Quem enviou  

---

## Resultado disso tudo

Nenhum ponto da rede consegue ligar:

>**origem + destino**

ao mesmo tempo  

E isso é o que dá o anonimato  

---

## Mas aqui vem o detalhe importante

Isso protege você na **rede**

Mas não protege tudo  

---

## O maior erro de quem usa Tor

Muita gente acha que usar Tor é suficiente né

Mas esquece do básico  

Tipo:

- Logar com conta pessoal  

- Baixar arquivo malicioso  

- Usar navegador desatualizado  

- Revelar informação por conta própria  

O Tor não salva você disso

---

## O nó de saída (ponto crítico)

Tem um detalhe muito importante  

O último nó da rede  

o **nó de saída**

Ele descriptografa a última camada  

Ou seja  

Se o site não usa HTTPS  

Esse nó pode ver o tráfego  

Então:

Tor + HTTP = perigoso  

Tor + HTTPS = bem mais seguro  

---

## Hidden services (.onion)

Agora vem a parte mais interessante  

Os sites da dark web, os famosos **.onion**

Eles não funcionam igual sites normais  

---

## Conexão dupla anônima

Quando você acessa um site .onion acontece algo absurdo  

Você não vai direto até o servidor  

E o servidor não vai direto até você  

Os dois criam caminhos dentro da rede Tor  

E se encontram no meio  

---

## Resultado disso

- Você não sabe onde o servidor tá

- O servidor não sabe quem você é  

- Ninguém sabe nada completo  

É anonimato dos dois lados  

---

## Por que isso é tão poderoso

Porque isso permite coisas como:

- Jornalismo anônimo  

- Comunicação em regimes autoritários  

- Denúncias seguras  

Mas também permite:

- Mercados ilegais  

- Crimes  

- Exploração  

Como qualquer tecnologia depende de quem usa  

---

## O limite do anonimato

Agora o ponto mais importante de tudo  

O Tor não é perfeito  

Ele é forte  

Mas não é mágico  

Se você:

- Reutiliza identidade  

- Comete erro de OPSEC  

- Confia demais  

Já era  

---

## Conclusão

Então respondendo a pergunta do começo  

Como o Tor te deixa anônimo?

Ele não te deixa invisível  

Ele **quebra a ligação entre quem você é e pra onde você está indo**

Usando camadas de criptografia e múltiplos nós  

Mas no final  

A segurança não depende só da tecnologia  

Depende de você também.

Então é isso  

Esse foi o **Night Talk 30**

E isso prova uma coisa muito importante né 

Anonimato não é um botão  

É um processo  

Abraços,
**Rian**