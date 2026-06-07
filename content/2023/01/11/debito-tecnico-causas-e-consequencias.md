---
title: "Débito Técnico, Causas e Consequências"
date: 2023-01-11
draft: false
tags: ["Software", "Engenharia de Software", "SCRUM", "Boas Práticas", "Gestão"]
categories: ["Software"]
description: "Uma visão geral sobre o débito técnico no desenvolvimento de software: o que é, suas principais causas e como calcular e gerenciar essa dívida ao longo do tempo."
cover:
  image: "https://blogger.googleusercontent.com/img/a/AVvXsEjXoVPptLKByOo9hqeh83IJi3R4YuBFFlPXfj5a36kN42xYIgRPGEn8YTaELcQurmtpWmmMqm0uAlfWNhnUk3oFtRx___Li2kdD--D5MQYTt1o-IbndX4TyWKQZB7LFMHLVMtlMh4nm4ab1_Kn8yUVe2Ux86FLsGXkf_cFhtx-mSIgDjWIgBeyZQqgO"
  alt: "Débito técnico"
canonical: "https://ronymarcolino.blogspot.com/2023/01/debito-tecnico-causas-e-consequencias.html"
---

O conceito de débito técnico tem seu uso mais comum no desenvolvimento de software, mas tem sua origem no mercado financeiro quanto aos efeitos dos juros sobre operações de empréstimos ao longo prazo.

Mas afinal, o que é o débito técnico no desenvolvimento de software?

Do inglês *technical debt*, o débito técnico diz respeito aos resultados de ações tomadas pelas equipes de desenvolvimento para agilizar a entrega de uma funcionalidade ou recurso do projeto e que por algum motivo precise ser refatorado no futuro.

## Principais Causas do Débito Técnico

### Atalhos

Pegar um atalho no desenvolvimento de software significa que o seu código alcança apenas o mínimo de requisitos para ser aceito no processo. Ninguém pode negar que em algum momento os gerentes podem fazer algum tipo de concessão e permitir pegar um atalho. Dada a pressão para se realizar uma entrega a tempo, os atalhos podem ser tentadoras e perigosas opções a serem tomadas se não atentarem para as consequências.

### Bibliotecas e *Frameworks* Desatualizados

Todos os desenvolvedores usam códigos que eles mesmos não escreveram (graças à comunidade e à cultura de código aberto ao redor do mundo). Utilizamos bibliotecas e *frameworks* para tornar a construção de software mais fácil, mais rápida e mais eficiente em termos de custo. Isso também cria um desafio: manter o código de terceiros.

Os desenvolvedores podem ter vários tipos de problemas com uma biblioteca, como documentação incompleta, falta de respostas pelo mantenedor e respostas desdenhosas. O projeto pode ser mal mantido ao longo do tempo e representar problemas para a manutenção ou expansão da própria funcionalidade envolvida. O que parecia eficiente e proveitoso no início pode criar bloqueios na trilha do desenvolvimento a longo prazo. A substituição ou revisão de tais componentes pode levar meses e criar um entrave no desenvolvimento das funcionalidades do seu produto.

### Desenvolvimento de Novos Produtos

Você está ansioso para construir esse novo recurso. Seus desenvolvedores apontam que a atual capacidade de produção não está realmente pronta para receber toda essa complexidade.

Para ser honesto com as partes interessadas, muitas vezes não temos certeza se esse recurso será um diferencial real. Geralmente, a tendência é ir por atalhos ou fazer alguns *hacks* no código para fazer acontecer sem grandes investimentos iniciais. Promete-se a todos que esses atalhos serão gerenciados no futuro quando o recurso der retorno.

![Networking](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh58pBCB608wYl9vHCupXRGsd8_MY2b9fCiG01-SOvdIkvkA5-iBTjsN62uJPiRzaUfrW2pVZ02GLkFZttcZ53Qni2MzHeGFWwEfEtPpfkS3YPdbAQ8ADmSfoyOd26Fs2q0rhZFCz_qVGRk8K0jKEwSiq1g8HaDoNSswua6IfQhF9sAb4oD9nlayW9S/s1200/Networking.jpg)

Além disso, seus desenvolvedores provavelmente precisarão de mais recursos de hardware. Servidores locais não escalam, então a migração para a nuvem (AWS ou similar) cria ainda mais desafios de implantação e migrações.

### Serviços de Terceiros

Vivemos em um mundo totalmente interligado e as tecnologias ainda mais. Um oceano de APIs parceiras precisa se comunicar entre si e o nosso sistema está incluído nessa lista.

Em algum momento bem inoportuno, seu parceiro lhe enviará um e-mail dizendo: *"Estamos melhorando nosso sistema e vamos depreciar a API xpto. Deixaremos de apoiá-los a partir da data X"*. Você não terá outra escolha: coloque isso no seu backlog, planeje o tempo de atualização e siga em diante.

## Como Determinar o Montante da Dívida Técnica

Não existe uma fórmula mágica para calcular o volume da dívida técnica. A razão é simples: para cada implementação ou mudança no sistema podemos ter diferenças no tempo ou nos recursos necessários. Mas podemos traçar alguns passos para estimar a dívida técnica:

![Comunicação em equipe](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhNujJ44ml71k69nyPWPMuFkFHApr4Utknl0Gw3IHBOyPoh4QSo9cA2Ap-l1u-bHgxs2b6iOsVhJm8yKodNur3CCOtbtRRMhfLvDHVfrp8gi48xqxPzplsTamLSUXPwrbE7EuW5uJIPcrpQogYvhmXdX13Jk7cvX9UXGNr9UIvHObz_TIGSIHvLOA3R/s1600/image-communication.jpeg)

### Passo 1: Crie um épico no SCRUM para calcular a dívida

A fim de criar visibilidade, crie um épico para a dívida técnica. Coloque aqui todas as histórias sobre as dívidas levantadas até então. Se ela se aplica a uma *feature* específica, você também pode apenas anexar as histórias de dívidas específicas à épica daquela *feature*. Anexar uma história a vários épicos garante que você possa ter uma visão total do débito e uma visão do débito ao nível de *features* a qualquer momento.

### Passo 2: *Spikes* primeiro, depois as histórias

Como a dívida técnica está dentro do seu sistema — principalmente em um nível técnico mais profundo — você precisará definir e clarificar a dívida real a fim de criar histórias. Histórias que não são 100% claras para sua equipe nunca devem passar de um sprint.

A resposta é: criar **Spikes**. Eles se parecem com histórias, mas sem pontos de história. Em vez disso, têm um tempo definido alocado (ex.: 5 horas para investigar X) e seu principal objetivo é investigar para esclarecer o que precisa ser feito. O resultado de um Spike é uma história.

É importante se livrar de todos os Spikes o mais cedo possível. Você e sua equipe precisam esclarecer a escala completa da dívida e estimá-la na primeira sessão de planejamento seguinte. Todos os pontos de história estimados combinados darão o número total da dívida.

### Passo 3: Faça ajustes no seu roteiro e considere os prazos

O próximo passo é planejar a dívida para execução a curto prazo e incorporar a redução da dívida técnica no roteiro de longo prazo. Em resumo, será como pagar uma dívida de empréstimo ao banco.

Não se deixe enganar: você sempre criará novas dívidas. O monitoramento da dívida técnica não é um exercício único, mas uma etapa que sempre acontece dentro do DNA da sua operação.

### Passo 4: Comunique aos interessados

Agora que todas as dívidas técnicas foram mapeadas e incorporadas na operação, é hora de se comunicar com as partes interessadas. O grupo mais importante será a alta administração, já que eles estão pagando a conta desta dívida. O mais importante é explicar como isso afetará a organização e, principalmente, seus clientes. Um segundo ponto a comunicar é como isso afetará a velocidade do desenvolvimento do produto.

Não é preciso aborrecê-los com toda a história do "o que é dívida técnica". Basta explicar os pontos-chave para que eles saibam a que você está se referindo em comunicações futuras.

![Sucesso](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhH44N1gaZZMvTuBP-5u8DbnDQp5V83KQ2-7R_tOFlKQ_FSyhTb355OC5iwIuWXJs6zS8xSaR_3MJiOFwghzUzt8c7lUaYwgAsbhAzDMgeDVgqdo0m_DM0vrUoLQR-8zziJJutErkmiqvwmGop4OZB3eJ_KBHyytPEULfNd_tRGUpVh3GIb3MGSzYk6/s600/Sucess.png)

## Referências

- [Cloudster — Débito Técnico](https://cloudster.com.br/blog/debito-tecnico/)
- [Melv1n — What is Technical Debt?](https://melv1n.com/what-is-technical-debt/)
