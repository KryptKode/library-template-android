# Library Template

This repository can be used as a template to create new GitHub repositories for Kotlin/Android 
libraries.

### Code Formatting

```gradle
./gradlew spotlessApply
```

### Check if Dependencies Are Up-to-Date

```gradle
./gradlew dependencyUpdates
```

### Publishing the Library to jCenter

Just have to execute:

```gradle
./gradlew bintrayUpload
```

But there are some pre-requisites:

1. Update [bintrayconfig.gradle](bintrayconfig.gradle) to contain your own Bintray username and 
the new library's matching details.
2. Add `bintray.user` and `bintray.apikey` entries to `local.properties` matching your own 
Bintray account.
3. With each release, update the version name and code in [dependencies.gradle](dependencies.gradle) 
and update [RELEASE_NOTES.md](RELEASE_NOTES.md).
