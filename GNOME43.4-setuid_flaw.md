## vulnerabilidade presente no GNOME Files 43.4 (_nautilus_) permite escalaçao local de privilegios  

esta vulnerabilidade existe porque o *nautilus* extrai os arquivos preservando seu`setuid` (*ou seja, em vez de executar o binario com as permissões do usuario que lançou, eh executado com as permissões do usuario que o criou, ou neste caso, extraiu o arquivo*). 

Uma vez que um usuario '_A_' com permissões elevadas extraia um arquivo 'F' (tendo seus atributos modificados com o `bit setuid`), um usuario malicioso podera executar 'F' com os atributos do usuario '_A_', violando assim varias propiedades de segurança do sistema




> [0daytoday (George Guninsky)](https://0day.today/exploit/38962)


*0x177*
