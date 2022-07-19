# FilterCondition
`toloka.client.filter.FilterCondition` | [Source code](https://github.com/Toloka/toloka-kit/blob/v1.0.1/src/client/filter.py#L50)

```python
FilterCondition(self)
```

You can select Tolokers to access pool tasks.


For example, you can select Tolokers by region, skill, or browser type (desktop or mobile).


**Examples:**

How to setup filter for selecting Tolokers.

```python
filter = (
   (toloka.filter.Languages.in_('EN')) &
   (toloka.client.filter.DeviceCategory.in_(toloka.client.filter.DeviceCategory.SMARTPHONE))
)
```
