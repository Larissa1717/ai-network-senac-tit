# 📘 Estrutura de Documentação de Rede — Estação Desktop

## 🖥️ 1. Informações Gerais do Equipamento

### 📂 Subcategoria: Identificação do Host

| Item | Valor |
|---|---|
| Nome do Computador | TIT0728105W11-1 |
| Sistema de Rede | Windows |
| Domínio DNS | senacsp.edu.br |

### 🧾 Resumo Simplificado
O computador está conectado à rede institucional do SENAC e possui identificação válida dentro da infraestrutura corporativa.

---

# 🌐 2. Adaptadores de Rede

## 📡 Subcategoria: Adaptador Ethernet Principal

| Item | Valor |
|---|---|
| Adaptador | Intel(R) Ethernet Connection (17) I219-LM |
| Tipo de Conexão | Ethernet Cabeada |
| Endereço MAC | D8-43-AE-E3-9A-8A |
| DHCP | Habilitado |
| IPv4 | 10.24.82.26 |
| Máscara de Rede | 255.255.255.0 |
| Gateway | 10.24.82.1 |
| DNS Primário | 10.24.40.190 |
| DNS Secundários | 10.1.1.195 / 10.1.1.242 |
| IPv6 Local | fe80::b64:7cbb:2e02:79db%12 |

### 🧾 Resumo Simplificado
A máquina está conectada corretamente à rede principal e recebe automaticamente suas configurações de internet e comunicação interna.

---

## 🧪 Subcategoria: Adaptador Virtual

| Item | Valor |
|---|---|
| Adaptador | VirtualBox Host-Only Ethernet Adapter |
| Endereço MAC | 0A-00-27-00-00-08 |
| IPv4 | 192.168.56.1 |
| Máscara | 255.255.255.0 |
| Gateway | Não definido |

### 🧾 Resumo Simplificado
Existe uma interface virtual instalada para utilização de máquinas virtuais no computador.

---

# 🧭 3. Configuração DHCP

## 📥 Subcategoria: Informações de Concessão

| Item | Valor |
|---|---|
| DHCP Ativado | Sim |
| Servidor DHCP | 10.24.40.190 |
| Concessão Obtida | 26/05/2026 13:37 |
| Expiração da Concessão | 27/05/2026 02:57 |

### 🧾 Resumo Simplificado
O computador recebe automaticamente suas configurações de rede sem necessidade de configuração manual.

---

# 🛣️ 4. Tabela de Rotas IPv4

## 📍 Subcategoria: Rotas Principais

| Destino | Máscara | Gateway | Interface |
|---|---|---|---|
| 0.0.0.0 | 0.0.0.0 | 10.24.82.1 | 10.24.82.26 |
| 10.24.82.0 | 255.255.255.0 | No vínculo | 10.24.82.26 |
| 192.168.56.0 | 255.255.255.0 | No vínculo | 192.168.56.1 |
| 127.0.0.0 | 255.0.0.0 | Loopback | 127.0.0.1 |

### 🧾 Resumo Simplificado
As rotas mostram que o computador consegue acessar a rede local, redes virtuais e também a internet através do gateway principal.

---

# 🌍 5. Tabela de Rotas IPv6

## 📘 Subcategoria: Rotas IPv6 Ativas

| Destino IPv6 | Interface |
|---|---|
| ::1/128 | Loopback |
| fe80::/64 | Interfaces Locais |
| ff00::/8 | Multicast |

### 🧾 Resumo Simplificado
O protocolo IPv6 está ativo parcialmente apenas para comunicação local e interna da máquina.

---

# 🔎 6. Configuração DNS

## 🧠 Subcategoria: Resolução de Nomes

| Item | Resultado |
|---|---|
| Servidor DNS Principal | TIT-EDUDC01.senacsp.edu.br |
| IP do DNS | 10.24.40.190 |
| Teste dns.google | Resolvido com sucesso |
| Teste google.com | Resolvido com sucesso |

### 🧾 Resumo Simplificado
O sistema consegue traduzir nomes de sites em endereços IP corretamente, indicando funcionamento adequado do DNS.

---

# 📶 7. Testes de Conectividade

## 🛰️ Subcategoria: Ping para DNS Google (8.8.8.8)

| Métrica | Resultado |
|---|---|
| Pacotes Enviados | 4 |
| Pacotes Recebidos | 4 |
| Perda | 0% |
| Latência Média | 3ms |

### 🧾 Resumo Simplificado
A conexão com a internet está estável e rápida, sem perdas de comunicação.

---

## 🌐 Subcategoria: Ping para google.com

| Métrica | Resultado |
|---|---|
| Pacotes Enviados | 4 |
| Pacotes Recebidos | 4 |
| Perda | 0% |
| Latência Média | 2ms |

### 🧾 Resumo Simplificado
O computador consegue acessar sites externos normalmente com excelente tempo de resposta.

---

# 🧱 8. Interfaces de Rede Identificadas

| Índice | Interface |
|---|---|
| 8 | VirtualBox Host-Only Ethernet Adapter |
| 12 | Intel(R) Ethernet Connection (17) I219-LM |
| 1 | Software Loopback Interface 1 |

### 🧾 Resumo Simplificado
O computador possui interfaces físicas, virtuais e internas funcionando corretamente.

---

# ⚠️ 9. Observações Técnicas Gerais

## 📋 Subcategoria: Análise da Infraestrutura

| Item Avaliado | Situação |
|---|---|
| Conectividade Local | ✅ Operacional |
| Acesso à Internet | ✅ Operacional |
| Resolução DNS | ✅ Funcional |
| DHCP | ✅ Funcional |
| IPv4 | ✅ Ativo |
| IPv6 | ⚠️ Parcial |
| Interface Virtual | ✅ Presente |
| Rotas Persistentes | ❌ Não configuradas |

### 🧾 Resumo Simplificado
A rede está funcionando corretamente. Não foram encontrados erros críticos de comunicação ou conectividade durante a análise.
