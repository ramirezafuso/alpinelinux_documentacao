# alpinelinux_documentacao
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
A OS selecionada é o Linux, a distribuidora é "Other Linux" e a OS Version é a "Other Linux (64-bit)"

### **Especificações da máquina**
A memória ram base definida será de 2000mb, equivalente a 2GB.
A quantidade de núcleos para a CPU será igual a duas.
Na seção para criar um HD virtual, definimos o tamanho para 16GB.

## 2° passo: Definições da máquina
### **Definições gerais**
Na primeira vez configurando o alpine, definimos primeiro o layout do teclado para português-brasileiro digitando `br`.
Após isso, definimos o nome do localhost de `alpine`. Seguindo, selecionamos a única interface disponível, a `etho`.
Para definirmos o endereço de ip, apertamos enter para usar `dhcp`. Também, não selecionamos a configuração manual de internet.
#### **Senha**
O terminal vai pedir a senha, lembrando que um dos requisitos de avaliação do projeto é usar a senha: `aluno`. Portando escrevemos ela.
#### **Timezone**
A timezone selecionada é a do `Brazil` do lado west.
#### **Proxy, Network Time Protocol e APK mirror**
Nas seguintes definições, a gente usou o padrão, apertando enter.
## 3º Passo: criação dos usuários
#### **Usuário aluno**
O terminal iniciará o processo de criação dos usuários. Primeiramente, definimos o nome para `aluno` e a senha de `aluno` também por exigência da avaliação.
Logo após isso, ele pergunta qual ssh server a gente precisará usar, selecionamos o `openssh`.
<img width="526" height="327" alt="image" src="https://github.com/user-attachments/assets/0744e336-ac43-4b43-8a06-87f3503d4185" />

#### **Disco e instalação**
Selecionamos o único disponível: `sda`. E para utilizarmos isso digitamos `sys`.
Limpamos o disco para continuar digitando `y`. A partir disso, o sistema é instalado de fato no disco.
Depois de concluído, fazemos uma reinicialização escrevendo `reboot`.

## 4° **Apagar o disco**
Por fim, forçamos a desmontagem do disco óptico virtual. Selecionando dentro das opções do VirtualBox na seguinte ordem: `dispositivos` -> `discos ópticos` -> `Remove Disk From Virtual Drive`. É necessário reinicializar novamente a máquina virtual. 

## 5° **Criando os outros usuários**
Acessamos o login de admin do root, com a senha ``aluno``. E digitamos o comando para criar o terceiro usuário `adduser ramirez.306541` com senha `aluno`. Após isso criamos o último usuário, digitando `adduser vitor.309703` com senha `aluno`. Portanto, temos no total os seguintes usuários:
- root (admin)
- aluno (criado na primeira configuração do alpine)
- ramirez.306541
- vitor.309703.
