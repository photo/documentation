Schema for a Tag object
=======================


----------------------------------------

### What's a Tag object for?

A Tag object stores information about a specific tag.
This includes but is not limited to the number of objects containing this tag.
The Tag objects schema is loose meaning that it can be flexible but at minimum it contains an `id`, `count`, `actor` and `owner`.

There are not currently any optional tag attributes.

----------------------------------------

### Schema for a Tag object

    {
      id: (string),
      count: (int),
      actor: (string),
      owner: (string),
    }

----------------------------------------

### Schema description

  * id, Base 36 value of a base 10 auto-incremented value
  * count, The number of objects with this tag
  * actor, Email address of the tag actor
  * owner, Email address of the tag owner

[User]: http://theopenphotoproject.org/documentation/schemas/User
[Photo]: http://theopenphotoproject.org/documentation/schemas/Photo
[Action]: http://theopenphotoproject.org/documentation/schemas/Action
[Tag]: http://theopenphotoproject.org/documentation/schemas/Tag
