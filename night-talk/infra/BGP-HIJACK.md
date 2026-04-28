# Night Talk 54 — BGP Hijack: como sequestrar a internet sem invadir nada

**27 de abril de 2026**

Então bora lá né pessoal  

Hoje eu quero começar com uma pergunta meio absurda  

---

**E se alguém pudesse “roubar” o tráfego da internet… sem hackear nenhum servidor?**

---

Sem invadir  

Sem malware  

Só mexendo no caminho  

---

Isso existe  

E tem nome  

---

**BGP Hijack**

---

## Primeiro, o que é BGP

BGP significa:

**Border Gateway Protocol**

---

Mas esquece o nome técnico  

---

Pensa assim  

---

BGP é o sistema que decide:

**por onde seu tráfego vai passar**

---

## Tipo um GPS da internet

Só que global  

---

Ele conecta:

- Provedores
  
- Países
  
- Empresas  

---

## Agora o detalhe importante

BGP funciona na base de confiança  

---

Um sistema anuncia:

“eu sei chegar nesse IP”  

---

E os outros acreditam  

---

## E aqui começa o problema

## O ataque

No BGP Hijack  

---

Um atacante anuncia:

“eu tenho o caminho pra esse destino”  

Mesmo não tendo  

---

## Resultado

O tráfego começa a ir pra ele  

---

## Simples assim

Não precisa invadir nada  

---

Só mentir pro roteamento  

---

## Exemplo

Você quer acessar:

site.com  

---

Normalmente o caminho é:

→ ISP → destino real  

---

No ataque:

→ ISP → atacante  

---

## E aí?

Depende do atacante  

---

Ele pode:

- Dropar o tráfego (derrubar serviço)
  
- Espionar dados
  
- Redirecionar  

---

## Isso é MUITO sério

Porque acontece em nível de infraestrutura  

---

Não é usuário  

Não é app  

---

É a internet em si  

---

## Casos reais

Isso já aconteceu várias vezes  

---

Tipo:

- Tráfego global sendo redirecionado por erro
  
- Empresas sequestrando rotas sem querer
  
- Até governos envolvidos  

---

Às vezes nem é ataque né

É erro humano  

---

## E mesmo assim causa caos

Porque BGP não valida muito  

Ele confia  

---

## Conectando com Anycast

Lembra do Talk 53?  

---

Anycast depende de anúncios BGP  

Então se alguém anunciar errado  

Pode quebrar tudo  

---

## Conecta com DNS também

Se você sequestra rota de DNS  

---

Você pode:

- Atrasar resposta
  
- Manipular tráfego
  
- Causar falha global  

---

## Defesa (e o problema)

Existem mecanismos tipo:

---

- RPKI (validação de rota)
  
- Filtros de anúncio  

---

Mas não é universal  

---

## Ou seja

Ainda depende de:

**configuração correta + confiança**

---

## Insight principal

O BGP Hijack não ataca o destino  

Ele ataca o caminho  

---

## E isso muda tudo

Porque:

- Você não vê
  
- Você não percebe
  
- Mas está sendo afetado
  
---

## Conclusão

Então voltando pra pergunta do começo  

---

Como alguém pode sequestrar tráfego sem hackear nada?

---

Resposta:

BGP  

---

Então é isso  

Esse foi o **Night Talk 54**

---

E esse aqui mostra uma coisa muito forte  

Na internet  

Quem controla o caminho

Controla o fluxo  

---

Abraços,
**Rian**
