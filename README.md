# WPF Blank .NET Core App with the Northwind Database


In this example, the blank sample project (.NET Core 3.1) is connected to the **Northwind** database.

Database structure:

![](/images/DatabaseStructure.png)

You can use this example to create DevExpress projects and explore our features.

This project includes the [DevExpress ThemedWindow](https://docs.devexpress.com/WPF/DevExpress.Xpf.Core.ThemedWindow) as a root element. Refer to the [Themes](https://docs.devexpress.com/WPF/7406/common-concepts/themes) topic for more information about custom-designed themes.

To create a project and connect it to a database:

1. Create a new project:

    ![](/images/WPF_DotNETCoreProject.png)

2. Select the DevExpress v20.1 WPF Blank App (.NET Core): 

    ![](/images/WPF_DotNETCoreTemplate.png)

3. Specify the Project name and click **Create**:

    ![](/images/WPF_DotNETCoreNamePath.png)

4. Add the `Microsoft.EntityFrameworkCore.SqlServer` and `Microsoft.EntityFrameworkCore.Tools` NuGet packages to the project:

    ![](/images/WPF_DotNETCoreNuGetPackages.png)

5. Open the [Package Manager Console](https://docs.microsoft.com/en-us/nuget/consume-packages/install-use-packages-powershell) and run the following command. This command generates code for a DbContext and entity types for a database:
 
    Scaffold-DbContext "Data Source=(LocalDB)\MSSQLLocalDB;AttachDbFilename=C:\Data\Northwind.mdf;Integrated Security=True" Microsoft.EntityFrameworkCore.SqlServer -OutputDir Models -Context NorthwindEntities -Tables "Categories","Customers","CustomerDemographics","Employees","Orders","Order Details","Products","Region","Shippers","Suppliers","Territories"

Refer to the [https://docs.microsoft.com/en-us/ef/core/miscellaneous/cli/powershell#scaffold-dbcontext](https://docs.microsoft.com/en-us/ef/core/miscellaneous/cli/powershell#scaffold-dbcontext) topic for more information on how to use the **Scaffold-DbContext** command.

Refer to the [https://docs.microsoft.com/en-us/dotnet/core/](https://docs.microsoft.com/en-us/dotnet/core/) topic for more information on how to work with .NET Core.
