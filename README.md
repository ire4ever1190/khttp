# khttp
[![Travis CI](https://img.shields.io/travis/jkcclemens/khttp/master.svg)](https://travis-ci.org/jkcclemens/khttp)
[![Codecov](https://img.shields.io/codecov/c/github/jkcclemens/khttp.svg)](https://codecov.io/github/jkcclemens/khttp)
[![VersionEye](https://www.versioneye.com/user/projects/56243e0a36d0ab0021000bf4/badge.svg)](https://www.versioneye.com/user/projects/56243e0a36d0ab0021000bf4)
[![License](https://img.shields.io/github/license/jkcclemens/khttp.svg)](https://github.com/jkcclemens/khttp/blob/master/LICENSE)
[![Gratipay](https://img.shields.io/gratipay/jkcclemens.svg)](https://gratipay.com/~jkcclemens/)
[![Documentation status](https://readthedocs.org/projects/khttp/badge/?version=latest)](http://khttp.readthedocs.org/en/latest/?badge=latest)

khttp is a simple library for HTTP requests in Kotlin. It functions similarly to Python's `requests` module.

```kotlin
import khttp.get

fun main(args: Array<out String>) {
    // Get our IP
    println(get("http://httpbin.org/ip").jsonObject.getString("origin"))
    // Get our IP in a simpler way
    println(get("http://icanhazip.com").text)
}
```

## Dependency

### Stable

Stable releases are hosted on [Jitpack](https://jitpack.io/).
first add this to your build.gradle

```xml
	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
```
Then add the dependency
```
dependencies {
        ...
		implementation 'com.github.ire4ever1190:khttp:0.2.0'
	}
```

### Development

Development builds are currently available through [JitPack](https://jitpack.io/#jkcclemens/khttp). Snapshot builds may
eventually be hosted on [OJO](https://oss.jfrog.org/), but are not currently available there.
