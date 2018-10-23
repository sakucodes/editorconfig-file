# Editor Config File for VS

When you inject something into a constructor, you can use the suggestion feature to let VS create a private field for you. But VS creates it without an underscore `_` and prepends the field assignment with a `this` in the constructor.

If you have already an `.editorconfig` file you can append this snippet to your file. 

```
# Add underscore to private fields
dotnet_naming_style.prefix_underscore.capitalization = camel_case
dotnet_naming_style.prefix_underscore.required_prefix = _

dotnet_naming_symbols.private_fields.applicable_kinds           = field
dotnet_naming_symbols.private_fields.applicable_accessibilities = private

dotnet_naming_rule.private_members_with_underscore.symbols  = private_fields
dotnet_naming_rule.private_members_with_underscore.style    = prefix_underscore
dotnet_naming_rule.private_members_with_underscore.severity = suggestion
```

If you don't have a file, create a new `.editorconfig` file beside the `.sln` file or just take the one in this repo.

More information links

- https://aka.ms/editorconfigdocs
- https://editorconfig.org
