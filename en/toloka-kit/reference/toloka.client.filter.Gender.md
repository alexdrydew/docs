# Gender
`toloka.client.filter.Gender` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.0.1/src/client/filter.py#L223)

```python
Gender(
    self,
    operator: IdentityOperator,
    value: Union[Gender, str]
)
```

Use to select Tolokers by gender.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`operator`|**[IdentityOperator](toloka.client.primitives.operators.IdentityOperator.md)**|<p>Comparison operator in the condition. For example, for a condition &quot;The Toloker must be 18 years old or older» used date of birth and operator GTE («Greater than or equal»). Possible key values operator depends on the data type in the field value</p>
`value`|**[Gender](toloka.client.filter.Gender.Gender.md)**|<p>Toloker&#x27;s gender.</p>
