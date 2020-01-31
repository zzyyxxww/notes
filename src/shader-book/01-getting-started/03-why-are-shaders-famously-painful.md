
# Why are shaders famously painful?

Because shaders are busy all the time and free their memory after every run,
they have two constraints:

They are **blind**, which is to say that it can't know what the other threads are doing.

They are also **memoryless**, which means that it can't remember what they were
doing before.
