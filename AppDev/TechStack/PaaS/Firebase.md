## Setup firebase locally

Install firetools globally
```
npm install -g firebase-tools
```

Login to firebase
```
firebase login
```
Initialize firebase in your project
```
firebase init
```

Once firebase is initialized, init emulator and select necessary emulators to start. You can use this command multiple times to add and remove emulators or emulator configurations
```
firebase init emulators
```

Use one of the commands to start the emulators
```
- firebase emulators:start
- firebase emulators:start --only firestore,authentication
```

By default, the Firebase emulator for Firestore and Authentication does not persist data across restarts

```
firebase emulators:start --import=./saved-data --export-on-exit=./saved-data
```


This command will:

- Import data from the ./saved-data directory when the emulator starts.
- Export data to the ./saved-data directory when the emulator exits.
- Use Ctrl-C to for a graceful shutdown so that data save works properly, be careful not to press it multiple times which might lead to force shutdown

**Note:**

- Found one issue emulators:start, failing repeated. If this occurs, clear all the log file and try. This worked for me.