## Para prosseguir com este container você precisará de um arquivo .env junto do docker-compose.yml.
O arquivo .env irá armazenar uma senha criptografada: ela será uma senha única de acesso ao seu vscode.<br>
Utilize o seguinte comando no terminal: 
```bash
echo "CONNECTION_TOKEN=$(openssl rand -hex 24)" > .env
```
Após este comando, o arquivo .env será criado na sua pasta e você poderá seguir com a criação do container.<br>
Com o container rodando, acesse seu serviço utilizando:
```
http://seu-ip:porta/?tkn=SEU_TOKEN
```
Essa ação precisa ser executada apenas uma única vez.
