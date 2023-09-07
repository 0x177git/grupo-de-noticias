# vulnerabilidade presente no GNOME Files 43.4 (nautilus) permite escalaçao local de privilegios através da extraçao de arquivos 

esta vulnerabilidade existe porque o *nautilus* extrai os arquivos com o setuid (ou seja, com as permissões do usuario), ou seja, supondo que um usuario 'A' com permissões elevadas extraia
um arquivo 'F', um usuario malicioso podera executar 'F' como o usuario 'A', violando assim varias propiedades de segurança do sistema
