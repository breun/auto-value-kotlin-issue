# auto-value-kotlin-issue

Running `./mvnw clean compile` on this Spring Cloud GCP 3.6.1 project results in this error:

```
[ERROR] /path/tp/.m2/repository/com/google/auto/value/auto-value/1.10.2/auto-value-1.10.2.jar!/META-INF/kotlin-stdlib-common.kotlin_module: Module was compiled with an incompatible version of Kotlin. The binary version of its metadata is 1.8.0, expected version is 1.6.0.
```

Downgrading to Spring Cloud GCP 3.6.0 downgrades `com.google.auto.value:auto-value` from 1.10.2 to 1.10.1, which does work with Kotlin 1.6.

Related GitHub issues:

* [auto-value 1.10.2 breaks compatibility with Kotlin 1.6 and 1.7](https://github.com/google/auto/issues/1574)
* [BigQuery: google-cloud-bigquery 2.31.0 breaks compatibility with Kotlin 1.6 / 1.7 via dependency on auto-value 1.10.2](https://github.com/googleapis/java-bigquery/issues/2852)
* [Spring Cloud GCP 3.6.1 breaks Kotlin 1.6 / 1.7 compatibility](https://github.com/GoogleCloudPlatform/spring-cloud-gcp/issues/2122)
