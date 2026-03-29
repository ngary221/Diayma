# Boutique Diayma
## 2. Projets de la solution
- La solution contient **un seul projet principal** : `Diayma`.

## 3. Version SDK .NET
- netcoreapp2.0

## 6. Explorez l’application. Signalez 2 bugs trouvés ?
- P2FixAnAppDotNetCode/Models/Repositories/ProductRepository.cs — ligne 15
--Le champ static List<Product> _products est recréé dans le constructeur à chaque nouvelle instance. Avec ProductRepository enregistré en Transient, l’inventaire est réinitialisé à chaque requête et les stocks ne sont pas conservés.
- P2FixAnAppDotNetCode/Components/CartSummaryViewComponent.cs — ligne 12
- Le constructeur fait cart as Cart sans vérification. Si l’injection DI fournit un ICart non convertible en Cart, _cart devient null, ce qui casse le rendu de la vue.

## 8. Espaces de noms, classes et méthodes visitées avant l'affichage des produits sur l'écran d'accueil
- P2FixAnAppDotNetCode.Program.Main()— Pas à pas principal (F10)
- P2FixAnAppDotNetCode.Program.CreateWebHostBuilder()— Pas à pas détaillé (F11)
- P2FixAnAppDotNetCode.Startup.ConfigureServices(IServiceCollection)— Pas à pas détaillé (F11)
- P2FixAnAppDotNetCode.Startup.Configure(IApplicationBuilder, IHostingEnvironment)— Pas à pas détaillé (F11)
- P2FixAnAppDotNetCode.Controllers.ProductController.Index()— Pas à pas détaillé (F11)
- P2FixAnAppDotNetCode.Models.Services.ProductService.GetAllProducts()— Pas à pas détaillé (F11)
- P2FixAnAppDotNetCode.Models.Repositories.ProductRepository.GetAllProducts()— Pas à pas détaillé (F11)
- P2FixAnAppDotNetCode.Components.CartSummaryViewComponent.Invoke()— Pas à pas principal (F10)
- P2FixAnAppDotNetCode.Components.LanguageSelectorViewComponent.Invoke()— Pas à pas principal (F10)

## 10. Lien vers l’exécutable

- Dossier publié : `P2FixAnAppDotNetCode/bin/Release/netcoreapp2.0/win-x64/publish/`
- Exécutable généré : `Diayma.exe`
- Lien de téléchargement : https://drive.google.com/drive/folders/1tfiBBD0K1tYtjNr7AhvTKWtkYJTQKbw0?usp=sharing
