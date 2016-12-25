Encode:

scrypt enc -t120 data.txt | base64 > data.enc.txt
Decode:

base64 -d data.enc.txt > data.enc
scrypt dec data.enc




% ssss-split -t 3 -n 5
Generating shares using a (3,5) scheme with dynamic security level.
Enter the secret, at most 128 ASCII characters: my secret root password
Using a 184 bit security level.
1-1c41ef496eccfbeba439714085df8437236298da8dd824
2-fbc74a03a50e14ab406c225afb5f45c40ae11976d2b665
3-fa1c3a9c6df8af0779c36de6c33f6e36e989d0e0b91309
4-468de7d6eb36674c9cf008c8e8fc8c566537ad6301eb9e
5-4756974923c0dce0a55f4774d09ca7a4865f64f56a4ee0

These shares can be combined to recreate the secret:
% ssss-combine -t 3
Enter 3 shares separated by newlines:
Share [1/3]: 3-fa1c3a9c6df8af0779c36de6c33f6e36e989d0e0b91309
Share [2/3]: 5-4756974923c0dce0a55f4774d09ca7a4865f64f56a4ee0
Share [3/3]: 2-fbc74a03a50e14ab406c225afb5f45c40ae11976d2b665
Resulting secret: my secret root password
    7  sudo apt-get install curl vim git pandoc 
   45  sudo apt-get install texlive-latex-recommended
   46  sudo apt-get install qrencode
   52  apt-get install ssss scrypt 
   64  sudo apt-get install texlive-fonts-recommended
   70  history  | grep apt-get
   71  history  | grep apt-get | egrep "7|45|46|52|64"
   72  history  | grep apt-get | egrep "7|45|46|52|64" >> example.md 
