# RoboticsBrno C++ code style
[[English version follows]](#english-version)

Doporučený styl pro C++ zdrojový kód v projektech na GitHub profilu [`RoboticsBrno`](https://github.com/RoboticsBrno) specifikovaný v [`.clang-format` souboru](/.clang-format).

Založeno na [WebKit Code Style Guidelines](https://webkit.org/code-style-guidelines/) s menšími úpravami:
- `AfterClass: true` => `class foo {};`
- `AfterFunction: false` => `void foo() {...`
- `BreakBeforeBraces: Attach` => `void foo() {...`
- `NamespaceIndentation: None` => kód uvnitř vnitřních `namespace` se neodsazuje
- `ReflowComments: false` => komentáře nejsou omezeny maximálním počtem znaků na řádek

### VS Code & Visual Studio 2017+

Specifikace v `.clang-format` souboru lze využít pro nastavení formátování ve [VS Code](https://code.visualstudio.com/docs/cpp/cpp-ide#_code-formatting) a [od verze 2017 také ve Visual Studiu](https://devblogs.microsoft.com/cppblog/clangformat-support-in-visual-studio-2017-15-7-preview-1/).

Pokud chcete aktivovat automatické formátování zdrojového kódu při uložení ve `VS Code`, přidejte si do `.vscode/setting.json` toto nastavení: `"editor.formatOnSave": true` (viz soubor [`setting.json`](/.vscode/settings.json) v tomto repozitáři).

Pro automatické formátování zdrojového kódu při uložení ve `Visual Studiu` je potřeba nainstalovat doplněk [Format document on Save](https://marketplace.visualstudio.com/items?itemName=mynkow.FormatdocumentonSave).

### clang-format z příkazové řádky

Specifikaci v `.clang-format` souboru lze na zdrojový kód aplikovat také pomocí command-line utility [Clang-format](https://clang.llvm.org/docs/ClangFormat.html).

Na Linuxu by měla být `Clang-format` utilita dostupná přes baličkovacího managera (`apt-get`...).

Na Windows si lze stáhnout oficiální [`clang-format.exe` soubor](https://prereleases.llvm.org/win-snapshots/clang-format-2663a25f.exe) ze [stránek LLVM](https://llvm.org/builds/) (autoři utility).

Pokud si stáhnete `clang-format.exe` do stejného adresáře, jako máte `.clang-format` soubor, stačí již jen zavolat příkaz tento příkaz v  příkazové řádce (`cmd`):
```
clang-format.exe -i CESTA\KE\ZDROJOVYM\SOUBORUM\*
```  

Přepínač `-i` znamená, že jsou změnu hned aplikovány na zdrojový kód. Bez tohoto přepínače se jen vypíše upravený kód do příkazové řádky, ale změny se neaplikují.

## English Version

Recommanded C++ code style for projects on [`RoboticsBrno's`](https://github.com/RoboticsBrno) GitHub profile specified in [`.clang-format` file](/.clang-format).

Based on [WebKit Code Style Guidelines](https://webkit.org/code-style-guidelines/) with some modification:
- `AfterClass: true` => `class foo {};`
- `AfterFunction: false` => `void foo() {...`
- `BreakBeforeBraces: Attach` => `void foo() {...`
- `NamespaceIndentation: None` => code inside `namespace` is not indented 
- `ReflowComments: false` => comments are not limited to maximal number of characters per line
