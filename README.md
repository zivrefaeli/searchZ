# Search Z
[![](https://jitpack.io/v/zivrefaeli/searchZ.svg)](https://jitpack.io/#zivrefaeli/searchZ)

Search for images for each keyword

## Installation
- Create a GCP project
- Add **Custom Search API** to your project
- Get API key from the [Overview](https://developers.google.com/custom-search/v1/overview) on *Get a Key*
- Create a [Programmable Search Engine](https://programmablesearchengine.google.com/about)
- Get the search engine's id (**CX**)

Add the JitPack repository to your build file
```gradle
allprojects {
      repositories {
            ...
            maven { url 'https://jitpack.io' }
      }
}
```

Add the dependency
```gradle
dependencies {
      implementation 'com.github.zivrefaeli:searchZ:Tag'
}
```

## Example
```java
SearchEngine engine = new SearchEngine(CONTEXT, API_KEY, CX);
engine.search(KEYWORD, (image, searches) -> {
    // use the response values:
    //      image (Bitmap)
    //      amount of keyword searches (String)
    // if error occured, null will be returned
});
```

## License
searchZ was created by Ziv Refaeli and released under the [MIT license](https://github.com/zivrefaeli/searchZ/blob/master/LICENCE).