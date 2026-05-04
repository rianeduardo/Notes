# Night Talk 56 — Chaos Engineering: quebrando seu próprio sistema de propósito

2 de maio de 2026

Hoje a gente vai falar de um conceito que, quando você escuta pela primeira vez, parece meio absurdo, né

---

Tipo:

> “Bora derrubar nosso próprio sistema… de propósito”

E não, não é piada

Isso aqui é **Chaos Engineering**

E é uma das práticas mais usadas por empresas gigantes pra garantir que quando der ruim de verdade, elas sobrevivam

## O que é Chaos Engineering, né

Chaos Engineering é a prática de injetar falhas controladas em um sistema

Pra testar:

- Se ele aguenta
  
- Como ele reage
  
- Onde ele quebra

Tipo assim:

> Em vez de esperar o problema acontecer em produção… você cria o problema

Mas de forma controlada

## A ideia base, tipo bem simples

Todo sistema vai falhar em algum momento

Isso não é “se”… é “quando”

Então a lógica é:

Melhor falhar em um ambiente controlado
Do que falhar do nada, com milhões de usuários

É tipo treino de guerra, né

Você simula o caos, pra não morrer no caos real

## O caso clássico: Netflix

A galera que popularizou isso foi a Netflix

Eles criaram uma ferramenta chamada Chaos Monkey, macacão do caos

O que ela fazia?

Matava servidores aleatoriamente em produção

Sim, produção mesmo

E aí:

Se o sistema sobrevivesse → ok
Se quebrasse → eles corrigiam a arquitetura

Resultado?

**Hoje a Netflix é absurdamente resiliente**

---

## Tipos de caos que dá pra simular

Aqui que fica interessante, né

Você pode causar vários tipos de falha, tipo:

- Derrubar servidores
  
- Aumentar latência de rede
  
- Corromper respostas
  
- Derrubar banco de dados
  
- Simular timeout em APIs
  
- Quebrar comunicação entre serviços

Ou seja…

Tu simula o pior cenário possível

---

## Ligando com SPOF

Lembra do Night Talk de Single Point of Failure? (O último no caso)

Então…

Chaos Engineering é uma forma de descobrir SPOFs na prática

Porque tipo:

Você derruba algo,
E vê o que acontece

Se tudo quebra, então

_Parabéns, você achou um SPOF kkkkk_

---

## Como funciona na prática

Não é sair quebrando tudo igual maluco, né

Tem método

**1. Definir comportamento normal**

Tipo: latência, disponibilidade, erro aceitável

**2. Criar uma hipótese**

Exemplo:
“Se eu derrubar esse serviço, o sistema continua funcionando”

**3. Injetar a falha**

Desligar, atrasar, corromper, etc

**4. Observar**

Logs, métricas, comportamento

**5. E por último, render e corrigir**

---

## Por que isso é tão importante hoje

Porque os sistemas modernos são:

- Distribuídos

- Complexos
  
- Cheios de dependência

E o problema é:

_Você não consegue prever tudo_

Então a única forma de saber se algo aguenta real

É testando de verdade

---

## O lado psicológico

Tem uma resistência gigante nisso

Porque tipo:

> “Como assim vou derrubar meu próprio sistema???”

Mas a real é:

> Seu sistema já vai cair alguma hora

Você só tá escolhendo quando e como isso acontece

---

## Exemplos de falhas reais que isso evitaria

- Queda de região inteira na cloud
  
- API crítica fora do ar
  
- Banco travando
  
- DNS falhando
  
- Serviço interno quebrando tudo

Se você nunca testou isso

Quando acontecer, tu descobre ao vivasso

## Chaos Engineering + Segurança

Isso aqui também conecta com pentest

Porque:

- Ajuda a ver impacto real de falhas

- Mostra caminhos de exploração indireta

- Revela dependências críticas

Às vezes você não precisa explorar uma vulnerabilidade

Só precisa causar uma falha estratégica

E o sistema colapsa

---

## O insight principal

Sistemas não falham só por bugs né

Eles falham por:

- Complexidade
  
- Dependência
  
- Interações inesperadas

Chaos Engineering aceita isso

E usa isso a seu favor

---

## Resumo rápido

Sistemas vão falhar

Chaos Engineering antecipa isso

Você simula falhas controladas

Descobre pontos fracos

Corrige antes do problema real

---

## Fechamento

Então tipo assim

Chaos Engineering é meio contraintuitivo, né

Mas faz total sentido

Porque no fim:

> Sistema resiliente não é o que nunca falha

> É o que sobrevive à falha

E se você nunca testou o caos

O caos vai te testar uma hora né

---

Esse foi o Night Talk 56

Abraços,
**Rian**
