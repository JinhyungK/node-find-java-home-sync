#node-find-java-home

Returns the location of JAVA_HOME as an absolute path on windows, mac, and 
linux.  It runs asynchronously.

##Algorithm
1. This module will first attempt to check for JAVA_HOME.  If that's set it
simply returns that value.  
2. On windows the registry is queried.
3. If neither of the previous methods worked, then the PATH is scanned for javac
4. On mac, the parent directory of javac is checked for a java_home binary.  If that binary exists then it is executed and the result is used
5. The grandparent directory of javac is used.  This is similar to `$(dirname $(dirname $(readlink `which javac`)))`

##Example
````javascript
require('./')(function(err, home){
  if(err)return console.log(err);
  console.log(home);
});
````

##License
````
Copyright 2013 Joseph Spencer.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

      http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
````
