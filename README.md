# API Template

This Template is designed for Web API used mostly for micro service.

![structure](https://github.com/ymcmatt/Read/blob/master/Capture3.PNG)

## Clean Structure
Graph + Link
This is a structure of the template code.

### api

* [.NetCore api](#netcore-api)
* [Biz](#biz)
* [Biz Test](#biztest)
* [Common](#common)
* [Data](#data)

### doc

This is where you put all the documentations at.

### release

* [Pipeline](#pipeline)
  - resource
  - publish
* [Scripts](#terraform-scripts)
  - terraform
  - powershell

## NetCore API

expose web API on .NetCore with API controller

```
OrderController.cs
```
Also provide basic configuration file for a .NetCore API project

## Biz

Biz layer contains basic business logic with service interface.

```
IOrderService.cs
```

## BizTest

BizTest layer contains unit test for business logic, eg

```
TestOrderService.cs
```

## Common

Provide some basic Utility functions like Error Handling functions and Key Vault Services 
```
loginstorage
redis cache
```

## Data

Data layer bases on .NetCore entity framework to connect with SQL server.


## Pipeline

#### Resource Pipeline

Provide you a resource pipeline, each with three possible Azure Services Template
```
aks
webApp
WebAppDocker
```
Yet, only the azure Service you choose on MSE Portal will actually work for the pipeline Building. The rest are merely templates created. You can also change the Azure Service and change the path under Pipeline to choose the Azure Service you want.

Each Azure Service has three template environments.

```
dev-pipeline
prod-pipeline
test-pipeline
```



#### Publish Pipeline

Provide you a publish pipeline. Structure is exactly the same as resource pipeline.

## Scripts

#### Terraform Scripts

Likewise, it provides a terraform script to manage Azure on all three Azure Services (aks,WebDocker and WebApp). But only the one you choose will actually be used.

The template file contains a number of terraform templates under different system, where you can modify to use according to your needs.

(p.s. main.tf is where the actual function take place. vars.tfvars is only a file that declares certain varaibles used in main.tf)



#### Terraform Scripts

It provides some basic powershell scripts for developers whom prefer powershell over terraform.

```
deployDatabase.ps1
getAzureResource.batch
updateRepositoryValue.ps1
```

## Versioning

This is under Version 1.0

## Authors

See the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

