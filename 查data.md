# 查data

```python
"""basic get"""
ref = db.reference('dinosaurs')
snapshot = ref.order_by_child('dimensions/height').get()
for key, val in snapshot.items():
    print('{0} was {1} meters tall'.format(key, val))

"""order"""
ref = db.reference('dinosaurs')
snapshot = ref.order_by_key().get()
print(snapshot)

"""Limit Query"""
ref = db.reference('dinosaurs')
# snapshot = ref.order_by_child('weight').limit_to_last(2).get()
snapshot = ref.order_by_child('height').limit_to_first(2).get()
snapshot = scores_ref.order_by_value().limit_to_last(3).get()
for key in snapshot:
    print(key)

"""Range Query"""
snapshot = ref.order_by_child('height').start_at(3).get()
# snapshot = ref.order_by_key().end_at('pterodactyl').get()
# snapshot = ref.order_by_key().start_at('b').end_at(u'b\uf8ff').get()
# snapshot = ref.order_by_child('height').equal_to(25).get()
for key in snapshot:
    print(key)
```
