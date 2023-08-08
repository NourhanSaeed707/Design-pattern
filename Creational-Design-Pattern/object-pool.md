# When Use Object Pool?
- In our system if **cost of creating an instance of class** is high and we need **a large number of objects** of this class for short duration then we use ***Object pool***.
- Mostly, performance is the key issue during the software development and the object creation, which may be a costly step.
- Object Pool Pattern says that " to reuse the object that are expensive to create".
- Basically, an Object pool is a container which contains a specified amount of objects. When an object is taken from the pool, it is not available in the pool until it is put back. **Objects in the pool have a lifecycle: creation, validation and destroy**.
