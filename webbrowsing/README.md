Load modules:
```bash
module load LUMI/24.03
module load systools    # provides Singularity/Apptainer
```



Build a writable development container

```bash
singularity build --sandbox web_browsing.sif web_browsing.def

singularity exec web_browsing.sif /bin/bash

lynx https://csc.fi/en/
```


