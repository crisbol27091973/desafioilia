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

          1. helm-chart-passos-instalar-configurar.txt - Comandos da instalação do Grafana ou Prometheus


# Terceiro passo do Desafio Ília

 ​✓ Criar um AWS Timestream ou Athena e adicionar dados de teste no mesmo.​

 Passo a Passo da minha criação do AWS Athena e adição dos dados de teste do mesmo:

 Passo 01 - Criação dos dados de teste para serem adicionados no Banco de Dados AWS Athena:

 Foram criados dois buckets: s3-bucket-athena-desafioilia e s3-bucket-athena-desafioilia-saida no Amazon S3. 
 O bucket: s3-bucket-athena-desafioilia foi criado para adicionar os quatros arquivos json e com eles serem criada uma tabela no Banco de Dados AWS Athena.
 Já o bucket: s3-bucket-athena-desafioilia-saida foi criado para receber as informações que serão criadas pelas consultas criadas com a tabela do Banco de Dados AWS Athena.

Evidência da tela de criação dos dois Buckets: s3-bucket-athena-desafioilia e s3-bucket-athena-desafioilia-saida segue abaixo:

![image](https://github.com/crisbol27091973/desafioilia/assets/48601776/d7cab6fd-39bf-4e94-83c9-53425f5358e1)

Evidência da tela do Bucket: s3-bucket-athena-desafioilia onde os arquivos json foram adicionados segue abaixo:

![image](https://github.com/crisbol27091973/desafioilia/assets/48601776/0cf5ff72-9820-427a-8375-ff64f138589f)

Evidência da tela do Bucket: s3-bucket-athena-desafioilia-saida onde ficam informações das consultas realizadas nos dados do Bucket: s3-bucket-athena-desafioilia-saida segue abaixo:

![image](https://github.com/crisbol27091973/desafioilia/assets/48601776/257dc515-114a-439c-93ea-cd75947831f9)

Passo 02 - Transformação dos dados de teste (arquivos json) em formato de tabela no Banco de Dados AWS Athena:

Foi criado um Grupo de Trabalho (Workspace): JsonConsulta para posterior criação da tabela dos arquivos json.

Evidência da tela de criação do Grupo de Trabalho: JsonConsulta baseado no Bucket: s3-bucket-athena-desafioilia-saida segue abaixo:

![image](https://github.com/crisbol27091973/desafioilia/assets/48601776/53d955de-0577-41b3-a047-6929265d3f56)

Evidência da tela de criação do Banco de Dados Athenas: s3jsontabelabd para criação da tabela: s3jsontabela segue abaixo:

![image](https://github.com/crisbol27091973/desafioilia/assets/48601776/7598e0f3-b5b5-4cb5-8cbc-869902864443)

Evidência da tela de criação da tabela: s3jsontabela criada no Banco de Dados Athenas: s3jsontabelabd segue abaixo:

![image](https://github.com/crisbol27091973/desafioilia/assets/48601776/c394ad35-6b6e-4821-9d0f-943da727386a)

Evidência da tela de consultas a tabela: s3jsontabela criada no Banco de Dados Athenas: s3jsontabelabd segue abaixo:

![image](https://github.com/crisbol27091973/desafioilia/assets/48601776/f2a05b38-1b2e-43bf-8fec-337f7a7b030e)

# Quarto passo do Desafio Ília

 ✓ Adicionar o datasource do Amazon Timestream ou Amazon Athena no Grafana e mostrar os dados do Timestream ou ​Athena por meio de algum dashboard. Você deverá criar gráficos, tabelas e painéis que apresentem as informações de forma​ clara e intuitiva.​

Evidência da tela onde ligampos o datasource: JsonConsulta ao Athena no Grafana segue abaixo:

![image](https://github.com/crisbol27091973/desafioilia/assets/48601776/8a78fc30-eca7-4498-986c-60d40978023a)

Evidência da tela de configuração do Grafana com a minha conta AWS ativada aos serviços do Grafana segue abaixo:

![image](https://github.com/crisbol27091973/desafioilia/assets/48601776/016d3264-6e0c-4535-bb16-015f1c82af0d)

Evidência da tela de Fonte de Dados do Grafana com a minha conta AWS ativada aos serviços do Grafana pronto para usar Amazon Timestream ou Amazon Athena segue abaixo:

![image](https://github.com/crisbol27091973/desafioilia/assets/48601776/a2f87f2a-57bb-4335-8298-37a548ff4e63)


                
            
        
        
