# What is Object Pool?
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

# Usage:
- When an application requires objects which are expensive to create. Eg: there is a need of opening too many connections for the database then it takes too longer to create a new one and the database server will be overloaded.
- When there are several clients who need the same resource at different times.

## Implementation of object pool:
- We start by creating class for object pool
- a thread-safe caching of objects should be done in pool.
- Methods to acquire and release objects should be provided and pool should reset cached objects before giving them out.
- We have to decide whether to create a new pooled objects when pool is empty or wait until an object become available, Choice is influenced by whether the object is tied to fixed number of external resource, So if your glass object is tied with an external resource which is limited in nature, then of course. You have to wait, Or if you have access to unlimited resources or if your object doesn't depend on any external resource, then you can keep on creating new objects and then cashing them when they are returned to your pool.

# Example: 
- java.util.concurrent.ThreadPoolExecutor
