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

O SD-WAN pode decidir qual conexão é mais adequada para cada tipo de tráfego e aplicação, considerando as políticas de desempenho, prioridade e custo.

---

### SASE — Secure Access Service Edge

SASE combina recursos de rede, como SD-WAN, com serviços de segurança entregues pela nuvem. Entre os recursos que podem compor essa arquitetura estão Secure Web Gateway (SWG), Cloud Access Security Broker (CASB), Firewall as a Service (FWaaS) e Zero Trust Network Access (ZTNA). O objetivo é oferecer acesso e proteção consistentes para usuários e dispositivos, estejam eles dentro ou fora da rede corporativa.
