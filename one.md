# Estudo de Segurança: Exposição e Reidentificação de CPF

## 1. Objetivo

Estudo independente realizado ao longo de aproximadamente dois meses, investigando exposição de dados pessoais e falhas de mascaramento em plataformas digitais.

Foram avaliadas quatro plataformas, identificando comportamentos que permitem correlacionar informações parcialmente ocultas e investigar riscos de reidentificação. Mais de 100 registros foram analisados durante a pesquisa.

## 2. Vulnerabilidade identificada

Em uma plataforma de telecomunicações, foi identificado um cenário em que informações cadastrais associadas aos clientes poderiam ser disponibilizadas durante fluxos de contratação.

A análise também identificou uma possível combinação de informações entre uma plataforma financeira e uma plataforma de telecomunicações, cujos mecanismos de mascaramento expõem segmentos diferentes do CPF.

O aspecto mais crítico investigado é a possibilidade de consultar registros de diferentes titulares e obter informações cadastrais sem autorização adequada, caso a falha de controle de acesso seja confirmada.

## 3. Impacto e severidade estimada

A exploração desse cenário poderia comprometer a confidencialidade de dados pessoais, incluindo CPF e nome completo, com potencial impacto em uma quantidade expressiva de titulares.

**Com a possibilidade de consultar CPFs de terceiros diretamente nos sistemas da empresa, sem autorização, a vulnerabilidade poderia receber classificação de severidade ALTA (CVSS 7.0–8.9), dependendo dos vetores de exploração e do impacto comprovado.**

Essa é uma estimativa preliminar, não uma pontuação oficial nem garantia de atribuição de CVE.

## 4. Escopo e responsabilidade

Este material possui finalidade exclusivamente educacional e de conscientização sobre segurança da informação e privacidade.

Os exemplos foram anonimizados. Não são publicados CPFs reais, credenciais, dados de sessão ou instruções para obtenção de informações de terceiros.

A pesquisa não autoriza acesso não permitido a sistemas ou dados pessoais. Eventuais vulnerabilidades devem ser comunicadas aos responsáveis por meio de canais apropriados de divulgação responsável.
