# Liens

- [Documentation de Flutter](https://flutter.dev/docs).
- [Gallerie d'applications](https://gallery.flutter.dev/)
- <https://flutterawesome.com/>
- <https://itsallwidgets.com/awesome-flutter-flutter-tutorials>
- <https://github.com/Solido/awesome-flutter>
- Plusieurs tutos détaillés pour créer des applications Flutter complètes : <https://flutter-pro.com/flutter>


# FAQ

### ça marche pas !

Vérifie étape par étape ton [installation](installation.md).
Analyse ton système avec `flutter doctor`.

### je n'arrive pas à créer une grille de tuiles avec des morceaux d'une même image

Créer une grille carrée de taille `_numberOfTilesOnWidth` qui affiche les widgets retournées par la méthode `createTapableCroppedImageTiles`. Cette méthode doit retourner une `List<Widget>` contenant `_numberOfTilesOnWidth*_numberOfTilesOnWidth` widgets.

```
SizedBox(
    width: size,
    height: size,
    child: Container(
        margin: EdgeInsets.all(20.0),
        child: GridView.count(
            primary: false,
            padding: const EdgeInsets.all(1),
            crossAxisSpacing: 1,
            mainAxisSpacing: 1,
            crossAxisCount: _numberOfTilesOnWidth,
            children: this.createTapableCroppedImageTiles())))
```
