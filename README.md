# Appetiser-Coding-Challenge
Create a master-detail application that contains at least one dependency. This application should display a list of items obtained from a iTunes Search API and show a detailed view of each item. The URL you must obtain your data from is as follows:


https://itunes.apple.com/search?term=star&country=au&media=movie&;all

(iTunes Web Service Documentation: https://affiliate.itunes.apple.com/resources/documentation/itunes-store-web-service-search-api/#searching)

Getting Started
Clone this repository by using the comamnd lines below
 - git clone https://github.com/Rebolos85/Appetiser-Coding-Challenge.git
  - find the directory folder 
  - import it via Android Studio
  
  Project Architecture that I used is called MVVM (Model View Viewmodel)
  
    -Model- The source of data in our app to be used by the remote and local to process the data
    -data - Contains the dao of for sql statement,ItunesItemDatabase db,remote api and ItunesRepository
   - di -  Contains the app dependency of the app such as retrofit, room, okhttp, Interceptor and dao  
   - other- Constains the DATABASE_NAME and ITUNES_TABLE_NAME
   
   - UseCase - Constain the business logic of the app coming from the repository
   
    - Viewmodel - Contains the business logic and observing what is happening in the usecase via resource wrapper class
   
    - Utils - constains the resource wrapper class and enums
     - View - It consists of the UI Code(Activity) XML and subscribing the observables in the viewmodel that it exposes to update the UI based on the
     business logic in the viemodel
     
why did I choose that particular one, any benefits, and disadvantages of using it?
 I choose this pattern in order to save configuration changes since the activity & fragment have a lifecycle once it is rotated the it will recreate which the data will be lost
 but using MVVM it can save the configuration changes since it has longer lifecycle compared to activity and fragment since it has onCleared and to have a separations of concern in order to easily mock unit testing and also 
 to make the code maintainable, testable and extensibility 
 
 To know more about pros and cons about the architecture that I've used follow this link https://www.tutorialspoint.com/mvvm/mvvm_advantages.htm
 
  Tech stack used
   - Kotlin Coroutines
   - Hilt Depedency Injection
   - Room
   - Retrofit
   - 
   -Glide- to display images and also to keep taking care of caching and keeping a low memory impact when doing image manipulations.
   - Swipe Refresher
   
   Authors and Acknowledgment
   This is for Appetiser Apps submission purposes only.
    Roberto A Rebolos Jr
  
