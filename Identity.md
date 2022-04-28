# Identity
ASP.NET Core ``Identity`` Is an API that supports user interface (UI) login functionality: Manages users, passwords, profile data, roles, claims, tokens, email confirmation, and more.

Users can create an account with the login information stored in Identity or they can use an external login provider. Supported external login providers include Facebook, Google, Microsoft Account, and Twitter.

Identity is typically configured using a SQL Server database to store user names, passwords, and profile data. Alternatively, another persistent store can be used, for example, Azure Table Storage.

There are three classes which represent the identity of a user: ``Claim``, ``ClaimsIdentity``, and ``ClaimsPrincipal``

## Claims
A Claim represents a single fact about the user. It could be the user's first name, last name, age, employer, birth date, or anything else that is true about the user. A single claim will contain only a single piece of information.

Claims are represented by the ``Claim`` class in ASP.Net Core. It's most common constructor accepts two strings: type and value. The 'type' parameter is the name of the claim, while the value is the information the claim is representing about the user.

### ClaimsIdentity
An Identity represents a form of identification or, in other words, a single way of proving who you are. In real life this could be a driver's license. In ASP.Net Core, it is a ``ClaimsIdentity``. This class represents a single form of digital identification.

### ClaimsPrincipal
A Principal represents the actual user. It can contain one or more instances of ``ClaimsIdentity``. just like in life a person may have a driver's license, concealed-carry permit, social security card, and a passport. Each of the identities is used for a different purpose and may contain a unique set of claims, but they all identify the same user in some form or another.

### Ref: [Identity](https://docs.microsoft.com/en-us/aspnet/core/security/authentication/identity?view=aspnetcore-6.0&tabs=visual-studio&viewFallbackFrom=aspnetcore-2.1) and [Authentication](https://digitalmccullough.com/blog/aspnetcore-auth-system-demystified/).

## Things I want to know more about
1. verbs that invoked by the authentication system.
2. how to test Identity.