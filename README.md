# Desafio Ília

Neste desafio, como solicitado devo demonstrar suas habilidades de DevOps utilizando AWS e as ferramentas Terraform, Kubernetes, Helm Charts e Grafana​:

    ​✓ Usar o Terraform para criar um cluster Kubernetes na AWS. Você deverá configurar o cluster de forma ​segura, escalável e eficiente.​
    
    ✓ Usar o Helm Charts para instalar e configurar um Grafana no cluster Kubernetes. Você deverá​ personalizar o Grafana de acordo com as necessidades.​

    ​✓ Criar um AWS Timestream ou Athena e adicionar dados de teste no mesmo.​
    
    ✓ Adicionar o datasource do AWS Timestream ou Athena no Grafana e mostrar os dados do Timestream ou ​Athena por meio de algum dashboard. Você deverá criar gráficos, tabelas e painéis que apresentem 
      as informações de forma​ clara e intuitiva.​

    ​✓ Prover observabilidade dos recursos criados durante o desafio. Você deverá monitorar o desempenho, a​ disponibilidade e o consumo dos recursos.​

# Desenho Visão Geral da Solução

![Captura de tela 2024-02-11 161503](https://github.com/crisbol27091973/desafioilia/assets/48601776/31479efb-aee5-4c56-a9f9-f2d085d15e2b)


# Primeiro passo do Desafio Ília

​✓ Usar o Terraform para criar um cluster Kubernetes na AWS. Você deverá configurar o cluster de forma ​segura, escalável e eficiente.​

    Terraform EKS (Elastic Kubernete Service)

      Arquivos do Terraform EKS:

          1. exemplo-completo.tf - Exemplo completo com VPC e EKS cluster 
          2. iniciar-exemplo.tf - DIY inicar exemplo com VPC (adicionar seu próprio código EKS)

# Segundo passo do Desafio Ília

✓ Usar o Helm Charts para instalar e configurar um Grafana no cluster Kubernetes. Você deverá​ personalizar o Grafana de acordo com as necessidades.​

 	  Arquivos do Helm Charts:

          1. helm-chart-passos-instalar-configurar.txt - Comandos da instlalação do Grafana ou Prometheus


# Terceiro passo do Desafio Ília

 ​✓ Criar um AWS Timestream ou Athena e adicionar dados de teste no mesmo.​

 		Passo a Passo da minha criação do AWS AThena e adição dos dados de teste do mesmo:

            Passo 01 - Criação dos dados de teste para serem adicionados no Banco de Dados AWS Athena:

                Foram criados dois buckets: s3-bucket-athena-desafioilia e s3-bucket-athena-desafioilia-saida no Amazon S3. 
                O bucket: s3-bucket-athena-desafioilia foi criado para adicionar os quatros arquivos json e com eles serem criada uma tabela no Banco de Dados AWS Athena.
                Já o bucket: s3-bucket-athena-desafioilia-saida foi criado para receber as informações que serão criadas pelas consultas criadas com a tabela do Banco de Dados AWS Athena.

                Evidência da tela de criação do BUckets: s3-bucket-athena-desafioilia e s3-bucket-athena-desafioilia-saida segue abaixo:

![image](https://github.com/crisbol27091973/desafioilia/assets/48601776/d7cab6fd-39bf-4e94-83c9-53425f5358e1)


                
            
        
        
