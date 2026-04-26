# Night Talk 52 — DNS Cache Poisoning: envenenando a internet

**25 de abril de 2026**

Então bora lá né pessoal  

Hoje eu quero começar com um cenário simples  

---

Você entra no site do seu banco  

---

Tudo parece normal  

layout certo  

URL certa  

---

Mas na real num é o banco

---

## Como isso seria possível?

---

Sem hackear o servidor  

Sem invadir o site  

---

Só mexendo no caminho  

---

Isso é:

**DNS Cache Poisoning**

---

## Primeiro relembrando rápido

DNS traduz:

site.com → IP  

---

E pra ser rápido  

ele usa cache  

---

Guarda respostas  

---

## Agora vem o ataque né

A ideia é simples  

---

**enganar o cache DNS**

---

Fazer ele guardar uma resposta falsa  

---

## Exemplo

Você pergunta:

“qual o IP de banco.com?”  

---

O DNS deveria responder:

IP real  

---

Mas o atacante injeta:

IP falso  

---

E o servidor guarda isso  

---

## Resultado

Todo mundo que perguntar depois  

---

Vai ser redirecionado pro IP falso  

---

## Isso escala MUITO

Não é só uma pessoa  

---

Pode afetar:

- Uma rede inteira  
- Um provedor  
- Milhares de usuários  

---

## E o mais bizarro

O site real continua normal  

---

Mas você não chega nele  

---

## Parece legítimo

Porque:

- domínio é o mesmo  
- navegador não suspeita  
- usuário confia  

---

## Isso é perigoso demais

Porque quebra um princípio básico  

---

**“se o domínio tá certo, tá seguro”**

_O TANTO de gente que fala isso é absurdo_

---

Não necessariamente  

---

## Como isso acontece na prática

Agora simplificando bem né

---

O atacante tenta:

- Prever requisições DNS  

- Mandar respostas falsas antes da legítima  

- Fazer o servidor aceitar  

---

É uma corrida basicamente

Quem responde primeiro ganha  

---

## Antigamente era pior

Antes de melhorias  

isso era bem mais fácil  

---

Hoje tem proteções  

---

Mas ainda existem cenários exploráveis  

---

## Impacto real

Com isso dá pra:

- Redirecionar tráfego  

- Fazer phishing avançado  

- Interceptar dados  

---

Sem tocar no alvo direto

---

## Conectando com pentest

Isso aqui é clássico de:

- Infraestrutura mal configurada  

- Servidores DNS abertos  

- Falta de validação  

---

## Defesa (resumido)

Algumas coisas ajudam:

---

- DNSSEC (validação de resposta)  

- Randomização de portas  

- IDs de query mais seguros  

---

Mas não é perfeito  

---

## Insight principal

O ataque não quebra o site  

---

Ele quebra a confiança no caminho  

---

## Conclusão

Então voltando pro começo  

---

Como você pode entrar num site certo… e estar no lugar errado?

---

Resposta:

**DNS comprometido**

---

Então é isso  

Esse foi o **Night Talk 52**

---

E esse aqui mostra uma coisa muito forte  

---

Na internet  

não basta o destino ser seguro  

---

O caminho também precisa ser  

---

Abraços,
**Rian**