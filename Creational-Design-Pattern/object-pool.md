# When Use Object Pool?
- In our system if **cost of creating an instance of class** is high and we need **a large number of objects** of this class for short duration then we use ***Object pool***.
- Here we either pre-create instance of this class or collect unused instances in a memory cache. When code need an object of this class we provided it from this cache.
- Mostly, performance is the key issue during the software development and the object creation, which may be a costly step.
- Object Pool Pattern says that " to reuse the object that are expensive to create".
- Basically, an Object pool is a container which contains a specified amount of objects. When an object is taken from the pool, it is not available in the pool until it is put back. **Objects in the pool have a lifecycle: creation, validation and destroy**.

# Advantage of Object Pool design pattern:
1. It boosts the performance of the application significantly.
2. It is most effective in a situation where the rate of initializing a class instance is high.
3. It manages the connections and provides a way to reuse and share them.
4. It can also provide the limit for the maximum number of objects that can be created.
