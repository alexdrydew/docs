# Languages
`toloka.client.filter.Languages` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.0.1/src/client/filter.py#L324)

```python
Languages(
    self,
    operator: InclusionOperator,
    value: Union[str, List[str]],
    verified: bool = False
)
```

Use to select Tolokers by languages specified by the Toloker in the profile.

## Parameters Description

| Parameters | Type | Description |
| :----------| :----| :-----------|
`operator`|**[InclusionOperator](toloka.client.primitives.operators.InclusionOperator.md)**|<p>Comparison operator in the condition. For example, for a condition &quot;The Toloker must be 18 years old or older» used date of birth and operator GTE («Greater than or equal»). Possible key values operator depends on the data type in the field value</p>
`value`|**Union\[str, List\[str\]\]**|<p>Languages specified by the Toloker in the profile (two-letter ISO code of the standard ISO 639-1 in upper case).</p>
`verified`|**-**|<p>If set to True, only the Tolokers who have passed a language test will be selected. Currently, you can use this parameter only with the following ISO codes : `DE`, `EN`, `FR`, `JA`, `PT`, `SV`, `RU`, `AR`, `ES`.</p>
