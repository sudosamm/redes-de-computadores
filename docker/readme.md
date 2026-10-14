## Instruções para a instalação do DOCKER e uso dos containers.
Para a versão atual dos computadores, instale o docker utilizando o seguinte comando:
```bash
sudo apt install docker docker.io docker-compose
```
Por garantia, utilize o comando a seguir para iniciar o serviço do Docker:
```bash
sudo systemctl start docker
```
Crie e acesse uma pasta com o nome do container que você deseja armazenar (o local é de livre escolha).<br>
Exemplo: 
```bash
mkdir /home/user/desktop/navidrome
cd /home/user/desktop/navidrome
```
Em seguida, acesse e dê permissões de leitura e gravação para o seu usuário na pasta que será utilizada (mude $USER para seu nome de usuário caso não funcione):
```bash
sudo chown -R $USER:$USER ./
```
Caso queira dar permissões para seu usuário e grupo, utilize o comando abaixo:
```bash
sudo chmod -R 775 ./
```
Se estiver em um local de testes, pode dar permissão de acesso para qualquer usuário (use com cuidado):
```bash
sudo chmod -R 777 ./
```
Após dar as permissões, crie um arquivo chamado docker-compose.yml e coloque as informações do container que você deseja criar (como por exemplo o [navidrome](https://raw.githubusercontent.com/sudosamm/redes-de-computadores/refs/heads/main/docker/navidrome/docker-compose.yml)). Quando tiver todas as informações inseridas, utilize CTRL+O para salvar o arquivo e CTRL+X para sair da tela de edição.
```bash
nano docker-compose.yml
```
Quando tudo estiver bem definido, basta executar o container:
```bash
sudo docker-compose up -d
```
Agora tente acessar o seu serviço utilizando `seu-ip:porta`. Caso ele não carregue ou caso mostre alguma mensagem de erro, utilize o comando abaixo para verificar o estado do container:
```bash
sudo docker ps
```
Caso o estado do container esteja "restarting", utilize o comando abaixo para verificar os logs e entender o que ocorreu:
```bash
sudo docker logs nome_do_container
```
Se quiser encerrar aquele container específico utilize:
```bash
sudo docker-compose down
```
