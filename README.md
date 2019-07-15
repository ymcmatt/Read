# API Template

This Template is designed for Web API used mostly for micro service.

## Clean Structure

This is a structure of the template code.

### api

* .NetCore api
* Biz Test
* Common
* Data

### doc

This is where you put all the documentations at.

### release

* Pipeline
* Terraform

## .NetCore API

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

## Terraform

SQL Server:
WebAppDocker:
WebAppWindows:



## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

See the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc
