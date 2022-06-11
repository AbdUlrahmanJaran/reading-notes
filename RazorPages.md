# Razor Pages
Razor Pages is a newer, simplified web application programming model. It removes much of the ceremony of ASP.NET MVC by adopting a file-based routing approach. Each Razor Pages file found under the Pages directory equates to an endpoint.<small>[ref](https://www.jetbrains.com/dotnet/guide/tutorials/basics/razor-pages/#:~:text=Razor%20Pages%20is%20a%20newer,directory%20equates%20to%20an%20endpoint.)</small>

Razor Pages is enabled in Program.cs by:
1. Razor Pages can make coding page-focused scenarios easier and more productive than using controllers and views.
2. ``builder.Services.AddRazorPages();`` adds services for Razor Pages to the app.
3. ``app.MapRazorPages();`` adds endpoints for Razor Pages.

Razor Pages is designed to make common patterns used with web browsers easy to implement when building an app. Model binding, Tag Helpers, and HTML helpers work with the properties defined in a Razor Page class.

Why Razor Pages?
1. It’s easier to get to web development for beginners as Razor pages are more lightweight than MVC. Besides beginners there are people who are coming from other scripting languages be it old ASP or PHP or something else.
2. Razor Pages fit well to smaller scenarios where building controllers and models as separate classes is overkill.

With Razor Pages, when you make a request (e.g. ``/contact``) the default ASP.NET Routing configuration will attempt to locate a Razor Page for that request in the Pages folder.
It simply looks for a page with the name used in the request (for a request to ``/contact`` that would be ``Contact.cshtml``) and routes directly to it.
The Razor Page then acts as though it were a controller action.

Every Razor Page can have a corresponding Page Model.
With Razor Pages your application code lives in these models, specifically in methods for the different HTTP verbs (e.g. GET, POST).

### Ref: [microsoft](https://docs.microsoft.com/en-us/aspnet/core/razor-pages/?view=aspnetcore-6.0&tabs=visual-studio&viewFallbackFrom=aspnetcore-2.2), [jonhilton](https://jonhilton.net/razor-pages-or-mvc-a-quick-comparison/) and [gunnarpeipman](https://gunnarpeipman.com/aspnet-core-razor-pages/).