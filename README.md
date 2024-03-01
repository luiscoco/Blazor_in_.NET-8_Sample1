# Blazor in .NET 8: Sample 1

Let's create a basic Blazor Server project.

**Prerequisites**:

- Install .NET 8 SDK (https://dotnet.microsoft.com/en-us/download/dotnet/8.0)

- A code editor like Visual Studio, Visual Studio Code, or Rider.

**Create Project**:

Open a terminal and run. This creates a project named "MyBlazorApp":

```
dotnet new blazorserver -o MyBlazorApp
```

**Basic Component**:

Navigate to your project folder

In the Pages folder, create a new file named Counter.razor

Add the following code to the Counter.razor file:

```cshtml
@page "/counter"

<h1>Counter</h1>

<p>Current count: @currentCount</p>

<button class="btn btn-primary" @onclick="IncrementCount">Click me</button>

@code {
    private int currentCount = 0;

    private void IncrementCount()
    {
        currentCount++;
    }
}
```

**Run the Project**:

From the terminal, inside your project folder, run: 

```
dotnet run
```

Open a web browser and go to http://localhost:5000/counter (or a similar port)

You should see your counter component

**Explanation**:

**@page "/counter"**: This directive marks the component as a routable page

**HTML Markup**: Standard HTML to display a heading, the current count, and a button

**@onclick="IncrementCount"**: The @onclick attribute binds the IncrementCount method to the button's click event

**@code {...}**: This block holds the C# code for your component's logic

