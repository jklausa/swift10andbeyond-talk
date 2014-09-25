![original](http://swiftwarsaw.com/stylesheets/img/bg.jpg)

# [fit] Swift: Road to 1.0 and beyond

# [fit] 25.09.2014 / Swift Warsaw #3

#### Jan Klausa / @klausa_qwpx / klausa.pl

___

# [fit] History lesson.

___

July:

* WWDC.

___

July:

* WWDC.

July - September:

* Beta 1-7.

___

# Lots of small changes.
___

# Swift In Flux
### github.com/ksm/SwiftInFlux

___

July:

* WWDC.

July - September:

* Beta 1-7.

September:

* 1.0!

___

# So, it's done, right?

___

# Not really.
___

# You *will* find compiler/IDE bugs.
___

![inline](https://pbs.twimg.com/media/BsSSVr6IgAA-Ys0.png:large)

___

```swift

func getTweetsForUser(user: String, closure: [[String:String]]? -> Void) -> Void 

let users = ["@klausa_qwpx", "@SwiftWarsaw"]
```

___

```swift
users.map {
    getTweetsForUser($0) {
        if let tweets = $0 {
            tweets.map {
                println("tweet: \(tweet["text"])")
            }
        }
    }
}

```

___

```swift
for user in users {
    getTweetsForUser(user) { 
        if let tweets = $0 as? [[String:String]] {
            tweets.map { (tweet: [String:String]) -> () in
                let text = tweet["text"]
                    println("tweet: \(text)")
            }
        }    
    }
}

```

___

# Workable, but not ideal.

___

# The road ahead

* Swift 1.1
* OS X support
* Exceptions?
* more?

___ 

# Let's talk community.

___ 

# Alamofire
### alamofire.io

___

# Moya
### github.com/AshFurrow/Moya

___ 

# [fit]Swift Playground Builder
## [fit]github.com/jas/swift-playground-builder

___

# ReactiveCocoa
# [fit] github.com/ReactiveCocoa/ReactiveCocoa/
### swift-development branch
___ 

# and many more!

___

# [fit] Resources, Events.

___

## Local meetups.

 
### Swift London, SwiftWro, Swift Warsaw, Swift<INSERTPLACEHERE>

___ 

# Hackathons.

___

# [fit] Swift Developer Weekly
### swiftdevweekly.co

___

# [fit] Functional Programming in Swift 
### objc.io 

___

# Swift In Flux
### github.com/ksm/SwiftInFlux

___

# [fit] #swift-lang @ freenode

___

# in a word: AWESOME.

___

# [fit] ...and that's all, folks!

# [fit] github.com/jklausa/swift10andbeyond-talk

### @klausa_qwpx
