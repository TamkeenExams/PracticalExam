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
    If you are running the solutino for the first time Entity Framework will go ahead and create the database objects in the server where the connection string (in appsettings.json) is pointing to, you should configure the connection string before pressing CTRL+F5. 
</p>
