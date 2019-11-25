# ProgImpAv-2020-Ex1
Modèle de départ pour exercices d'introduction à Visual Studio Code, au débogueur, à la gestion de versions et github.com.

## Instructions de départ

1. Créez un compte github.com.
1. Créez une clé SSH. (Pas strictment nécéssaire mais évite d'avoir à retaper votre mot de passe github.)
    - Suivez ces instructions: https://help.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent.
    - Et celles-ci: https://help.github.com/en/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account.
1. Créez votre dépot sur github.com en utilisant ce dépôt-ci (https://github.com/thierryseegers/ProgImpAv-2020-Ex1) comme modèle.
    - Suivez ces instructions: https://help.github.com/en/github/creating-cloning-and-archiving-repositories/creating-a-repository-from-a-template.
    - Choisissez l'option `Private` à l'étape 5.
1. Ajoutez le professeur comme collaborateur à votre dépot.
    - Suivez ces instructions: https://help.github.com/en/github/setting-up-and-managing-your-github-user-account/inviting-collaborators-to-a-personal-repository
        - Nom d'utilisateur à ajouter: `thierryseegers`.
1. Clonez votre dépot vers votre espace de travail local.
    - Suivez ces instructions: https://help.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository
    - Attention à ne pas cloner https://github.com/thierryseegers/ProgImpAv-2020-Ex1 mais bien votre dépôt nouvellement créé.
1. Lancez Visual Studio Code.
    - À l'invite de commande:
        - `> cd [nom de votre dépôt]`
        - `> code .`
1. Installez l'extension `C/C++` pour Visual Studio Code.
    - Suivez ces instructions: https://code.visualstudio.com/docs/languages/cpp#_install-the-microsoft-cc-extension.
1. Pour travailler sous MacOS, installez aussi Xcode et l'extension `CodeLLDB` pour Visual Studio Code.
    - Installez Xcode via le App Store.
    - Installez "Xcode Command Line Tools". À l'invite de commande: `> xcode-select --install`
    - https://marketplace.visualstudio.com/items?itemName=vadimcn.vscode-lldb
1. Compilez une première fois le programme.
    - Menu: `View` > `Command Palette` > `Tasks: Run Build Task`
1. Executez une première fois le programme avec le débogueur.
    - Menu: `View` > `Debug`
    - Choisissez la cible correspondant à votre system opérateur.
        - Menu déroulant `DEBUG`: {`test (Linux)`, `test (MacOS)`}
    - Menu: `Debug` > `Start debugging`
    - Vous devriez voir dans l'onglet `DEBUG CONSOLE` le résultat suivant:
        - `Launching: [chemin d'acces]/a.out Process exited with code 23.`

Vous pouvez voir la valeur retournée par le programme dans l'onglet `DEBUG CONSOLE` comme décrit ci-haut.
Vous pouvez aussi voir la valeur retournée par le dernier programme lancé à l'invite de commandes avec `echo $?`.
Dans l'example suivant, le programme `a.out` a retourné la valeur `23`.
```
> ./a.out
> echo $?
23
```

## Objectif

Le programme contient quatre fonctions qui contiennent des erreurs.
Ces fonctions sont testées par un macro qui compare le résultat reçu avec le résultat attendu.
Si les résultats ne correspondent pas, un compteur de résultat final est incrementé de un.
À la fin du programme, ce compteur final est retourné au system opérateur.
L'objectif est de réparer toutes les fonctions et que le programme retourne `0`.

Il vous est permis: 
- De modifier les définitions des fonctions `palindrome`, `inverse`, `en_chaine` et `anagramme` à votre gré.

Il ne vous est pas permis:
- De modifier les déclarations des fonctions `palindrome`, `inverse`, `en_chaine` et `anagramme`. (Leurs types de retour et les types de leurs paramètres ne peuvent être modifiés.)
- De modifier la définition de la fonction `main`.

## Instructions de travail

1. Au fur et à mesure de vos modifications au code, intégrez-les au dépôt local avec une description des modifications apportées.
    - `> git add main.c`
    - `> git commit -m "Description des modifications apportées"`
1. Périodiquement, publiez votre branche de votre dépôt local à votre dépôt sur github.com.
    - `> git push`

Seul le code sur github.com compte.

## "J'ai un problème !"

Il est parfaitement acceptable de demander de l'aide sur Internet.
Par contre, sur Internet, les questions d'étudiant se reniflent de loin alors soyez honnête dans la formulation de votre question et demandez bien *de l'aide*, ne demandez pas *la réponse*.

#### Comment demander de l'aide
1. https://stackoverflow.com/help/how-to-ask
1. https://en.wikipedia.org/wiki/Wikipedia:Reference_desk/How_to_ask_a_software_question
1. http://www.catb.org/%7Eesr/faqs/smart-questions.html

#### Où demander de l'aide
1. stackoverflow.com
1. reddit.com/r/codinghelp
