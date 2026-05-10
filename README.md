# script_excel_estacionamento
🚗 Integração Python + Google Sheets: Registro de Veículos
Este projeto consiste em um sistema de automação que captura informações de veículos e funcionários em tempo real e as envia diretamente para uma planilha do Google Sheets via requisição HTTP (API/Web App).  

🚀 Funcionalidades
O script oferece uma interface de console para coleta de dados com as seguintes características:

Entrada de Dados Dinâmica: Captura a placa do veículo, o modelo do carro e o nome do funcionário responsável pelo registro.  

Registro de Timestamp: Gera automaticamente a data e hora exata do registro no formato brasileiro (dia/mês/ano hora:minuto:segundo).  

Comunicação via API: Utiliza o método POST da biblioteca Requests para enviar os dados em formato JSON para um script de backend (Google Apps Script).  

Loop de Operação: Mantém o sistema ativo para múltiplos registros até que o usuário decida encerrar.  

🧠 Lógica e Métodos Utilizados
Requests (POST): Diferente do método GET (coleta), o POST é utilizado aqui para enviar informações para o servidor.  

JSON: Os dados são empacotados em um formato de objeto (chave e valor) para que a planilha consiga interpretar as colunas corretamente.  

Datetime (strftime): Formatação customizada da data e hora para garantir que o registro siga o padrão local, facilitando auditorias posteriores.  

Controle de Status: O sistema valida o status_code 200 para confirmar que a planilha recebeu os dados com sucesso.  

🛠️ Tecnologias Utilizadas
Python 3

  

Requests: Para comunicação com a URL do Google Macros.  

JSON: Para estruturação dos dados enviados.  

Google Apps Script: (Backend receptor configurado na URL do projeto).  

📝 Exemplo de Uso
Ao executar o script, o fluxo de interação será:

Plaintext
--------------------------------------------------
informe a placa do carro: 4521dc
informe o modelo do carro: Renegade
informe o funcionario que registrou: Tiago
enviando dados para a tabela...
Dados enviados com sucesso!
deseja sair? S/N
