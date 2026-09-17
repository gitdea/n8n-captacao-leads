# n8n-captacao-leads

Automação de captação de leads com formulário web, banco de dados e emails automáticos.

## O que este projeto faz

Este workflow automatiza o processo completo de captação de leads para empresas:

1. **Formulário web público** — Página de cadastro gerada automaticamente pelo n8n
2. **Armazenamento em banco** — Leads salvos em Data Table estruturada
3. **Notificação instantânea** — Email para a equipe quando nova lead chega
4. **Boas-vindas automáticas** — Email de confirmação para o lead

## Problema que resolve

Empresas que recebem contatos pelo site frequentemente:
- Perdem leads por não ter notificação em tempo real
- Gastam tempo manual respondendo cada contato
- Não organizam leads em um só lugar

Este workflow elimina esses problemas com automação completa.

## Stack utilizada

- **n8n** — Orquestração do workflow
- **Form Trigger** — Formulário web integrado
- **Data Tables** — Banco de dados para leads
- **Gmail API** — Envio de emails transacionais

## Screenshots

### Canvas do Workflow
<img width="801" height="409" alt="captacao-leads1" src="https://github.com/user-attachments/assets/21b21d75-877f-4935-8842-7431c6aea946" />

*Fluxo completo: Formulário → Salvar → Notificar → Boas-vindas*

### Formulário Público
<img width="470" height="658" alt="captacao-leads2" src="https://github.com/user-attachments/assets/2bfbc314-1a32-43c7-a9dd-4855fa3e45a2" />

*Interface do formulário que os leads preenchem*

### Email de Notificação
<img width="1296" height="572" alt="captacao-leads3" src="https://github.com/user-attachments/assets/13e7c7f1-63e4-4dd0-b416-e8088f1774fe" />

*Email recebido pela equipe quando nova lead chega*

<img width="500" alt="Email de Boas-vindas" src="https://github.com/user-attachments/assets/7aed1fc5-c3d0-4025-bf79-767d84a04231" />

*Email automático enviado para o lead*


## Configuração

## Pré-requisitos

- Conta n8n (cloud ou self-hosted)
- Conta Gmail com OAuth2 configurado
- Data Table criada no n8n

## Instalação

1. Importe o arquivo `Captacao-de-Leads.json` no seu n8n
2. Configure a credencial do Gmail nos nós de email
3. Ajuste o email de destino da notificação no nó "Notificar Nova Lead"
4. Publique o workflow
5. Compartilhe o link do formulário: `https://seu-n8n.com/form/captacao-leads`

## Personalização

## Campos do formulário

Edite o nó "Formulario de Captacao" para adicionar/remover campos:
- Nome completo (obrigatório)
- E-mail (obrigatório)
- Telefone (obrigatório)
- Empresa (opcional)
- Área de interesse (dropdown)

## Textos dos emails

Personalize os nós "Notificar Nova Lead" e "Enviar Boas-Vindas" com:
- Logo da empresa
- Tom de voz da marca
- Links e informações adicionais

## Banco de dados

Substitua a Data Table por:
- Google Sheets
- PostgreSQL/MySQL
- Airtable
- CRM (HubSpot, Pipedrive, etc.)

## Dados coletados

Cada lead registrado contém:
- `nome` — Nome completo
- `email` — E-mail de contato
- `telefone` — Telefone/WhatsApp
- `empresa` — Empresa (opcional)
- `interesse` — Área de interesse selecionada
- `origem` — Origem do lead (formulário)
- `captado_em` — Data/hora da captação

## Privacidade

- Dados fictícios usados nos exemplos
- Em produção, configure LGPD/GDPR compliance
- Considere adicionar campo de consentimento no formulário

## Licença

Este projeto é open-source e está disponível para uso pessoal e comercial.

## Autora

**Andrea Cruz Leonardo**
- LinkedIn: [linkedin.com/in/andrea-cruz-leonardo](https://linkedin.com/in/andrea-cruz-leonardo)
- GitHub: [@gitdea](https://github.com/gitdea)

---

