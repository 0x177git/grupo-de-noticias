# Apple corrige falha de segurança critica (zero-day) que afeta o motor de renderização (WebKit) do safari que podia permitir execução de codigo remoto (CVE-2023-37450)

através do mais novo projeto de resposta rápida em segurança ([RSR](https://support.apple.com/en-us/HT201224))  a Apple conseguiu corrigir uma vulnerabilidade que foi reportada por um pesquisador anônimo que possivelmente teria sido explorada silenciosamente
Requisições ao **Safari** com tipos de dados especiais dentro de paginas web podiam explorar esta vulnerabilidade dada a natureza do seu **_WebKit_** e podia executar código remoto

a Apple nao revelou mtos detalhes sobre esta vulnerabilidade (*como sempre*) mas se sabe que a implementação desta correção trouxe instabilidade e diversos problemas ao abrir paginas web bastante conhecidas

Ate agr nao existem registros públicos ou em fóruns sobre provas de conceito ou detalhes desta vulnerabilidade mas eh interessante conhecer este sistema de respostas rápidas que jah vem implementados por padrão nos  produtos apple e permite instalar atualizações de segurança de forma automática, tendo seu principal foco orientado a vulnerabilidades que podem ser consideradas ameaças criticas.  Sem necessidade de haver uma reinicialização do sistema ou grande interações do usuário

*fontes*:  

- [TheHackerNews](https://thehackernews.com/2023/07/apple-issues-urgent-patch-for-zero-day.html)
- [Socradar.io](https://socradar.io/apple-addresses-critical-zero-day-exploit-cve-2023-37450-with-rapid-security-response-updates/)


        Detalhe: esta vulnerabilidade foi corrigida na gama de versões mais recentes, podendo existir ainda em versões anteriores que não fazem parte deste projeto 🏴‍☠️
