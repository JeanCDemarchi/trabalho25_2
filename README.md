🐄 Sistema de Monitoramento de Gado com BLE e Raspberry Pi

Este projeto tem como objetivo monitorar a movimentação de bovinos utilizando beacons BLE (Bluetooth Low Energy) e um Raspberry Pi como receptor.
O sistema detecta os sinais emitidos pelos beacons e registra as leituras em um banco de dados local (SQLite), permitindo identificar quando um animal se afasta da área delimitada.

🚀 Tecnologias Utilizadas

Python 3

beacontools (para leitura dos beacons BLE)

SQLite3 (para armazenamento local)

Raspberry Pi (como unidade de recepção)

⚙️ Funcionamento

O Raspberry Pi inicia o scanner BLE usando o beacontools.

Cada beacon detectado tem seus dados coletados:

Endereço Bluetooth

Força do sinal (RSSI)

Tipo de pacote (UID, URL, TLM)

Informações adicionais

As leituras são salvas no banco leituras.db através do SQLite.

As informações armazenadas podem ser usadas para monitorar distância e presença dos animais.

🧩 Estrutura dos Arquivos
📂 projeto-gado-ble
 ├── main.py           # Código principal em Python (scanner BLE)
 ├── database.py       # Funções de criação e inserção no banco SQLite
 ├── leituras.db       # Banco de dados local (gerado automaticamente)
 ├── README.md         # Documentação do projeto

💡 Motivação

O projeto busca oferecer uma solução de baixo custo e baixo consumo de energia para controle de rebanhos, evitando fugas e melhorando o manejo rural.
