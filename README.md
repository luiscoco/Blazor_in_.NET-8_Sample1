# Blazor in .NET 8: What is Blazor?

Blazor is a component based **SPA(Single Page Application)** that achieves interactiviy with C#

See also this video in youtube: https://www.youtube.com/watch?v=gq1ySblcyA8

![image](https://github.com/luiscoco/Blazor_video1/assets/32194879/27ce5b9f-874e-4a04-be45-eaca8dc9d896)

## 1. What is Blazor?

Blazor is a powerful web framework from Microsoft that lets you build interactive web applications using C# instead of relying solely on JavaScript. Here's why it's interesting:

**C# Everywhere**: If you know C#, you can build both the frontend (what the user sees) and backend (server-side logic) of your web applications

**Component-Based Architecture**: Similar to modern JavaScript frameworks like React or Vue, Blazor uses components as building blocks. These components encapsulate UI elements, logic, and reusability

**Flexibility**: Blazor offers two main flavors:

**Blazor Server**: Your components run on the server, and UI updates are sent to the browser over a real-time connection (SignalR). Excellent for fast initial page load and real-time applications

**Blazor WebAssembly (Wasm)**: Your components run directly in the browser using WebAssembly (a low-level, high-performance code format). Great for offline capabilities and reducing server load

**.NET 8 Enhancements**

**Static Server-Side Rendering (SSR)**: Render your Blazor components into static HTML on the server for lightning-fast first-page loads and improved SEO

**Streaming Rendering**: Start sending HTML to the browser before the entire page is fully rendered, resulting in quicker perceived loading times

**Enhanced Navigation and Forms**: More control over navigation and form handling

**Auto Mode Interactivity**: Components can intelligently switch between Blazor Server and Blazor WebAssembly based on specific needs

## 2. Essential Blazor Capabilities

**Component-Based Architecture**: Building modular, reusable UI blocks:

- Basic components

- Parameter passing

- Event handling

**Routing**: Navigation and deep-linking within your Blazor application

**Forms and Validation**: Creating forms, input binding, and validating user input

**Data Binding**: Synchronizing component state with data

**Templating**: Providing flexible layouts and content structures for components

**Dependency Injection**: Injecting services and components

## 3. More Advanced Blazor Capabilities

**JavaScript Interop**: Calling JavaScript functions from C# and vice versa

**State Management**: Managing data and its flow across different components

**Error Handling and Boundaries**: Gracefully handling exceptions and providing fallback UI

**Authentication and Authorization**: Securing routes, components, and managing user permissions

**Offline Capabilities**: Building Blazor WebAssembly applications that function even when the device is offline

**Custom Rendering**: Fine-grained control over how components render their output (useful for specialized UI elements)

**Server-Side Rendering (SSR)**: Pre-rendering components on the server for improved SEO and first-load performance

-------------------------------------------------------------------------------------------------------------------------------------

**Additional Samples and Areas to Explore** (still PENDING)

**Dependency Injection (advanced)**: Complex service injection scenarios, configuring DI containers

**State Management (advanced)**: Using dedicated state management libraries like Redux or Fluxor

**Component Libraries**: Integrating third-party Blazor component libraries for rich UI elements

**Server-Side Rendering (SSR)**: Detailed examples of setting up SSR in Blazor apps

**Blazor WebAssembly Performance Optimization**: Profiling and techniques to improve Blazor Wasm performance

**Blazor Testing**: Unit and integration testing of Blazor components

-------------------------------------------------------------------------------------------------------------------------------------

## 4. Simple Blazor Sample

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

