## ModAPI.util

ModAPI.util provides and exposes a large number of utilities for interacting with ModAPI.

Properties:

- `StaticProps_ProxyConf: ProxyConfiguration`
  - This is the proxy configuration used for exposing `ModAPI.items`, `ModAPI.blocks`, `ModAPI.enchantments` and `ModAPI.materials`
  - See: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Proxy/Proxy
- `TeaVM_to_BaseData_ProxyConf: ProxyConfiguration`
  - This is a non-recursive proxy config for removing prefixes from java objects.
- `TeaVM_to_Recursive_BaseData_ProxyConf: ProxyConfiguration`
  - This is a recursive proxy config for removing prefixes from java objects. It handles properties (both object and array) as well as function outputs. Used for `ModAPI.player`, `ModAPI.mc`, `ModAPI.world`, `ModAPI.network` and more.
- `TeaVMArray_To_Recursive_BaseData_ProxyConf: ProxyConfiguration`
  - This is a recursive proxy config for handling arrays from `TeaVM_to_Recursive_BaseData_ProxyConf`

Methods:

- `ModAPI.util.str(jsString: String) : java.lang.String`
  - Converts a javascript string to a java string, for use in java methods and constructors.
  - Alias: `ModAPI.util.string()`
- `ModAPI.util.unstr(jclString: java.lang.String) : String`
  - Converts a java string to a javascript string.
  - Alias: `ModAPI.util.ustr()`
  - Alias: `ModAPI.util.unstring()`
  - Alias: `ModAPI.util.jclStrToJsStr()`
- `ModAPI.util.getMethodFromPackage(classId: String, methodName: String)`
  - Takes a class id (eg: `net.minecraft.client.Minecraft`) and a method name (eg: `middleClickMouse`) and returns its key in `ModAPI.hooks.methods`.
- `ModAPI.util.stringToUint16Array(string: String) : Uint16Array`
  - Encodes a string into a uint16array.
- `ModAPI.util.setStringContent(jclString: java.lang.String, contents: String) : void`
  - Writes a new javascript string into the contents of a java string.
- `ModAPI.util.getMethodFromPackage(classId: String, methodName: String)`
  - Takes a class id (eg: `net.minecraft.client.Minecraft`) and a method name (eg: `middleClickMouse`) and returns its key in `ModAPI.hooks.methods`.