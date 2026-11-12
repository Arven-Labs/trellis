# Arven Code — ideia inicial e pesquisa de base tecnológica

> Documento complementar. Registra apenas as ideias novas discutidas sobre uma possível plataforma de colaboração em código da Arven Labs.
## 1. Conceito

Explorar uma plataforma de desenvolvimento open source inspirada no GitHub, mas alinhada aos objetivos da Arven Labs: soberania digital, interoperabilidade e redução da dependência de plataformas centralizadas.

Nome de trabalho: **Arven Code**. O nome ainda não está decidido.

A ideia não é reimplementar Git, issues, pull requests e todo o ecossistema de desenvolvimento do zero. A primeira etapa deve ser estudar projetos open source existentes e escolher uma base que permita validar a proposta com menos trabalho.

## 2. Princípio principal

**Reutilizar a infraestrutura existente e desenvolver somente o diferencial necessário.**

Uma alternativa ao GitHub não precisa começar como uma plataforma totalmente nova. É possível aproveitar um forge existente para os recursos tradicionais e investir gradualmente em identidade soberana, verificabilidade, interoperabilidade e, caso exista uma necessidade concreta, descentralização adicional.

É importante não confundir:
- **Self-hosted:** a instância é operada por quem a administra, mas continua sendo um servidor central para seus usuários.
- **Descentralizado/P2P:** repositórios e colaboração podem ser replicados entre diferentes participantes, reduzindo a dependência de uma instância específica.
- **Código aberto:** permite estudar, modificar e hospedar o software, mas não torna automaticamente a rede descentralizada.

## 3. Bases que vale investigar

### Opção A — Gitea

Site: https://about.gitea.com/  
Código-fonte: https://github.com/go-gitea/gitea

**Por que avaliar**
- Já oferece recursos comuns de uma plataforma de colaboração em código, como repositórios Git, issues, pull requests, permissões e integrações.
- Permite partir de uma experiência familiar para desenvolvedores.
- Pode acelerar a criação de uma primeira versão utilizável.

**Limitação importante**
O Gitea é uma plataforma self-hosted, não uma rede P2P nativa. Hospedar uma instância própria dá controle operacional, mas não resolve por si só replicação distribuída nem elimina a dependência do servidor da instância.

**Hipótese de uso**
Usar Gitea como base de uma versão inicial, caso a prioridade seja lançar rapidamente um serviço web familiar e explorar personalização e integrações.

### Opção B — Radicle

Site: https://radicle.dev/  
Código-fonte: https://github.com/radicle-dev

**Por que avaliar**
- É focado em colaboração de código descentralizada, baseada em Git e comunicação P2P.
- Investiga problemas mais próximos da soberania dos repositórios e da replicação entre participantes.
- Pode evitar a necessidade de inventar um protocolo de colaboração descentralizada do zero.

**Limitação importante**
A experiência, o fluxo de trabalho e a maturidade para o público pretendido precisam ser avaliados na prática. Não se deve presumir que substitua diretamente todas as funções, integrações e conveniências do GitHub.

**Hipótese de uso**
Considerar Radicle se o objetivo principal for uma rede P2P de colaboração, e não apenas uma instância web autogerida.

### Opção C — Abordagem híbrida ou evolutiva

Investigar se faz sentido começar com uma forge tradicional e, ao mesmo tempo, manter aberta a possibilidade de integrar protocolos de replicação e colaboração descentralizada.

Essa opção não deve ser presumida como simples: a interoperabilidade entre plataformas e protocolos precisa ser demonstrada, não apenas desenhada no papel.

## 4. Diferencial potencial da Arven Code

O projeto só justificaria existir como iniciativa própria se oferecesse valor claro além de uma instalação personalizada de Gitea ou de uma interface para Radicle.

Possíveis linhas de investigação:

1. **Identidade portátil:** explorar integração com TruthID para autenticação e identidade entre serviços, evitando criar um segundo sistema de identidade.
2. **Autoria e verificabilidade:** facilitar a verificação de assinaturas, autoria de commits, releases e proveniência de software.
3. **Interoperabilidade:** permitir que projetos e desenvolvedores não dependam exclusivamente de uma única plataforma ou interface.
4. **Agentes de desenvolvimento:** no futuro, o Warden poderia ajudar a encontrar projetos, analisar issues, preparar patches e auxiliar em revisões. Ações com impacto real precisariam de permissões limitadas, trilhas de auditoria e aprovação adequada.
5. **Financiamento de open source:** explorar doações, recompensas por issues ou financiamento transparente somente se houver um caso de uso claro. Blockchain e tokens não devem ser adicionados apenas para caracterizar o projeto como Web3.

Esses pontos são hipóteses, não requisitos fechados nem compromissos de implementação.

## 5. Relação com o ecossistema Arven

- **TruthID:** identidade e autenticação portáteis. Não criar outro SDK de identidade apenas para a plataforma.
- **Warden:** possível assistência automatizada ao desenvolvimento, com acesso controlado.
- **Arven Code:** eventual ambiente de colaboração e descoberta de projetos.

A integração entre os projetos deve ser útil e opcional sempre que possível. A Arven Code não deve exigir que todo desenvolvedor use os outros produtos da Arven para colaborar.

## 6. O que evitar

- Recriar Git, issues, pull requests e CI/CD sem uma razão concreta.
- Criar uma blockchain própria ou um token apenas para dizer que a plataforma é Web3.
- Confundir hospedagem própria com descentralização.
- Criar uma nova identidade quando TruthID já atende a essa função.
- Começar com uma arquitetura complexa de nós, relays e incentivos antes de validar a necessidade.
- Construir uma plataforma inteira antes de testar se desenvolvedores realmente querem usá-la.
- Assumir que uma interface nova, por si só, resolve o efeito de rede e a descoberta de projetos.

## 7. Plano de investigação

### Etapa 1 — Comparar as bases

Testar Gitea e Radicle com tarefas reais:
- criar e clonar um repositório;
- abrir e revisar uma contribuição;
- gerenciar issues;
- configurar permissões e identidades;
- verificar assinaturas e histórico;
- fazer backup e recuperar os dados;
- avaliar a experiência de quem contribui de fora;
- verificar quais recursos dependem de um servidor central;
- avaliar documentação, manutenção, licenciamento e integrações.

### Etapa 2 — Definir o objetivo

Responder antes de escolher uma arquitetura:

- A prioridade é um **site acessível pelo navegador**, com uma experiência familiar e identidade mais soberana?
- Ou é uma **rede P2P**, na qual os participantes podem replicar repositórios e colaborar sem depender de um servidor central?
- A primeira versão precisa ser compatível com fluxos existentes de Git e ferramentas populares?
- Qual problema real a Arven Code resolve que Gitea ou Radicle, sozinhos, não resolvem?

### Etapa 3 — Validar um diferencial pequeno

Escolher um único diferencial que possa ser demonstrado em uma prova de conceito, como integração opcional com TruthID ou verificação de autoria e releases. Evitar construir várias camadas ao mesmo tempo.

### Etapa 4 — Decidir se vale manter um projeto próprio

Se a necessidade for atendida por configuração, plugins ou contribuições a um projeto existente, preferir esse caminho. Criar uma plataforma própria somente quando houver uma lacuna clara, útil a terceiros e difícil de resolver contribuindo diretamente para a base existente.

## 8. Critério provisório de decisão

- **Gitea:** investigar primeiro se a meta é lançar rapidamente uma experiência web de colaboração familiar.
- **Radicle:** investigar primeiro se a meta central é colaboração P2P e maior independência de servidores centrais.
- **Abordagem híbrida:** considerar apenas depois de comprovar a compatibilidade e o valor da integração.

Ainda não há decisão final de tecnologia. O próximo passo é estudar e testar as opções, não começar a implementação de uma plataforma completa.
