# Matemaatiline kartograafia 2023
Antud juhendid toetavad geograafia eriala magistriõppe kursust <b>Matemaatiline kartograafia LOOM.02.007</b> ja keskenduvad Pythoni matemaatilise kartograafia ja visualiseerimise teegi [Cartopy](https://scitools.org.uk/cartopy/docs/latest/) võimalustele.

Esimene juhend annab ülevaate kaardiakna loomisest, erinevate projektsioonide kasutamisest ja lihtsamate kaardielementide (kaardivõrk, tekst) konstrueerimisest:
* https://github.com/LandscapeGeoinformatics/mcarto2023/blob/main/Kaardiakna_juhtimine.ipynb

Teine juhend keskendub täiendavate kaardielementide lisamisele, mille hulka kuuluvad nii lisadetailid (punkttähised, tekst ja legend) kui erinevad matemaatilised ja kartograafilised konstruktsioonid (ortodroom jms):
* https://github.com/LandscapeGeoinformatics/mcarto2023/blob/main/Kaardielemendid.ipynb

## Ettevalmistus
Juhendite kasutamine eeldab [Anaconda](https://conda.io/en/main/miniconda.html) olemasolu, mis peaks olema arvutiklassi arvutites tagatud. Kes soovib seda seadistada oma arvutis, võib selleks kasutada Alex Kmochi vastavat [juhendit](https://kodu.ut.ee/~kmoch/geopython2020/L0/Installing_Miniconda_GIS.html).

Pärast Anaconda installimist laadi alla ja paki kuhugi kausta lahti käesolev repositoorium koos kõigi failidega.

`Code -> Download ZIP`

![download_zip](https://github.com/LandscapeGeoinformatics/mcarto2023/blob/main/img/download_zip.png)

Seejärel leia ja ava käsurea kaudu nn Anaconda Prompt.

Liigu käsu `cd` abil kausta, kuhu pakkisid eelnevalt lahti GitHubist alla laaditud ZIP faili.

`cd C:\Users\Holger\mcarto2023-main\mcarto2023-main`

Käsu `ls` abil peaks nähtavale tulema kausta sisu, sh praktikumis kasutatavad Jupyteri töövihikud.

![folder](https://github.com/LandscapeGeoinformatics/mcarto2023/blob/main/img/folder.png)

Alustuseks loome Anaconda keskkonna nimega `mcarto2023` ning installime sellesse `cartopy` ja `jupyterlab` teegid, mida kasutame praktikumi ülesannetes. Parameeter `-c conda-forge` määrab Pythoni teekide lähtekanaliks [conda-forge](https://conda-forge.org/) repositooriumi.

`conda create -n mcarto2023 -c conda-forge cartopy jupyterlab`

![create_env](https://github.com/LandscapeGeoinformatics/mcarto2023/blob/main/img/create_env.png)

Järgmine rida aktiveerib äsjaloodud keskkonna.

`conda activate mcarto2023`

![activate_env](https://github.com/LandscapeGeoinformatics/mcarto2023/blob/main/img/activate_env.png)

Before we start Python coding we will make our newly created conda Python environment known to the Jupyter notebook system by installing the kernel, basically the execution engine link from Jupyter web notebook to our Python environment.

`python -m ipykernel install --user --name mcarto2023`

![install_kernel](https://github.com/LandscapeGeoinformatics/mcarto2023/blob/main/img/install_kernel.png)

Lõpuks aktiveeri Jupyteri keskkond.

`jupyter lab`

Avaneb brauser, kus klõps failil laiendiga *.ipynb* avab vastava töövihiku, mida saab brauseri aknas kasutama hakata.
