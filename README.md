# IA-contraturno

1- C

2- A API key fica no arquivo .env para separar as configurações mais "fracas" do código-fonte, garantindo a segurança do sistema e facilitando a alteração de credenciais entre diferentes ambientes nos arquivos. se não for no .env, pode acontecer cesso não autorizado por terceiros, que podem roubar dados.

3- D

4- total = 0
while True:
n = int(input("Número (0 para sair): "))
if n == 0:
break  
total += n  
print(f"Soma: {total}")

5- A: Pois a IA tem um Padrao, ou seja, a IA sem historico, toda vez que for mandar mensagem com ela, ela te tratada como se fosse a primeira vez que ele te visse
   B: criar uma lista com array e la deixar as mensagens anteriores, como se fosse um historico.

6- B

7- 
def carregar_contexto(caminho: str = "contexto.txt") -> str:
    try:
        with open(caminho, encoding="utf-8") as arquivo:
            texto = arquivo.read().strip()
    except FileNotFoundError:
        print(f"Aviso: arquivo '{caminho}' não encontrado. Seguindo sem contexto.")
        return ""

8- A: import streamlit as st
if "historico" not in st.session_state:
    st.session_state.historico = []
pergunta = st.chat_input("Digite...")
if pergunta:
st.session_state.historico.append({"role": "user", "content": pergunta})

B: Usamos st.session_state porque o Streamlit executa o código novamente a cada interação. Uma variável comum perde seu valor nessas atualizações, enquanto o session_state mantém os dados durante a sessão, preservando o histórico de mensagens.
