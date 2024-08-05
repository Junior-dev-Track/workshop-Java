# Workshop Java

## 1. Installation de Java 21

### Linux

#### Installation via le gestionnaire de paquets

Certains gestionnaires de paquets pourraient ne pas encore proposer Java 21 directement. Dans ce cas, l'installation manuelle est recommandée.

1. **Ubuntu/Debian (via PPA) :**
   - Ajoutez le PPA (si disponible) pour Java 21, ou installez manuellement :
   ```bash
   sudo add-apt-repository ppa:linuxuprising/java
   sudo apt update
   sudo apt install oracle-java21-installer
   ```

2. **Fedora :**
   - Téléchargez et installez manuellement si Java 21 n'est pas disponible via DNF.

3. **Arch Linux :**
   - Utilisez l'AUR pour installer Java 21, si disponible :
   ```bash
   yay -S jdk21-openjdk
   ```

#### Installation manuelle

1. Téléchargez le JDK depuis le site officiel d'Oracle ou un autre fournisseur de JDK (comme Adoptium).
2. Extrayez l'archive téléchargée :
   ```bash
   tar -xzf openjdk-21_linux-x64_bin.tar.gz
   ```
3. Déplacez le dossier extrait vers `/usr/local/java` :
   ```bash
   sudo mv jdk-21 /usr/local/java/
   ```
4. Mettez à jour les alternatives pour utiliser Java 21 :
   ```bash
   sudo update-alternatives --install /usr/bin/java java /usr/local/java/jdk-21/bin/java 1
   sudo update-alternatives --config java
   ```

### macOS

#### Installation via Homebrew

1. Assurez-vous d'avoir Homebrew installé. Si ce n'est pas le cas, installez-le en suivant les instructions sur [brew.sh](https://brew.sh/).
2. Installez OpenJDK 21 :
   ```bash
   brew install openjdk@21
   ```
3. Ajoutez le JDK à votre PATH :
   ```bash
   echo 'export PATH="/usr/local/opt/openjdk@21/bin:$PATH"' >> ~/.zshrc
   source ~/.zshrc
   ```

### Windows

#### Installation via l'installateur

1. Téléchargez l'installateur pour Windows depuis le site officiel d'Oracle ou Adoptium.
2. Exécutez l'installateur et suivez les instructions pour installer Java 21.
3. Après l'installation, assurez-vous que le répertoire `bin` de l'installation de Java est ajouté à la variable d'environnement `PATH`. Pour cela :
   - Ouvrez le Panneau de configuration → Système et sécurité → Système → Paramètres système avancés.
   - Cliquez sur **Variables d'environnement** et dans la section **Variables système**, trouvez la variable `Path` et cliquez sur **Modifier**.
   - Ajoutez le chemin vers le dossier `bin` du JDK, par exemple `C:\Program Files\Java\jdk-21\bin`.

## 2. Configuration de l'environnement de développement

### Visual Studio Code

1. **Installer les extensions nécessaires :**
   - Ouvrez Visual Studio Code.
   - Allez dans le gestionnaire d'extensions (`Ctrl+Shift+X` ou `Cmd+Shift+X` sur macOS).
   - Recherchez et installez les extensions suivantes :
      - **Java Extension Pack** (fournit des outils pour le développement Java).
      - **Debugger for Java** (pour le débogage).

2. **Configurer le JDK :**
   - Ouvrez la palette de commandes (`Ctrl+Shift+P` ou `Cmd+Shift+P` sur macOS) et tapez `Java: Configure Java Runtime`.
   - Sélectionnez le JDK 21 que vous avez installé.

### IntelliJ IDEA

1. **Téléchargement et installation :**
   - Téléchargez IntelliJ IDEA depuis le [site officiel de JetBrains](https://www.jetbrains.com/idea/download/).
   - Installez IntelliJ IDEA en suivant les instructions pour votre système d'exploitation.

2. **Configurer le JDK :**
   - Ouvrez IntelliJ IDEA.
   - Créez ou ouvrez un projet Java.
   - Allez dans `File` > `Project Structure` > `Project`.
   - Sous `Project SDK`, cliquez sur `New...` et sélectionnez le chemin du JDK 21 que vous avez installé.
   - Appliquez les modifications.

3. **Créer un projet Java :**
   - Pour créer un nouveau projet Java, allez dans `File` > `New` > `Project`.
   - Sélectionnez "Java" et choisissez le SDK approprié.
   - Suivez les étapes pour configurer votre projet.

## 3. Vérification de l'installation

### Vérifier la version de Java

Pour vous assurer que Java 21 est correctement installé, ouvrez un terminal ou une invite de commande et exécutez :

```bash
java -version
```

Cela devrait afficher une sortie indiquant que Java 21 est installé.

### Test simple de compilation et d'exécution

Créez un fichier `HelloWorld.java` avec le contenu suivant :

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

Compilez et exécutez le fichier :

```bash
javac HelloWorld.java
java HelloWorld
```

Vous devriez voir la sortie `Hello, World!`.
