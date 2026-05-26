# Guia Prático — Importação da Máquina Virtual Ubuntu Server 22.04.4 LTS no Oracle VirtualBox 7.2

## Curso Livre de Inteligência Artificial Voltada a Redes de Computadores
### SENAC São Paulo — Unidade Lapa Tito

---

# 🎯 Objetivo

Importar a máquina virtual:

`UbuntuServer-OnPremises.ova`

no Oracle VirtualBox 7.2, configurar a rede em modo **Bridge (Ponte)** utilizando a rede cabeada do laboratório e iniciar a máquina virtual para acesso remoto via **SSH**.

---

# 🖥️ Ambiente do Laboratório

| Item | Informação |
|---|---|
| Sistema Operacional | Microsoft Windows 11 |
| Virtualizador | Oracle VirtualBox 7.2 |
| Processador | Intel Core i7-14700K |
| Memória RAM | 32 GB |
| Disco | 1 TB |
| Rede Local | 10.24.82.0/24 |
| Gateway | 10.24.82.1 |

---

# 📥 ETAPA 1 — Abrir o Oracle VirtualBox

## 🔹 Passos

1. Clique no menu **Iniciar** do Windows.
2. Pesquise por:

```text
VirtualBox
```

3. Clique em:

```text
Oracle VM VirtualBox
```

---

# 📦 ETAPA 2 — Importar a Imagem OVA

## 🔹 Passos

### 1️⃣ No menu superior clique em:

```text
Arquivo → Importar Appliance
```

---

### 2️⃣ Clique no ícone da pasta 📁

Localize o arquivo:

```text
Downloads\UbuntuServer-OnPremises.ova
```

---

### 3️⃣ Clique em:

```text
Próximo
```

---

### 4️⃣ Verifique as configurações da máquina virtual

Confirme:

- Nome da VM
- Memória RAM
- CPUs
- Disco Virtual

---

### 5️⃣ Clique em:

```text
Finalizar
```

⏳ Aguarde a importação da máquina virtual.

Esse processo pode levar alguns minutos.

---

# 🌐 ETAPA 3 — Configurar Rede em Bridge (Ponte)

## 🎯 Objetivo

Permitir que a máquina virtual receba um endereço IP da rede do laboratório e possa ser acessada via SSH.

---

## 🔹 Passos

### 1️⃣ Selecione a VM

Clique na máquina virtual:

```text
UbuntuServer-OnPremises
```

---

### 2️⃣ Clique em:

```text
Configurações ⚙️
```

---

### 3️⃣ Acesse:

```text
Rede
```

---

### 4️⃣ Em “Adaptador 1”

Configure:

| Configuração | Valor |
|---|---|
| Habilitar Placa de Rede | ✅ Marcado |
| Conectado a | Adaptador em Ponte |
| Nome | Placa de Rede Ethernet do Laboratório |

---

## ⚠️ IMPORTANTE

Escolha a placa de rede:

```text
Ethernet
```

❌ NÃO escolha:

- Wi-Fi
- VirtualBox Host-Only
- VPN
- Bluetooth

---

### 5️⃣ Modo Promíscuo

Configure:

```text
Permitir Tudo
```

---

### 6️⃣ Cabo Conectado

✅ Marque a opção:

```text
Cabo Conectado
```

---

### 7️⃣ Clique em:

```text
OK
```

---

# ▶️ ETAPA 4 — Iniciar a Máquina Virtual

## 🔹 Passos

### 1️⃣ Selecione a VM

```text
UbuntuServer-OnPremises
```

---

### 2️⃣ Clique em:

```text
Iniciar ▶️
```

---

# 🔍 ETAPA 5 — Verificar Endereço IP do Ubuntu

Após o boot do Ubuntu:

Faça login com o usuário informado pelo professor.

---

## 🔹 Executar o comando:

```bash
ip addr
```

ou

```bash
hostname -I
```

---

## ✅ Exemplo de Resultado

```text
10.24.82.50
```

Esse IP será utilizado para acesso remoto SSH.

---

# 🔐 ETAPA 6 — Testar o Serviço SSH

## 🔹 Verificar status do SSH

Execute:

```bash
sudo systemctl status ssh
```

---

## ✅ Resultado esperado

```text
active (running)
```

---

# 💻 ETAPA 7 — Acessar via SSH no Windows 11

## 🔹 Abrir o PowerShell

Pressione:

```text
Windows + X
```

Clique em:

```text
Terminal
```

ou

```text
PowerShell
```

---

## 🔹 Conectar via SSH

Execute:

```bash
ssh usuario@IP_DO_UBUNTU
```

---

## ✅ Exemplo

```bash
ssh aluno@10.24.82.50
```

---

## 🔹 Primeira conexão

Digite:

```text
yes
```

---

## 🔹 Informar senha

Digite a senha do usuário Ubuntu.

⚠️ A senha não aparece na tela.

---

# ✅ Resultado Esperado

Após autenticar corretamente, aparecerá algo semelhante a:

```bash
usuario@ubuntu:~$
```

Isso indica que:

- ✅ A VM foi importada corretamente
- ✅ A rede Bridge está funcionando
- ✅ O Ubuntu recebeu IP da rede
- ✅ O SSH está operacional

---

# 🧪 Comandos Úteis

## Ver IP

```bash
hostname -I
```

---

## Ver Interfaces de Rede

```bash
ip addr
```

---

## Verificar SSH

```bash
sudo systemctl status ssh
```

---

## Reiniciar SSH

```bash
sudo systemctl restart ssh
```

---

# 🚨 Possíveis Problemas e Soluções

| Problema | Solução |
|---|---|
| VM sem internet | Verificar Bridge |
| Sem IP | Confirmar placa Ethernet |
| SSH não conecta | Verificar firewall e SSH |
| Adaptador errado | Selecionar Ethernet |
| SSH parado | Reiniciar serviço SSH |

---

# 📌 Resumo Final

## Fluxo da atividade

```text
Importar OVA
        ↓
Configurar Rede Bridge
        ↓
Iniciar Ubuntu
        ↓
Verificar IP
        ↓
Testar SSH
        ↓
Acesso Remoto
```

---

# 👨‍🏫 Observação

Essa máquina virtual será utilizada nas aulas práticas de:

- Inteligência Artificial
- Redes de Computadores
- Infraestrutura Linux
- Serviços de Rede
- Automação
- Ambientes On-Premises

---

# ✅ Fim do Guia
