# Profile
`toloka.client.filter.Profile` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.0.1/src/client/filter.py#L159)

```python
Profile(
    self,
    *,
    operator: Any,
    value: Any
)
```

Use to select Tolokers based on profile data.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`operator`|**Any**|<p>Comparison operator in the condition. For example, for a condition &quot;The Toloker must be 18 years old or older» used date of birth and operator GTE («Greater than or equal»). Possible key values operator depends on the data type in the field value</p>
`value`|**Any**|<p>Attribute value from the field key. For example, the ID of the region specified in the profile, or the minimum skill value.</p>
