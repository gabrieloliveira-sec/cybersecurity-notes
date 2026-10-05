# 🛡️ Fortinet NSE 1 — Fundamentos de Cibersegurança

| **Atributo** | **Detalhe** |
|---|---|
| **Curso** | Fortinet Certified Associate / NSE 1 |
| **Categoria** | Fundamentos / Cibersegurança / Blue Team |
| **Data** | Outubro de 2026 |

---

## 📌 Visão Geral

O treinamento **Fortinet NSE 1** aborda a base conceitual da segurança da informação e a relevância da proteção digital no cenário tecnológico atual. 

Com a transformação digital, a infraestrutura expandiu-se para ambientes híbridos e em nuvem, aumentando a superfície de ataque. A cibersegurança atua como camada essencial para garantir a continuidade dos negócios, resiliência operacional e proteção de ativos críticos.

---

## 1. 🔺 Princípios Fundamentais de Cibersegurança

### Tríade CIA (CIA Triad)

Modelo Pilar da Segurança da Informação:

* **Confidencialidade (*Confidentiality*):** Restringe o acesso aos dados apenas a entidades autorizadas.
* **Integridade (*Integrity*):** Preserva a exatidão e a confiabilidade dos dados contra alterações não autorizadas ou acidentais.
* **Disponibilidade (*Availability*):** Garante que os sistemas e serviços estejam acessíveis quando solicitados.

* ### Modelo AAA (Authentication, Authorization & Accounting)

> [!NOTE]
> O modelo AAA é fundamental para governança de acesso e trilhas de auditoria em ambientes corporativos.

* **Autenticação (*Authentication*):** Validação de identidade (*"Quem é você?"*).
  * *Exemplos:* Credenciais, MFA (Autenticação Multi-Fator), Biometria, Certificados Digitais.
* **Autorização (*Authorization*):** Definição de privilégios (*"O que você pode fazer?"*).
  * *Exemplo:* Controle de Acesso Baseado em Funções (RBAC).
* **Contabilização / Auditoria (*Accounting*):** Rastreabilidade e registros de eventos (*"O que você fez?"*).
  * *Exemplo:* Logs de eventos, rastros de auditoria para investigação de incidentes.

---

## 2. 🎯 Prevenção, Ameaças e Motivações

A postura de segurança moderna deve ser **preventiva e proativa**, identificando riscos antes que se tornem incidentes operacionais.

### Perfil dos Atacantes (*Threat Actors*)
As motivações por trás de um ataque cibernético variam conforme o perfil do adversário:
- **Financeira:** Extorsão via *Ransomware*, fraude bancária.
- **Espionagem:** Roubo de propriedade intelectual ou segredos industriais.
- **Hacktivismo / Política:** Desfiguração de sites (*Defacement*), ataques de negação de serviço (DDoS).
- **Sabotagem / Efetividade:** Danos à infraestrutura crítica.

---

## 3. 🔎 Threat Intelligence & Indicadores de Comprometimento

### Inteligência de Ameaças (*Threat Intelligence*)
Processo de coleta e análise de dados sobre ameaças para antecipar comportamentos e fortalecer defesas.

### Indicadores de Comprometimento (*IoCs*)
Artefatos operacionais observados em uma rede ou sistema que indicam uma intrusão maliciosa:
* **Hashes de Arquivos:** MD5, SHA-256 de artefatos maliciosos.
* **Rede:** Endereços IP maliciosos, URLs de *Phishing*, Domínios C2 (*Command & Control*).
* **Sistema:** Chaves de registro alteradas, processos suspeitos em execução.

### Matriz MITRE ATT&CK®
Estrutura global que categoriza táticas, técnicas e procedimentos (TTPs) utilizados por adversários, auxiliando equipes de **SOC** no mapeamento de lacunas de detecção e resposta.

---

## 4. ⚠️ Engenharia Social & Phishing

Vetores de ataque focados no fator humano através de manipulação psicológica:

* **Phishing:** Ataques genéricos ou direcionados via e-mail ou páginas falsas.
* **Smishing:** Phishing realizado via SMS ou mensagens instantâneas.
* **Vishing:** Phishing realizado via chamadas de voz (Engenharia Social por telefone).

---

## 5. 🔐 Criptografia & Proteção de Dados

Mecanismos criptográficos garantem a confidencialidade, autenticidade e não repúdio.

### Conceito Básico
$$\text{Plaintext} + \text{Key} \xrightarrow{\text{Cipher}} \text{Ciphertext}$$

### Métodos Criptográficos
* **One-Time Pad (OTP):** Método que oferece *Perfect Secrecy* (Sigilo Perfeito), desde que a chave seja aleatória, do mesmo tamanho da mensagem, secreta e utilizada **apenas uma vez**.
* **Cifras de Bloco (*Block Ciphers*):** Processam dados em blocos de tamanho fixo (Exemplo: **AES**).
* **Cifras de Fluxo (*Stream Ciphers*):** Processam dados bit a bit/byte a byte continuamente (Exemplo: **ChaCha20**).

---

## 6. 🔢 Funções Hash, Assinatura Digital & PKI

### Funções Hash
Geração de um resumo de tamanho fixo para validação de **Integridade**. Qualquer alteração no conteúdo altera completamente a hash (*Efeito Avalanche*).

* `Arquivo Original` $\rightarrow$ `SHA-256` $\rightarrow$ `a3f...8b2`
* `Arquivo Modificado` $\rightarrow$ `SHA-256` $\rightarrow$ `7e1...9c4`

### Assinatura Digital
Garante **Autenticidade** e **Integridade** através de criptografia assimétrica:
* 🔐 **Chave Privada:** Assina o documento/código.
* 🔓 **Chave Pública:** Valida a assinatura e confirma a identidade do emissor.

### Infraestrutura de Chaves Públicas (PKI)
Estrutura hierárquica responsável pela emissão, gerenciamento e revogação de certificados digitais baseados em Autoridades Certificadoras (CAs).

---

## 7. ⚛️ Cibersegurança Quântica (*Quantum Security*)

Preparação dos sistemas criptográficos contra as ameaças da computação quântica, que poderá comprometer algoritmos assimétricos tradicionais (como RSA e ECC).
* **Solução:** Adoção de algoritmos de **Criptografia Pós-Quântica (PQC)** resistentes a ataques quânticos.

---

## 🧩 Conexão do Fluxo de Segurança

```text
[👤 Identidade] ──► [🔑 Autenticação] ──► [🚪 Autorização]
                                                │
                                                ▼
[🔎 SOC / Resposta] ◄── [🛡️ Threat Intel] ◄── [🔐 Criptografia & Hash]

# 🌐 Fundamentos de Redes e Segurança

Anotações sobre conceitos de redes, arquitetura de segurança e defesa em profundidade.

---

## WAN, SD-WAN e SASE

### WAN — Wide Area Network

WAN é uma rede utilizada para conectar redes ou unidades geograficamente distantes.

Exemplos:

- Matriz ↔ Filial
- Empresa ↔ Datacenter
- Empresa ↔ Cloud
- Filial ↔ Filial

**Resumo:**

> WAN conecta redes distantes.

---

### SD-WAN — Software-Defined WAN

SD-WAN é uma tecnologia que gerencia a WAN de forma inteligente.

Ela consegue escolher o melhor caminho para o tráfego considerando fatores como:

- Latência
- Jitter
- Perda de pacotes
- Disponibilidade do link
- Tipo de aplicação
- Prioridade
- Custo do link

Exemplo:

```text
Filial
  ↓
SD-WAN
  ├── Fibra
  ├── MPLS
  └── 5G
```

O SD-WAN pode decidir qual conexão é mais adequada para cada
