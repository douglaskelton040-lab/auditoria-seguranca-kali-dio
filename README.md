# 🔐 Auditoria de Segurança com Kali Linux

## 📌 Sobre o projeto

Este repositório documenta uma atividade prática de cibersegurança, com foco em reconhecimento de rede, identificação de serviços, auditoria de autenticação, análise de vulnerabilidades e aplicação de medidas de mitigação.

O projeto utiliza o Kali Linux como máquina auditora e ambientes próprios de laboratório para executar testes controlados.

## 🎯 Objetivos

- Realizar reconhecimento de dispositivos e serviços.
- Identificar portas abertas e serviços disponíveis.
- Auditar configurações do protocolo SMB.
- Estudar testes controlados de autenticação com Medusa.
- Praticar auditoria de serviços FTP.
- Utilizar DVWA para estudar vulnerabilidades web.
- Aplicar medidas de mitigação.
- Documentar evidências e resultados.

## 🧰 Ferramentas utilizadas

| Ferramenta       | Finalidade                                 |
| ---------------- | ------------------------------------------ |
| Kali Linux       | Sistema operacional de auditoria           |
| Nmap             | Reconhecimento e identificação de serviços |
| smbclient        | Testes de conexão e autenticação SMB       |
| Medusa           | Testes controlados de autenticação         |
| DVWA             | Laboratório de vulnerabilidades web        |
| Metasploitable 2 | Ambiente vulnerável de laboratório         |
| PowerShell       | Auditoria e configuração do Windows        |

## 🖥️ Ambiente de laboratório

O ambiente é composto por:

- Kali Linux: máquina auditora.
- Windows: máquina própria submetida à auditoria SMB.
- Metasploitable 2: ambiente vulnerável para testes controlados.
- DVWA: aplicação web vulnerável para estudos.

Os endereços IP utilizados nas capturas públicas serão anonimizados quando necessário.

## 📂 Estrutura do projeto

```text
auditoria-seguranca-kali-dio/
│
├── README.md
│
├── ambiente/
│   ├── configuracao-kali.md
│   ├── configuracao-windows.md
│   └── configuracao-rede.md
│
├── testes/
│   ├── reconhecimento-nmap.md
│   ├── auditoria-smb.md
│   ├── auditoria-ftp.md
│   └── auditoria-dvwa.md
│
├── mitigacao/
│   └── recomendacoes.md
│
└── images/
    ├── ambiente/
    ├── reconhecimento/
    ├── testes/
    └── resultados/
```

## 🔎 Atividades realizadas

### 1. Reconhecimento com Nmap

Identificação do computador Windows na rede local, portas abertas e serviços disponíveis.

**Status:** Concluído.

### 2. Auditoria SMB

Foram realizados testes de enumeração de compartilhamentos, análise de permissões e autenticação.

Principais descobertas:

- Compartilhamentos inicialmente acessíveis sem autenticação.
- Conta Convidado habilitada.
- Permissões excessivas para a identidade Todos.
- Conexões SMB anônimas aceitas inicialmente.

Medidas aplicadas:

- Desativação da conta Convidado.
- Manutenção do SMB1 desabilitado.
- Habilitação do SMB2/3.
- Habilitação da assinatura SMB.
- Criação de usuário específico para autenticação na rede.
- Validação do bloqueio de conexões anônimas.

**Resultado:** conexões sem autenticação passaram a retornar `NT_STATUS_ACCESS_DENIED`, enquanto a autenticação com usuário específico foi bem-sucedida.

**Status:** Em andamento — revisão das permissões dos compartilhamentos ainda pendente.

### 3. Auditoria FTP com Medusa

Etapa planejada para ambiente controlado, utilizando contas descartáveis e serviço de laboratório.

**Status:** Pendente.

### 4. Análise de vulnerabilidades com DVWA

Etapa planejada para estudar vulnerabilidades web em aplicação propositalmente vulnerável.

**Status:** Pendente.

### 5. Testes de autenticação SMB

Etapa planejada para estudar password spraying em ambiente isolado, com contas de laboratório e sem utilizar credenciais pessoais.

**Status:** Pendente.

## 🛡️ Segurança e autorização

Todos os testes são realizados em equipamentos próprios ou ambientes de laboratório autorizados.

Não são realizadas tentativas de acesso a dispositivos de terceiros, contas pessoais ou arquivos privados.

Senhas, credenciais e informações sensíveis não fazem parte deste repositório.

## 📸 Evidências

As capturas de tela, comandos e resultados serão organizados na pasta `images/` e documentados nos respectivos relatórios.

## 📚 Aprendizados

Durante o desenvolvimento serão registrados conhecimentos sobre:

- Reconhecimento de redes.
- Enumeração de serviços.
- Protocolos SMB e FTP.
- Auditoria de autenticação.
- Vulnerabilidades web.
- Mitigação e hardening.
- Documentação técnica de segurança.

## 👨‍💻 Autor

**Kelton Douglas da Silva Nascimento**

Projeto desenvolvido como atividade prática de estudos em cibersegurança — DIO.

---

*Projeto educacional em desenvolvimento. Os resultados documentados correspondem aos testes efetivamente realizados no laboratório.*
