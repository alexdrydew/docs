# UserAgentFamily
`toloka.client.filter.UserAgentFamily` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.0.1/src/client/filter.py#L576)

```python
UserAgentFamily(
    self,
    operator: IdentityOperator,
    value: Union[UserAgentFamily, str]
)
```

Use to select Tolokers by user agent family.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`operator`|**[IdentityOperator](toloka.client.primitives.operators.IdentityOperator.md)**|<p>Comparison operator in the condition. For example, for a condition &quot;The Toloker must be 18 years old or older» used date of birth and operator GTE («Greater than or equal»). Possible key values operator depends on the data type in the field value</p>
`value`|**[UserAgentFamily](toloka.client.filter.UserAgentFamily.UserAgentFamily.md)**|<p>User agent family.</p>
