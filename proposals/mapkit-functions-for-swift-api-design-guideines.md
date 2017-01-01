# Modernize MapKit functions for Swift API Design Guidelines

* Proposal: [SE-NNNN](https://github.com/scotteg/swift-evolution/blob/master/proposals/mapkit-functions-for-swift-api-design-guideines.md)
* Author: [Scott Gardner](https://github.com/scotteg)
* Review Manager: TBD
* Status: **Preparing**
* Decision Notes: [Rationale](https://lists.swift.org/pipermail/swift-evolution/)
* Bugs: 

## Introduction

The existing `MapKit` framework functions use C-style syntax. To adopt the Swift API design guidlines, this proposal outlines changes to the MapKit framework.

For example, this is how you would currently determine if the user is currently within the visible map view:

```swift
let userPoint = MKMapPointForCoordinate(mapView.userLocation.coordinate)
let mapRect = mapView.visibleMapRect
let inside = MKMapRectContainsPoint(mapRect, userPoint)
```

This should be more easily accomplished, such as by doing this:

```swift
let userPoint = mapView.userLocation.coordinate.mapPoint
let inside = mapView.visibleMapRect.contains(userPoint)
```

There are [39 MapKit functions](https://developer.apple.com/reference/mapkit/1612565-mapkit_functions?language=swift) that should be updated.

[Swift Evolution Discussion](https://lists.swift.org/pipermail/swift-evolution/)

## Motivation



## Proposed solution



## Detailed design



## Source compatibility



## Effect on ABI stability



## Effect on API resilience



## Alternatives considered



