# Web Scraping Jogo Bicho

Este projeto é feito para automatizar o processo de extração dos 
resultados do jogo do bicho. Após essa coleta do dados, é realizado o
tratamento e esses são salvos no banco de dados. A consulta dos dados 
se dará através de uma API.

Link da API: 

## Estrutura do web scraping

Site fonte dos dados: Deu no poste

Tag fonte dos dados: tbody, tr

Identificadores das tags: class="twelve"

## Como utilizar

Utilizando as URLs da API, você terá acesso aos dados coletados e algumas outras informações processadas por esse projeto.

Rota principal : http://www.api-leo/bicho

### Endpoints da API


| Método | URL | Descrição|
|--------|---------|------|
| POST| /login | Retorna o token de autenticação do usuário.|
| POST | /resultados/hoje | Retorna o resultado do jogo da data atual. |
| POST | /resultados/hoje/{tipoAposta} | Retorna o resultado do tipo de aposta especificado. |
| POST | /resultados/historicos/partidaPorPeriodo | Retorna o historico dos resultados de uma partida por período  |
| POST| /resultados/historicos/partidaPorPeriodo/{tipoAposta}| Retorna o histórico de resultado de um tipo de aposta num período |

### Convensões
Com o intuito de sanar eventuais dúvidas vou especificar o sentido de alguns termos utilizados nesse projeto.
- Tipo de aposta: São as modalidades possíveis de realizar um aposta no jogo do bicho:
    - Grupo
    - Duque de grupo
    - Passe vai e vem
    - Dezena
    - Passe vai
    - Terno de grupo
    - Duque de dezena
    - Centena
    - Milhar 1 a 5
    - Terno seco
    - Milhar seco
- Seco: Referece a resultados exatos,  populamente chamado de "_na cabeça_". 
- Partida: Referece aos 5 resultados diários publicados no site fonte dos dados.
    - PTM
    - PT
    - PTV
    - PTN
    - COR

