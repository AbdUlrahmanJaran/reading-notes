# View Components
A view component renders a chunk rather than a whole response, includes the same separation-of-concerns and testability benefits found between a controller and view and can have parameters and business logic.
It is typically invoked from a layout page.

View components don't use model binding, they depend on the data passed when calling the view component.

### A view component consists of two parts:
1. The class, typically derived from ViewComponent
2. The result it returns, typically a view. 

### View Components are used in:
- Dynamic navigation menus.
- Tag cloud, where it queries the database.
- Sign in panel.
- Shopping cart.
- Recently published articles.
- Sidebar content on a blog.
- A sign in panel that would be rendered on every page and show either the links to sign out or sign in, depending on the sign in state of the user.

### A view component class can be created by any of the following:
1. Deriving from ``ViewComponent``.
2. Decorating a class with the `[ViewComponent]` attribute, or deriving from a class with the `[ViewComponent]` attribute.
3. Creating a class where the name ends with the suffix `ViewComponent`.

To prevent a class that has a case-insensitive ViewComponent suffix from being treated as a view component, decorate the class with the `[NonViewComponent]` attribute.

In Razor views, we can use the `Component` helper and its `Invoke` method to render view components.

### Ref: [View Components documentation](https://docs.microsoft.com/en-us/aspnet/core/mvc/views/view-components?view=aspnetcore-6.0&viewFallbackFrom=aspnetcore-2.1).