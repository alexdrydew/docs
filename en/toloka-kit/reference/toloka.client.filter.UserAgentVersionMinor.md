# UserAgentVersionMinor
`toloka.client.filter.UserAgentVersionMinor` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.0.1/src/client/filter.py#L638)

```python
UserAgentVersionMinor(
    self,
    operator: CompareOperator,
    value: Optional[int] = None
)
```

Use to select Tolokers by minor browser version.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`operator`|**[CompareOperator](toloka.client.primitives.operators.CompareOperator.md)**|<p>Comparison operator in the condition. For example, for a condition &quot;The Toloker must be 18 years old or older» used date of birth and operator GTE («Greater than or equal»). Possible key values operator depends on the data type in the field value</p>
`value`|**Optional\[int\]**|<p>Minor browser version.</p>
