function hitungJumlahHariBersamamu(tglAwal){
    const tglSetAwal = new Date(tglAwal);
    const tglSekarang = new Date();
    const selisihWaktu = Math.floor(
        (tglSekarang - tglSetAwal) / (1000 * 60 * 60 * 24),
    );

    const formatTglAwal = tglSetAwal.toLocaleString('id-ID', {
        day: 'numeric',
        month: 'long',
        year: 'numeric',
    });

    const formatTglSekarang = tglSekarang.toLocaleDateString('id-ID', {
        day: 'numeric',
        month: 'long',
        year: 'numeric',
    })

    return `Day Since ${formatTglAwal}\nJumlah Hari Berlalu\n${selisihWaktu}hari\n${formatTglAwal} - ${formatTglSekarang}`;
}

const tglAwal = '2022-01-01';
const result = hitungJumlahHariBersamamu(tglAwal);
console.log(result);
