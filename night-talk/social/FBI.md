# Night Talk 29 — Como o FBI derruba sites da dark web

**18 de março de 2026**

Hoje eu quero começar com uma pergunta  

Se a dark web é anônima, se o Tor esconde o IP, se tudo é criptografado...

**Como que o FBI derruba sites lá dentro?**

Tipo, como que pegaram o dono da Silk Road, se o cara fez um puta sistema anônimo?

Como que derrubam marketplaces inteiros?  

>Se teoricamente não dá pra rastrear nada  

Então hoje eu vou explicar um pouco como isso acontece na prática, porque não é magia  

E também não é só “hackear tudo”  

Na maioria das vezes  

É erro humano mesmo  

---

## Primeiro, o mito da invencibilidade

A primeira coisa que a gente precisa quebrar é essa ideia de que a dark web é impossível de rastrear  

Ela não é  

O que o Tor faz é esconder o caminho da conexão, mas ele não torna você invisível em todos os aspectos  

Ele só protege **uma parte do problema**

Então o erro já começa aí  

Muita gente acha que tá 100% seguro  

Mas não tá, é bem seguro comparado a um navegador comum, pique um chrome, mas não ta 100% anônimo, e convenhamos, nunca vai estar, e tu vai entender o porque

---

## Como o Tor funciona (bem resumido)

O Tor funciona com algo chamado **roteamento em camadas**, bagulho militar isso ok?

Sua conexão passa por vários nós  

Cada nó sabe só uma parte do caminho  

Então ninguém sabe:

- De onde veio  

- Pra onde vai  

>Ao mesmo tempo  

Por isso ele dá anonimato  

Mas isso é só na **rede**, não protege outras coisas  

---

## O ponto fraco sempre é o humano

Agora vem o ponto principal  

A maioria das quedas de sites da dark web não acontece por quebra de criptografia  

Acontece por:

- Erro humano  

- Configuração errada  

- Vazamento de informação  

Um exemplo clássico é o Silk Road, que já falamos aqui no talk uma vez, a história completa, desde a infância do criador até sua queda e legado

O criador usou o pseudônimo “Altoid” em fóruns  

Mas em um momento ele colocou o próprio email pessoal  

Pronto, já era

---

## Vazamento de IP

Outro erro comum  

Servidores mal configurados  

Se um site .onion faz alguma requisição errada  

Ele pode vazar o IP real do servidor, foi exatamente assim que localizaram o servidor do Silk Road

Um simples erro de configuração...

---

## Infiltração

Outro método muito usado é **infiltração**

Agentes entram no sistema fingindo ser usuários  

Vendedores, ou até administradores  

Com o tempo eles ganham confiança  

E começam a coletar informação  

Isso aconteceu várias vezes  

Inclusive com agentes que chegaram a operar dentro das plataformas  

---

## Engenharia social

Isso aqui é clássico né pessoal

Não precisa hackear o sistema  

Hackeia a pessoa  

Convencer alguém a:

- Revelar informação  

- Clicar em algo  

- Baixar um arquivo  

Isso quebra muito mais sistema do que qualquer exploit, e sim, descobrir info, chantagear, controlar alguém, é tecnicamente hacking na essência né

---

## Malware e exploits

Agora sim entra a parte mais técnica  

Às vezes o governo usa exploits pra identificar usuários né

Isso já aconteceu com:

- Navegadores  

- Plugins  

- Sistemas desatualizados  

Eles enviam um payload que revela o IP real da pessoa  

Mesmo usando Tor  

---

## Operações coordenadas

Também existem operações grandes  

Onde várias agências trabalham juntas  

Um exemplo famoso foi a operação que derrubou vários marketplaces ao mesmo tempo  

A ideia é simples, atacar vários alvos simultaneamente  

>Pra evitar migração de usuários  

---

## O erro mais comum de todos

Mas no final o maior problema continua sendo um só  

**Erro humano**

Pode ser:

- Um login fora do Tor  

- Um email pessoal  

- Um descuido  

- Um padrão repetido  

Anonimato exige perfeição  

E humanos não são perfeitos  

---

## Conclusão

Então respondendo a pergunta do começo  

Como o FBI derruba sites da dark web?

Não é porque o Tor é fraco  

Mas porque o sistema inteiro envolve muito mais coisas do que só criptografia  

- Envolve comportamento  

- Configuração  

- Erros  

- Confiança  

E no final sempre existe algum ponto fraco  

E geralmente esse ponto fraco é humano  

---

Então é isso  

Esse foi o **Night Talk 29**

E isso mostra uma coisa interessante  

No mundo da segurança:

>A tecnologia pode ser perfeita, mas o humano nunca é

Abraços,
**Rian**
