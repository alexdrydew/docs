# Education
`toloka.client.filter.Education` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.0.1/src/client/filter.py#L267)

```python
Education(
    self,
    operator: IdentityOperator,
    value: Union[Education, str]
)
```

Use to select Tolokers by education.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`operator`|**[IdentityOperator](toloka.client.primitives.operators.IdentityOperator.md)**|<p>Comparison operator in the condition. For example, for a condition &quot;The Toloker must be 18 years old or older» used date of birth and operator GTE («Greater than or equal»). Possible key values operator depends on the data type in the field value</p>
`value`|**[Education](toloka.client.filter.Education.Education.md)**|<p>Toloker&#x27;s education.</p>
