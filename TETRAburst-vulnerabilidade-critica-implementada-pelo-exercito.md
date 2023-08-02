# Tecnologia de transmissão cifrada de radio (*_TETRA:Terrestrial Trunked Radio_*) usada por organizações militares e privadas, pelo ministério de segurança de multiplos países europeus e pelo exercito brasileiro, além de organizações pelo mundo inteiros possuem uma serie de vulnerabilidades criticas 
### **(_spoiler, seu algoritmo era privativo e ainda estas organizações de risco critico usavam sem um escrutínio analítico_)**
_a tecnologia TETRA eh um desses algoritmos mundialmente implementados e que acreditava-se seguro, mas esqueceram de um detalhe, seu nucleo de cifrado era privativo_

Não vou aprofundar mto sobre esta tecnologia em si, há mto conteúdo por ai, mas eh preciso saber que ***TETRA** eh um sistema de radio com protocolo cifrado móvel bidirecional (ou seja, comunicação simétrica).
Estes sistemas de comunicação possuem varias propriedades que facilitam a comunicação em diversos ambientes e estruturas, possui uma escalabilidades bastante ampla, `permitindo integrar vários terminais e ter uma implementação de áreas de risco e de difícil acesso, sendo usado por empresas de mineração, siderurgia, óleo & gás, por aeroportos, e sendo especificamente desenvolvido pra segurança publica`

Acho que já fico claro o quanto a segurança deste protocolo eh critica a nível de infraestrutura internacional, no brasil foi implementado pelo exercito a longa escala, pelo governo estadual do [rio de janeiro](http://infraroi.com.br/2016/08/24/exercito-adota-tecnologia-de-ponta-de-comunicacao-para-atuar-rj/) além de estar presente em operações do [ministeiro de segurança brasileiro](http://www.sgex.eb.mil.br/sg8/005_normas/01_normas_diversas/08_departamento_de_ciencia_e_tecnologia/port_n_081_dct_06set2018.html) (seja embebado em seus dispositivos de radio ou em implementação direta)
## vulnerabilidades descobertas e estudadas pela [Midnight Blue](https://www.midnightblue.nl/) e classificadas pelo nome [TETRA:burst](https://tetraburst.com/)
> Acontece que este protocolo possui vulnerabilidades que podem ser facilmente exploradas pra modificar mensagens mesmo fora do escopo de transmissão, pra exfiltrar os pacotes enviados pelos terminais
>
o nucleo do algoritmo de criptografia destes pacotes é privativo, chamados _TETRA Authentication Algorithm_ <sup>(TAA1)</sup>  (há varias propriedades interessantes neste sistema) mas uma questão bastante relevante é que **_este modelo de politicas é uma violação do principio em criptografia de Kerckhoffs_** (apenas a chave deve ser sigilosa, o sistema não)
esta serie de vulnerabilidades foram descobertas em 2022, mas apenas devidamente documentadas agora já que os pesquisadores quiseram dar um tempo as organizações e provedores de implementarem patchs, porém algumas desta vulnerabilidades não podem ser devidamente corrigidas e muitos deste provedores nem sequer chegaram a responder os pesquisadores (como é o caso da Motorola que prove os dispositivos do exercito brasileiro implementando TETRA)

![TETRA details]()
