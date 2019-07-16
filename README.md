# API Template

This Template is designed for Web API used mostly for micro service.

## Clean Structure
Graph + Link
This is a structure of the template code.

### api

* [.NetCore api](#netcore-api)
* [Biz Test](#biz)
* [Common](#common)
* [Data](#data)

### doc

This is where you put all the documentations at.

### release

* [Pipeline](#pipeline)
* [Terraform](#terraform-scripts)

## NetCore API

Provide a basic Template for .NetCore API with an API controller

```
[HttpGet]
[HttpGet("{id}")]
[HttpPost]
```
Also provide basic configuration file for a .NetCore API project

## Biz

Provide a basic Business Ordering System Framwork involving various Order Services like

```
IList<OrderVM> GetAllOrders();
OrderVM GetOrderById(int orderId);
void UpdateOrder(OrderVM orderVm);
```
and its corresponding test file BizTest
## Common

Provide some basic Error Handling functions and Key Vault Services for example
```
BizCustomException
KeyValutService
```

## Data

Provide you the basic model to create object table in database about Order, OrderProduct and Product (each with some common parameters)

## Pipeline

Provide you a publish and resource pipeline, each with three possible Azure Services Template
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

## Terraform Scripts

Likewise, it provides a terraform script to manage Azure on all three Azure Services (aks,WebDocker and WebApp). But only the one you choose will actually be used.

## Versioning

This is under Version 1.0

## Authors

See the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

