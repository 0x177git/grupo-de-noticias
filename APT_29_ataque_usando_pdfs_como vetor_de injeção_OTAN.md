# Grupo APT 29 (_ligado ao serviço de inteligência estrangeira da Rússia_) enviou versões do malware Duke através de PDF's que diziam ser "Convites da Embaixada Alemã" pra ministros e negociantes de países membros da OTAN

supostos convites com o titulo "o dia da união alemã" ou "Adeus embaixador da Alemanha" continham JavaScript embebido que direcionava um ataque através de [_html smuggling_](https://www.cyfirma.com/outofband/html-smuggling-a-stealthier-approach-to-deliver-malware/) (basicamente redirecionava a uma suposta pagina html) que carregava uma versão do já conhecido Duke, efetuando duas fases, uma de reconhecimento e um de infecção.
Redirecionando pra um domínio supostamente legitimo (<sub>~~bahamas.gov.bs~~</sub>), que já foi usado em outras ocasiões pelo mesmo grupo 

Neste ataque é invocado um arquivo html que ao ser carregado no motor de arquivos e tarefas basseadas em html (_.hta_) interno do windows (_Microsoft Application Host_), amplamente utilizado pra carregar tarefas maliciosas dentro de utilitarios do sistema operacional ([LOLBins](https://www.sidechannel.blog/lolbins-como-ferramentas-nativas-sao-utilizadas-para-tornar-ameacas-mais-furtivas/))

baixando assim um arquivo zip (*Invitation_Farewall_DE_EMB*) do endereço controlado pelo APT (<sub>~~sgrh.org.pk~~</sub>) contendo tres arquivos, pra depois serem carregados na pasta  _C:\Windows\Task_ utilizando `DLL sideloading` 
### arquivos contidos no zip malicoso:

* **AppVIsvSubsystems64.dll** _carregado dentro de um componente que faz parte da biblioteca do Office_
* **Mso.dll** _uma variante direta do já conhecido Duke_
* **Msoev.exe** _um componente legitimo do Windows que faz parte do Office que neste caso se encarrega de inicializar a variante do Duke_


pra conhecer como este malware burlava a *Import Address Table* (utilizando _API hashing_) e se comunicava veja [Eclecticiq](https://blog.eclecticiq.com/german-embassy-lure-likely-part-of-campaign-against-nato-aligned-ministries-of-foreign-affairs) (<sup>proveedor de serviço de proteção contra ameaças persistentes, a maior parte do post foi retirada e adaptada do reporte feito pela sua equipe</sup>)

algo interessante a denotar é que pra se comunicar com seus operadores este malware utilizava a feramenta open-source Zullip, uma ferramenta de comunicação direta e colaboração legitima que utiliza os serviços web da Amazon, pelo qual se aproveitando disto, o trafego de C2C do malware 
pareceria confiavel 



![image](https://github.com/0x177git/grupo-de-noticias/assets/138733317/9a40abec-4188-4c35-967e-1e31e042d3c1)


*@rubyofsec* / *0x177*
