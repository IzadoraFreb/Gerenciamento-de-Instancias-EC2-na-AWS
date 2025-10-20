# Caso de uso: Interação entre sistema, EC2, EBS, Lambda e S3
---
### Este caso representa um fluxo simples de interação entre um sistema externo e serviços da AWS, com foco em processamento, armazenamento e automação.
### Um sistema envia dados para uma instância EC2 hospedada na AWS Cloud. A instância EC2 é responsável por receber e processar esses dados. 
### O armazenamento inicial ocorre em um volume EBS, que funciona como o disco da instância.
### A aplicação que roda na EC2 pode conter uma lógica que verifica se os dados atendem a determinados critérios. Quando essa condição(trigger) é satisfeita, uma função Lambda é acionada. Essa função executa uma tarefa específica, como enviar os dados para um bucket S3.
### O S3 é utilizado para armazenar os dados de forma persistente e escalável, permitindo acesso posterior, compartilhamento ou integração com outros serviços.
---
## Esse fluxo é útil em cenários onde é necessário processar dados localmente na EC2, manter controle sobre o armazenamento temporário via EBS e automatizar o envio para o S3 com base em regras definidas.
