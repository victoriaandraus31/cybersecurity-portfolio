# Checklist de Conformidade com a LGPD – Flor de Ipê Cosméticos

> Projeto de portfólio em **cenário simulado**: a Flor de Ipê Cosméticos é uma empresa fictícia. O objetivo é mostrar, na prática, como avaliar se uma empresa está em conformidade com a **Lei Geral de Proteção de Dados (Lei nº 13.709/2018)** e montar um plano de adequação.

---

## 1. Contexto

A **Flor de Ipê Cosméticos** é uma empresa do interior de São Paulo que fabrica e vende cosméticos naturais, com **cerca de 60 funcionários** e vendas principalmente pela **loja virtual** e por **marketplaces**.

Este projeto é a continuação da **Matriz de Riscos de TI** da mesma empresa (projeto 2 deste portfólio). Naquela análise, o único risco classificado como **crítico** foi o **vazamento de dados de clientes com sanções da LGPD (R04)**. Por isso, a diretoria pediu uma avaliação detalhada de como a empresa está em relação à lei.

### Quais dados pessoais a empresa trata

| Quem | Quais dados | Para quê |
|---|---|---|
| **Clientes** (cerca de 25 mil) | Nome, CPF, endereço, telefone, e-mail, histórico de compras | Vendas, entrega, nota fiscal, atendimento e marketing |
| **Funcionários** (cerca de 60) | Dados cadastrais, bancários, documentos e atestados de saúde | Contratação, folha de pagamento e obrigações trabalhistas |
| **Fornecedores e parceiros** | Nome e contato dos representantes | Compras e contratos |

## 2. Escopo e objetivo

- **Escopo:** dados pessoais de clientes, funcionários e fornecedores, nos sistemas (ERP, CRM, loja virtual, e-mail), em planilhas, no WhatsApp e em papel.
- **Objetivo:** descobrir o quanto a empresa já cumpre a LGPD, onde estão as principais falhas e o que precisa ser feito primeiro.

## 3. Metodologia

O checklist tem **29 perguntas**, organizadas em **9 temas** da LGPD. Cada pergunta indica o artigo da lei relacionado e recebeu um status:

| Status | Significado | Pontos |
|:---:|---|:---:|
| ✅ Atende | A empresa cumpre o requisito | 1 |
| ⚠️ Atende parcialmente | Existe algo, mas está incompleto ou informal | 0,5 |
| ❌ Não atende | O requisito não é cumprido | 0 |

O **percentual de conformidade** é a soma dos pontos dividida pelo número de perguntas:

| Conformidade | Classificação |
|:---:|---|
| Abaixo de 40% | 🔴 Baixa |
| 40% a 69% | 🟡 Em desenvolvimento |
| 70% ou mais | 🟢 Boa |

## 4. Checklist de conformidade


### 1. Mapeamento dos dados

| ID | Pergunta | Artigo | Status | Situação encontrada |
|---|---|:---:|:---:|---|
| L01 | A empresa sabe quais dados pessoais coleta, onde eles ficam e quem tem acesso? | Art. 37 | ❌ | Não existe mapeamento. Os dados estão espalhados no ERP, no CRM, em planilhas e no WhatsApp. |
| L02 | Existe um registro das atividades de tratamento (o que é feito com cada dado e por quê)? | Art. 37 | ❌ | Não existe registro. |
| L03 | Os dados pessoais sensíveis (como atestados de saúde de funcionários) estão identificados e protegidos? | Art. 11 | ⚠️ | O RH sabe que guarda atestados, mas eles ficam em pasta comum na rede, sem restrição de acesso. |

### 2. Bases legais e consentimento

| ID | Pergunta | Artigo | Status | Situação encontrada |
|---|---|:---:|:---:|---|
| L04 | Cada uso de dados pessoais tem uma base legal definida (contrato, obrigação legal, consentimento etc.)? | Art. 7 | ❌ | Nunca foi feita essa análise. |
| L05 | O consentimento para marketing (e-mail e WhatsApp) é livre, claro e registrado? | Art. 8 | ⚠️ | No site, a caixa de aceite já vem marcada. Pelo WhatsApp, o consentimento não é registrado. |
| L06 | A empresa coleta apenas os dados necessários para cada finalidade? | Art. 6, III | ⚠️ | O cadastro da newsletter pede CPF e data de nascimento, que não são necessários. |

### 3. Transparência e direitos dos titulares

| ID | Pergunta | Artigo | Status | Situação encontrada |
|---|---|:---:|:---:|---|
| L07 | Existe uma política de privacidade publicada, em linguagem clara? | Art. 9 | ✅ | Política publicada no site, em linguagem simples. |
| L08 | Existe um canal para o cliente pedir acesso, correção ou exclusão dos seus dados? | Art. 18 | ⚠️ | Os pedidos chegam pelo SAC, mas não há um fluxo definido para tratá-los. |
| L09 | Os pedidos dos titulares são respondidos dentro do prazo legal (até 15 dias)? | Art. 19 | ❌ | Não há controle de prazo; alguns pedidos ficam sem resposta. |
| L10 | Quando o cliente pede exclusão, os dados são apagados em todos os sistemas? | Art. 18, VI | ⚠️ | O descadastro remove o cliente da newsletter, mas os dados continuam no CRM. |

### 4. Encarregado (DPO)

| ID | Pergunta | Artigo | Status | Situação encontrada |
|---|---|:---:|:---:|---|
| L11 | A empresa nomeou um encarregado pelo tratamento de dados pessoais? | Art. 41 | ❌ | Ninguém foi nomeado. |
| L12 | A identidade e o contato do encarregado estão divulgados no site? | Art. 41, §1º | ❌ | Não há essa informação no site. |

### 5. Segurança da informação

| ID | Pergunta | Artigo | Status | Situação encontrada |
|---|---|:---:|:---:|---|
| L13 | O acesso aos dados de clientes segue o princípio do menor privilégio (cada um vê só o que precisa)? | Art. 46 | ❌ | Todos os atendentes têm o mesmo perfil e podem exportar a base inteira. |
| L14 | Os sistemas com dados pessoais exigem verificação em duas etapas (MFA)? | Art. 46 | ❌ | Nenhum sistema exige MFA. |
| L15 | Os backups são protegidos e testados? | Art. 46 | ⚠️ | Backup diário, mas guardado no mesmo servidor e nunca testado. |
| L16 | Os computadores têm antivírus e atualizações em dia? | Art. 46 | ⚠️ | Antivírus em todas as máquinas, mas as atualizações são irregulares. |
| L17 | É proibido compartilhar planilhas de clientes por canais não autorizados (WhatsApp, e-mail pessoal)? | Art. 46 | ❌ | Planilhas de clientes circulam por WhatsApp e e-mail. |
| L18 | Os acessos de ex-funcionários são bloqueados no desligamento? | Art. 46 | ⚠️ | O RH avisa o TI por e-mail, mas nem sempre. |

### 6. Fornecedores e compartilhamento

| ID | Pergunta | Artigo | Status | Situação encontrada |
|---|---|:---:|:---:|---|
| L19 | Existe uma lista dos fornecedores que tratam dados pessoais em nome da empresa? | Art. 39 | ⚠️ | Os fornecedores são conhecidos (loja virtual, gateway, transportadora, e-mail marketing), mas não há lista formal. |
| L20 | Os contratos com esses fornecedores têm cláusulas de proteção de dados? | Art. 39 | ❌ | Todos usam contrato padrão, sem cláusulas de LGPD. |
| L21 | As transferências de dados para fora do Brasil estão identificadas e amparadas? | Art. 33 | ⚠️ | E-mail e ferramenta de e-mail marketing usam servidores no exterior, sem análise formal. |

### 7. Incidentes de segurança

| ID | Pergunta | Artigo | Status | Situação encontrada |
|---|---|:---:|:---:|---|
| L22 | Existe um plano de resposta a incidentes com dados pessoais? | Art. 48 | ❌ | Não existe plano. |
| L23 | Existe procedimento para comunicar a ANPD e os titulares quando houver incidente relevante? | Art. 48 | ❌ | A empresa não conhece o procedimento nem o prazo (3 dias úteis, segundo a ANPD). |
| L24 | Os incidentes que acontecem são registrados? | Art. 48 | ❌ | Não há registro de incidentes. |

### 8. Retenção e descarte

| ID | Pergunta | Artigo | Status | Situação encontrada |
|---|---|:---:|:---:|---|
| L25 | Existem prazos definidos para guardar cada tipo de dado pessoal? | Arts. 15 e 16 | ❌ | Os dados são guardados para sempre. |
| L26 | O descarte de documentos e equipamentos é feito de forma segura? | Art. 16 | ⚠️ | Papéis vão para a fragmentadora, mas computadores antigos são doados sem apagar os dados com segurança. |

### 9. Treinamento e cultura

| ID | Pergunta | Artigo | Status | Situação encontrada |
|---|---|:---:|:---:|---|
| L27 | Os funcionários recebem treinamento sobre LGPD e proteção de dados? | Art. 50 | ❌ | Nunca houve treinamento. |
| L28 | Existe uma política interna de proteção de dados e de uso de IA? | Art. 50 | ❌ | Não existe política interna. |
| L29 | Os funcionários assinam termo de confidencialidade? | Art. 47 | ✅ | O termo faz parte do contrato de trabalho. |

## 5. Resultado

| Tema | Itens | ✅ | ⚠️ | ❌ | Conformidade |
|---|:---:|:---:|:---:|:---:|:---:|
| 1. Mapeamento dos dados | 3 | 0 | 1 | 2 | 17% – 🔴 Baixa |
| 2. Bases legais e consentimento | 3 | 0 | 2 | 1 | 33% – 🔴 Baixa |
| 3. Transparência e direitos dos titulares | 4 | 1 | 2 | 1 | 50% – 🟡 Em desenvolvimento |
| 4. Encarregado (DPO) | 2 | 0 | 0 | 2 | 0% – 🔴 Baixa |
| 5. Segurança da informação | 6 | 0 | 3 | 3 | 25% – 🔴 Baixa |
| 6. Fornecedores e compartilhamento | 3 | 0 | 2 | 1 | 33% – 🔴 Baixa |
| 7. Incidentes de segurança | 3 | 0 | 0 | 3 | 0% – 🔴 Baixa |
| 8. Retenção e descarte | 2 | 0 | 1 | 1 | 25% – 🔴 Baixa |
| 9. Treinamento e cultura | 3 | 1 | 0 | 2 | 33% – 🔴 Baixa |
| **Total geral** | **29** | **2** | **11** | **16** | **26% – 🔴 Baixa** |

**Em resumo:** a empresa atende **2 de 29** requisitos por completo, atende **11** parcialmente e não atende **16**. A conformidade geral é de **26%**, considerada **baixa**.

Os temas mais críticos, com **0% de conformidade**, são: Encarregado (DPO), Incidentes de segurança.

## 6. Plano de adequação priorizado

As ações foram divididas em três fases, começando pelas que são **rápidas, baratas e reduzem mais o risco**.

### Fase 1 – Primeiros passos (até 30 dias)

| Ação | Itens resolvidos | Responsável |
|---|---|---|
| Nomear um encarregado (DPO) e publicar o contato no site | L11, L12 | Diretoria |
| Ativar a verificação em duas etapas (MFA) nos sistemas com dados pessoais | L14 | TI |
| Proibir o envio de planilhas de clientes por WhatsApp e e-mail pessoal | L17 | TI + Diretoria |
| Reduzir o cadastro da newsletter a nome e e-mail | L06 | Marketing |
| Restringir a pasta do RH com atestados de saúde | L03 | RH + TI |
| Criar o checklist de desligamento entre RH e TI | L18 | RH + TI |
| Criar rotina mensal de atualizações e apagar com segurança os discos de computadores antigos | L16, L26 | TI |

### Fase 2 – Estruturação (até 90 dias)

| Ação | Itens resolvidos | Responsável |
|---|---|---|
| Fazer o mapeamento de dados e o registro das atividades de tratamento, com a base legal de cada uso | L01, L02, L04, L19 | Encarregado + Jurídico + TI |
| Criar um canal e um fluxo para os pedidos dos titulares, com controle do prazo de 15 dias | L08, L09, L10 | Encarregado + SAC |
| Corrigir a coleta de consentimento para marketing no site e no WhatsApp | L05 | Marketing + TI |
| Criar perfis de acesso por função (menor privilégio) e backup 3-2-1 testado | L13, L15 | TI |
| Criar o plano de resposta a incidentes, com o procedimento de comunicação à ANPD e o registro de incidentes | L22, L23, L24 | Encarregado + TI |
| Publicar a política interna de proteção de dados e de uso de IA e fazer o primeiro treinamento | L27, L28 | Encarregado + RH + TI |

### Fase 3 – Consolidação (até 180 dias)

| Ação | Itens resolvidos | Responsável |
|---|---|---|
| Assinar aditivos de proteção de dados com os fornecedores | L20 | Jurídico |
| Avaliar e registrar as transferências de dados para fora do Brasil | L21 | Jurídico + TI |
| Criar a tabela de temporalidade (quanto tempo guardar cada dado) | L25 | Encarregado + Jurídico |
| Atualizar a política de privacidade com base no mapeamento | L07 | Jurídico |

## 7. Conclusão

A Flor de Ipê Cosméticos já deu alguns passos, como ter **política de privacidade publicada** e **termo de confidencialidade** com os funcionários, mas ainda está no começo da adequação à LGPD. Os pontos mais urgentes são a **falta de um encarregado**, o **desconhecimento sobre onde estão os dados pessoais** e a **ausência de um plano para incidentes**. Juntos, eles explicam por que o vazamento de dados de clientes apareceu como risco crítico na matriz de riscos.

A boa notícia é que a Fase 1 pode ser feita em um mês, com ações simples e de baixo custo. Com as três fases concluídas, a empresa passa a ter **governança de dados pessoais**: sabe quais dados tem, por que os usa, quem é responsável por eles e como agir se algo der errado.

## 8. Competências demonstradas

`LGPD (Lei nº 13.709/2018)` · `Avaliação de conformidade` · `Mapeamento de dados` · `Bases legais` · `Direitos dos titulares` · `Gestão de incidentes` · `Gestão de fornecedores` · `Plano de adequação` · `Governança de dados` · `Controles internos`
