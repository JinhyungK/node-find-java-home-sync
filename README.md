#node-find-java-home

Returns the location of JAVA_HOME as an absolute path on windows, mac, and 
linux.  It runs asynchronously.

##Example
````javascript
require('./')(function(err, home){
  if(err)return console.log(err);
  console.log(home);
});
````

````
Finds the location of java home on any system.
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