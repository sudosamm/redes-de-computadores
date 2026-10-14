## Para prosseguir com este container você precisará de alguns passos extras ANTES de iniciá-lo.
Para começar, gere um arquivo .env com a sua senha encriptada: ela será uma senha única de acesso ao seu vscode
Utilize o seguinte comando no terminal: ```echo "CONNECTION_TOKEN=$(openssl rand -hex 24)" > .env```<br>
Em seguida dê permissões de leitura e gravação para o seu usuário na pasta do arquivo via terminal (mude $USER para seu nome de usuário caso não funcione):
```sudo chown -R $USER:$USER ./workspace```<br>
Caso queira dar permissões para seu usuário e grupo, utilize o comando abaixo:
```sudo chmod -R 775 ./workspace```<br>
Se estiver em um local de testes, pode dar permissão de acesso para qualquer usuário (use com cuidado):
```sudo chmod -R 777 ./workspace```