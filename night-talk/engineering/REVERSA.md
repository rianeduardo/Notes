# Night Talk 57 — Engenharia Reversa: entendendo sistemas que ninguém quis explicar

04 de maio de 2026

Hoje a gente vai falar de uma skill que, na minha opinião, separa curioso, skid, criança no Kali, de um hacker de verdade, né

_Engenharia Reversa_

Que basicamente na essência bem essencializada é:

> “Já que ninguém me explicou como isso funciona, eu vou descobrir sozinho”

E isso aqui é poderoso pra caralho

---

## O que é engenharia reversa, tipo direto

Engenharia reversa é o processo de pegar algo pronto, e entender como aquilo funciona por dentro

Sem ter acesso ao código original, documentação ou nada

Pode ser:

- Um software
  
- Um app mobile
  
- Um malware
  
- Um protocolo
  
- Um firmware
  
- Até um hardware

É com isso inclusive que a galera muitas vezes vai piratear software tá?

Então sempre **MUITO** cuidado ao baixar coisa crackeada por aí

Tu ta basicamente baixando uma cópia de um software, que foi modificada por alguém (mal intencionado na essência)

---

## Exemplo simples

Imagina um app fechadão

Você **NÃO** tem o código

Mas você quer saber:

Como ele autentica,
Que API ele usa,
Como ele protege dados, entre outros

Então tu basicamente:

- Analisa o tráfego
  
- Decompila o app
  
- Observa comportamento

E vai meio que montando um quebra-cabeça

---

## Por que isso é tão importante

Porque no mundo real…

> Ninguém te entrega tudo mastigado

Empresas escondem lógica,
Sistemas são fechados,
E malware obviamente não vem com manual né

Então se tu quer:

- Fazer pentest sério
  
- Analisar malware
  
- Quebrar proteções
  
- Ou até aprender mais rápido

Engenharia reversa é essencial

---

## Onde isso aparece na prática

Isso aqui tá em TODO lugar, tipo:

- Apps Android (APK reverse)
  
- Binários no Windows/Linux
  
- Jogos (modding, cheat, etc)
  
- Malware analysis
  
- Protocolos fechados
  
- APIs não documentadas

Tu já usou engenharia reversa sem perceber **COM CERTEZA**

---

## Técnicas comuns

Aqui começa a ficar mais técnico, vou tentar pegar de todos os mundos aqui, tanto de desktop, quanto de mobile

Análise estática:

**Você olha o código sem executar**

- Decompilar APK
  
- Ler assembly
  
- Inspecionar strings

Análise dinâmica:

**Tu executa e observa**

- Debug (tipo x64dbg ou GDB)
  
- Hooking
  
- Monitorar chamadas
  
- Interceptação de tráfego

Muito usado em mobile:

- Proxy tipo Burp (pra ver o que o app manda pra rede)
- Frida (esse aqui é bruxaria, tu vê o que o app tá pensando em tempo real)

Instrumentação:

**Modificar o comportamento do app**

- Hook de funções
  
- Alterar fluxo

**POUQUÍSSIMA** gente sabe isso de verdade, falando sério

---

## E se eu dominar isso?

Aqui é onde fica roubado

Se tu faz engenharia reversa bem:

Tu entende a lógica interna, ou seja:

- Descobre endpoints escondidos

- Vê validações client-side

- Encontra chaves hardcoded (secrets no geral né, tipo chave de AWS ou Firebase que nego esquece lá)

- Identifica falhas de auth

Ou seja

_Tu para de testar “no escuro”_

É tipo a Matrix, sabe? Tu não vê mais o app bonitinho, tu começa a ver os dados escorrendo na tela enquanto você usa

---

## O lado mais insano

Tem coisa que só aparece com reverse

Tipo:

- Função que não é usada na UI
  
- Feature escondida
  
- Código morto mas vulnerável
  
- Backdoors esquecidos

Isso aqui é bug bounty **puro**, grana flui legal com isso

Achar uma secret crítica num APK de uma fintech, por exemplo, é o tipo de coisa que faz teu relatório brilhar e o bounty vir gordíssimo, barrigudinho

---

## A barreira de entrada

Não vou romantizar não, né

Engenharia reversa é difícil, não é pouco, é BEM difícil mesmo

Tem:

- Assembly
  
- Obfuscação
  
- Anti-debug
  
- Anti-tamper

Não adianta baixar o Ghidra ou o IDA Pro se tu não tiver a paciência de um monge pra ler instrução de baixo nível, né

Mas tipo assim

Depois que você pega o jeito, vira um superpoder mesmo sabe

---

## Insight importante

Programas são caixas pretas só até alguém abrir

E alguém sempre abre

Então segurança por obscuridade?

**NÃO segura muito tempo**

---

## Resumo rápido

Engenharia reversa = entender algo sem código

Usada em segurança, malware, apps, tudo

Usa análise estática + dinâmica

Dá **visão interna** do sistema

É difícil, mas extremamente poderosa

---

## Fechamento

Então tipo assim

Se tu quer sair do nível:

> “Testar o que aparece”

E ir pro nível:

> “Entender como funciona por dentro”

Tu precisa de engenharia reversa

Porque no fim

_Quem entende o sistema por dentro, joga OUTRO jogo, totalmente diferente_

---

Esse foi o Night Talk 57

Abraços,
**Rian**
