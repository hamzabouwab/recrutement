# Site-de-recrutement

# Code pour la création de la base de données

  ## Création des tables 
  #### table offres 
  create table offres(
  id int primary key auto_increment,
  specialite varchar(50) not null,
  recruteur varchar(50) not null,
  grade varchar(30) not null,
  date_debut date not null,
  date_fin date not null,
  date_offre datetime default current_timestamp,
  nombre_poste varchar(6) NOT null
  
  );
  ### tables candidats
create table candidats(
  id int primary key auto_increment,
  nom_complet varchar(15) not null,
  cin varchar(10) not null,
  date_naiss date not null,
  ref int not null,
      constraint f_k foreign key(ref) references offres(id)
  );
  ### table users
  create table users(
  id int primary key auto_increment,
  nom varchar(15) not null,
  prenom varchar(15) not null,
  email varchar(50) not null,
  password varchar(20) not null,
  date_insc datetime default current_timestamp
  )
  
