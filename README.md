 run :

    ./gradlew copy

It's gonna fail with :

```
* Where:
Build file '/Users/adah/tmp/basic-demo/distribution/kit/build.gradle' line: 6

* What went wrong:
A problem occurred evaluating project ':terracotta-db'.
> Could not get unknown property 'javadocJar' for project ':terracotta-ehcache-client' of type org.gradle.api.Project.
```

Unless you change distribution/kit/build.gradle with :

    from ':terracotta-ehcache-client:javadocJar'


and it's gonna work.

In my full gradle build, with 4.4, the project() form works; but in this simple use case, it does not :-(
