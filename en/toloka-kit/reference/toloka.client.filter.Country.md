# Country
`toloka.client.filter.Country` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.0.1/src/client/filter.py#L245)

```python
Country(
    self,
    operator: IdentityOperator,
    value: str
)
```

Use to select Tolokers by country.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`operator`|**[IdentityOperator](toloka.client.primitives.operators.IdentityOperator.md)**|<p>Comparison operator in the condition. For example, for a condition &quot;The Toloker must be 18 years old or older» used date of birth and operator GTE («Greater than or equal»). Possible key values operator depends on the data type in the field value</p>
`value`|**str**|<p>Country of the Toloker (two-letter code of the standard ISO 3166-1 alpha-2).</p>
