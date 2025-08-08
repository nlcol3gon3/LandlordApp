# LandlordApp – Lab 4: ViewModel, LiveData, Data Binding

## Summary of Changes

This project has been updated to follow MVVM architecture as part of Lab 4 requirements.

### Implemented Features

- Introduced `TenantViewModel` to manage tenant data in a lifecycle-aware way.
- Used `MutableLiveData` and `LiveData` to store and observe tenant information.
- Applied `Transformations.map()` to convert tenant info to uppercase without changing the original data.
- Enabled **data binding** in the layout to update the UI automatically when data changes.
- Eliminated the need for `findViewById()` using `DataBindingUtil`.
- Added a **tenant counter** using `LiveData<Int>`.

### How it Works

- The user inputs tenant name, unit, and rent.
- On clicking **Add Tenant**, the data is sent to `TenantViewModel`.
- The ViewModel updates the LiveData, which is observed by the layout.
- The TextView displays tenant info in uppercase, and the counter increases.
- All updates happen reactively using LiveData and data binding.

### Key Files Modified

- `AddTenant.kt`
- `TenantViewModel.kt`
- `addtenant_activity.xml`
- `build.gradle.kts`
- `libs.versions.toml`
- `build.gradle`

### Bonus Feature: Tenant Counter

A tenant counter was implemented using `LiveData<Int>` in the ViewModel.  
Each time a tenant is added, the counter increments and is displayed live in the UI.

---

