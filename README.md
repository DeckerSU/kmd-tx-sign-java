# KMD Transaction Signing in Java

### Description

I am not a Java programmer and had never worked with Java before this project. Concepts like how Java operates, what Gradle is, how to structure projects and subprojects, and the purposes of `build.gradle` and `settings.gradle` were completely unfamiliar to me. However, I was asked to create a Java-based demo showcasing offline signing of KMD transactions.

To accomplish this, I dedicated almost an entire day to writing this example, which is based on the `bitcorej` library. A significant amount of time was spent understanding how to resolve dependency builds with `Gradle 8.11.1` and how to include `bitcorej` in the demo project. In the end, everything came together successfully.

### How to Build and Test

1. Clone the repository:
   ```bash
   git clone https://github.com/DeckerSU/kmd-tx-sign-java
   cd kmd-tx-sign-java
   ```

2. Update submodules:
   ```bash
   git submodule update --init --recursive
   ```

3. Build and run the project:
   ```bash
   gradle clean build
   gradle run
   ```

Ensure that **Gradle 8.11.1** and **JVM 17.0.13** are properly installed on your system.

### Result

After running the project, the following output will be generated:

```
Public key (address): t1TJ4H8jvUmTV2af9TwTesp7yPjeeUrbC2A
Secret key: 38cb1b39ad35f3f9402f373ca4dcde2469307fa17d011cf3b21ac3ba74d78967
[38cb1b39ad35f3f9402f373ca4dcde2469307fa17d011cf3b21ac3ba74d78967]
{
  "inputs": [
    {
      "txid": "ddf306c1c7229b3e14767ead6c2c4d2a8f9920eb49d7380fddbaa53b86002fe3",
      "vout": 1,
      "output": {
        "amount": "0.05000000",
        "script": "76a91467590bd560ce578129e9661c5782ec3fe9e8cc9c88ac"
      }
    }
  ],
  "outputs": [
    {
      "amount": "0.05000000",
      "script": "76a91467590bd560ce578129e9661c5782ec3fe9e8cc9c88ac"
    }
  ]
}

{"txid":"dea028973e6a211bbf50363427ab74126070dc656dec4efb0c6f329b7f0baa75","raw":"0400008085202f8901e32f00863ba5badd0f38d749eb20998f2a4d2c6cad7e76143e9b22c7c106f3dd010000006b483045022100be02bf5f90a260425f69e3a8347b84523789f6359c4faadaaffd2519dabb7fbf0220243fa31dcb669c1295597581cf2f421692ca9599e2c52d269eea056b43ba5175012102faef4f497fc37fd8e44f7cba0d96b9324c19b20343951c2597923a2d74a8f011ffffffff01404b4c00000000001976a91467590bd560ce578129e9661c5782ec3fe9e8cc9c88ac00000000000000000000000000000000000000"}
Decker was here! I am not a Java coder =)
```

As you can see, the KMD transaction was successfully signed offline and broadcasted to the network. You can view the transaction here: [dea028973e6a211bbf50363427ab74126070dc656dec4efb0c6f329b7f0baa75](https://kmdexplorer.io/tx/dea028973e6a211bbf50363427ab74126070dc656dec4efb0c6f329b7f0baa75).

