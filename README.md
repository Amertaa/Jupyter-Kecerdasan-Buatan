# Kecerdasan Buatan: Notebook Jupyter

Marsa Naufal (04231047). Kumpulan notebook untuk tiga topik, masing-masing di folder sendiri.

| Folder | Topik | Notebook |
|---|---|---|
| [GA/](GA) | Genetic Algorithm (PyGAD) | `genetic_algoritm.ipynb` (hyperparameter tuning & Vehicle Routing Problem), `05_applications_ga_checkpoint.ipynb` (contoh penerapan) |
| [NN/](NN) | Neural Network (PyTorch) | `finance_nn.ipynb` (deteksi fraud & skoring kredit, termasuk tuning hyperparameter), `neural_network.ipynb` (latihan klasifikasi `make_circles`) |
| [PSO/](PSO) | Particle Swarm Optimization (PySwarms) | `particle_swarm_opt.ipynb`, `05.applications_pso.ipynb`, `pso_pengembangan/` (PSO untuk smart city home) |

`data_janji_jiwa.csv` di root dipakai bersama oleh notebook GA dan PSO (dibaca lewat `../data_janji_jiwa.csv`).

## Menjalankan

```bash
python3 -m venv .venv && source .venv/bin/activate
pip install jupyter numpy pandas matplotlib scikit-learn   # semua notebook
pip install torch                                          # NN
pip install pygad                                          # GA
pip install pyswarms                                       # PSO
jupyter lab
```

Buka notebook dari folder masing-masing agar path relatif (`../data_janji_jiwa.csv`) benar.

## Catatan

- `NN/finance_nn.ipynb` memakai data **sintetis**; hasilnya bukan performa dunia nyata. Referensi: [PyTorch Classification](https://www.learnpytorch.io/02_pytorch_classification/) dan [Nielsen, Bab 1](http://neuralnetworksanddeeplearning.com/chap1.html).
- Gambar `img/...` di notebook `05_*` tidak ikut di repo, jadi tampil rusak.
- `test.ipynb`, `IKN-car-plate-gas-electrict-6/`, `runs/`, dan `*.pt` (percobaan YOLO) ada di root, tidak masuk ketiga topik, dan `runs/` serta `*.pt` diabaikan git karena ukurannya besar.
