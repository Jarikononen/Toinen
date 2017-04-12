h2. a) Tee tämän kotitehtävän raportti GitHubiin MarkDownilla
b) Tee puppet-moduli, joka tekee asetukset jollekin komentorivi- tai graafisen käyttöliittymän ohjelmalle.

Ensiksi asennetaan Kubuntu käyttöjärjestelmä kannattavalle tietokoneelle.

->
Asennetaan: sudo apt-get install puppet

->

Luodaan /etc/puppet/ kansioon 

->

sudo mkdir /toinen/

->

/etc/puppet/modules/toinen/

sudo mkdir templates ja mkdir manifests

->

Luodaan manifests alikansion = sudo kate init.pp

class toinen {
             file {’/etc/bash.bashrc’:
	   content => template( ’alias/bash.bashrc.erb’)
              }

->

mennään kansioon /etc/puppet/modules/toinen/template/

->

sudo -cp -n /etc/bash.bashrc .

Ja

sudo -mv -n /etc/bash.bash.bashrc .



->

sudo kate bash.bashrc

ja lisätään rivi: alias v=’vlc’

tämän jälkeen tallennus.

->

ajetaan komento: sudo puppet apply -e ’class {toinen:}’

->

Ja saamme virheilmoituksen: Could not find template…



->

Tämä harjoiteosa kaatui valitettavasti tähän.
