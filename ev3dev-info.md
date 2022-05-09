# Web Links

# EV3 Environment Comparisons
* [PyBricks vs ev3dev2](https://github.com/pybricks/pybricks-api/issues/22#:~:text=The%20short%20answer%3A%20the%20ev3dev2%20module%20and%20pybricks,particular%20functionality%20which%20is%20only%20available%20in%20ev3dev-lang-python.?msclkid=9cfb4ebfcf5a11ec8cf3984471c0347e)

```
 Thanks for your elaborate reply @WasabiFan, I think that covers it very well.

I [...] don't know what is/isn't supported or what the roadmap looks like.

You can view the supported API here.
The Pybricks roadmap is here.
David and Laurens started developing pybricks much more recently, with the aim of supporting other MINDSTORMS platforms which then also grew to include stock ev3dev (at least, based on my recollection). The pybricks interfaces are very well-designed, carefully-considered APIs for core robot programming, without the external signs of any particular driver design.

This is entirely correct. To add some more detail: Pybricks includes its own set of motor drivers so they could be used on all the embedded programmable hubs beyond EV3. This also allowed us to integrate drive base synchronization, and things like working ramping/acceleration and stall detection.

Historically, EV3 support for Pybricks mainly started because ev3dev was a lot easier to debug than the embedded hubs we were originally targeting. We could design high level control code, debug and datalog it extensively, and glue it back onto the more minimal embedded systems when we knew the high level things were stable. After a while though, it was natural step to include EV3 in the main roadmap. It is now quite fully-featured.

But a noteworthy advantage of ev3dev2 (and this will remain so), is that it can run with regular python3, which can be invaluable if you need certain Python libraries.

are they converging or diverging going forward?

So to get back to the original question, I think they might continue to exist in parallel. EV3 support in Pybricks is essentially final, and we do currently not plan to change any of the API in a breaking way. It sounds like the same holds for ev3dev2, so they might neither converge nor diverge.
```

