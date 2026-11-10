# Android app

Native Android application using Kotlin, Jetpack Compose and Gradle.

Suggested packages:
- `core/` — networking, storage, common UI and utilities
- `feature/` — feature-oriented screens and state
- `data/` — repositories and DTO mappings
- `domain/` — use cases and domain models (keep this lightweight)

Use MVVM/UDF, coroutines and Flow. Use Retrofit/OkHttp for API access,
DataStore for preferences, and secure platform storage for auth tokens.
Do not commit `local.properties`, signing keys or secrets.
