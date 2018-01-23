# Additional Contact Points

There are some cases where it is important to list multiple contact points for an organization, particularly in cases where each contact point may deal with enquiries in particular languages only.

This extension adds an array of `additionalContactPoints` to the `organization` object, and introduces an `availableLanguage` array of language codes to `ContactPoint`.

When this extension is used, publishers should always include a **primary contact point** for the `contactPoint` property, on the basis that many applications will not be aware of the `additionalContactPoints` array.

## Example

The example below shows a procuring entity with two contact points. A primarily contact

```json
{
  "parties":[{
            "id":"GB-LAC-E09000003",
            "role":["procuringEntity"],
            "identifier": {
                "scheme": "GB-LAC",
                "id": "E09000003",
                "legalName": "AnyTown Council"
            },
            "name": "AnyTown Council",
            "address": {
                "streetAddress": "4, North London Business Park, Oakleigh Rd S",
                "locality": "London",
                "region": "London",
                "postalCode": "N11 1NP",
                "countryName": "United Kingdom"
            },
            "contactPoint": {
                "name": "Procurement Team",
                "email": "procurement-team@example.com",
                "telephone": "01234 345 346",
                "availableLanguage":["en"]
            },
            "additionalContactPoints":[
              {
                "name": "Procurement Team (International Enquiries)",
                "email": "procurement-team-international@example.com",
                "telephone": "01234 345 346 Extension 123",
                "availableLanguage":["es","fr","de"]
              }
            ]
    }]
}
```

## Issues

Report issues for this extension in the [ocds-extensions repository](https://github.com/open-contracting/ocds-extensions/issues), putting the extension's name in the issue's title.
