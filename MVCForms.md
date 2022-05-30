# MVC Forms
## Views in ASP.NET Core MVC
In the Model-View-Controller (MVC) pattern, the view handles the app's data presentation and user interaction. A view is an HTML template with embedded Razor markup which is a code that interacts with HTML markup to produce a webpage that's sent to the client.

In ASP.NET Core MVC, views are ``.cshtml`` files that use the C# programming language in Razor markup. View files are grouped into folders named for each of the app's controllers. The folders are stored in a Views folder at the root of the app.

### Benefits of using views
1. Views are generally grouped by app feature. This makes it easier to find related views when working on a feature.
2. The parts of the app are loosely coupled. You can build and update the app's views separately from the business logic and data access components.
3. It's easier to test the user interface parts of the app because the views are separate units.
4. Due to better organization, it's less likely that you'll accidentally repeat sections of the user interface.

## 4 Ways To Create Form In ASP.NET MVC
### 1. WEAKLY TYPED
This is the easiest and quickest way to create forms in MVC.

Advantage:
1. It is easy to create a form using Weakly Typed mechanism
2. Mostly used when you need to create a form with one or two input items.

Disadvantage:
1. Have higher chance of getting exception and runtime error messages.
2. Very difficult to manage when forms have multiple input items and controls.

### 2. STRONGLY TYPED
Sending objects (model) instead of sending each item as parameter. It is easy to maintain because you don't need to remember each input item and IntelliSense will show you automatically the each item.

IntelliSense is a general term for various code editing features including: code completion, parameter info, quick info, and member lists.

### 3. STRONGLY TYPED AJAX (ASYNCHRONOUS)
It is a very magical way to submit data to the controller without happening page load. **Asynchronous AJAX** simply post back the data to the controllers and update the only that part of the page, which has to display output. by using  ``JQuery-Unobstrusive-AJAX`` package.

### 4. PURE HTML FORMS WITH AJAX AND JQUERY
Sending data from input controls and use html elements like `<p>…</p>`, `<span>…</span>` to send data to controllers. This is pure ``JQuery`` and ``AJAX`` query.

## Things I want to know more about
1. Razor class library (RCL).
2. FormCollection objects.

## Ref: [Views](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/overview?view=aspnetcore-6.0&viewFallbackFrom=aspnetcore-2.2), [Forms](https://www.completecsharptutorial.com/asp-net-mvc5/4-ways-to-create-form-in-asp-net-mvc.php#two) and [IntelliSense](https://code.visualstudio.com/docs/editor/intellisense#:~:text=IntelliSense%20is%20a%20general%20term,%2C%20and%20%22code%20hinting.%22).