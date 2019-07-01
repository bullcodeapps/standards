#Bullcode Standards

##Projects

- Every project must have these commands for running/building
```json
...
  "scripts": {
    "start": "...",
    "start:dev": "...",
    "build": "...",
    "build:release": "...",
    ...
  }
... 
```

###Angular
```json
...
  "scripts": {
    "start": "ng serve",
    "start:dev": "ng serve",
    "build": "node pre-build.js && ng build --prod --aot",
    "build:release": "npm run build",
    ...
  }
... 
```

###Ionic
```json
...
  "scripts": {
    "start": "ionic cordova run android",
    "start:dev": "ionic cordova run android --device -lcs",
    "build": "ionic cordova build",
    "build:release": "npm run build:release:android && npm run build:release:ios",
    "build:release:android": "ionic cordova build android --prod --aot --minifyjs --minifycss --optimizejs --release",
    "build:release:ios": "ionic cordova build ios --prod --aot --minifyjs --minifycss --optimizejs --release",
    ...
  }
... 
```

###React
