## Perubahan Code

1. load model di app.py (karena ga match versi waktu ngubah model jadi pickle)
    
        10. # import pickle <-- diubah
        429. # model = pickle.load(model_file) <--- diganti

        jadi

        11. from joblib import load
        429. model = load(model_file)

2. Chart Competitive Position Chart (karena ada data yang mines (-) di dataset jadi error)

        821. size=comp_df['Gap'], # <-- ini diganti

        jadi

        821. size=comp_df['Gap'].abs()
