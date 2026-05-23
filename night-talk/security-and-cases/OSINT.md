# Night Talk 58 — OSINT: o que você posta é munição

22 de maio de 2026

(Faz um TEMPÃO que não posto, perdão)

No último talk a gente falou de escovar bit com engenharia reversa, né, mas hoje o papo é sobre algo que vem antes de qualquer exploit

OSINT (Open Source Intelligence)

Que no bom português é: inteligência de fontes abertas

Sabe aquele papo de que "informação é poder"? Na segurança, informação é alvo, tipo, literal

---

## O que é essa parada, direto ao ponto

OSINT é a arte de coletar dados que estão aí, dando sopa na internet, e transformar isso em algo útil pra um ataque (ou pra defesa, né)

Não tem nada de invasão de sistema aqui ainda

**É só saber procurar o que ninguém pensou em esconder**

Pode ser:

- Um post no Linkedin

- Um comentário num fórum de 2012

- Um commit esquecido no GitHub

- Uma foto dos fundos da empresa no Instagram

---

## O erro clássico do "eu não sou importante"

O pessoal tem essa mania de achar que hacker só quer saber de senha, né

Mas ó, imagina que eu quero entrar numa empresa XPTO

Eu não começo tentando quebrar o firewall deles, spammando um yottabyte de phishing pra todos os funcionários

---

**Eu vou no Linkedin:**

- Vejo quem é o sysadmin

- Vejo a stack que ele postou orgulhoso que "acabou de implementar"

- Vou no Instagram dele e vejo uma foto da mesa de trabalho

- No canto da foto, tem o modelo do roteador ou um post-it com o nome de um projeto interno

Pronto, simples assim kkkkkk

Eu já sei o que atacar sem ter mandado UM mísero pacote pro servidor deles

---

E cara, essa parada do Linkedin é **MUITO SÉRIO** tá? É uma rede social bem bem bem problemática mesmo

Tem gente que revela muita coisa sem perceber, porque quer ficar postando que fez tal coisa, que terminou tal projeto

NÃO façam isso, e se forem fazer, façam com moderação e sempre se perguntem:

> "Tem alguma mísera chance de eu deixar meu espaço de trabalho vulnerável com esse post?"

Se depois de muito pensamento, a resposta for não, manda bala no post

Mas sério, toma cuidado

---

## Onde a galera mais vacila

Isso aqui é bizarro, mas acontece MUITO (é sério):

**O crachá no story:**
Tu posta a foto do café e o crachá tá do lado. Alguém printa, replica o QR Code ou o layout e entra na tua empresa andando pela porta da frente, né

**Metadata de foto:**
Tu posta foto do servidor novo, mas esquece que o arquivo da foto tem as coordenadas GPS de onde foi tirada. Parabéns, deu a localização exata do seu DC

**GitHub pessoal:**
O dev sobe um projeto de teste e, sem querer, vai uma chave de API ou um usuário de banco de dados no código. O robô dos caras lê isso em segundos

---

## Por que isso é perigoso pra caralho

_Porque o OSINT é passivo_

O alvo NÃO SABE que está sendo vigiado

Se eu rodo um scan de portas, o firewall apita (se for bom, né)

Se eu fico 2 semanas lendo tudo que você e seus funcionários postam, ninguém nota

É o silêncio antes do estrago absoluto

---

## Como sair do nível amador nisso

Se tu quer ser _bom_ de OSINT, tu tem que virar um stalker profissional, mas com ética, né kkkk

Algumas técnicas básicas:

**Google Dorks:**
Saber usar o Google de verdade. `site:empresa.com filetype:pdf "confidencial"` e sim, isso é real

**Busca Reversa:**
Imagem, e-mail, telefone. Cruzar dados de redes sociais diferentes pra achar o "buraco" na privacidade do cara

**Ferramentas:**

- Maltego (pra ver as conexões)

- Shodan (o Google dos dispositivos conectados, esse aqui dá medo)

- Wayback Machine (pra ver o que o cara apagou, mas a internet não esqueceu)

---

## O Insight de hoje

Privacidade é uma ilusão que a gente alimenta todo dia com um post novo

No mundo do hacking, o técnico é importante, mas o psicológico e a informação estratégica ganham o jogo muito antes do primeiro código rodar

Segurança por obscuridade não funciona, mas exposição desnecessária é pedir pra ser o próximo talk aqui do repo né

---

## Resumo rápido

OSINT = coletar dado público pra virar inteligência

O ataque começa muito antes do código

Rede social é um mapa da mina pra atacante

Se tá na rede, alguém pode usar contra você, e muito provavelmente algum dia vai

---

## Fechamento

Então tipo assim

Antes de sair tentando rodar script de invasão, aprende a ler o que o alvo tá te dizendo de graça

Porque no fim

Quem domina a informação, escolhe o momento certo de atacar né

Esse foi o Night Talk 58

_Nota: Fiquei bastante tempo sem postar pois estava tentando começar outros projetos em parelelo á este, inclusive tentei começar a fazer um hub desse repositório na web, provavelmente no mês de Junho ele funcione bem)_

---

Abraços,
**Rian**
