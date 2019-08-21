# Be.Vlaanderen.Basisregisters.AspNetCore.Mvc.Middleware.AddRemoteIpAddress

Middleware component which adds a the remote IP id as a claim `urn:be:vlaanderen:vbr:ip` for the user on the request context.

The claim name is configurable as well.

## Usage

```csharp
public void Configure(IApplicationBuilder app, ...)
{
    app
        ...
        .UseMiddleware<AddRemoteIpAddressMiddleware>()
        ...
}
```

```csharp
public void Configure(IApplicationBuilder app, ...)
{
    app
        ...
        .UseMiddleware<AddRemoteIpAddressMiddleware>("urn:custom-claim:ip")
        ...
}
```