# FlixPrototype

## Flix Part 2

### User Stories

#### REQUIRED (10pts)
- [x] (5pts) User can tap a cell to see more details about a particular movie.
- [x] (5pts) User can tap a tab bar button to view a grid layout of Movie Posters using a CollectionView.

#### BONUS
- [ ] (2pts) User can tap a poster in the collection view to see a detail screen of that movie.
- [ ] (2pts) In the detail view, when the user taps the poster, a new screen is presented modally where they can view the trailer.

### App Walkthrough GIF
![git](https://user-images.githubusercontent.com/52833369/92985556-957d1480-f468-11ea-929f-182d5a77f3cc.gif)

### Notes
Overall experience was good. But, I got stuck in connecting the views to swift files. And initially the poster sizes were very small, which I corrected later.
## Flix Part 1
Flix is an app that allows users to browse movies from the [The Movie Database API](http://docs.themoviedb.apiary.io/#).

```swift
let url = URL(string: "https://api.themoviedb.org/3/movie/now_playing?api_key=a07e22bc18f5cb106bfe4cc1f83ad8ed")!
let request = URLRequest(url: url, cachePolicy: .reloadIgnoringLocalCacheData, timeoutInterval: 10)
let session = URLSession(configuration: .default, delegate: nil, delegateQueue: OperationQueue.main)
let task = session.dataTask(with: request) { (data, response, error) in
   // This will run when the network request returns
   if let error = error {
      print(error.localizedDescription)
   } else if let data = data {
      let dataDictionary = try! JSONSerialization.jsonObject(with: data, options: []) as! [String: Any]

      // TODO: Get the array of movies
      // TODO: Store the movies in a property to use elsewhere
      // TODO: Reload your table view data

   }
}
task.resume()
```

### User Stories

#### REQUIRED (10pts)
- [x] (2pts) User sees an app icon on the home screen and a styled launch screen.
- [x] (5pts) User can view and scroll through a list of movies now playing in theaters.
- [x] (3pts) User can view the movie poster image for each movie.

#### BONUS
- [ ] (2pt) User can view the app on various device sizes and orientations.
- [ ] (1pt) Run your app on a real device. (Since I don't have an iPhone, I couldn't test it on a real device)

### App Walkthrough GIF
![ezgif com-video-to-gif](https://user-images.githubusercontent.com/52833369/92207581-53d3e480-ee3e-11ea-8323-6a44cd6b2ca8.gif)
### Notes
As I am from Software Development background, I did not find this assignment much challenging. But I am not familiar with iOS development, so I am struggling a bit through Swift concepts.
