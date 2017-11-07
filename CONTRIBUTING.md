# Contributing

Pull requests are welcome.


## Tests

There's a main class that can be used to test the integration. It's also useful to read this class to see how to integrate with the notification client.

On a command line build the project with Maven:

```shell
> mvn test
```

Then run Java via the Maven exec command with the following arguments:

```shell
> mvn exec:java -Dexec.mainClass=TestNotificationClient -Dexec.args="api-key-id https://api.notifications.service.gov.uk"
```

You'll be prompted to select an option to submit the API call.


## Readme updates
Update README.md as required - but you do not need to update the version numbers: 
both occurrences are automatically updated when you run `./update_version.sh`.

Note: If you add another instance of the version number in README.md, then the `./update_version.sh` script needs to be adjusted.


## Deploying

[For internal notify use only]
Make sure your `~/.m2/settings.xml` file is up to date with the file found at `credentials/bintray/settings.xml`

Then, from the notifications-java-client directory, run

```shell
./update_version.sh
./deploy.sh
```
