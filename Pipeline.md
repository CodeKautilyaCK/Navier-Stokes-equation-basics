CFD_NS_1D_2D/
│
├── geometry.py           # Defines geometries for 1D and 2D simulations
├── 1d.py                 # 1D Navier–Stokes solver (FDM/FVM)
├── 2d.py                 # 2D Navier–Stokes solver (FDM/FVM)
├── main.py               # Driver file to run simulations & generate logs/animations
├── README.md             # Project description, explanation, equations
├── requirements.txt      # Python dependencies
├── LOG/                  # Folder to store simulation logs and animations
│    ├── 1D/              # 1D simulation results/animations
│    └── 2D/              # 2D simulation results/animations
└── PINN/                 # Optional future folder for PINN implementations
     ├── 1D_PINN.py
     └── 2D_PINN.py
