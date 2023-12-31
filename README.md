<h1 align="center">Welcome to Terraformando o EKS 👋</h1>
<p>
  <img alt="Version" src="https://img.shields.io/badge/version-v0-blue.svg?cacheSeconds=2592000" />
  <a href=".docs/" target="_blank">
    <img alt="Documentation" src="https://img.shields.io/badge/documentation-yes-brightgreen.svg" />
  </a>
  <a href="LICENSE" target="_blank">
    <img alt="License: MIT" src="https://img.shields.io/badge/License-MIT-yellow.svg" />
  </a>
  <a href="https://twitter.com/fidelissauro" target="_blank">
    <img alt="Twitter: fidelissauro" src="https://img.shields.io/twitter/follow/fidelissauro.svg?style=social" />
  </a>
</p>

> Codebase da série de videos Terraformando o EKS no Youtube

### 🏠 [Guia](/)

* **Aula #00 - Conceitos básicos e VPC** - [Exemplos](https://github.com/msfidelis/terraformando-eks/tree/aula00_vpc) - [Video](https://www.youtube.com/watch?v=-ghbb9PyGxY)

* **Aula #01 - Terraformando o EKS Cluster** - [Exemplos](https://github.com/msfidelis/terraformando-eks/tree/aula01_eks) - [Video](https://www.youtube.com/watch?v=-ghbb9PyGxY)

* **Aula #02 - Node groups** - [Exemplos](https://github.com/msfidelis/terraformando-eks/tree/aula02_nodes) - [Video](https://www.youtube.com/watch?v=kXqiqZ5Nap8)

* **Aula #03 - Traefik no EKS** - [Exemplos](https://github.com/msfidelis/terraformando-eks/tree/aula03_traefik) - [Video](https://www.youtube.com/watch?v=ThONqZT2Mfs&t=9s)

* **Aula #04 - Auto Scale do Cluster** - [Exemplos](https://github.com/msfidelis/terraformando-eks/tree/aula04_scale) - [Video](https://www.youtube.com/watch?v=tYikrqYRAaQ)

### ✨ [Demo](/)

## Instalação

```sh
terraform init
```
## Validação de sintaxe 

```sh
terraform validate
```
## Formatação/indentação de código

```sh
terraform fmt
```
## Aplicando

```sh
terraform apply --auto-approve
```

## Validação

```sh
terraform validate
```

## Adicionando o contexto do nosso cluster ao kubectl

```bash
aws eks --region us-east-1 update-kubeconfig --name nome-do-cluster
aws eks --region us-east-1 update-kubeconfig --name k8s-demo
```

```bash
kubectl get nodes
```

## Deploy o Ingress

```bash
kubectl apply -f kubernetes/traefik/ingress.yml
```

## Deploy demo services

* [Whois App](https://github.com/msfidelis/microservice-nadave-whois)
* [Faker App](https://github.com/msfidelis/microservice-nadave-fake-person)
* [Pudim](https://github.com/msfidelis/pudim)

```bash
kubectl apply -f kubernetes/apps/whois.yml
kubectl apply -f kubernetes/apps/faker.yml
kubectl apply -f kubernetes/apps/pudim.yml
```

## Deploy do Metric Server

```bash
kubectl apply -f kubernetes/metric-server/metric-server.yml
```

## Author

👤 **Matheus Fidelis**

* Website: https://raj.ninja
* Twitter: [@fidelissauro](https://twitter.com/fidelissauro)
* Github: [@msfidelis](https://github.com/msfidelis)
* LinkedIn: [@msfidelis](https://linkedin.com/in/msfidelis)

## 🤝 Contributing

Contributions, issues and feature requests are welcome!<br />Feel free to check [issues page](/issues). 

## Show your support

Give a ⭐️ if this project helped you!

## 📝 License

Copyright © 2020 [Matheus Fidelis](https://github.com/msfidelis).<br />
This project is [MIT](LICENSE) licensed.

***
_This README was generated with ❤️ by [readme-md-generator](https://github.com/kefranabg/readme-md-generator)_