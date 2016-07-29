###Javascript File

The module that will be installed in the app and called from the app's javascript.

module.exports will be inserted in the namespace specified in the clobbers target. 
 
```
module.exports = {
    greet: function (name, successCallback, errorCallback) {
        cordova.exec(successCallback, errorCallback, "HelloNotWorld", "greet", [name]);
    }
};
```