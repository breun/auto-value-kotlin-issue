# auto-value-kotlin-issue

Running `./mvnw clean compile` on this Spring Cloud GCP 3.6.1 project results in this error:

```
[ERROR] /path/tp/.m2/repository/com/google/auto/value/auto-value/1.10.2/auto-value-1.10.2.jar!/META-INF/kotlin-stdlib-common.kotlin_module: Module was compiled with an incompatible version of Kotlin. The binary version of its metadata is 1.8.0, expected version is 1.6.0.
```

Downgrading to Spring Cloud GCP 3.6.0 downgrades `com.google.auto:auto-value` from 1.10.2 to 1.10.1, which does work with Kotlin 1.6.