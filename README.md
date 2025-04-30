# Dotnet 8 WebAPI with AWS Lambda

This project is an **ASP.NET Core Web API** built with **.NET 8**, designed to run in an **AWS Lambda** environment.

## 🛠 Technologies Used
- **.NET 8** – The latest version with improved performance and advanced features.
- **AWS Lambda** – A platform for running code without managing servers.
- **Amazon API Gateway** – Used for exposing the Web API and routing requests.
- **AWS CLI** – For managing and monitoring cloud processes.

## 🚀 Installation & Setup

1. Ensure the following tools are installed:
   - **.NET SDK 8**
   - **AWS CLI**
   - **Amazon Lambda Tools** for `dotnet` (install using the following command):
     ```bash
     dotnet tool install -g Amazon.Lambda.Tools
     ```

2. Restore project dependencies:
   ```bash
   dotnet restore
   ```

3. Build the project:
   ```bash
   dotnet build
   ```

## 🏗️ Deploying to AWS Lambda
To deploy the function to AWS Lambda, use the following command:

```bash
dotnet lambda deploy-function
```

This process will package your code, ensure it is suitable for cloud execution, and publish it to AWS Lambda.

## 📄 Useful Links
- [AWS Lambda Documentation](https://docs.aws.amazon.com/lambda/latest/dg/welcome.html)
- [ASP.NET Core Web API in .NET 8](https://learn.microsoft.com/en-us/aspnet/core/web-api/?view=aspnetcore-8.0)
- [Amazon.Lambda.Tools](https://github.com/aws/aws-lambda-dotnet)

## ✨ Credits
This project was built to leverage modern cloud development techniques efficiently using the latest technologies.
