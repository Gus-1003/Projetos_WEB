# AULA 1: (Protocolo HTTP)

## Protocolo HTTP (Hypertext Transfer Protocol - ProtocOLO): 
    - Conjunto de regras/padrões para enviar pacotes de informações pela rede ethernet;
    - Protocolo de transfêrencia de Hipermédia;
    - Roda sobre TCP/IP;
    - Importancia: Serve para dar uma base para os mais variados ambientes, softwares e tipos de clientes;
      * Essencial para uma comunicação viavel entre o cliente (Emissor)  e um servidor (Receptor);

## Localilizado do protocolo: 
    - Camada de Aplicação do modelo OSI;
      * UDP: 
        + Não necessita de conexão
        + Não possui controle de erro
        + É mais simples e mais rápido
        Aplicação: streaming de voz ou de vídeo
      * TCP: 
        + Orientado a Conexão
        + Possui um controle de Erro
        + Garante a entrega
        + Entrega ordenada	

## Comunicação Cliente - Servidor
    - Cliente Web = Aparelho que consegue fazer requisições atraves do protocolo;
    - Servidor Web = Maquina que recebe a solicitação e prepara uma resposta;

## Tipos de mensagem:
    - Requisição (Cliente) - Solicitação com base nas reações do usuário;
      * Obs.: Ao receber a resposta do servidor o Browser tera o papel de interpreata a resposta e exibi ao cliente; 
    - Resposta (Servidor) - A partir da solicitação o servidor vai processar a mensagem e responder de forma adequada;

## Componente estruturais da mensagem:
    - Startline (Linha inicial):
      * Requisição:
        + Método HTTP;
          # GET (Buscar algo no servidor)
          # POST (Enviar algo para o servidor)
          # HEAD
          # PUT
          # DELETE
          # TRACE
          # OPTIONS
          # CONNECT
        + URL / URI (Endereço);
        + Versão do protolo HTTP;
      * Resposta:
        + Versão do protolo HTTP;
        + Código da resposta;
        + Texto desse código;
        
    - Headers (Cabeçalho):
      * Requisição:
        + Accept: Tipo de conteudo;
        + Accept: Detalhamento do conteudo; (Optativo)
        + Linha em branco;
      * Resposta:
        + Content-Type (nome) : Valor do cabeçario;
        + Content-Length;
        + Linha em branco;
        
    - Body (Corpo) (Opicional):
      - HTML;
      - Imagens / Audios;
      - JS;
      - Objetos CML;
      - Objetos JSON;
      .......

## Códigos de resposta (Faixas de Status):
    - Linha inicial de uma resposta HTTP;
    
    - 1XX = Informacional
    
    - 2XX = Sucesso
      * ex.: 200 = Comunicação realiza com sucesso;
      
    - 3XX = redirecionamento
    
    - 4XX = Erro de cliente
      * ex.: 404 = Erro de conexão com um servidor inexistente;
      
    - 5XX = Erro de servidor
      * ex.: 500 = Solicitação travou / confundiu o servidor;
      * ex.: 503 = Serviço não disponivel (Uso do método errado);

## Conceitos Importantes:
    - Sessão HTTP
      * Espaço de mémoria temporario criado pelo servidor para um que aja uma comunicação com determinado cliente;
      * Problema: Se houver mais clientes que espaços vagos pessoas ficarão impossibilitadas de se comunicar com o servidor;
        + Solução: Adicionar mais mémoria ao servidor (Exige recusos, principalmente espaço físico)
      * Geralmente utilizada a porta 80;
    - Cookies
      * Dados de comunicação cliente e servidor que persistem no aparelho;
      * Guardam informações entre conexões anteriores;
        + Ex.: Te mantem logado em páginas;
        + Ex.: Da a possibilidade de criar um perfil de compra para o usuario; 
