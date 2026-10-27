# Kecerdasan Buatan: Notebook Jupyter

Marsa Naufal (04231047). Notebook mata kuliah Kecerdasan Buatan, satu folder per topik.

| Folder | Topik | Notebook |
|---|---|---|
| [GA/](GA) | Genetic Algorithm (PyGAD) | `genetic_algoritm.ipynb` (hyperparameter tuning & Vehicle Routing Problem), `05_applications_ga_checkpoint.ipynb` (contoh penerapan) |
| [NN/](NN) | Neural Network (PyTorch) | `finance_nn.ipynb` (deteksi fraud & skoring kredit, termasuk tuning hyperparameter), `neural_network.ipynb` (latihan klasifikasi `make_circles`) |
| [PSO/](PSO) | Particle Swarm Optimization (PySwarms) | `particle_swarm_opt.ipynb`, `05.applications_pso.ipynb`, `pso_pengembangan/` (PSO untuk smart city home) |
| [Fuzzy/](Fuzzy) | Fuzzy Logic Mamdani (scikit-fuzzy) | `fuzzy_spare_parts.ipynb`: stok suku cadang (Problem 1: n untuk m=0.4, s=0.45, ρ=0.45; Problem 2: permukaan 3D untuk ρ=0) dan kasus tambahan risiko kredit; `contoh_fuzzy/` berisi 5 notebook contoh dari dosen (Sugeno, Tsukamoto, Mamdani, Tipping, project risk) |
| [UTS/](UTS) | UTS Kecerdasan Buatan 2026/2027 (seed 47) | `soal_03_ga.ipynb` (GA, seleksi fitur wine), `soal_07_pso.ipynb` (PSO, Energy Efficiency multi-output), `soal_12_fuzzy.ipynb` (Mamdani FIS, grid stability), `soal_16_mlp.ipynb` (MLP horsepower Auto MPG), `soal_23_pso_cnn.ipynb` (PSO tuning 1D-CNN, HAR); laporan LaTeX dan PDF-nya ada di `laporan/` |

Notebook GA dan PSO sama-sama membaca `data_janji_jiwa.csv` di root lewat `../data_janji_jiwa.csv`.

## Menjalankan

```bash
python3 -m venv .venv && source .venv/bin/activate
pip install jupyter numpy pandas matplotlib scikit-learn   # semua notebook
pip install torch                                          # NN
pip install pygad                                          # GA
pip install pyswarms                                       # PSO
pip install -U scikit-fuzzy                                # Fuzzy
pip install openpyxl                                       # UTS soal 7 (membaca .xlsx)
jupyter lab
```

Buka notebook dari foldernya masing-masing supaya path relatif seperti `../data_janji_jiwa.csv` benar. Notebook UTS membaca dataset UCI dari `UTS/data/` (wine+quality, energy+efficiency, Data_for_UCI_named.csv, auto+mpg, human+activity+recognition+using+smartphones).

## Catatan

- `Fuzzy/fuzzy_spare_parts.ipynb`: soal hanya memberi rentang, jadi bentuk fungsi keanggotaan (segitiga) adalah asumsi saya; asumsi dan hasilnya dijelaskan di notebook. Hasil Problem 1: n ≈ 0.34 (dinormalisasi).
- `NN/finance_nn.ipynb` memakai data sintetis, jadi angkanya tidak menggambarkan performa pada data nyata. Referensi: [PyTorch Classification](https://www.learnpytorch.io/02_pytorch_classification/) dan [Nielsen, Bab 1](http://neuralnetworksanddeeplearning.com/chap1.html).
- Gambar `img/...` di notebook `05_*` tidak ikut di repo, jadi tampil rusak.
- `test.ipynb`, `IKN-car-plate-gas-electrict-6/`, `runs/`, dan `*.pt` di root adalah percobaan YOLO di luar topik kuliah. `runs/` dan `*.pt` diabaikan git karena ukurannya besar.
