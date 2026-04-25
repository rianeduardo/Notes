# Night Talk 51 — DNS: o sistema nervoso da internet

**24 de abril de 2026**

Então bora lá né pessoal  

Hoje eu quero começar com uma pergunta bem simples  

---

**Como que a internet sabe pra onde ir?**

---

Tipo  

Tu vai lá e digita:

github.com

---

E simplesmente funciona  

---

Mas como?

---

## Primeiro, o que é DNS

DNS significa:

**Domain Name System**

---

Mas esquece o nome técnico por um segundo  

---

Pensa assim  

---

DNS é tipo a agenda de contatos da internet né, um porteiro do condomínio ali

---

Ele pega:

google.com  

---

E transforma em:

142.250.xxx.xxx  

---

Que é o IP real do servidor  

---

## Sem DNS

Agora pensa nisso  

---

Sem DNS  

---

Você teria que acessar tudo assim:

142.250.xxx.xxx  

Impraticável né, eu nem mexeria no pc se fosse assim 

A internet ainda existiria né  

Mas ninguém saberia chegar nos lugares, e quem soubesse, ia ser uma encheção de saco imensa

---

## O processo (simplificado)

Quando você digita um site  

acontece isso aqui:

---

- Seu dispositivo pergunta: “qual o IP desse domínio?”  

- Um servidor DNS responde  

- Você conecta no IP  

---

Tudo isso em milissegundos  

---

## O detalhe que pouca gente vê

DNS não é um servidor só  

---

É uma hierarquia  

---

Tipo:

- Root servers  

- TLD (.com, .br)  

- Autoritativos  

---

É literalmente um sistema distribuído global  

---

## Cache

Pra não repetir esse processo toda hora  

- Existe cache  

- Seu computador guarda respostas  

- Seu provedor guarda respostas  

- CDNs também  

---

## O resultado

Mais rápido  

Mas tem um detalhe  

---

## TTL (Time To Live)

Toda resposta DNS tem um tempo de vida  

Depois disso precisa consultar de novo  

---

## Isso explica muita coisa

Tipo quando:

- Você muda DNS e não atualiza na hora  

- Um site “fica estranho” por um tempo  

---

Não é bug  

É propagação  

---

## Agora vem a parte pesada

DNS é crítico  

Se DNS falha  

Nada resolve, nada mesmo 

---

## Exemplo real

Você tenta acessar um site  

E dá erro  

Mas o site tá online  

O problema pode ser DNS, e muitas vezes é

---

## Apagões da Cloudflare

Lembra dos apagões da Cloudflare? (Ja fiz talk disso nesse diretório inclusive!)

Muitos deles impactam DNS  

E aí não é só um site que cai  

É meio mundo junto  

---

## DNS também é alvo

Agora vem o lado segurança que eu gosto né

---

Ataques comuns:

- DDoS em servidores DNS
  
- DNS poisoning
  
- Hijacking  

---

## Tradução disso

Você pode:

- Derrubar resolução
  
- Redirecionar usuários
  
- Manipular tráfego  

Sem tocar no servidor real  

---

## Isso é bizarro

Você não hackeia o site  

Você hackeia o caminho até ele  

---

## O insight principal

DNS não é só “tradutor de IP”  

Ele é ponto central de controle  

---

## Se alguém controla DNS…

Pode controlar:

- Para onde você vai
  
- O que você vê
  
- Ou se você vê algo

---

## Conclusão

Então voltando pra pergunta do começo  

---

Como a internet sabe pra onde ir?  

---

Resposta:

DNS  

Mas não é só isso pra conclusão

---

DNS é uma das coisas mais críticas da internet  

E ao mesmo tempo uma das mais ignoradas  

---

Então é isso  

Esse foi o **Night Talk 51**

---

E se você quer entender infra de verdade, começa por aqui  

Porque sem DNS  

A internet ainda existe né, porémmmm

Ninguém acha mais nada  

---

Abraços,
**Rian**
