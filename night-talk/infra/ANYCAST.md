# Night Talk 53 — Anycast: como 1 IP existe no mundo inteiro

**26 de abril de 2026**

Então bora lá né pessoal  

Hoje eu quero começar com uma parada meio absurda  

---

**Como que o mesmo IP pode existir em vários lugares ao mesmo tempo?**

---

Tipo assim  

um servidor em São Paulo  

outro em Nova York  

outro na Europa  

---

E TODOS usam o MESMO IP  

---

Parece errado  

---

Mas funciona  

---

Isso é:

**Anycast**

---

## Primeiro, o “normal”

Normalmente (unicast)  

---

Um IP aponta pra um servidor  

---

Você faz requisição  

Vai praquele lugar específico  

Simples  

---

## Agora o Anycast

Aqui quebra tudo  

---

O mesmo IP  

é anunciado em vários lugares do mundo  

---

Vários servidores  

mesmo IP  

---

## Então pra onde você vai?

---

Boa pergunta  

---

A resposta é:

**pro mais “próximo” de você**

---

## Mas não é proximidade física só

É proximidade de rede  

---

Quem decide isso é o roteamento né

---

## Como funciona na prática

Você acessa um serviço  

Seu tráfego entra na internet  

Os roteadores analisam  

E escolhem o caminho mais eficiente  

---

Resultado:

você cai no servidor mais próximo  

---

## Isso é absurdo de útil

Porque permite:

---

- Baixa latência  

- Alta disponibilidade  

- Escala global  

---

## Exemplo real

Serviços como:

- DNS (tipo Cloudflare)  

- CDNs  

- APIs globais  

---

Usam Anycast  

---

## Por isso às vezes é MUITO rápido

Você não tá acessando “um servidor lá longe”  

---

Você tá acessando um servidor perto de você  

Sem saber  

---

## Failover automático

Isso é muito doido

Se um servidor cai  

---

Outro já tá lá  

Mesmo IP  

O tráfego simplesmente muda de rota  

Sem você perceber  

---

## Isso é poderoso demais

Porque não precisa:

- Mudar DNS  

- Atualizar nada  

---

A rede resolve  

---

## Mas não é perfeito

Agora vem o lado real  

---

Anycast tem desafios né 

---

## Consistência

Você pode cair em servidores diferentes  

---

Isso pode causar:

- Sessões quebradas  

- Comportamento estranho  

---

## Ataques

Se alguém anuncia rota errada (BGP hijack)  

---

Pode:

- Sequestrar tráfego  

- Redirecionar usuários  

---

Olha a conexão com o próximo talk ai, vamos falar sobre BGP, da uma olhada depois

---

## Conecta com DNS

Muitos serviços DNS usam Anycast  

---

Então quando você faz uma query  

Ela vai pro servidor mais próximo  

Isso melhora MUITO o tempo de resposta  

---

## Insight principal

Anycast não é “um servidor em vários lugares”  

---

É basicamente:

**vários servidores fingindo ser um só**

---

## Isso muda tudo

Porque abstrai localização  

---

Você não sabe onde está o servidor  

E nem precisa saber  

---

## Conclusão

Então voltando pra pergunta do começo  

---

Como um IP pode existir no mundo inteiro?

---

Resposta:

Anycast  

---

E isso é uma das coisas mais elegantes da internet né, fato não opinião 

---

Então é isso  

Esse foi o **Night Talk 53**

---

E esse aqui mostra algo muito forte  

A internet não é só conexão  

É engenharia absurda por trás  

---

Abraços,
**Rian**