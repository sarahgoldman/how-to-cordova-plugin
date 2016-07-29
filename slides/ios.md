###iOS Implementation

When the javascript calls cordova's exec method, it will use the package files specified for the given feature.

####Header file (HNWHelloNotWorld.h)

```
#import <Cordova/CDV.h>

@interface HNWHelloNotWorld : CDVPlugin

- (void)greet:(CDVInvokedUrlCommand*)command;

@end

```