# Simulator Configuration APP

This project contains all the UI Code for SimLocal Web App

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

```
1. Install Visual Studio 2017 and above.
2. Install .net Framework 4.6 (This comes by default with Visual Studio 2017).
3. SQL Express 2017 with instance name localhost\sqlexpress and Integrated Security as true(Install with management studio for quering database).
4. TortoiseGit (Optional for better and easy git exprience).
5. Install Microsoft WinAppDriver v1.0 from link https://github.com/Microsoft/WinAppDriver/releases/tag/v1.0 for E2E test. (This requires Windows 10)
```

### Installing

A step by step series of examples that tell you how to get a development env running


```
1. Open Command Prompt and move to the folder where you want to checkout travel win repository. Run below command to clone the repo to your local if not already done.
git clone https://github.com/TravelWin/TravelWinRepo.git

2. Open Sql Server Management studio and connect to localhost\sqlexpress. Open "New Query Window" and select database "SIMulatorDB" and execute query 
"update AspnetUsers set Email = 'type in you email here', PasswordHash = 'ALXUC9yVauOaI+uUFRhtEXOTzQYdrJZHUJT8atnXyXNfZ7eCx/VluorWZiRQX8HPsw==' where Email = 'kerrie.mcgarvey@travelwin.com'". 
Now these credentials can be used to login to Simulator Configuration Web App. Your password to login is "abc12345#"

3. Open Project Src\Platform\Tools\Cryptography.WinUI\Cryptography.WinUI.sln in visual studio and run the project. Select "Simulator Database" in dropdown.
Put your mac address in "ENTER DATA TO ENCRYPT" field (Without spaces and hashes) and click on encrypt button. Open file "SimSLCM-Add-MacAddres.sql".
Go to line 26 and replace it with this "SET @clientDeviceName = 'test.simpos.yournamehere-work';" (replace yournamehere with your name)
Go to line 35 and replace it with "SET @encryptedMacAddress = 'put your encrypted mac address here';"
Save the file open in SQL Server Management Studio and select "SIMulatorDB" and execute it.

4. Open the solution "TravelWinRepo\Src\SIMulator\Api.WebApi\SIMulator.WebApi.sln" in visual studio expand folder "Application Layer" right click on "SIMulator.WebAPI" project and select Set as Startup Project.
Run the project. You must run this project inorder to run the Configuration Web App.

5. Open the solution "TravelWinRepo\Src\SIMulator\ConfigurationManager.WebUi\SIMulator.ConfigurationManager.WebUi.sln"
Run the project. 

Login with your email address and abc12345# password.

Happy Coding!
```

## Running the tests

Explain how to run the automated tests for this system

### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **John Rowan** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc
