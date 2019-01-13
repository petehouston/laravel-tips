# Eloquent computed attributes

Read the detailed explanation at https://blog.petehouston.com/make-computed-attributes-for-eloquent-models/

**Computed attribute** is the value made up from other attributes. Apparently, in this case, full name is a computed attribute because it is made from the concatenation of first name and last name attributes.

**1. Create a computed attribute**

```php
/**
 * This is the computed attribute
 *
 * @return string
 */
public function getFullNameAttribute() {
    return $this->first_name . ' ' . $this->last_name;
}
```

**2. Access computed attribute**

```php
$user = User::first();
echo $user->full_name;
```