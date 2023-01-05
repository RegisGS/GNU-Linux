# RUNLEVELS

### Verificando o runlevel atual

   systemctl get-default 
   
 ### Verificando o número do runlevel atual  
 
   /sbin/runlevel
 
### Desliga o computador

   /sbin/init 0
   
* Help

/sbin/init --help

init [OPTIONS...] COMMAND

* telinit

/sbin/telinit 0

* Help

/sbin/telinit --help
  
telinit [OPTIONS...] COMMAND
  
### Reinicia o Computador

   /sbin/shutdown -h now

### Deligar de forma bruta o computador

   /sbin/halt

   /sbin/poweroff  
  
### Runlevel = niveus de execução
     
   * RUNLEVELS

    0 <- DESLIGA O COMPUTADOR
    1 <- MONO-USUÁRIO SEM REDE (TAREFAS ADIMINISTRATIVAS 'grub')
    2 <- MULTI-USUÁRIOS SEM REDE
    3 <- MULTI-USUÁRIOS COM REDE
    4 <- PROPOSITOS ESPECIAIS
    5 <- X (SERVIDOR GRAFICO)
    6 <- REINICIAR O COMPUTADOR

man 8 runlevel

man -k runlevel
