INSTRUCOES: 
Clonar o Repositório

Iniciar os Contêineres
docker-compose up -d
Backend: http://localhost:3020
Frontend: http://localhost:8080
Proxy Reverso: http://localhost:8081

Simular Falhas no Backend

docker stop <repescagemm>

Induzir Erros:
Altere o código do backend para lançar erros, recompile e teste o impacto:
docker-compose up --build

Parar o Sistema
docker-compose down




