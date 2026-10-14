## Para prosseguir com este container você precisará de um arquivo .env junto do docker-compose.yml.
O arquivo .env irá armazenar uma senha criptografada: ela será uma senha única de acesso ao seu vscode.<br>
Utilize o seguinte comando no terminal: ```echo "CONNECTION_TOKEN=$(openssl rand -hex 24)" > .env```<br>
Após este comando, o arquivo .env será criado na sua pasta e você poderá seguir com a criação do container.
