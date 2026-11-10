<h1 align="center">Joseph Santiago</h1>
<p align="center">
  <b>Desenvolvedor Full-Stack &amp; Mobile · I.A. aplicada (agentes, RAG) · Arquitetura de sistemas · Automação · Dashboards</b><br>
  Crio de ponta a ponta: o app, a I.A. que atende o cliente, a API, o painel que mostra os números e o servidor onde tudo roda.
</p>

<p align="center">
  <a href="mailto:josephsantiago250@gmail.com"><img src="https://img.shields.io/badge/E--mail-josephsantiago250%40gmail.com-D14836?logo=gmail&logoColor=white" alt="E-mail"></a>
  <a href="https://play.google.com/store/apps/developer?id=joseph+santiago"><img src="https://img.shields.io/badge/Google_Play-meus_apps-414141?logo=googleplay&logoColor=white" alt="Google Play"></a>
  <a href="https://josephsantiagos.github.io"><img src="https://img.shields.io/badge/Site-josephsantiagos.github.io-0A66C2?logo=googlechrome&logoColor=white" alt="Site"></a>
</p>

---

## 🚀 O que já entreguei (em produção)

| Área | O que é | Números |
|---|---|---|
| 🤖 **I.A. no WhatsApp para clínicas** | Agentes de I.A. que atendem, tiram dúvidas, agendam e transferem para humano, com um núcleo único (Clean Architecture) para todos os robôs | 14 robôs em produção |
| 📨 **Mensageria de lembretes e confirmação** | Lembra, confirma e reagenda consultas pelo WhatsApp, integrado ao ERP de cada clínica, com fila RabbitMQ e reenvio controlado | 25 serviços · 2.517 lembretes num dia, 0 bloqueios |
| 👓 **I.A. para rede de óticas** | Atendimento automático por loja, com fila RabbitMQ e histórico de conversa à prova de falhas | 13 lojas · 6.000+ mensagens/dia, 0 falhas |
| 📊 **Dashboards e painéis** | Painéis por clínica, painel da diretoria, Admin Master com login por pessoa, raio-X da demanda e monitor em tempo real das filas e das I.As | 11+ painéis |
| 💬 **CRM omnichannel** | CRM de atendimento via WhatsApp, portal de login próprio (GoTrue + PostgREST sobre Postgres) e apps Android/iOS | Web + Android + iOS |
| 💈 **SaaS para barbearias** | Vitrine de modelos, editor do site, painel master, provisionador automático, atendente de I.A. e app (PWA + Flutter) | Multi-cliente |
| 🧾 **Fiscal brasileiro** | ERPNext v16 com NF-e, NFC-e e NFS-e e assinatura digital ICP-Brasil (certificado A1), editor de XML da NF-e e monitor da SEFAZ | — |

## 📱 Mobile

- **25+ apps criados para a Google Play** em Flutter/Dart e Kotlin: finanças, utilidades, saúde, produtividade e jogos, com monetização AdMob, compras no app, testes fechados e publicação pela Play Console.
- **App Store (iOS):** app publicado e aprovado na loja da Apple ([Quero Treinar](https://apps.apple.com/br/app/quero-treinar/id6822551392)).
- **Jogos:** *Sarcófago*, um RPG de ação 3D em **Unity 6 / C#** com 10 regiões e chefões ([jogar/baixar](https://josephsantiagos.github.io/sarcofago-download/)), além de jogos casuais em Flutter (puzzle, corrida infinita).
- **Destaques:** [Calculadora Financeira e Juros](https://play.google.com/store/apps/details?id=com.josephsantiago.calculadoraemprestimos) (com [site de SEO](https://josephsantiagos.github.io) de 30+ simuladores), [Assinador de PDF com certificado digital A1](https://josephsantiagos.github.io/assinador/), scanner de QR/código de barras, consulta de placa e FIPE.

## 🧠 Inteligência Artificial

- Agentes conversacionais com LLMs (Claude, GPT e modelos locais via **Ollama**), com ferramentas, memória e regras de negócio
- **RAG (Retrieval-Augmented Generation):** base de conhecimento com busca semântica. Os documentos viram trechos com embeddings (OpenAI `text-embedding-3`), guardados no **banco vetorial pgvector** (PostgreSQL, índice HNSW). A busca usa limiar de similaridade e top-K, a resposta cita a fonte, e cada cliente só enxerga o próprio acervo (isolamento feito dentro do banco).
- **Gateway de LLMs próprio** (FastAPI) que roteia entre modelos locais (Ollama / llama.cpp) e de nuvem (OpenRouter)
- **LLM como juiz**: um robô que avalia as respostas dos outros agentes em produção
- Transcrição de voz local (**Whisper**), geração de voz (TTS) e vídeos tutoriais gerados automaticamente
- Servidores **MCP**, automação de navegador (Chrome DevTools Protocol) e orquestração de vários agentes
- GPU na nuvem (Colab T4) ligada a agentes internos

## 🏗️ Arquitetura de sistemas

- **Clean Architecture:** a regra de negócio fica num núcleo independente (domínio + casos de uso), e WhatsApp, ERPs, banco e LLMs entram como adaptadores. Um núcleo atende os 14 robôs de I.A., e outro atende as 25 mensagerias. Trocar um fornecedor não mexe na regra.
- **Mensageria assíncrona com RabbitMQ:** produtores e consumidores desacoplados, fila por cliente, controle de vazão para respeitar o limite de cada API, reentrega sem envio duplicado (idempotência) e reprocessamento seguro.
- **Multi-tenant:** vários clientes no mesmo sistema, com isolamento dos dados de cada organização no próprio PostgreSQL.
- **Observabilidade:** monitor das filas e das I.As, alertas no painel e conferência entre o que o painel mostra e o que o log registra.

## 🛠️ Stack

**Linguagens**
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![Dart](https://img.shields.io/badge/Dart-0175C2?logo=dart&logoColor=white)
![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?logo=kotlin&logoColor=white)
![C#](https://img.shields.io/badge/C%23-512BD4?logo=dotnet&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?logo=postgresql&logoColor=white)
![Shell](https://img.shields.io/badge/Shell-4EAA25?logo=gnubash&logoColor=white)

**Mobile e jogos**
![Flutter](https://img.shields.io/badge/Flutter-02569B?logo=flutter&logoColor=white)
![Android](https://img.shields.io/badge/Android-3DDC84?logo=android&logoColor=white)
![iOS](https://img.shields.io/badge/iOS-000000?logo=apple&logoColor=white)
![Unity](https://img.shields.io/badge/Unity_6-000000?logo=unity&logoColor=white)
![AdMob](https://img.shields.io/badge/AdMob-EA4335?logo=googleads&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?logo=firebase&logoColor=black)

**Back-end e dados**
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?logo=flask&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?logo=nodedotjs&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?logo=postgresql&logoColor=white)
![Oracle](https://img.shields.io/badge/Oracle_DB-F80000?logo=oracle&logoColor=white)
![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?logo=rabbitmq&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?logo=redis&logoColor=white)
![pgvector](https://img.shields.io/badge/pgvector-4169E1?logo=postgresql&logoColor=white)
![Supabase](https://img.shields.io/badge/GoTrue_%2B_PostgREST-3FCF8E?logo=supabase&logoColor=white)
![ERPNext](https://img.shields.io/badge/ERPNext_%2F_Frappe-0089FF?logo=frappe&logoColor=white)

**Front-end e dashboards**
![React](https://img.shields.io/badge/React-20232A?logo=react&logoColor=61DAFB)
![Tailwind](https://img.shields.io/badge/Tailwind_CSS-06B6D4?logo=tailwindcss&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![GSAP](https://img.shields.io/badge/GSAP-88CE02?logo=greensock&logoColor=black)

**I.A.**
![Claude](https://img.shields.io/badge/Claude-D97757?logo=anthropic&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?logo=openai&logoColor=white)
![RAG](https://img.shields.io/badge/RAG-embeddings_%2B_busca_sem%C3%A2ntica-6E40C9)
![Ollama](https://img.shields.io/badge/Ollama-000000?logo=ollama&logoColor=white)
![llama.cpp](https://img.shields.io/badge/llama.cpp-000000)
![OpenRouter](https://img.shields.io/badge/OpenRouter-6566F1?logo=openrouter&logoColor=white)
![Whisper](https://img.shields.io/badge/Whisper-74AA9C?logo=openai&logoColor=white)
![MCP](https://img.shields.io/badge/MCP-111111?logo=anthropic&logoColor=white)

**Integrações**
![WhatsApp](https://img.shields.io/badge/WhatsApp_Cloud_API-25D366?logo=whatsapp&logoColor=white)
![Meta](https://img.shields.io/badge/Meta_for_Developers-0467DF?logo=meta&logoColor=white)
![Mercado Pago](https://img.shields.io/badge/Mercado_Pago-00B1EA?logo=mercadopago&logoColor=white)
![Bling](https://img.shields.io/badge/Bling_ERP-2E7D32)
![Google Calendar](https://img.shields.io/badge/Google_Calendar-4285F4?logo=googlecalendar&logoColor=white)
![NF-e](https://img.shields.io/badge/NF--e_%7C_NFS--e_%7C_SEFAZ-00875A)

**Infra, DevOps e segurança**
![Linux](https://img.shields.io/badge/Linux-FCC624?logo=linux&logoColor=black)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![Proxmox](https://img.shields.io/badge/Proxmox-E57000?logo=proxmox&logoColor=white)
![Caddy](https://img.shields.io/badge/Caddy-1F88C0?logo=caddy&logoColor=white)
![systemd](https://img.shields.io/badge/systemd-201A1E)
![Git](https://img.shields.io/badge/Git-F05032?logo=git&logoColor=white)
![OpenVAS](https://img.shields.io/badge/OpenVAS_%2F_Trivy_%2F_Nuclei-66CC33)

## 🧩 Competências

- **Produto ponta a ponta:** do requisito à publicação na loja, com QA, monitoramento e correção em produção
- **Infraestrutura:** servidor Proxmox com ~20 VMs, ~100 containers Docker, proxy reverso, backups e observabilidade
- **Segurança:** varredura de vulnerabilidades (OpenVAS/Greenbone, Trivy, Nuclei), avaliação NIST CSF, auditoria de servidores e endurecimento
- **Automação:** robôs de navegador, scripts de operação, integração com ERPs e APIs de terceiros
- **Desktop Linux:** extensões do GNOME Shell (GJS) e ajustes de desempenho

## 📌 Projetos públicos

Os projetos fixados abaixo podem ser abertos por qualquer pessoa. A maior parte do código dos clientes fica em repositórios privados, e posso mostrar em entrevista.

---
<p align="center"><i>Aberto a novas oportunidades e projetos · fale comigo pelo e-mail acima</i></p>
