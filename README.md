# ripsvs-full-img
Forked from [williamdee1/ripsvs](https://github.com/williamdee1/ripsvs/)

Changes made:
* The preview image is saved on its full resolution
* The extracted 512px tiles are deleted after preview.jpeg is generated

## Limited Initial Deployment
Currently designed to download online .svs files hosted by Aperio ImageScope. 

Initially tested for the .svs files in the [Nikiforov BoxA samples](http://image.upmc.edu:8080/NikiForov%20EFV%20Study/BoxA/view.apml?listview=1).

Further work may extend to additional image hosting domains.

## Getting Started

```bash
# Download and build the extraction tool:
git clone https://github.com/gilbertzaini/ripsvs-full-img
cd ripsvs-full-img
go build .

# Download the full image from url
 ./ripsvs --url "http://image.upmc.edu:8080/NikiForov%20EFV%20Study/BoxA/" A009 # Linux
 or
ripsvs.exe --url "http://image.upmc.edu:8080/NikiForov%20EFV%20Study/BoxA/" A009 # Windows
```

An "output" folder will be created with separate folders for each .svs file processed. Within those folders will be the whole slide image stored in .jpeg format.
