<<<<<<< HEAD
🧩 1. Importar a imagem .OVA

📁 Arquivo: UbuntuServer-OnPremises.ova (na pasta Downloads)

Passos:
Abra o VirtualBox
Clique em 📂 Arquivo → Importar Appliance

Clique em 📁 e selecione:

Downloads\UbuntuServer-OnPremises.ova
Clique em Próximo
(Opcional) Ajuste recursos:
🧠 RAM: 4096 MB ou 8192 MB
⚙️ CPU: 2 ou mais núcleos
Clique em ✔️ Importar
Aguarde finalizar
⚙️ 2. Ajustar recursos da máquina virtual

Após importar:

Selecione a VM → ⚙️ Configurações
🔹 Sistema → Processador
CPU: 2+ núcleos
🔹 Sistema → Placa-mãe
Memória: mínimo 4GB (ideal 8GB)
🌐 3. Configurar rede em modo Bridge (Ponte)

Objetivo: VM na mesma rede do laboratório (IP real da rede)

Passos:
Vá em ⚙️ Configurações → Rede
Em Adaptador 1:
✔️ Marcar: Habilitar placa de rede
🔽 Conectado a: Placa em modo Bridge
🔽 Nome: selecione a interface cabeada
(exemplo: Ethernet, Intel(R) Ethernet Connection)

📌 Importante:

Use rede cabeada (LAN) do laboratório
NÃO use Wi-Fi
▶️ 4. Iniciar a máquina virtual
Selecione a VM
Clique em ▶️ Iniciar

Aguarde o boot do Ubuntu Server 22.04.4 LTS

🔎 5. Descobrir o IP da VM

Dentro da VM, execute:

ip a

ou

hostname -I

📌 Procure algo como:

192.168.x.x
🔐 6. Acesso remoto via SSH

No Windows (PowerShell ou Prompt):

ssh usuario@IP_DA_VM

Exemplo:

ssh aluno@192.168.0.50

📌 Se pedir confirmação:

yes
=======
🧩 1. Importar a imagem (.OVA)

📁 Arquivo: Downloads\UbuntuServer-OnPremises.ova

Abra o VirtualBox<br>
Clique em 📂 Arquivo → Importar Appliance<br>
Clique em 📁 e selecione:<br>
UbuntuServer-OnPremises.ova<br>
Clique em ➡️ Avançar<br>
Revise as configurações (pode manter padrão)<br>
Clique em ✅ Importar<br>
Aguarde o processo finalizar<br>

⚙️ 2. Ajustar configurações da VM

Após importar:

Selecione a VM UbuntuServer-OnPremises
Clique em ⚙️ Configurações
🧠 Sistema
Verifique RAM e CPU (não alterar se já estiver definido pelo professor)
🌐 3. Configurar rede em modo Bridge (Ponte)
Vá em 🌐 Rede
Em Adaptador 1:
✔️ Marcar: Habilitar placa de rede
🔽 Conectado a: Bridge Adapter (Placa em modo Bridge)
🔽 Nome:
Escolher a placa Ethernet cabeada (ex: Ethernet, Realtek, Intel)
Clique em OK

📌 Objetivo: A VM receberá um IP da mesma rede do laboratório

▶️ 4. Iniciar a máquina virtual
Selecione a VM
Clique em ▶️ Iniciar
Aguarde o boot do Ubuntu Server 22.04.4 LTS
🔐 5. Verificar IP da VM

No terminal da VM:

Digite:

ip a

🔎 Procure algo como:

inet 192.168.x.x

📌 Esse será o IP para acesso remoto

💻 6. Acesso remoto via SSH

No computador host (Windows 11):

Abra o Prompt de Comando ou PowerShell
Execute:
ssh usuario@IP_DA_VM

📌 Exemplo:

ssh aluno@192.168.0.50
Digite a senha quando solicitado
>>>>>>> 0c879b6a94849d9a0a2eccdb6e681e69efa434e5
🧪 7. Teste de conectividade (opcional)

No Windows:

ping IP_DA_VM

<<<<<<< HEAD
Se responder → rede OK ✔️

⚠️ Boas práticas para laboratório
💾 Não alterar a imagem original
🔄 Sempre desligar corretamente (sudo poweroff)
🌐 Garantir cabo de rede conectado
🧠 Evitar alocar toda RAM do host
✅ Resultado esperado
VM rodando normalmente ✔️
IP válido na rede do laboratório ✔️
Acesso SSH funcionando ✔️


---

segundo pompt
=======
Se responder → rede OK ✅

⚠️ Observações importantes
🔌 Use rede cabeada (Ethernet) — Wi-Fi pode não funcionar corretamente em Bridge
🔐 Verifique se o SSH está ativo na VM:
sudo systemctl status ssh
Caso não esteja:
sudo systemctl start ssh
✅ Resultado esperado
VM importada com sucesso
Rede em modo Bridge funcionando
IP válido na rede do laboratório
Acesso remoto via SSH operacional

---

Segundo Prompt
>>>>>>> 0c879b6a94849d9a0a2eccdb6e681e69efa434e5

---

