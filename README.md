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


## 1. Baixando os arquivos necessários no github e criando meu diretório público
1.1 - Entre no repositório que contém o site: https://github.com/GoogleCloudPlatform/microservices-demo 

1.2 - Crie um repositório e coloque somente o arquivo release/kubernetes-manifests.yaml

## 2. Instalando o Rancher Desktop
2.1 - Baixe o instalador do site oficial: https://rancherdesktop.io
2.2 - Instale o rancher depois de baixar o instalador.
2.3 - Depois de instalar  configure o Rancher Desktop 
2.4 - Vá em Settings → WSL Integration, ative o Ubuntu que você usa no WSL
2.5 - Isso fará com que o kubectl, nerdctl e o contexto Kubernetes do Rancher Desktop fiquem disponíveis dentro do Ubuntu.

## 3. Instalando o ArgoCD
3.1 - Crie uma namespace chamada argocd:
``` kubectl create namespace argocd ```

3.2 - Instale o argocd:

```kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml ```

3.3 - Instale o CLI do argoCD no linux, digite os seguntes comandos:

```curl -SSL -o argocd https://github.com/argoproj/argo-cd/releases/latest/download/argocd-linux-amd64```

```chmod +x argocd ```

```mv argocd /usr/local/bin/ ```
