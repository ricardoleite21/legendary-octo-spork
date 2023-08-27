# Criando_uma_API_com_Flask_no_Ambiente_COLAB

Guia dos passos para criar uma API simples usando o framework Flask no ambiente Colab e ler uma planilha de dados no formato JSON. 

###**Desafio da Formação Python Developer pela Digital Innovation One**

Segue o passo a passo para a criação de uma API com Flask

**Passo 1:** Instale o Flask se ainda não estiver instalado. Execute o seguinte comando:

!pip install Flask

**Passo 2:** Importe as bibliotecas necessárias e configure sua aplicação Flask:

from flask import Flask, jsonify

app = Flask(__name__)

**Passo 3:** Crie uma rota para ler a planilha de dados JSON.

# Simulando dados de uma planilha em formato JSON
dados = [
    {"nome": "João", "idade": 30},
    {"nome": "Maria", "idade": 25},
    {"nome": "José", "idade": 35},
]

@app.route('/dados', methods=['GET'])
def obter_dados():
    return jsonify(dados)

if __name__ == '__main__':
    app.run()

**Passo 4:** Execute o aplicativo Flask no ambiente

!pip install flask-ngrok
from flask_ngrok import run_with_ngrok

run_with_ngrok(app)  # Inicializa o ngrok quando o aplicativo é executado

if __name__ == '__main__':
    app.run()

**Passo 5:** Após executar o aplicativo, você verá um link que termina com ".ngrok.io" no terminal do Colab. Esse é o link para a sua API.

**Observação:** Agora você tem uma API Flask simples que lê dados de uma planilha JSON e fornece-os quando você acessa /dados no seu navegador.

Lembre-se de que este é apenas um exemplo básico. Você pode personalizar sua API Flask e a forma como ela lê e fornece dados JSON de acordo com suas necessidades específicas. Certifique-se de também lidar com arquivos JSON reais da maneira apropriada no ambiente Colab.
