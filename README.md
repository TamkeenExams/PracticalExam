# PracticalExam

This Repo is dedicated to the Practical Exam's service. The first step to get the underlining code up and running is to download the zip file named "EmployeesTamkeenAPI.zip", extract it, then launch the project solution file using Visual Studio 2022. (problems may arise if attempting to launch the solution file with older versions of Visual Studio).

The API services's solution contains various components that need to be set up first as follows:
1. Entity Framework components that need to be add first via NuGET package manager. Right click on the solution explorer, click "Manage NuGet packages for solution", in the search box type "Entity Framework", click on the search result and choose install. (important: make sure that the version of the .NET framework is compatible with Entity framework's version).

2. Make sure that Swagger UI is configured to run the APIs in development (swagger is a tool that uses OpenAPI specifications to easily lauch and browse and test REST APIs), to do this go the program.cs and make sure it has something that looks like this:
<code>if (app.Environment.IsDevelopment())
{
    app.UseSwagger();
    app.UseSwaggerUI();
}</code>

3. Run the solution: press CTRL+F5, this should load the services API in your browser (using swagger).

<p>
    If you are running the solution for the first time Entity Framework will go ahead and create the database objects in the server where the connection string (in appsettings.json) is pointing to, you should configure the connection string before pressing CTRL+F5. In this case, it will create dbo.Products table in the local database. 
</p>

4. In Swagger UI browse and test all 4 CRUD operations with ease. 

5. Authentication: Although I understand claims based security and federation authenticaion, the concepts of the JWT framework are totally new to me, I have not been coding for almost 5 years and this framework was not around back then. Therefore I would like to be frank and save the reviewer's time by saying that I couldn't do the JWT part. My apologies.
