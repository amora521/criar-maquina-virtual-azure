# ☁️ Como Criar uma Máquina Virtual - Portal Azure

Neste guia vou ensinar como criar uma máquina virtual (VM) no Microsoft Azure usando o portal web. Ideal para testes e aprendizado.

## 🧰 Pré-requisitos

- Conta no [Microsoft Azure](https://portal.azure.com/)
- Cartão de crédito (obrigatório para validação da conta)

## 🚀 Etapas para Criar a Máquina Virtual

### 1. Acesse o portal Azure
Vá para o [portal do Azure](https://portal.azure.com) e faça login da forma que preferir.
![image](https://github.com/user-attachments/assets/9edf2051-da6c-46fc-a684-2549732e54e1)

### 2. Criar um novo recurso

Neste passo existem algumas formas de dar inicio.

#### 1. Por pesquisa, na barra de pesquisa
![Barra de Pesquisa (AZURE)](https://github.com/user-attachments/assets/85bebb2a-06dc-4ba7-adeb-5642c5887f8b)  

Clique em "+ Criar" e Logo em seguida em "Máquina virtual do Azure"  

![image](https://github.com/user-attachments/assets/269d5981-3fd8-4b90-974e-4965d96e8e12)

#### 2. Seleção da Maquina Virtual na Home Page
![Seleção na Home (AZURE)](https://github.com/user-attachments/assets/224306bb-c319-47ff-8a13-282c1cc76899)  

Esse Caminho é igual ao anterior

#### 3. Seleção de Criação de recurso na Home Page
![Seleção na Home (AZURE)](https://github.com/user-attachments/assets/9be984c4-14dc-4bd7-929a-59fb0d0eb3bf)  

Selecione a Máquina virtual  

![image](https://github.com/user-attachments/assets/3b66e25c-7264-4154-ad25-44bdb12b8ef1)

### 3. Configurações básicas
- Dê um nome para a sua máquina virtual  
  ![image](https://github.com/user-attachments/assets/7ca925f8-4e78-4292-9e98-b8d7ce3e99cb)
- Em "Imagem", escolha a aplicação ou o sistema operativo base da Máquina Virtual  
  ![image](https://github.com/user-attachments/assets/cb1ebc46-3f4d-404c-9e23-2e00b8e0a4fe)
- Selecione um Nome e Senha (com no mínimo 12 caracteres e atender a requisitos de complexidade definidos) para o Administrador  
  ![image](https://github.com/user-attachments/assets/2746e352-e8fc-4863-9e31-5857a1e30e73)
- Em "Regras de porta de entrada" permita as portas selecionadas, HTTP (80) e RDP (3389)  
![image](https://github.com/user-attachments/assets/159d21e4-49d1-4e3f-bbae-5b2ab993c772)
- Deixe todo o restante padrão e clique em "Rever + criar"  
![image](https://github.com/user-attachments/assets/c22dce1c-febd-477d-9f3d-c66a91b020d2)
- Após a validação, clique em "Criar"  
![image](https://github.com/user-attachments/assets/396333cc-ee3c-4cc6-adb9-e69a5098c936)
- Em seguida clique em "Ir para recurso"  
![image](https://github.com/user-attachments/assets/4e5132e0-cf6d-4585-a5fe-5ab9e8ebd4d2)

### 4. Conectando a Máquina Virtual
- Clique em "Ligar"  
![image](https://github.com/user-attachments/assets/9b7a355d-0bc2-4f7f-a166-42f806de3ee0)
- Baixe o arquivo RDP  
![image](https://github.com/user-attachments/assets/76a253f9-ab13-4a86-810a-1be41e9ee40f)
- Abra o arquivo que foi instalado  
![image](https://github.com/user-attachments/assets/04ec57ac-457a-4851-8126-f86f6ae3352e)
- Vá em "Mais Opções"  
![image](https://github.com/user-attachments/assets/53fd5a2e-ee35-4838-b9f2-9db4a811c61a)
- "Usar uma conta diferente"  
![image](https://github.com/user-attachments/assets/779b11ab-e84e-40c1-91fc-c3a2e5a3ae00)
- Insira o Nome e Senha que criou para o Administrador
- Você poderá receber um aviso do certificado durante esse processo, clique em "Sim"

### 5. Instalar Servidor Web
Abra um PowerShell e digite:  
``` PowerShell
Install-WindowsFeature -name Web-Server -IncludeManagementTools
```

### 6. Fazer as configurações que quiser
