# Encapsulation

Enforce encapsulation with the protection keywords. Class members should almost always be declared private unless they are part of the public/protected interface to the class. Use your best judgment, but always be aware that a lack of accessors makes it hard to refactor later without breaking plugins and existing projects.
If particular fields are only intended to be usable by derived classes, make them private and provide protected accessors.
Use `sealed`/`readonly` if your class is not designed to be derived from.

