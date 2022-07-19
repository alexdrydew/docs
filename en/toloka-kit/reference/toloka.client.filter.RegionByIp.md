# RegionByIp
`toloka.client.filter.RegionByIp` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.0.1/src/client/filter.py#L414)

```python
RegionByIp(
    self,
    operator: InclusionOperator,
    value: int
)
```

Use to select Tolokers by their region determined by IP address.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`operator`|**[InclusionOperator](toloka.client.primitives.operators.InclusionOperator.md)**|<p>Comparison operator in the condition. For example, for a condition &quot;The Toloker must be 18 years old or older» used date of birth and operator GTE («Greater than or equal»). Possible key values operator depends on the data type in the field value</p>
`value`|**int**|<p>The Toloker&#x27;s region.</p>
