# Introdução a Redes Hierárquicas
Atividade prática desenvolvida no Cisco Packet Tracer para compreender e implementar uma estrutura de Redes Hierárquicas em três camadas:  Acesso, Distribuição e Núcleo (Core).

## 1. Laboratório de Redes Hierárquicas 
O projeto a seguir tem por abjetivo compreender o processo de implementação de uma rede Hierárquica Corporativa dividida em trÊs camadas, sendo estas a :
-Camada de Acesso
-Camada de Distribuição
-Camada de Núcleo (Core)

## 2. Obejetivos
-Compreender o modelo Hierárquico
-Entender as funções de cada camada da rede
-Montar a topologia no Cisco Packet Tracer;
-Configurar endereçamento IPv4;
-Configurar a interface do roteador;
-Ativar a interface utilizando no shutdown;
-Testar conectividade utilizando ping;
-Observar o tráfego ICMP no modo Simulation.

## 3. Dispositivos e Materiais Utilizados
Camada	              Equipamento	    Modelo        Quantidade
Núcleo	              Roteador        4331         	    1
Distribuição	        Switch          3650-24PS	        1
Acesso	              Switch          2960-24TT	        2
Dispositivos finais	  PCs	                -             4
Cabeamento            Cabos Diretos (Straight-Through)                

## 4. Arquitetura
<img width="1916" height="1010" alt="topologia" src="https://github.com/user-attachments/assets/f31a2530-b66e-446e-ac71-085da1864ac8" />

## 5. Endereçamentos
| Dispositivo | Interface            | Endereço IP  | Máscara       | Gateway     |
| ----------- | -------------------- | ------------ | ------------- | ----------- |
| Router-Core | GigabitEthernet0/0/0 | 192.168.1.1  | 255.255.255.0 | —           |
| PC-Lab01     | FastEthernet0       | 192.168.1.10 | 255.255.255.0 | 192.168.1.1 |
| PC-Lab02     | FastEthernet0       | 192.168.1.11 | 255.255.255.0 | 192.168.1.1 |
| PC-Sec01     | FastEthernet0       | 192.168.1.20 | 255.255.255.0 | 192.168.1.1 |
| PC-Sec02     | FastEthernet0       | 192.168.1.21 | 255.255.255.0 | 192.168.1.1 |

## 6. Configuração do Roteador
documentacao/comandos-roteador.txt

## 7. Testes e Simulação
Foram realizados 4 teste e simulação:
### PC-Lab01 ping no Roteador
`ping 192.168.1.1`
Resultado:  Sucesso

### PC-Lab01 ping no Sec01
`ping 192.168.1.20`
Resultado:  Sucesso

<img width="883" height="713" alt="teste-ping-lab1" src="https://github.com/user-attachments/assets/b1cec1e4-fbbe-4905-b726-53cec6e9a692" />

### PC-Sec01 ping no Roteador
`ping 192.168.1.1`
Resultado:  Sucesso

### PC-Sec01 ping no Lab01 
`ping 192.168.1.10`
Resultado:  Sucesso

<img width="881" height="713" alt="teste-ping-sec1" src="https://github.com/user-attachments/assets/79c5b62f-55b8-4278-85a1-2f98f4282772" />

### Simulação ICMP
<img width="1919" height="1013" alt="simulacao-icmp" src="https://github.com/user-attachments/assets/08fccaa4-cf5d-4d22-b4f7-9e487703b124" />

