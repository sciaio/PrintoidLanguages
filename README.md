# Printoid Languages

This public repository contains the string resources for the internationalization of Printoid for OctoPrint.

## Contributing

Everyone can contribute to the internationalization of Printoid, by editing the existing language files or adding translations to a new locale.

All the informations are available on the official website:

[Contribute to the internationalization of Printoid](https://printoid.net/contribute-to-the-internationalization-of-printoid/)

If you want to contribute to the Printoid project and make it better, your help is very welcome. Contributing is also a great way to learn more about social coding on Github.

## Prerequisites

You don't need to be a developer to help me to translate Printoid :) You don't need any programming skills. You just have to edit XML files which contains the string resources (the words, sentences, etc. used in the application).

### Where are located the resources

The resources are located in the **/app/src/main/res/** folder.

- **values** contains the default values, in english
- **values-fr** contains the values translated in french
- **values-de** contains the values translated in german
- **values-es** contains the values translated in spanish
- **values-ru** contains the values translated in russian
- **values-nl** contains the values translated in dutch

### Create translations to a new language

To create the translations to a new language, you need to create a new folder in **/app/src/main/res/**.

For example, to introduce these new languages:

- **values-it** for italian translations
- **values-pt** for portuguese translations
- **values-pl** for polish translations
- ...

Then, copy all the **xml** files from an existing folder. For example:
- if you want to translate from English to Italian, then copy the files from **values** to **values-it**
- if you want to translate from French to Polish, then copy the files from **values-fr** to **values-pl**
- ...

Please, don't rename the files. Keep the files name (the strings are ordered by app features).

### Some translation examples

**A basic example**

In the file *values*/string_connect.xml :

```
<string name="connection_dialog_title">Connection to your server</string>
<string name="connection_dialog_message">Printoid is connecting to your server, please wait...</string>
```

The translation in french would look like, in **values-fr**/string_connect.xml :

```
<string name="connection_dialog_title">Connexion au serveur</string>
<string name="connection_dialog_message">Printoid se connecte à votre serveur, veuillez patienter...</string>
```

Please, don't rename the resource's names. You should only translate what's inside the ...> </string>

**An example with qualifiers**

Sometimes you will find some exotic characters, such as %d, %s, %.1f. These are qualifiers, where Printoid will inject dynamic values. For example:

```
<string name="config_say_hello">Hello %s!</string>
```

should be translated in french as:

```
<string name="config_say_hello">Bonjour %s !</string>
```

so Printoid will be able to inject the username, for example: "Hello Patrick!" and "Bonjour Patrick !"

Some qualifiers also have index to order the dynamic values: %1$s, %2$s, %3%s. For example:

```
<string name="config_introduce_developer">The developer is %1$s, and he is %2$d.</string>
```

should be translated in french as:

```
<string name="config_introduce_developer">Le développeur s\'appelle %1$s, et il a %2$d ans.</string>
```

**Character escapments**

And, last but not least, some characters have to be escaped, such as quotes. To escape a character, you have to add a backslash in front of it.

```
<string name="config_introduce_developer_age">He\'s 27 years old.</string>
```

And for carriage returns, that's **\n** :

```
<string name="connection_progress_dialog_message">The app is trying to communicates with your 3D printer.\nYou can drink a coffee for the next 2 seconds.</string>
```

## How to contribute

Please follow these indications if you want to contribute to the internationalization of Printoid.

### How to make a clean pull request

- Create a personal fork of the project on Github.
- Clone the fork on your local machine. Your remote repo on Github is called `origin`.
- Add the original repository as a remote called `upstream`.
- If you created your fork a while ago be sure to pull upstream changes into your local repository.
- Create a new branch to work on from `master`.
- Implement/fix the language files
- Follow the code style of the project, including indentation.
- Squash your commits into a single commit with git's [interactive rebase](https://help.github.com/articles/interactive-rebase). Create a new branch if necessary.
- Push your branch to your fork on Github, the remote `origin`.
- From your fork open a pull request in the correct branch. Target the project's `develop` branch if there is one, else go for `master`!
- Once the pull request is approved and merged you can pull the changes from `upstream` to your local repo and delete
your extra branch(es).

And last but not least: Always write your commit messages in the present tense. Your commit message should describe what the commit, when applied, does to the code – not what you did to the code.

Here is a great and complete tutorial to do pull requests: [Create Pull Requests (tutorial)](https://yangsu.github.io/pull-request-tutorial/)

And a beautiful video: [Create Pull Requests (video)](https://www.youtube.com/watch?v=oFYyTZwMyAg)

## Deployment

Printoid Languages is embedded in Printoid as a library. All the changes in this repository will be included in the next releases of Printoid.

## Authors

* **Anthony STEPHAN** - *Initial work* 🇬🇧 *English translations* 🇫🇷 *French translations* - [AnthonySt91](https://github.com/anthonyst91)

* **Dmitriy CHERNYY** - *🇷🇺 Russian translations*

* **Nico HIRSCH** - *🇩🇪 German translations*

* **Gorka HERRERO** - *🇪🇸 Spanish translations*

* **Angel DEL PINO JIMENEZ** - *🇪🇸 Spanish translations*

* **Ruud RADEMAKER** - *🇳🇱 Dutch translations*


## License

This project is licensed under the Apache License 2.0 - see the [LICENSE.md](LICENSE.md) file for details

```
Copyright 2018 WindSekirun (DongGil, Seo)

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
