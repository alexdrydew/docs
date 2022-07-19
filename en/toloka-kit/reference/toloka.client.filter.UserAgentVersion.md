# UserAgentVersion
`toloka.client.filter.UserAgentVersion` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.0.1/src/client/filter.py#L616)

```python
UserAgentVersion(
    self,
    operator: CompareOperator,
    value: Optional[float] = None
)
```

Use to select Tolokers by full browser version.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`operator`|**[CompareOperator](toloka.client.primitives.operators.CompareOperator.md)**|<p>Comparison operator in the condition. For example, for a condition &quot;The Toloker must be 18 years old or older» used date of birth and operator GTE («Greater than or equal»). Possible key values operator depends on the data type in the field value</p>
`value`|**Optional\[float\]**|<p>Full browser version. &lt;Major version&gt;.&lt;Minor version&gt;.</p>
