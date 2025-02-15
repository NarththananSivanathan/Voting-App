# Utilisation de l'image officielle .NET SDK pour la compilation
FROM mcr.microsoft.com/dotnet/sdk:7.0 AS build
WORKDIR /app

# Copier les fichiers projet et restaurer les dépendances
COPY *.csproj .
RUN dotnet restore

# Copier le reste du code et compiler en mode Release
COPY . .
RUN dotnet publish -c Release -o /out

# Utilisation de l'image officielle .NET runtime pour l'exécution
FROM mcr.microsoft.com/dotnet/aspnet:7.0 AS runtime
WORKDIR /app

# Copier les fichiers compilés depuis l'étape de build
COPY --from=build /out .

# Définir la commande d'exécution du service
CMD ["dotnet", "Worker.dll"]