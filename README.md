# 🚀 Instalação do Minikube e Helm 🚀

Este guia fornece instruções passo-a-passo para instalar o Minikube e o Helm no Linux e no macOS.

## 1. Instalação do Minikube
O Minikube permite que você execute o Kubernetes localmente em uma máquina virtual.

### Linux

1. Baixe o binário do Minikube:

    ```bash
      curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
    ```

2. Instale o Minikube:

    ```bash
      sudo install minikube-linux-amd64 /usr/local/bin/minikube && rm minikube-linux-amd64
    ```

### macOS

1. Baixe o binário do Minikube:

    ```bash
      curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-darwin-arm64
    ```

2. Instale o Minikube:

    ```bash
      sudo install minikube-darwin-arm64 /usr/local/bin/minikube
    ```

### Verificando a instalação

Execute o comando abaixo para verificar se o Minikube foi instalado corretamente:

  ```bash
    minikube version
  ```

## 2. Instalação do Helm
O Helm é um gerenciador de pacotes para Kubernetes que simplifica a instalação e o gerenciamento de aplicativos.

### Linux

1. Baixe o script de instalação do Helm:

    ```bash
      curl -fsSL -o get_helm.sh https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3    
    ```
2. Dê permissão de execução ao script:

    ```bash
      chmod 700 get_helm.sh
    ```

3. Execute o script:

    ```bash
      ./get_helm.sh
    ```

### macOS
Use o Homebrew para instalar o Helm:

  ```bash
    brew install helm
  ```
#### Verificando a instalação
Execute o comando abaixo para verificar se o Helm foi instalado corretamente:

```bash
  helm version
```

🎉 **Parabéns!** Você instalou com sucesso o Minikube e o Helm. Agora você pode iniciar seu cluster Kubernetes local e começar a implantar aplicativos com o Helm. 🎉

## Próximos passos

- Inicie o Minikube: `minikube start`
- Explore o dashboard do Kubernetes: `minikube dashboard`
- Adicione repositórios de Charts do Helm: `helm repo add <NOME_DO_REPOSITORIO> <URL_DO_REPOSITORIO>`
- Instale seu primeiro aplicativo com o Helm: `helm install <NOME_DO_APP> <NOME_DO_CHART>`

## Recursos adicionais

- [Documentação do Minikube](https://minikube.sigs.k8s.io/docs/)
- [Documentação do Helm](https://helm.sh/docs/)

## Dicas

- Use o `minikube addons enable ingress` para habilitar o ingress no seu cluster Minikube.
- Explore os comandos `helm search`, `helm show` e `helm list` para encontrar e gerenciar Charts.
- Utilize o `helm create` para criar seus próprios Charts.



