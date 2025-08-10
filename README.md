<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Formulir Pendaftaran Pasien</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f8fb;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #0077b6;
            color: white;
            padding: 15px;
            text-align: center;
        }
        form {
            background-color: white;
            max-width: 600px;
            margin: 20px auto;
            padding: 25px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }
        h2 {
            text-align: center;
            color: #0077b6;
        }
        label {
            display: block;
            margin-top: 10px;
            font-weight: bold;
        }
        input, select, textarea {
            width: 100%;
            padding: 8px;
            margin-top: 5px;
            border: 1px solid #ccc;
            border-radius: 5px;
            box-sizing: border-box;
        }
        textarea {
            resize: vertical;
        }
        .btn {
            display: flex;
            justify-content: space-between;
            margin-top: 20px;
        }
        button {
            padding: 10px 15px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
        .submit-btn {
            background-color: #0077b6;
            color: white;
        }
        .reset-btn {
            background-color: #ccc;
        }
        button:hover {
            opacity: 0.9;
        }
        footer {
            text-align: center;
            padding: 15px;
            background-color: #0077b6;
            color: white;
            margin-top: 30px;
        }
    </style>
</head>
<body>

<header>
    <h1>Rumah Sakit Sehat Selalu</h1>
    <p>Formulir Pendaftaran Pasien</p>
</header>

<form action="proses_pendaftaran.php" method="POST">
    <h2>Data Pribadi</h2>
    <label>Nama Lengkap</label>
    <input type="text" name="nama" required>

    <label>Nomor Identitas (KTP/SIM)</label>
    <input type="text" name="identitas" required>

    <label>Tanggal Lahir</label>
    <input type="date" name="tgl_lahir" required>

    <label>Jenis Kelamin</label>
    <select name="jk" required>
        <option value="">-- Pilih --</option>
        <option value="Laki-laki">Laki-laki</option>
        <option value="Perempuan">Perempuan</option>
    </select>

    <label>Alamat</label>
    <textarea name="alamat" rows="2" required></textarea>

    <label>Nomor HP</label>
    <input type="tel" name="hp" required>

    <label>Email</label>
    <input type="email" name="email" required>

    <h2>Data Medis</h2>
    <label>Keluhan Utama</label>
    <textarea name="keluhan" rows="2"></textarea>

    <label>Riwayat Penyakit</label>
    <textarea name="riwayat" rows="2"></textarea>

    <label>Alergi</label>
    <textarea name="alergi" rows="2"></textarea>

    <h2>Pilihan Pendaftaran</h2>
    <label>Poli Tujuan</label>
    <select name="poli" required>
        <option value="">-- Pilih Poli --</option>
        <option value="Umum">Poli Umum</option>
        <option value="Gigi">Poli Gigi</option>
        <option value="Anak">Poli Anak</option>
        <option value="Kandungan">Poli Kandungan</option>
    </select>

    <label>Tanggal Kunjungan</label>
    <input type="date" name="tgl_kunjungan" required>

    <label>Jam Kunjungan</label>
    <input type="time" name="jam_kunjungan" required>

    <div class="btn">
        <button type="submit" class="submit-btn">Kirim Pendaftaran</button>
        <button type="reset" class="reset-btn">Reset</button>
    </div>
</form>

<footer>
    &copy; 2025 Rumah Sakit Sehat Selalu
</footer>

</body>
</html>
