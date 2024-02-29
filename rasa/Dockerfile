# Use a imagem base do Rasa
FROM rasa/rasa:3.0.0

# Copie os arquivos necessários para o diretório de trabalho
COPY ./rasa /app/rasa

# Configure o diretório de trabalho
WORKDIR /app/rasa

# Treine o modelo Rasa
RUN rasa train

# Exponha a porta necessária
EXPOSE 5005

# Comando para iniciar o servidor Rasa
CMD ["rasa", "run", "-p", "5005", "--enable-api"]