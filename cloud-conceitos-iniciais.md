# Cloud Computing — Conceitos Iniciais

📅 Data: 22/09/2026
📁 Categoria: Fundamentos / Cloud Security

## On-premises vs Cloud

**On-premises**: a empresa possui e administra sua própria infraestrutura (servidores, 
rede, armazenamento) em datacenter próprio ou dedicado.

**Cloud**: a empresa utiliza recursos de infraestrutura fornecidos por um provedor 
(AWS, Azure, GCP), sem precisar administrar o hardware físico.

> Analogia: no on-premises você possui a casa e é responsável por tudo. No cloud, 
> você utiliza uma casa fornecida por outra empresa, com responsabilidades divididas.

## Modelos de Serviço

| Modelo | O que o provedor entrega | O que o cliente administra |
|--------|---------------------------|------------------------------|
| **IaaS** | Infraestrutura física (servidores, rede, energia, datacenter) | SO, aplicações, usuários, rede, dados |
| **PaaS** | Infraestrutura + ambiente pronto para desenvolvimento | Apenas o código/aplicação |
| **SaaS** | Infraestrutura + aplicação completa (ex: Google Docs) | Apenas os próprios dados |

**Analogia da casa:**
- IaaS → "Alugo a casa, eu decido o sistema elétrico e organizo os móveis"
- PaaS → "Alugo uma casa já estruturada, só coloco minhas coisas"
- SaaS → "Uso o serviço pronto, só insiro meus dados"

**Responsabilidade compartilhada**: parte da segurança fica com o provedor, parte 
fica com o cliente — a proporção muda conforme o modelo (IaaS = cliente assume mais, 
SaaS = provedor assume mais).

## Principais Falhas de Segurança em Cloud

| Problema | Como reduzir o risco |
|----------|----------------------|
| Misconfiguration | Revisar configurações, IaC, ferramentas de CSPM |
| IAM inadequado / permissões excessivas | Least Privilege, revisão periódica de IAM |
| Credenciais expostas | MFA, secret managers, rotação de chaves |
| Vazamento de dados | Criptografia, controle de acesso, backups |
| Vulnerabilidades em aplicações | Patching, SAST/DAST, dependency scanning |
| Falhas de rede | Firewalls, Security Groups, segmentação |
| Falta de monitoramento | Logs, SIEM, alertas, auditoria |

## O que eu aprendi

Entendi a diferença prática entre os modelos de serviço em cloud e como a 
responsabilidade de segurança muda dependendo de quanto controle o cliente tem 
sobre a infraestrutura. Também mapeei as principais falhas de segurança em 
ambientes cloud e suas mitigações, o que é essencial pra entender o trabalho 
de um analista de segurança nesse contexto.
