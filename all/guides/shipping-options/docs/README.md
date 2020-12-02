SortOrder: 0
# Introduction

A Carrier Service can be registered by merchants to their shops, and then provide real time shipping rates to their buyers,
by implementing the following *SPI* (Service Provider Interface).

#### Reporting Failures

When a carrier service doesn't have enough information, or received invalid information, and is un-able
to calculate shipping rates due to that, we expect the following payload to be returned alone with HTTP `400` status:

```json
{
  "message": "We are missing important information",
  "details": {
    "validationError": {
      "fieldViolations": [
        {
          "field": "postalCode",
          "description": "MISSING"
        }
      ]
    }
  }
}
```
Currently, the following options for each one of the fields are supported:
* message - can be any free text message or empty;
* field - `postalCode`;
* description - `MISSING`, `INVALID`;
