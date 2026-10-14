# Matriz de Riscos de TI – Flor de Ipê Cosméticos

> Projeto de portfólio em **cenário simulado**: a Flor de Ipê Cosméticos é uma empresa fictícia. O objetivo é mostrar, na prática, como identificar, avaliar e tratar riscos de TI usando como base a **ISO 31000**, a **ISO/IEC 27005** e o **NIST SP 800-30**.
---

## 1. Contexto da empresa

A **Flor de Ipê Cosméticos** é uma empresa do interior de São Paulo que fabrica e vende cosméticos naturais. Tem **cerca de 60 funcionários** e vende principalmente pela **loja virtual** e por **marketplaces**, com uma pequena loja física.

Alguns números e características importantes:

- Cerca de **25 mil clientes cadastrados**, com nome, CPF, endereço, telefone e histórico de compras. Por isso, a empresa precisa seguir a **LGPD**.
- A área de TI tem **apenas 2 pessoas**, que cuidam de tudo: computadores, sistemas, acessos e suporte.
- Sistemas usados no dia a dia:
  - **ERP** (estoque, faturamento e notas fiscais), instalado em um servidor dentro da empresa;
  - **Loja virtual** em uma plataforma terceirizada;
  - **E-mail e arquivos** no Microsoft 365;
  - **CRM** e **WhatsApp Business** para o atendimento;
  - **Gateway de pagamento** e contas da marca nas **redes sociais**.

Nos últimos dois anos, as vendas online cresceram rápido, mas os controles de segurança não acompanharam esse crescimento. A diretoria pediu uma análise de riscos para saber **onde investir primeiro**.

## 2. Escopo e objetivo

- **Escopo:** sistemas, dados, pessoas, processos e fornecedores ligados à operação de TI da empresa.
- **Fora do escopo:** riscos financeiros do negócio (como câmbio ou crédito) e a segurança da fábrica.
- **Objetivo:** identificar os principais riscos de TI, entender quais são mais graves e propor um plano de ação priorizado, com responsáveis e prazos.

## 3. Metodologia

Cada risco foi descrito em uma frase com **causa → evento → consequência**, para ficar claro *por que* ele existe e *o que* pode acontecer.

Depois, cada risco recebeu duas notas de 1 a 5:

| Nota | Probabilidade (chance de acontecer) | Impacto (tamanho do estrago) |
|:---:|---|---|
| 1 | Rara – menos de uma vez a cada 5 anos | Insignificante – quase não afeta a operação |
| 2 | Improvável – uma vez a cada 2 a 5 anos | Menor – interrupção curta, pequena perda |
| 3 | Possível – cerca de uma vez por ano | Moderado – serviço importante parado por horas |
| 4 | Provável – algumas vezes por ano | Maior – sistema crítico parado por dias ou vazamento de dados |
| 5 | Quase certa – todo mês ou já acontecendo | Catastrófico – negócio parado, vazamento grande, sanções da ANPD |

O **nível de risco** é a multiplicação **Probabilidade × Impacto**:

| Nível | Classificação | O que fazer |
|:---:|---|---|
| 1 a 4 | 🟢 Baixo | Acompanhar |
| 5 a 9 | 🟡 Médio | Tratar no planejamento normal |
| 10 a 16 | 🟠 Alto | Tratar com prioridade |
| 20 a 25 | 🔴 Crítico | Agir imediatamente e reportar à diretoria |

Para cada risco foi escolhido um **tratamento**:

- **Mitigar:** colocar controles para diminuir a chance ou o estrago.
- **Aceitar:** o risco é pequeno ou tratar custaria mais do que ele.
- **Transferir:** passar parte do risco para outra empresa, por exemplo por contrato ou seguro.
- **Evitar:** deixar de fazer a atividade que gera o risco.

Por fim, foi estimado o **risco residual**, ou seja, como cada risco deve ficar **depois** que a ação for feita.

## 4. Matriz de riscos

### 4.1 Riscos identificados

| ID | Risco | Ativo | Categoria | Controles atuais | P | I | Nível |
|---|---|---|---|---|:---:|:---:|:---:|
| R01 | Como o e-mail não exige verificação em duas etapas (MFA), um funcionário que caia em phishing pode ter a senha roubada, e o golpista acessa pedidos e dados de clientes. | E-mail (Microsoft 365) | Tecnologia | Antivírus; filtro de spam | 4 | 4 | 🟠 16 |
| R02 | Como os backups ficam no mesmo servidor e algumas máquinas estão desatualizadas, um ransomware pode travar o ERP e os backups juntos, parando vendas por dias. | Servidor do ERP e backups | Tecnologia | Antivírus; backup diário no próprio servidor | 3 | 5 | 🟠 15 |
| R03 | Como todos os atendentes usam o mesmo perfil no ERP e no CRM, qualquer um pode ver e exportar a base inteira de clientes. | ERP e CRM | Processos | Login individual | 4 | 4 | 🟠 16 |
| R04 | Como não há mapeamento de dados pessoais e planilhas de clientes circulam por e-mail e WhatsApp, um vazamento pode expor 25 mil clientes e gerar sanções da LGPD. | Base de clientes | Conformidade | Política de privacidade no site | 4 | 5 | 🔴 20 |
| R05 | Como o contrato da loja virtual não tem SLA, uma queda na Black Friday pode causar grande perda de vendas. | Loja virtual (terceirizada) | Fornecedores | Contrato padrão | 3 | 4 | 🟠 12 |
| R06 | Como o RH não avisa o TI de forma padronizada sobre desligamentos, ex-funcionários podem manter acesso aos sistemas. | Contas de usuários | Processos | Aviso por e-mail, quando lembrado | 3 | 3 | 🟡 9 |
| R07 | Como as senhas das redes sociais, do marketplace e do gateway são fracas e ficam numa planilha compartilhada, alguém de fora pode invadir e aplicar golpes em nome da marca. | Redes sociais, marketplace e gateway | Pessoas | Nenhum | 4 | 4 | 🟠 16 |
| R08 | Como o ERP roda em um servidor antigo e sem garantia, uma falha pode deixar a empresa sem emitir notas fiscais. | Servidor do ERP | Tecnologia | Nobreak; técnico chamado sob demanda | 2 | 4 | 🟡 8 |
| R09 | Como não há regras para o uso de IA generativa, funcionários podem colar dados de clientes em ferramentas públicas. | Dados de clientes e informações internas | Pessoas | Nenhum | 4 | 3 | 🟠 12 |
| R10 | Quedas de energia curtas podem interromper o trabalho por alguns minutos. | Escritório e equipamentos | Física | Nobreak no servidor e na rede | 2 | 2 | 🟢 4 |

### 4.2 Tratamento de cada risco

| ID | Tratamento | Ação proposta | Responsável | Prazo | Residual |
|---|---|---|---|---|:---:|
| R01 | Mitigar | Ativar MFA para todos e fazer treinamento de phishing a cada semestre | Coordenação de TI | 30 dias | 🟡 6 |
| R02 | Mitigar | Backup 3-2-1 (com cópia fora da empresa e offline), teste mensal de restauração e rotina de atualizações | Coordenação de TI | 60 dias | 🟡 6 |
| R03 | Mitigar | Perfis de acesso por função (menor privilégio) e revisão de acessos a cada 3 meses | TI + gestores de área | 60 dias | 🟡 6 |
| R04 | Mitigar | Mapear os dados pessoais, nomear um encarregado (DPO), proibir planilhas de clientes no WhatsApp e criar plano de resposta a incidentes | Diretoria + Jurídico + TI | 90 dias | 🟡 8 |
| R05 | Transferir | Renegociar o contrato com SLA e multa por indisponibilidade e criar um plano de contingência para datas de pico | Diretoria Comercial + TI | 90 dias | 🟡 6 |
| R06 | Mitigar | Checklist de desligamento entre RH e TI, com bloqueio dos acessos no último dia | RH + TI | 30 dias | 🟢 3 |
| R07 | Mitigar | Gerenciador de senhas corporativo, troca de todas as senhas e MFA nessas contas | TI + Marketing | 30 dias | 🟢 4 |
| R08 | Mitigar | Avaliar migração do ERP para a nuvem ou contratar manutenção com prazo garantido | TI + Financeiro | 120 dias | 🟢 4 |
| R09 | Mitigar | Publicar uma política de uso de IA, indicar ferramentas aprovadas e orientar as equipes | TI + RH | 45 dias | 🟢 4 |
| R10 | Aceitar | Manter o nobreak e verificar as baterias uma vez por ano | Coordenação de TI | Contínuo | 🟢 4 |

## 5. Mapa de calor

O mapa mostra onde cada risco está, cruzando **probabilidade** (linhas) e **impacto** (colunas). Quanto mais para o canto superior direito, mais grave o risco.

**Legenda:** 🟢 Baixo · 🟡 Médio · 🟠 Alto · 🔴 Crítico

### Antes do tratamento

| Probabilidade ↓ / Impacto → | 1 Insignificante | 2 Menor | 3 Moderado | 4 Maior | 5 Catastrófico |
|---|:---:|:---:|:---:|:---:|:---:|
| **5 Quase certa** | 🟡 | 🟠 | 🟠 | 🔴 | 🔴 |
| **4 Provável** | 🟢 | 🟡 | 🟠 R09 | 🟠 R01, R03, R07 | 🔴 R04 |
| **3 Possível** | 🟢 | 🟡 | 🟡 R06 | 🟠 R05 | 🟠 R02 |
| **2 Improvável** | 🟢 | 🟢 R10 | 🟡 | 🟡 R08 | 🟠 |
| **1 Rara** | 🟢 | 🟢 | 🟢 | 🟢 | 🟡 |

### Depois do tratamento

| Probabilidade ↓ / Impacto → | 1 Insignificante | 2 Menor | 3 Moderado | 4 Maior | 5 Catastrófico |
|---|:---:|:---:|:---:|:---:|:---:|
| **5 Quase certa** | 🟡 | 🟠 | 🟠 | 🔴 | 🔴 |
| **4 Provável** | 🟢 | 🟡 | 🟠 | 🟠 | 🔴 |
| **3 Possível** | 🟢 | 🟡 | 🟡 | 🟠 | 🟠 |
| **2 Improvável** | 🟢 | 🟢 R07, R09, R10 | 🟡 R01, R02, R03, R05 | 🟡 R04 | 🟠 |
| **1 Rara** | 🟢 | 🟢 | 🟢 R06 | 🟢 R08 | 🟡 |

### Resumo

| Classificação | Antes do tratamento | Depois do tratamento |
|---|:---:|:---:|
| 🔴 Crítico | 1 | 0 |
| 🟠 Alto | 6 | 0 |
| 🟡 Médio | 2 | 5 |
| 🟢 Baixo | 1 | 5 |
| **Total** | **10** | **10** |

## 6. Plano de ação priorizado

As ações foram agrupadas pelo que resolvem e ordenadas pela gravidade dos riscos.

1. **Proteger os dados dos clientes e cumprir a LGPD** (R04, R03, R09) – *até 90 dias*
   Mapear quais dados pessoais a empresa guarda e onde, nomear um encarregado de dados, limitar o acesso de cada pessoa ao que ela precisa para trabalhar e criar regras para o uso de IA. É a prioridade número 1 porque envolve o único risco **crítico** e pode gerar multas e perda de confiança na marca.

2. **Fechar as portas de entrada mais usadas por golpistas** (R01, R07) – *até 30 dias*
   Ativar a verificação em duas etapas (MFA), adotar um gerenciador de senhas e treinar a equipe para reconhecer phishing. São ações **rápidas e baratas** que reduzem muito o risco.

3. **Garantir que a empresa volte a funcionar depois de um ataque ou falha** (R02, R08) – *até 120 dias*
   Ter um backup separado e testado e resolver a dependência do servidor antigo do ERP.

4. **Reduzir a dependência de fornecedores em datas de pico** (R05) – *até 90 dias*
   Incluir no contrato da loja virtual garantias de disponibilidade e ter um plano B para a Black Friday.

5. **Organizar a saída de funcionários** (R06) – *até 30 dias*
   Criar um checklist simples entre RH e TI para bloquear os acessos no último dia de trabalho.

## 7. Conclusão

A análise mostrou que a Flor de Ipê Cosméticos tem **1 risco crítico e 6 riscos altos**, quase todos ligados a três pontos: **dados de clientes desprotegidos**, **acessos sem controle** e **falta de um backup confiável**. Se nada for feito, a empresa fica exposta a vazamento de dados, sanções da LGPD, golpes em nome da marca e paradas nas vendas.

A boa notícia é que boa parte das soluções é **simples e de baixo custo**, como MFA, gerenciador de senhas, perfis de acesso, checklist de desligamento e treinamento das equipes. Com o plano de ação, **nenhum risco fica crítico ou alto**: todos passam para médio ou baixo, e a empresa ganha uma base mais segura para continuar crescendo.

## 8. Competências demonstradas

`Gestão de riscos de TI` · `ISO 31000` · `ISO/IEC 27005` · `NIST SP 800-30` · `Análise de probabilidade e impacto` · `Mapa de calor` · `Plano de tratamento de riscos` · `LGPD` · `Controles internos` · `Menor privilégio` · `Continuidade de negócios` · `Gestão de fornecedores`
