# Hahn.ApplicatonProcess.Application
Hahn.ApplicatonProcess.Application is a set of APIs and front end to save an application.

# Features!
  - POST, PUT, DELETE or GET APPLICANT data.
  - Functional Tests to test all functionality.
  - Swagger API to validate API functionality.
  - Logging
  - Aurelia based UI
  - Client Side & Server side validation
  - Built with Visual Studio 2019 community edition

### Tech
Hahn.ApplicatonProcess.Application uses a number of open source technology stacks:
* .net core 3.1 - Microsoft's open source, cross platform, light weight technology stack !
* Entity Framework Core In Memory DB : In memory DB, fast development platform
* Swagger - Open source API documentation and development tool
* xUnit - Free, open source testing framework for unit and functional tests
* Serilog - Diagnostic logging to files, the console, and elsewhere. Used for service
* Aurelia - Front end SPA framework
* Uses Aurelia i18N internationalization - setting available in main.ts file as "de" currently.

### Installation of published code
Hahn.ApplicatonProcess.Application requires .net framework core 3.1 runtime. Published code folder can be hosted on IIS.
### Debugging with Visual Studio on Development environment
``` From the Visual Studio solution -- for development environment.
$ Hahn.ApplicatonProcess.Application is developed with Visual Studio 2019 community edition 
$ open Hahn.ApplicatonProcess.Application.sln
$ restore dot net packages - Run "dot net restore" command
$ restore packages in client app folder > Run "yarn" command
$ Build entire solution
$ Right click solution --> Properties --> Build. 
    Check XML documentation path is ..\..\..\swaggerHahn_API.xml
$ select Hahn.ApplicatonProcess.May2020.Web as startup project. Click Start
$ Swagger UI page opens with API list. Details mentioned in software help document 
$ To View and Run Tests --> Open Test --> Test Explorer. Click run all tests 
$ Right click Hahn.ApplicatonProcess.May2020.Web > Properties > Debug. 
App Url: http://localhost:60000
Swagger is available at http://localhost:60000/swagger
```

### Testing
API has been extensively tested with Swagger UI created along side API. Example is available in swagger UI which can be copy pasted. 

### API Endpoints 
#### Auth means Authorization header bearer token is required 
| Endpoint | HttpMethod | Auth | Function |
| ------ | ------ |------ | ------ |
| /swagger | Get | No | Swagger UI API Url page |
| /api/Applicants/{id} | Get | No | Gets applicant by Id - default 1 and 2 |
| /api/Applicants/{id} | Put | No | Put data for Id - 1 or 2 by default |
| /api/Applicants/{id} | Delete | No | Delete applicant by Id |
| /api/Applicants | Post | No | Create a new record |

### Points to Note
$ As each check is created, dummy data for applicants is created.
$ No oAuth server, authentication or authorization is setup at this stage of application development.
$ Application has no email sending capability.
