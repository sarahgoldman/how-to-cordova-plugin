###Plugin Manifest File

Defines the structure and settings for the plugin

- metadata like name, description, author
- js module
- platform files
- dependencies

```
<?xml version="1.0" encoding="UTF-8"?>
<plugin xmlns="http://www.phonegap.com/ns/plugins/1.0"
	id="cordova-plugin-hello-not-world"
	version="0.0.1">
	
	<name>Hello Not World</name>

	<js-module src="www/helloNotWorld.js" name="helloNotWorld">
		<clobbers target="helloNotWorld" />
	</js-module>
	
	<platform name="ios">
		<config-file target="config.xml" parent="/*">
			<feature name="HelloNotWorld">
				<param name="ios-package" value="HNWHelloNotWorld" />
			</feature>
		</config-file>
		<header-file src="src/ios/HNWHelloNotWorld.h" />
		<source-file src="src/ios/HNWHelloNotWorld.m" />
	</platform>

</plugin>

```
