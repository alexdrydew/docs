# ClientType
`toloka.client.filter.ClientType` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.0.1/src/client/filter.py#L451)

```python
ClientType(
    self,
    operator: IdentityOperator,
    value: Union[ClientType, str]
)
```

Use to select Tolokers by their application type.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`operator`|**[IdentityOperator](toloka.client.primitives.operators.IdentityOperator.md)**|<p>Comparison operator in the condition. For example, for a condition &quot;The Toloker must be 18 years old or older» used date of birth and operator GTE («Greater than or equal»). Possible key values operator depends on the data type in the field value</p>
`value`|**[ClientType](toloka.client.filter.ClientType.ClientType.md)**|<p>Client application type.</p>
