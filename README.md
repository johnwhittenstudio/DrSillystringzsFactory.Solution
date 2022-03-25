# ➰  ⚙️ 🧵 🥽  **Dr. Sillystringz's Factory**  🧶 🦺  🛠️ ➿   

#### _a C# MVC many-to-many app to enable a factory manager to add a list of engineers, a list of machines, and specify which engineers are licensed to repair which machines._

#### by John Whitten**

#### March 24, 2022

## Technologies Used

- C#
- .NET 5.0
- REPL
- MySQL
- Razor
- ASP.NET Core

## Description

A many-to-many app to enable a factory manager to keep track of their hired engineers, installed machines, and specify which engineers are licensed to repair which machines.

### Dr. Sillystringz's Factory
_You've been contracted by the factory of the famous Dr. Sillystringz to build an application to keep track of their machine repairs. You are to build an MVC web application to manage their engineers, and the machines they are licensed to fix. The factory manager should be able to add a list of engineers, a list of machines, and specify which engineers are licensed to repair which machines. There should be a many-to-many relationship between Engineers and Machines. An engineer can be licensed to repair (belong to) many machines (such as the Dreamweaver, the Bubblewrappinator, and the Laughbox) and a machine can have many engineers licensed to repair it._

### User Stories
- As the factory manager, I need to be able to see a list of all engineers, and I need to be able to see a list of all machines.
- As the factory manager, I need to be able to select a engineer, see their details, and see a list of all machines that engineer is licensed to repair. I also need to be able to select a machine, see its details, and see a list of all engineers licensed to repair it.
- As the factory manager, I need to add new engineers to our system when they are hired. I also need to add new machines to our system when they are installed.
- As the factory manager, I should be able to add new machines even if no engineers are employed. I should also be able to add new engineers even if no machines are installed
- As the factory manager, I need to be able to add or remove machines that a specific engineer is licensed to repair. I also need to be able to modify this relationship from the other side, and add or remove engineers from a specific machine.
- I should be able to navigate to a splash page that lists all engineers and machines. Users should be able to click on an individual engineer or machine to see all the engineers/machines that belong to it.

### Schema

![Schema](./Factory/wwwroot/img/schema_01.png)

## Project Setup/Installation Instructions

### Install C#, .NET, MySQL Community Server and MySQL Workbench

- Open the terminal on your local machine
- If [C#](https://docs.microsoft.com/en-us/dotnet/csharp/) and [.NET](https://docs.microsoft.com/en-us/dotnet/) are not installed on your local device, follow the instructions here [here](https://www.learnhowtoprogram.com/c-and-net-part-time/getting-started-with-c/installing-c-and-net).
- If [MySQL Community Server](https://dev.mysql.com/downloads/mysql/) and [MySQL Workbench](https://www.mysql.com/products/workbench/) are not installed on your local device, follow the instructions [here](https://www.learnhowtoprogram.com/c-and-net-part-time/getting-started-with-c/installing-and-configuring-mysql).

### Clone the project

- Open the terminal on your local computer.
- Navigate to the parent directory of your preference.
- Clone this project using `$ git clone https://github.com/johnwhittenstudio/DrSillystringzsFactory.Solution`
- Navigate to the directory: `$ cd DrSillystringzsFactory.Solution`
- Open in Vs code: `$ code .`

### Import and connect the database

- Launch the MySQL server with the command `mysql -uroot -p[YOUR-PASSWORD-HERE]`
- After the server starts running, open MySQL Workbench.
- Select the MySQL instance in the _MySQLConnections_ section.
- Select the **Navigator>Administration** tab.
- In the Navigator>Administration window, select **Data Import/Restore**; the Data Import window will open.
- In the **Import Options** section of the Data Import window, select **Import from Self-Contained File**.
- Click the dots at the end of the **Import from Self-Contained** file field (three dots for windows, two dots for Mac) and a pop up box will open. In the pop up box, navigate to the `john_whitten.sql` file in the root directory of the project (BestRest.Solution/). Once correct file is selected, click open. The pop up box will close itself.
- In the **Default Schema to be Imported To**, select the **New** button.
- In the pop up box, name the schema `john_whitten`. Click **Ok**.
- Navigate to the tab called **Import Progress** and click **Start Import** at the bottom right corner of the window.
- After you are finished with the above steps, reopen the **Navigator > Schemas** tab. Right click and select **Refresh All**. Your new test database will appear.
- Navigate to BestRest: `$ cd Factory` and type the following command in the terminal `$ touch appsettings.json`
- In the appsettings.json file enter the following code:

```
{
    "ConnectionStrings": {
        "DefaultConnection": "Server=localhost;Port=3306;database=john_whitten;uid=root;pwd=[YOUR-PASSWORD-HERE];"
    }
}
```

### Run the project

- Navigate to BestRest: `$ cd Factory` and type the following command in the terminal `$ dotnet restore`
- Build the program with the command `$ dotnet build`
- Run the program with the command `$ dotnet run`

## Known Bugs

- _None._

## License

[MIT License](https://opensource.org/licenses/MIT) © 2022 _John Whitten_

## Contact

John Whitten: [johnwhitten.studio@gmail.com](mailto:johnwhitten.studio@gmail.com)
