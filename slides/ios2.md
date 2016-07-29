####Implementation file (HNWHelloNotWorld.m)

```
#import "HNWHelloNotWorld.h"

@implementation HNWHelloNotWorld

- (void)greet:(CDVInvokedUrlCommand*)command
{

    NSString* name = [[command arguments] objectAtIndex:0];
    CDVPluginResult* result = nil;
    
    if ([name isEqualToString:@"World"]) {
	    result = [CDVPluginResult resultWithStatus:CDVCommandStatus_ERROR messageAsString:@"Cannot greet 'World'"];
    } else {
	    NSString* msg = [NSString stringWithFormat: @"Hello, %@", name];
	    result = [CDVPluginResult resultWithStatus:CDVCommandStatus_OK messageAsString:msg];
	}
	
    [self.commandDelegate sendPluginResult:result callbackId:command.callbackId];
}

@end
```
