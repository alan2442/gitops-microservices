# Projeto 3 Compass.uol

# Objetivo do Projeto:
Executar um conjunto de microserviços (Online Boutique) em Kubernetes local usando 
Rancher Desktop, controlado por GitOps com ArgoCD, a partir de um repositório público 
no GitHub. 

# Requisitos:
• Rancher Desktop  
• Kubectl configurado (kubectl get nodes funcionando) 
• ArgoCD instalado no cluster 
• Conta no GitHub com repositório público 
• Git instalado 
• Docker funcionando localmente 


# 1. Baixando os arquivos necessários no github e criando meu diretório público
1.1 - Entre no repositório que contém o site: https://github.com/GoogleCloudPlatform/microservices-demo 

1.2 - Crie um repositório e coloque somente o arquivo release/kubernetes-manifests.yaml

# 2. Instalando o ArgoCD
2.1 - Crie uma namespace chamada argocd:
``` kubectl create namespace argocd ```
