# Design and Development of Digital Learning Game

## Generate Report
```bash
docker run --rm -u `id -u`:`id -g` -v `pwd`:/pandoc sintoris/pandocker:twemoji -d pdf.yaml -N -M link-citations=true --citeproc
```