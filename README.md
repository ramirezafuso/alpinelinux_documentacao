# Alpine Linux Documentação
Este repositório documenta a criação, a configuração e a instalação do
Alpine Linux Standard x86_64 em uma máquina virtual no Oracle VirtualBox.

A máquina foi configurada com 2 GB de memória RAM, dois processadores
virtuais e um disco virtual de 16 GB.

- [x] Sistema: Alpine Linux Standard x86_64
- [x] Ram: 2 GB
- [x] disco virtual: 16 GB
- [x] Processadores: 2
- [x] 4 usuários: aluno, admin, aluno1.matricula, aluno2.matricula (senha: aluno)

## 1° passo: Instalação
### **Instalação** <br>
Primeiramente definimos o nome "VM_Alpine_2B", depois selecionamos o local de instalação na pasta padrão. 
Adiconamos a iso `alpine-extend-3.24.4-x86_64.iso`
A OS selecionada é o Linux, a distribuidora é `Other Linux` e a OS Version é a `Other Linux (64-bit)`
<img width="827" height="335" alt="image (1)" src="https://github.com/user-attachments/assets/61e5b3cd-d4d4-48b0-b792-d0a275421870" />

### **Especificações da máquina**
A memória ram base definida será de 2000mb, equivalente a 2GB.
A quantidade de núcleos para a CPU será igual a duas.
Na seção para criar um HD virtual, definimos o tamanho para 16GB.
<img width="840" height="190" alt="image (2)" src="https://github.com/user-attachments/assets/3d9946fa-3bc4-4ee0-9bdf-9b6b68122516" />
<img width="831" height="201" alt="image (3)" src="https://github.com/user-attachments/assets/cb7ee1ea-e809-4dcb-ba61-8af26a56d662" />


## 2° passo: Definições da máquina
### **Definições gerais**
Na primeira vez configurando o alpine, definimos primeiro o layout do teclado para português-brasileiro digitando `br`.
Após isso, definimos o nome do localhost de `309703` uma matrícula. 
Seguindo, selecionamos a única interface disponível, a `etho`. Para definirmos o endereço de ip, apertamos enter para usar `dhcp`, no IPv4 selecionamos `dhcp` e no IPv6 `auto`.
Também, não selecionamos a configuração manual de internet.
<img width="945" height="249" alt="image (4)" src="https://github.com/user-attachments/assets/740e6f0b-80e9-4e26-b691-1790bd96e4ac" />
<img width="719" height="63" alt="hostname" src="https://github.com/user-attachments/assets/e72b8e63-4cf2-461f-840d-5cbdfd851bf8" />
<img width="558" height="210" alt="image (5)" src="https://github.com/user-attachments/assets/16fd9578-e87d-4830-b854-c141f4d6d23b" />


#### **Senha**
O terminal vai pedir a senha, lembrando que um dos requisitos de avaliação do projeto é usar a senha: `aluno`. Portando escrevemos ela.
<img width="405" height="238" alt="image (6)" src="https://github.com/user-attachments/assets/b7419614-b90d-4559-a520-84aeb8d8f6a2" />

#### **Timezone**
A timezone selecionada é a do `Brazil` do lado west.
<img width="959" height="340" alt="image (7)" src="https://github.com/user-attachments/assets/a9d2f4bd-8073-41cd-aa4a-26eaa4744c9f" />

#### **Proxy, Network Time Protocol e APK mirror**
Nas seguintes definições, a gente usou o padrão, apertando enter.
<img width="626" height="406" alt="apk_proxy_netwoek" src="https://github.com/user-attachments/assets/f910ebca-502f-47a0-b392-32bb7b89fd81" />

## 3º Passo: criação dos usuários
#### **Usuário aluno**
O terminal iniciará o processo de criação dos usuários. Primeiramente, definimos o nome para `aluno` e a senha de `aluno` também por exigência da avaliação.
Logo após isso, ele pergunta qual ssh server a gente precisará usar, selecionamos o `openssh`.
<img width="526" height="327" alt="image" src="https://github.com/user-attachments/assets/0744e336-ac43-4b43-8a06-87f3503d4185" />

#### **Disco e instalação**
Selecionamos o único disponível: `sda`. E para utilizarmos isso digitamos `sys`.
Limpamos o disco para continuar digitando `y`. A partir disso, o sistema é instalado de fato no disco.
Depois de concluído, fazemos uma reinicialização escrevendo `reboot`.
<img width="712" height="389" alt="image (10)" src="https://github.com/user-attachments/assets/734d1c1e-69f4-49a8-80b5-25be47ce5c3e" />

## 4° **Apagar o disco**
Por fim, forçamos a desmontagem do disco óptico virtual. Selecionando dentro das opções do VirtualBox na seguinte ordem: `dispositivos` -> `discos ópticos` -> `Remove Disk From Virtual Drive`. É necessário reinicializar novamente a máquina virtual.
<img width="777" height="269" alt="image (8)" src="https://github.com/user-attachments/assets/fc5d7656-0edc-44bf-9464-d2b9ce8b371c" />
<img width="349" height="222" alt="image (9)" src="https://github.com/user-attachments/assets/615b7a47-ae2a-4332-ab5f-82db602d13f2" />


## 5° **Criando os outros usuários**
Acessamos o login de admin do root, com a senha ``aluno``. E digitamos o comando para criar o terceiro usuário `adduser ramirez.306541` com senha `aluno`. Após isso criamos o último usuário, digitando `adduser vitor.309703` com senha `aluno`. Portanto, temos no total os seguintes usuários:
- root (admin)
- aluno (criado na primeira configuração do alpine)
- ramirez.306541
- vitor.309703.
<img width="557" height="409" alt="user_aluno" src="https://github.com/user-attachments/assets/3c570eb9-b5da-4db2-90b9-b9f4a4854cda" />
