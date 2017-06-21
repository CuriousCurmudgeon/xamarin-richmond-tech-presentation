# Cross Platform Native Application Development with Xamarin

#### Brian Meeker

---

---?image=irt_logo.png&size=auto

---?image=innovation_center_logo.png&size=auto

---

### About Me

* http://brianmeeker.me/
* Email: brian@brianmeeker.me
* Twitter: @CuriousCurmudge
* Github: CuriousCurmudgeon

---

### What is Xamarin?

> With a C#-shared codebase, developers can use Xamarin tools to write native Android, iOS, and Windows apps with native user interfaces and share code across multiple platforms, including Windows and macOS.
> -- <cite>Wikipedia</cite>

---
### Why Xamarin?

---

* Cross-Platform
* Shared code
* Native

---

### Supported Platforms
* Android
* iOS
* Windows UWP (Windows 10, Xbox One, Windows 10 Mobile, Hololens)
* Mac OS (Preview)
* Tizen

---

### Competitors
* RubyMotion
* React Native
* Cordova

---

### Used By
https://www.xamarin.com/customers

---

### A Brief History of the Xamarin World

---

### Mono
* Open source .NET implementation started in 2001 by Miguel de Icaza, who worked for Ximian.
* Novell acquires Ximian (and Mono) in 2003.
* Attachmate acquires Novell in 2011. They layoff the Mono team.
* Miguel de Icaza starts Xamarin to focus on MonoTouch and Mono for Android.

---

### Xamarin
* December 2012: Xamarin.Mac released. First product.
* February 2013: Xamarin 2.0 released. Introduces Xamarin.iOS and Xamarin.Android. Introduces Xamarin Studio, a rebranded version of MonoDevelop, and integration with Visual Studio.

---

### Microsoft
* February 2016: Acquired by Microsoft.
* April 2016: Microsoft open sources the Xamarin SDK under the MIT license and bundles it for free with Visual Studio.
* April 2017: Xamarin Studio rebranded as Visual Studio for Mac.

---

### Cross-Platform .NET

---

### Shared Asset Projects
* Allows you to share code across projects, but compile them for each platform with conditional compilation.
* The contents of the shared project are basically copied into each referencing project.

---

### Portable Class Libraries (PCLs)
* Allows you to choose which platforms to target.
* Gives you the intersection of libraries available on those platforms.

---

### .NET Standard
* Defines uniform set of Base Class Library (BCL) APIs for all .NET platforms to implement, independent of workload.
* Enables developers to produce portable libraries that are usable across .NET runtimes, using this same set of APIs.
* Reduces and hopefully eliminates conditional compilation of shared source due to .NET APIs, only for OS APIs.

---

### IDEs
* Visual Studio
* Xamarin Studio
* Visual Studio for Mac

---

### Xamarin vs Xamarin.Forms

---

### Xamarin
* Shared business code.
* UI code is not shared.
* UI is defined using tools native to each platform.

---

### Xamarin.Forms
* Shared business code.
* Shared UI code (XAML)
* Hooks to create platform-specific UI as needed.

---

### Model-View-ViewModel (MVVM)

---

### Model
* The application's domain model. Same as in Model-View-Controller.

---

### View
* Defines the structure, layout, and appearance of what the user sees on screen.
* Limited amount of code. Business logic is delegated to View Model.

---

### View Model
* Intermediary between view and model. Handles view logic and transforms model data into a form the view needs.
* Typically a one-to-one relationship between views and view models.

---

### Xamarin.Android

---

### Xamarin.iOS

---

### Xamarin.Forms

---

### Extensible Application Markup Language (XAML)

---

```html
<?xml version="1.0" encoding="utf-8" ?>
<ContentPage xmlns="http://xamarin.com/schemas/2014/forms"
             xmlns:x="http://schemas.microsoft.com/winfx/2009/xaml"
             x:Class="MarvelDemo.Views.MainView"
             Title="The Avengers">
  <ListView x:Name="CharactersListView"
            ItemsSource="{Binding Characters}"
            ItemSelected="CharactersListView_OnItemSelected">
    <ListView.ItemTemplate>
      <DataTemplate>
        <ImageCell ImageSource="{Binding Thumbnail.FullPath}"
                   Text="{Binding Name}"/>
      </DataTemplate>
    </ListView.ItemTemplate>
  </ListView>
</ContentPage>
```

---

### Binding

---

### INotifyPropertyChanged
* Interface commonly implemented by view models used to notify clients, typically binding clients, that a property value has changed.

---

### MainActivity
* By convention, the initial activity in your Android app.
* Manages application lifecycle events (start, suspend, resume, terminate)

---

### AppDelegate
* Effectively the root object of your iOS app.
* Manages application lifecycle events (start, suspend, resume, terminate)
---

### Demo
