# Estudo de Segurança: Exposição e Reidentificação de CPF

## 1. Objetivo

Estudo independente realizado ao longo de aproximadamente dois meses, investigando exposição de dados pessoais e falhas de mascaramento em plataformas digitais.

Foram avaliadas quatro plataformas entre Financeiras e Telecomunicações, identificando comportamentos que permitem correlacionar informações parcialmente ocultas e investigar riscos de reidentificação. Mais de 100 registros foram analisados durante a pesquisa.

## 2. Vulnerabilidade identificada

Em uma plataforma de telecomunicações, foi identificado um cenário em que informações cadastrais associadas aos clientes poderiam ser disponibilizadas durante fluxos de contratação ou compra.
<img width="1125" height="481" alt="image" src="https://github.com/user-attachments/assets/f563a9f4-cf08-4670-8954-1d5d9fe05f67" />
A análise também identificou uma possível combinação de informações entre uma plataforma financeira e uma plataforma de telecomunicações, cujos mecanismos de mascaramento expõem segmentos diferentes do CPF.

O aspecto mais crítico investigado é a possibilidade de consultar registros de diferentes titulares e obter informações cadastrais sem autorização adequada, caso a falha de controle de acesso seja confirmada.

## 3. Impacto e severidade estimada

A exploração desse cenário poderia comprometer a confidencialidade de dados pessoais, incluindo CPF e nome completo, com potencial impacto sobre uma quantidade expressiva de titulares.

**Dado possibilidade de consultar CPFs de terceiros diretamente nos sistemas da empresa de telecomunicações, sem autorização, o cenário poderá ser classificado como de severidade ALTA (CVSS 7.0–8.9)**, dependendo das condições de exploração e do impacto comprovado.

### Exemplo de exposição por correlação de dados

Durante a pesquisa, foi identificado um cenário envolvendo duas plataformas de segmentos distintos, uma financeira e outra de telecomunicações, que apresentavam diferentes partes de um mesmo identificador pessoal.

Exemplo ilustrativo dos padrões observados:

- **Plataforma A — Telecomunicações:** `123.***.***-99`
- **Plataforma B — Financeira:** `***.456.789-**`

Cada plataforma ocultava segmentos diferentes do CPF. A correlação dessas informações demonstrou um risco de reidentificação, pois dados que individualmente pareciam parcialmente protegidos poderiam, em conjunto, revelar o identificador completo.

O aspecto mais crítico da investigação foi a possibilidade de exposição de registros de um banco de dados vindo diretamente no console.

<text color="secondary" size="xs">Os valores apresentados são fictícios e servem exclusivamente para demonstrar o padrão de mascaramento, sem divulgar identificadores reais.</text>

**Nota:** a classificação apresentada é uma estimativa preliminar. A pontuação CVSS depende da validação técnica da vulnerabilidade; a atribuição de um CVE é um processo independente.

## 4. Escopo e responsabilidade

Este material possui finalidade exclusivamente educacional e de conscientização sobre segurança da informação e privacidade.

Os exemplos foram anonimizados. Não são publicados CPFs reais, credenciais, dados de sessão ou instruções para obtenção de informações de terceiros.

A pesquisa não autoriza acesso não permitido a sistemas ou dados pessoais. Eventuais vulnerabilidades devem ser comunicadas aos responsáveis por meio de canais apropriados de divulgação responsável.
