# SISTEMAS DE MANIPULAÇÃO DE LOGS

* /var/log - Diretório padrão para registro de logs

* /var/log/auth.log --> Debian

* /var/log/audit/auth.log/ --> Red Hat

### Buscando logs de erro 

   grep Failed /var/log/auth.log --color --> Debian

   grep invalid /var/log/audit/audit.log --> Red Hat

### Verificar logs de Erros na inicialização do sistema

    /var/log# cat kern.log | grep fail

## DAEMONS

* SYSLOG (SYSLOGD)
* rsyslog (rsyslogd)
* syslog-ng
* journal (systemd) - systemd-journald


### Facilidade          VS          Prioridade

* auth             -          Mesagem de segurança - autorização
* authpriv         -          Idem ao anterior - mas, de caráter privativo                  
* cron             -          Mesagens geradas pelo daemon cron
* daemon           -          Mesagens geradas por diversos daemons em execução no sistema
* ftp              -          Mesagens que são vinculadas ao FTP
* kern             -          Mesagens do Kernel
* lpr              -          Mesagens do sistema de impressão
* mail             -          Mesagens do sistema de e-mail
* news             -          Mesagens oriudas do daemon news
* syslog           -          Mesagens geradas pelo próprio syslogd
* user             -          Mesagens a nível de usuário
* uupc             -          Mesagens de daemon uupc

* local0 até local7          Mesagens de aplicações/scripts definidas localmente

### Prioridades

* Valor - Quanto memor for o valor maior é a prioridade

* 0 - emerg Mesagens de pânico -sistema encontra-se inutilizável
* 1 - alert Mesagens representando falhas urgentes e mensagens de erro relativas a sistema primários
* 2 - crit idem ao anterior , mas relacionads a sistemas secundários
* 3 - err  Falhas (mas não urgente) - mesagens de erro também
* 4 - warn Mesagens indicativas de que um algum erro poderá ocorre caso nda seja feito
* 5 - notice Mesagens de caráter anormal (mas que não represantam tanta preocupação)
* 6 - info Mesagens de operação normal
* 7 - debug Mesagens a nível de depuração/debug (para o desenvolvimento de aplicações)
