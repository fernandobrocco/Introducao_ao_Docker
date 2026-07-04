# API de Votação (TechVotos) - DevOps

Este projeto foi desenvolvido como Projeto Integrador Final com o objetivo de empacotar, automatizar e monitorar uma API de votação em Python/Flask. Isolei a aplicação utilizando containers Docker e configurei a orquestração do ambiente multi-serviço (App, Prometheus e Grafana) via Docker Compose. 

Ele permite que o Prometheus realize coletas consecutivas a cada 5 segundos e o Grafana exiba painéis visuais para tomada de decisão.

Um projeto integrador para testar os conhecimentos em Docker e conteinerização ministrado pelo Professor Eden Ricardo Dosciatti na matéria Automação de Software e Infraestrutura.

## 🚀 Como Iniciar o Projeto (Passo a Passo)

Para rodar todo o ambiente na sua máquina sem precisar configurar o Python ou os bancos de dados manualmente, você só precisa ter o **Docker** e o **Docker Compose** instalados no seu sistema.

1. **Baixar o Projeto:** Abra o terminal na sua máquina, clone este repositório com o comando `git clone https://github.com/fernandobrocco/Introducao_ao_Docker.git` e entre na pasta usando `cd Introducao_ao_Docker`.

2. **Subir a Infraestrutura:** Execute o comando `docker compose up -d` para baixar as imagens necessárias e iniciar todos os serviços de forma isolada em segundo plano.

3. **Votar na API:** Abra o seu navegador de internet e acesse `http://localhost:5000/`. A página inicial do sistema de votação estará online. Para computar votos e testar o funcionamento, você pode acessar diretamente os endereços `http://localhost:5000/votar/a` ou `http://localhost:5000/votar/b`.

4. **Verificar as Métricas do Prometheus:** Para checar se o coletor de dados está funcionando e se comunicando com a aplicação, acesse `http://localhost:9090/targets`. Nas metricas coloque `app_votos_total` para ver a quantidade de votos entre A e B.

5. **Acessar o Painel Visual no Grafana:** Entre no endereço `http://localhost:3000/` usando as credenciais padrão do sistema (`admin` para usuário e senha) para acessar a interface visual onde é possível criar gráficos e acompanhar os votos em tempo real.
