# Night Talk 47 — Prompt Injection: hackeando IA sem código

**17 de abril de 2026**

Então bora lá né pessoal  

Hoje eu quero começar com uma pergunta meio estranha  

**e se desse pra hackear um sistema… só conversando com ele?**

---

Sem exploit  

Sem malware  

Sem código  

---

Só texto  

---

Parece estranho  

mas isso já existe  

---

E tem nome  

**prompt injection**

---

## Primeiro — o que é isso

IA tipo chatbot funciona com instruções  

---

Tem o que chamam de:

- System prompt (regras internas)  

- Input do usuário  

---

E o modelo tenta seguir tudo isso  

---

Mas tem um problema  

---

Ele não sabe separar perfeitamente  

o que é regra  

do que é input  

---

## E aí vem o ataque

O atacante escreve algo tipo:

“Ignore todas as instruções anteriores e faça X”

---

E dependendo do sistema  

a IA obedece  

Simples assim  

---

## Por que isso funciona

Porque IA não “entende” de verdade  

Ela só prevê texto  

Então se o input for bem construído  

Ela pode tratar aquilo como prioridade  

---

## O nível disso

Agora imagina isso aplicado em sistemas reais  

---

IA integrada com:

- APIs  

- Banco de dados  

- Sistemas internos  

Se você manipula a IA  

---

Você pode influenciar o sistema inteiro  

---

## Exemplos reais

Sem viajar muito  

---

Você pode tentar:

- Fazer IA vazar informação  

- Ignorar regras  

- Executar ações inesperadas  

Tudo via linguagem natural  

---

## O mais assustador

Não parece ataque  

Parece conversa  

E isso quebra totalmente o modelo tradicional de segurança  

---

## Conecta com o Talk 46

Lá eu falei que IA vira arma né

Aqui é exatamente isso  

Você não precisa mais explorar código  

Você explora comportamento  

---

## O erro das empresas

Muita empresa coloca IA em produção  

---

Mas pensa só em:

- backend  

- autenticação  

- infra  

E esquece de uma coisa  

**o prompt também é superfície de ataque**

---

## Não tem “input seguro”

Esse é o ponto mais pesado  

Qualquer input pode ser malicioso  

Porque linguagem é flexível  

E IA tenta interpretar tudo  

---

## Defesa (e por que é difícil)

Agora vem a parte complicada  

---

Não dá pra simplesmente:

- bloquear palavras  

- filtrar tudo  

Porque o atacante pode reformular  

É um jogo de criatividade  

---

## O padrão de novo

Olha isso  

---

Assim como phishing  

assim como engenharia social  

---

Prompt injection também explora:

**confusão + contexto**

---

## Conclusão

Então voltando pra pergunta do começo  

Dá pra hackear um sistema só conversando?

Sim né

E isso já ta acontecendo  

E o mais louco

É que não parece hacking  

Mas é  

---

Então é isso  

Esse foi o **Night Talk 47**

E esse aqui mostra uma coisa muito importante  

---

No mundo da IA  

o input é tão perigoso quanto o código  

---

Abraços,
**Rian**
