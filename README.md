# MoeMoeSongs
A small library that uses [animethemes](https://animethemes.moe) index and data.
 
### How to use
Clone this repository and then launch maven package goal.
 
### Features
Everything is handled by **MoeCore** class. To browse anime entries and their songs, you must first load them once.
```java
public class MyClass {
    
    public static void main(String[] args) {
        MoeCore.updateAnimeList();
        
        //do your stuff
    }
}
```
Please note that updating anime list will require some time (in seconds), code will wait until everything is done.
 
Currently available methods are:
* `getOpenings`
* `getEndings`
* `getFromTitle(String title)`
* `getFromSongTitle(String songTitle)`
* `getFromFilter(FilterOptions filterOptions)`
 
##### getOpenings
Returns only opening songs.
  
##### getEndings
Returns only ending songs.
 
##### getFromTitle(String title)
Returns songs whose anime source's title contains given text.
 
##### getFromSongTitle(String songTitle)
Returns songs whose title contains given text.
 
##### getFromFilter(FilterOptions filterOptions)
Returns songs that matches multiple parameters at once. Currently:
* `VERSION` (opening/ending, version etc)
* `SOURCE` (anime title/anime alternate title)
* `SONG_TITLE` (song title, duh).
 
Every given parameter in every method will be matched partially (or fully).