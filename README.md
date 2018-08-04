# Secret Login User
En suivant ce README, vous allez pouvoir recreer une application qui geres les sessions utilisateurs par des logins et passwords. Rendez votre application et fonctionnalités disponibles que pour certains utilisateurs. Organiser votre base de donnée et à vous la gloire !

# 1. La création de l'application 
Commencer par créer votre application rails gr^âce à la commande suivante : 

```sh
$ cd le_dossier_dans_lequel_tu_veux_creer_ton_app
$ rails new le_nom_trop_cool_de_ton_app
```
Puis ouvre ton app dans ton IDE préféré : 
```sh
$ atom le_nom_trop_cool_de_ton_app
$ cd le_nom_trop_cool_de_ton_app
```
Modifie le Gemfile cette ligne : 
```sh
8  # Use sqlite3 as the database for Active Record
9  gem 'sqlite3'
```
Par :  
```sh 
group :development, :test do
 gem 'sqlite3'
end

group :production do
  gem 'pg', '>= 0.18', '< 2.0'
end
```
Enfin, lance le bundle avec cette commande :
```sh
$ bundle install --wihthout production
```
Nous allons ensuite créer une application Heroku : 

```sh
heroku create nom-de-ton-app-trop-cool
```
Dans ton terminal, tu devrais avoir quelque chose comme ça : 
```sh
Creating ⬢ solo-secret... done
https://solo-secret.herokuapp.com/ | https://git.heroku.com/solo-secret.git
```
Youpie ton app est en ligne ! 
