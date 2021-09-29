# 基本get

```python
# Import database module.
from firebase_admin import db
# Get a database reference to our posts
ref = db.reference('server/saving-data/fireblog/posts')
# Read the data at the posts reference (this is a blocking operation)
print(ref.get())
```
Node.js and Java 會自動 apply listener, 獲得DataSnapshot
- 可以放 Child Added、Child Changed、Child Removed、Child Moved
python 直接拿data
