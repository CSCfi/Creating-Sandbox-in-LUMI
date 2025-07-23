module load LUMI/24.03 systools

# Build a writable development container
singularity build --sandbox online_shopping.sif online_shopping.def

singularity exec online_shopping.sif /bin/bash

lynx https://www.amazon.com

Option B: Private browsing using Tor

tor --version           # Check version
tor &                   # Start Tor service
torsocks lynx https://check.torproject.org
torsocks lynx https://www.amazon.com
