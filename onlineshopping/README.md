Load modules:
```bash
module load LUMI/24.03
module load systools    # provides Singularity/Apptainer
```



Build a writable development container

```bash
singularity build --sandbox onlineshopping.sif onlineshopping.def

singularity exec online_shopping.sif /bin/bash

lynx https://www.amazon.com
```

Option B: Private browsing using Tor

```bash
tor --version           # Check version
tor &                   # Start Tor service
torsocks lynx https://check.torproject.org
torsocks lynx https://www.amazon.com
```
