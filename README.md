# Dotnet 8 WebAPI with AWS Lambda

This project is an **ASP.NET Core Web API** built with **.NET 8**, designed to run in an **AWS Lambda** environment.

## 🛠 Technologies Used
- **.NET 8** – The latest version with improved performance and advanced features.
- **AWS Lambda** – A platform for running code without managing servers.
- **Amazon API Gateway** – Used for exposing the Web API and routing requests.
- **AWS CLI** – For managing and monitoring cloud processes.
- **Amazon.Lambda.AspNetCoreServer.Hosting** – A package required for hosting ASP.NET Core applications in AWS Lambda.

## 🚀 Installation & Setup

1. Ensure the following tools are installed:
   - **.NET SDK 8**
   - **AWS CLI**
   - **Amazon Lambda Tools** for `dotnet` (install using the following command):
     ```bash
     dotnet tool install -g Amazon.Lambda.Tools
     ```
   - **Amazon.Lambda.AspNetCoreServer.Hosting** (install using NuGet):
     ```bash
     dotnet add package Amazon.Lambda.AspNetCoreServer.Hosting
     ```

2. Restore project dependencies:
   ```bash
   dotnet restore
   ```

3. Build the project:
   ```bash
   dotnet build
   ```

## 🏗️ AWS Lambda Configuration
To enable Lambda hosting in your application, modify the `Program.cs` file as follows:

```csharp
builder.Services.AddAWSLambdaHosting(LambdaEventSource.HttpApi);
```

This ensures that the application correctly handles incoming requests from AWS API Gateway.

## 📄 `aws-lambda-tools-defaults.json`
The `aws-lambda-tools-defaults.json` file contains default settings for deploying the application to AWS Lambda. It includes configurations such as the function name, AWS region, memory size, timeout duration, and other deployment settings. This file simplifies the deployment process by eliminating the need to specify these parameters manually in CLI commands.

## 🚀 Deploying to AWS Lambda
To deploy the function to AWS Lambda, use the following command:

```bash
dotnet lambda deploy-function
```

This process will package your code, ensure it is suitable for cloud execution, and publish it to AWS Lambda.

## 📄 Useful Links
- [AWS Lambda Documentation](https://docs.aws.amazon.com/lambda/latest/dg/welcome.html)
- [ASP.NET Core Web API in .NET 8](https://learn.microsoft.com/en-us/aspnet/core/web-api/?view=aspnetcore-8.0)
- [Amazon.Lambda.Tools](https://github.com/aws/aws-lambda-dotnet)
- [Amazon.Lambda.AspNetCoreServer.Hosting](https://www.nuget.org/packages/Amazon.Lambda.AspNetCoreServer.Hosting)

## ✨ Credits
This project was built to leverage modern cloud development techniques efficiently using the latest technologies.
