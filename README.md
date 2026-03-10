![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

# laboratorio redes 01 - Projeto de Rede Local
**Aluno:** Felippe Camargo <br>
**Professor:** José de Assis <br>
**Data:** 09/03/26

---

## 1. Objetivo
Implementar uma rede Local slimples conectando 3 notebooks a um roteador wireless com switch e uma impressora de rede

O Projeto será divido em duas etapas

1. Simulação da Rede no Cisco Packet Tracer
2. Implementação da rede no laboratorio Real

---

## 2. Equipamentos utilizados neste Laboratorio

- 3 Notebooks
- 1 Roteador Wireless com uma porta Wan e 4 portas Lan
- 1 Impressora de Rede
- Cabos de Rede

---

## 3. Topologia da Rede

Diagrama Logico da Rede Usada neste Laboratorio
```mermaid
graph TD

WAN[Internet / WAN do Provedor]

Router[Roteador Wireless<br>1 Porta Wan<br>4 Portas Lan]

PC1[Notebook 1]
PC2[Notebook 2]
PC3[Notebook 3]


Printer[Impressora de Rede]

WAN --> |Porta Wan| Router

Router --> |LAN 1| PC1
Router --> |LAN 2| PC2
Router --> |LAN 3| PC3
Router --> |LAN 4| Printer
```
---

## Imagem da Topologia usada neste Laboratorio:
  
<img width="753" height="449" alt="Topologia" src="https://github.com/user-attachments/assets/a02e2844-80f0-49f7-9a29-0d5239ab737f" />

---

## 4. Plano de Endereçamento IP

**Rede:** 192.168.0.0/24

**Gateway:** 192.168.0.1

| Dispositivo | Tipo de IP | Endereço IP | Observação|
|-------------|------------|-------------|-----------|
| Roteador | Estático | 192.168.0.1 | IP do Roteador |
| Impressora | Reserva DHCP | 192.168.0.105 | IP Reservado pelo roteador|
| PC1 | Reserva DHCP | 192.168.0.104 | IP Reservado Pelo Roteador |
| PC2 | DHCP | Automático | IP Atribuido Pelo Roteador |
| PC3 | DHCP | Automático | IP Atribuido Pelo Roteador |

**Observação**

- A impressora e um dos notebooks utilizam reserva DHCP.
- O Roteador Sempre atribui o mesmo endereço IP a Estes Dispositivos.

---

