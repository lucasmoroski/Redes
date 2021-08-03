# Redes
Trabalho - Camada de Enlace
Utilizando o GNS3 da VM disponibilizada:

1 - Elaborar um topologia em anel, com 5 switches. Incluir pelo menos dois hosts configurados com os IPs: 192.168.0.1 e 192.168.0.2. Utilizar o link entre os switches com vlan trunk (802.1q, tagged). Utilizar o ID da vlan os 3 últimos dígitos do seu GRR. Os hosts devem ser configurados no modo access (untagged).

2 - Provocar e identificar um loop de camada 2.

3 - Configurar STP (spanning-tree) para evitar loop

4 - Descrever o status de cada porta e explicar como que o loop foi evitado com STP.
	- Descrever o estado de cada porta
	- Descrever a função de cada porta

5 - Verificar o tempo de convergência habilitando e desabilitando o loop.

6 - Voltar ao passo 3 e alterar a configuração para RSTP (rapid spanning-tree)

Video: https://youtu.be/4DM8_AF7i6c


Trabalho Camada de Redes 

1) Elaborar um plano de endereçamento para uma organização que necessita de 600 endereços entre duas filiais, uma em SP e outra no PR. A filial de SP está dividida em 4 departamentos e a do PR em apenas um. A demanda de endereçamento é a seguinte:

SP1: 230 endereços
SP2: 150 endereços
SP3: 100 endereços
SP4: 70 endereços
PR1: 50 endereços

- Utilizar um espaço de endereçamento contíguo para a organização proveniente de 200.XXX.0.0/19, onde GRR é o resto da divisão do números do seu GRR por 255, ou seja, GRR % 255. Exemplo:  20205176 % 255 == 251

- Os prefixos de rede não utilizados devem ser roteados para o PR.

2) Configurar o GNS3 para endereçar os 5 departamentos, configurados com um roteador central, ligado a outros dois roteadores, um para SP e outro para PR. A ligação dos roteadores deve utilizar endereçamento privado da rede 192.168.XXX.0/24 através de sub-redes /30. 

3) Estabelecer todas as rotas para os prefixos de rede utilizados em SP e PR. 

O roteador central deve rotear todo prefixo de rede da organização para SP através de uma rota menos específica. Adicionar rotas para blackhole dos prefixos não utilizados. 

4) (vai precisar utilizar vlan tagged!). Altere o roteador de SP para trabalhar com apenas duas interfaces: Uma para WAN (eth0) e outra para WAN (eth1). Utilizar o OpenVSwitch na porta eth1. Utilize os seguintes IDs para cada VLAN:

SP1: 100
SP2: 200
SP3: 300
SP4: 400

Video: https://youtu.be/VMoohDby28U
