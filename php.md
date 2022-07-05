<?php
   @$civilite=$_POST["civilite"];
   @$nom=$_POST["nom"];
   @$prenom=$_POST["prenom"];
   @$email=$_POST["email"];
   @$pass=$_POST["pass"];
   @$repass=$_POST["repass"];
   @$valider=$_POST["valider"];
   
   if(isset($valider)){
      if(empty($nom))
         $message='<div class="erreur">Nom laissé vide.</div>';
      elseif(empty($prenom))
         $message='<div class="erreur">Prénom laissé vide.</div>';
      elseif(empty($email))
         $message='<div class="erreur">Email laissé vide.</div>';
      elseif(empty($pass))
         $message='<div class="erreur">Mot de passe laissé vide.</div>';
      elseif($pass!=$repass)
         $message='<div class="erreur">Les mots de passe ne sont pas identiques.</div>';
      else{
         $message='<div class="rappel"><b>Rappel:</b><br />';
         $message.=$civilite.' '.ucfirst(strtolower($prenom)).' '.strtoupper($nom).'<br />';
         $message.='Email: '.$email;
         $message.='</div>';
      }
   }
?>
