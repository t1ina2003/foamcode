# pandas

- df.loc  
```python
>>> df
            max_speed  shield
cobra               1       2
viper               4       5
sidewinder          7       8
>>> df.loc[['viper', 'sidewinder']]
            max_speed  shield
viper               4       5
sidewinder          7       8
```