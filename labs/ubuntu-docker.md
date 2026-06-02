# 📋 Documentação Técnica do Servidor — ctlinux01

> **Data de coleta:** Março de 2026 | **Responsável:** SysAdmin | **Versão do documento:** 1.0

---

## 1️⃣ Informações Gerais do Servidor

| Categoria | Descrição | Configuração |
|-----------|-----------|--------------|
| 🖥️ Geral | Nome do Servidor (Hostname) | ctlinux01 |
| 🖥️ Geral | Sistema Operacional | Ubuntu 24.04.4 LTS (Noble Numbat) |
| 🖥️ Geral | Kernel | Linux 6.8.0-107-generic |
| 🖥️ Geral | Arquitetura | x86-64 |
| 🖥️ Geral | Tipo de Máquina | Máquina Virtual (VM) |
| 🖥️ Geral | Plataforma de Virtualização | Oracle VirtualBox |
| 🖥️ Geral | Fabricante do Hardware Virtual | innotek GmbH |
| 🖥️ Geral | Machine ID | 05c2865e767d44c4870777b482ba0652 |
| 🖥️ Geral | Boot ID (Sessão atual) | a5a81cd031274f22b58fcf4ab580cf85 |
| 🕐 Uptime | Tempo de funcionamento contínuo | 2 horas e 3 minutos |
| 👥 Usuários | Usuários conectados simultaneamente | 10 usuários ativos |
| 📊 Carga | Load Average (1min / 5min / 15min) | 0.10 / 0.05 / 0.01 |

> 💬 **Em linguagem simples:** Este servidor é uma máquina virtual rodando Ubuntu Linux, uma versão profissional e estável do sistema. Ele estava ligado por pouco mais de 2 horas no momento da coleta e estava com carga de trabalho muito baixa — o que indica que estava operando de forma tranquila, sem sobrecarga.

---

## 2️⃣ Informações de Hardware do Servidor

| Categoria | Descrição | Configuração |
|-----------|-----------|--------------|
| 🧠 Memória RAM | Total disponível | 3.915 MB (~4 GB) |
| 🧠 Memória RAM | Em uso | 582 MB |
| 🧠 Memória RAM | Livre | 2.936 MB |
| 🧠 Memória RAM | Cache/Buffer do sistema | 617 MB |
| 🧠 Memória RAM | Disponível para novos processos | 3.333 MB |
| 💾 Swap (Memória extra) | Total | 3.914 MB (~4 GB) |
| 💾 Swap (Memória extra) | Em uso | 0 MB (não está sendo utilizado) |
| 🗄️ Disco Principal (sda) | Capacidade total | 50 GB |
| 🗄️ Disco — Partição Boot | /boot — Tamanho / Uso / Disponível | 2 GB / 200 MB / 1,6 GB (11% usado) |
| 🗄️ Disco — Partição Principal | / (raiz do sistema) — Tamanho / Uso / Disponível | 47 GB / 8,5 GB / 37 GB (19% usado) |
| 🗄️ Disco — Volume LVM | ubuntu-vg/ubuntu-lv | 48 GB (LVM — gerenciamento avançado de disco) |

> 💬 **Em linguagem simples:** O servidor possui 4 GB de memória RAM, sendo que apenas 15% está em uso — excelente sinal de que há capacidade disponível. O armazenamento (disco) tem 50 GB no total e apenas 19% está ocupado, o que garante espaço suficiente para crescimento a curto e médio prazo. O servidor não está usando memória de emergência (Swap), o que indica boa saúde operacional.

---

## 3️⃣ Informações de Rede do Servidor

| Categoria | Descrição | Configuração |
|-----------|-----------|--------------|
| 🌐 Interface Principal | Nome da interface de rede | enp0s3 |
| 🌐 Interface Principal | Endereço IPv4 | 10.24.82.200/24 |
| 🌐 Interface Principal | Endereço IPv6 (link local) | fe80::a00:27ff:fe42:90a5/64 |
| 🌐 Interface Principal | Endereço MAC (físico) | 08:00:27:42:90:a5 |
| 🌐 Interface Principal | MTU (tamanho do pacote) | 1500 |
| 🐳 Interface Docker | Nome da interface | docker0 |
| 🐳 Interface Docker | Endereço IPv4 | 172.17.0.1/16 |
| 🐳 Interface Docker | Endereço MAC | 4e:15:bd:3d:de:85 |
| 🔁 Loopback | Endereço interno do sistema | 127.0.0.1/8 |
| 🛣️ Rota Padrão (Gateway) | Saída padrão para a internet/rede | 10.24.82.1 via enp0s3 |
| 🛣️ Rota Local | Rede local acessível diretamente | 10.24.82.0/24 |
| 🛣️ Rota Docker | Rede interna dos containers | 172.17.0.0/16 |
| 🔍 DNS Primário | Servidor de resolução de nomes | 8.8.8.8 (Google) |
| 🔍 DNS Secundário | Servidor de resolução de nomes | 8.8.4.4 (Google) |
| 🔒 Portas Abertas | SSH (acesso remoto seguro) | 0.0.0.0:22 (acesso de qualquer origem) |
| 🔒 Portas Abertas | Portainer (gerenciamento Docker) | 0.0.0.0:9000 e [::]:9000 |
| 🔒 Portas Abertas | DNS local do sistema | 127.0.0.54:53 e 127.0.0.53:53 |

> 💬 **Em linguagem simples:** O servidor tem um endereço de rede fixo (10.24.82.200) e utiliza os servidores DNS do Google para resolução de nomes. Ele possui duas "portas abertas" visíveis na rede: a porta 22 (para acesso remoto de administração) e a porta 9000 (para o painel de gerenciamento dos containers chamado Portainer). Isso é esperado para um servidor de containers.

---

## 4️⃣ Informações de Serviços e Processos

| Categoria | Descrição | Status |
|-----------|-----------|--------|
| 🐳 Container | containerd — Motor de execução de containers | ✅ Ativo |
| 🐳 Container | docker — Plataforma de containers Docker CE | ✅ Ativo |
| 🐳 Container | portainer — Painel Web de gerenciamento Docker | ✅ Ativo |
| 🔐 Acesso Remoto | ssh — Servidor de acesso remoto seguro (OpenSSH) | ✅ Ativo |
| 📡 Rede | systemd-networkd — Gerenciamento de configuração de rede | ✅ Ativo |
| 📡 Rede | systemd-resolved — Resolução de nomes DNS | ✅ Ativo |
| 🕐 Sincronização | systemd-timesyncd — Sincronização de horário via rede | ✅ Ativo |
| 📝 Logs | rsyslog — Serviço de registro de eventos do sistema | ✅ Ativo |
| 🔔 Sistema | dbus — Barramento de comunicação entre processos | ✅ Ativo |
| ⚙️ Sistema | systemd-udevd — Gerenciamento de dispositivos | ✅ Ativo |
| 👤 Usuários | systemd-logind — Gerenciamento de sessões de usuários | ✅ Ativo |
| 🔌 Hardware | udisks2 — Gerenciador de discos | ✅ Ativo |
| 🔌 Hardware | upower — Gerenciamento de energia | ✅ Ativo |
| 🔌 Hardware | ModemManager — Gerenciamento de modems | ✅ Ativo |
| 🛡️ Segurança | polkit — Gerenciador de permissões e autorizações | ✅ Ativo |
| 🔧 Firmware | fwupd — Serviço de atualização de firmware | ✅ Ativo |
| 🔄 Manutenção | unattended-upgrades — Atualizações automáticas de segurança | ✅ Ativo |
| ⏰ Agendamento | cron — Agendador de tarefas automáticas | ✅ Ativo |
| 🖥️ Terminal | getty@tty1 — Terminal de acesso local | ✅ Ativo |
| 👤 Sessões | Usuários com sessão ativa (UIDs) | 1001, 1002, 1004, 1005, 1006, 1008, 1009, 1011, 1012, 1013 |
| ⚡ Multipath | multipathd — Controlador de múltiplos caminhos de disco | ✅ Ativo |

> 💬 **Em linguagem simples:** O servidor está executando todos os serviços essenciais para seu funcionamento como plataforma de containers Docker. O destaque é o Portainer — uma interface visual acessível pelo navegador na porta 9000 — que permite gerenciar os containers sem precisar de conhecimento técnico avançado. O sistema também realiza atualizações de segurança automaticamente, o que é uma boa prática para manter o ambiente protegido.

---

## 5️⃣ Informações de Softwares e Atualizações

| Categoria | Descrição | Versão Atual | Versão Disponível |
|-----------|-----------|--------------|-------------------|
| 🐳 Docker | docker-ce — Motor Docker CE | 29.2.1 | 29.4.0 |
| 🐳 Docker | docker-ce-cli — Interface de linha de comando | 29.2.1 | 29.4.0 |
| 🐳 Docker | docker-ce-rootless-extras | 29.2.1 | 29.4.0 |
| 🐳 Docker | docker-buildx-plugin — Plugin de build avançado | 0.31.1 | 0.33.0 |
| 🐳 Docker | docker-compose-plugin — Plugin Docker Compose | 5.1.0 | 5.1.1 |
| 📦 Container | containerd.io — Runtime de containers | 2.2.1 | 2.2.2 |
| 🔧 Sistema | systemd — Gerenciador do sistema (e pacotes relacionados) | 255.4-ubuntu8.14 | 255.4-ubuntu8.15 |
| 🌐 Rede | netplan.io — Configuração de rede | 1.1.2-ubuntu24.04.1 | 1.1.2-ubuntu24.04.2 |
| 🌐 Rede | nftables — Firewall do sistema | 1.0.9-1build1 | 1.0.9-1ubuntu0.1 |
| 🛠️ Utilitários | coreutils — Utilitários básicos do sistema | 9.4-3ubuntu6.1 | 9.4-3ubuntu6.2 |
| 🛠️ Utilitários | binutils — Ferramentas de compilação | 2.42-4ubuntu2.8 | 2.42-4ubuntu2.10 |
| 🛠️ Utilitários | lshw — Ferramenta de inventário de hardware | 02.19.git.2021.06.19.996aaad9c7-2build3 | 02.19.git.2021.06.19.996aaad9c7-2ubuntu0.24.04.1 |
| 🛠️ Utilitários | sosreport — Ferramenta de diagnóstico e suporte | 4.9.2 | 4.10.2 |
| 🔒 Segurança | linux-base — Base do kernel Linux | 4.5ubuntu9+24.04.1 | 4.5ubuntu9+24.04.2 |
| 🔌 Drivers | ubuntu-drivers-common — Gerenciador de drivers | 1:0.9.7.6ubuntu3.5 | 1:0.9.7.6ubuntu3.6 |
| 📊 Total de pacotes com atualização disponível | | | **38 pacotes** |

> 💬 **Em linguagem simples:** Existem **38 pacotes de software** aguardando atualização, incluindo componentes críticos como o próprio Docker e o systemd (gerenciador central do sistema). Recomenda-se **agendar uma janela de manutenção** para aplicar essas atualizações, especialmente as relacionadas ao Docker (que subiu da versão 29.2 para 29.4) e ao systemd. Atualizações do systemd geralmente requerem reinicialização do servidor.

---

## 📌 Resumo Executivo

| Indicador | Status | Observação |
|-----------|--------|------------|
| 🟢 Sistema Operacional | Estável | Ubuntu 24.04.4 LTS — versão com suporte de longo prazo |
| 🟢 Uso de Memória RAM | Baixo (15%) | Capacidade disponível para crescimento |
| 🟢 Uso de Disco | Baixo (19%) | Espaço disponível suficiente |
| 🟢 Carga do Servidor | Mínima | Servidor operando sem sobrecarga |
| 🟢 Serviços Essenciais | Todos ativos | Docker, Portainer e SSH funcionando normalmente |
| 🟡 Atualizações Pendentes | 38 pacotes | Requer agendamento de manutenção |
| 🟡 Versão do Docker | Desatualizada (29.2.1) | Versão 29.4.0 disponível |

> 💬 **Conclusão para a gestão:** O servidor está saudável, com baixo uso de recursos e todos os serviços de containers funcionando corretamente. O único ponto de atenção é a existência de 38 pacotes desatualizados, incluindo o Docker e componentes de sistema. Recomenda-se agendar uma manutenção preventiva para aplicar essas atualizações em horário de baixo impacto para os negócios.

---

*Documento gerado automaticamente com base nos dados coletados manualmente no servidor ctlinux01 — Ubuntu 24.04.4 LTS*
