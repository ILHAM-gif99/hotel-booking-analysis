# Hotel Booking Analysis

## Project Overview

Analisis data **119.390 booking hotel** menggunakan Power BI, Power Query, DAX, dan Google Sheets untuk memahami pola booking, cancellation, customer type, market segment, pola musiman, serta estimasi nilai booking.

## Business Problem

Hotel perlu memahami:
- Jumlah booking dan pembatalan.
- Perbedaan performa City Hotel dan Resort Hotel.
- Customer type dan market segment utama.
- Segment dengan cancellation rate tinggi.
- Pola booking berdasarkan bulan.
- Strategi promosi yang sesuai berdasarkan hotel dan pelanggan.

## Objectives

1. Menganalisis booking berdasarkan jenis hotel.
2. Mengukur cancellation rate.
3. Menganalisis customer type dan market segment.
4. Menganalisis tren booking bulanan.
5. Menganalisis ADR dan Lead Time.
6. Menghitung Estimated Booking Value.
7. Menghasilkan insight dan rekomendasi bisnis.

## Tools

- Microsoft Power BI
- Power Query
- DAX
- Google Sheets
- Pivot Table
- Data Cleaning
- Exploratory Data Analysis (EDA)
- Data Visualization

## Dataset

Dataset yang digunakan adalah **Hotel Booking Demand** dengan 119.390 data booking.

Kolom utama:
- `hotel`
- `is_canceled`
- `lead_time`
- `arrival`
- `stays_in_weekend_nights`
- `stays_in_week_nights`
- `customer_type`
- `market_segment`
- `adr`
- `reservation_status`

### Data Transformation

**Total Nights**
```text
Total Nights = stays_in_weekend_nights + stays_in_week_nights
```

**Estimated Booking Value**
```text
Estimated Booking Value = ADR × Total Nights
```

> Estimated Booking Value adalah estimasi berdasarkan ADR × total malam, bukan revenue aktual.

## Key Results

### Hotel Performance

| Hotel | Booking | Cancellation Rate | Average Stay |
|---|---:|---:|---:|
| City Hotel | 79.330 | 41,73% | 2,98 malam |
| Resort Hotel | 40.060 | 27,76% | 4,32 malam |

### Overall Booking

- Total Booking: **119.390**
- Tidak Dibatalkan: **75.166**
- Dibatalkan: **44.224**
- Cancellation Rate: **37,04%**

### Customer Type

| Customer Type | Booking | Persentase |
|---|---:|---:|
| Transient | 89.613 | 75,06% |
| Transient-Party | 25.124 | 21,04% |
| Contract | 4.076 | 3,41% |
| Group | 577 | 0,48% |

### Market Segment

| Market Segment | Booking | Persentase |
|---|---:|---:|
| Online TA | 56.477 | 47,30% |
| Offline TA/TO | 24.219 | 20,29% |
| Groups | 19.811 | 16,59% |
| Direct | 12.606 | 10,56% |
| Corporate | 5.295 | 4,44% |

### Cancellation by Market Segment

- Groups: **61,06%**
- Online TA: **36,72%**
- Offline TA/TO: **34,32%**
- Direct: **15,34%**

### Monthly Booking

- Highest: **August — 13.877 booking**
- Lowest: **January — 5.929 booking**

## Descriptive Statistics

| Variable | Mean | Median | Std Dev |
|---|---:|---:|---:|
| Lead Time | 104,01 | 69,00 | 106,86 |
| ADR | 190,71 | 95,00 | 2.020,32 |
| Total Nights | 3,43 | 3,00 | 2,56 |
| Estimated Booking Value | 869,89 | 267,30 | 16.503,78 |

## Key Insights

1. **City Hotel** memiliki volume booking terbesar, tetapi cancellation rate lebih tinggi daripada Resort Hotel.
2. **Resort Hotel** memiliki rata-rata lama menginap lebih tinggi, yaitu 4,32 malam.
3. **Transient** merupakan customer type dominan dengan 75,06% booking.
4. **Online TA** merupakan market segment terbesar dengan 47,30% booking.
5. **Groups** memiliki cancellation rate tertinggi sebesar 61,06%.
6. Booking tertinggi terjadi pada **August**, sedangkan terendah pada **January**.
7. ADR dan Estimated Booking Value memiliki variasi besar sehingga median perlu dipertimbangkan bersama mean.

## Business Recommendations

### City Hotel
- Terapkan early booking promotion.
- Berikan benefit untuk non-refundable booking.
- Kirim reminder sebelum tanggal kedatangan.
- Dorong direct booking melalui website hotel.

### Resort Hotel
- Fokus pada paket long-stay.
- Buat paket 3–4 malam.
- Tawarkan paket kamar + fasilitas/aktivitas hotel.
- Gunakan promosi pada low season.

### Customer Type
Untuk **Transient**:
- Personalized promotion.
- Loyalty program.
- Repeat booking discount.
- Direct booking incentives.

Untuk **Transient-Party**:
- Paket untuk beberapa orang.
- Weekend promotion.
- Group kecil package.

### Market Segment
Untuk **Online TA**:
- Optimalkan listing hotel.
- Gunakan promo saat low season.
- Tingkatkan kualitas foto, informasi kamar, dan review.

Untuk **Direct**:
- Berikan benefit khusus direct booking.
- Free upgrade jika tersedia.
- Promo khusus website hotel.

### Mengurangi Cancellation

Karena **Groups memiliki cancellation rate 61,06%**:
- Terapkan deposit/down payment.
- Tetapkan batas waktu konfirmasi.
- Gunakan cancellation policy bertingkat.
- Lakukan konfirmasi ulang sebelum kedatangan.

### Strategi Musiman

- January: gunakan early-year promotion dan discount campaign.
- July–August: optimalkan harga dan persiapkan kapasitas karena volume booking tinggi.

## Dashboard

Dashboard Power BI menampilkan:

- Total Booking: **119.390**
- Cancellation Rate: **37,04%**
- Estimated Booking Value: **103,86 juta**
- Average Stay: **3,43 malam**
- Average Lead Time: **104,01 hari**
- Booking by Hotel
- Cancellation Rate by Hotel
- Customer Type
- Market Segment
- Monthly Booking Trend

## Dashboard Preview

Tambahkan screenshot dashboard ke folder `images`, lalu gunakan:

```markdown
![Hotel Booking Dashboard](images/hotel-booking-dashboard.png)
```

## Project Structure

```text
hotel-booking-analysis/
├── README.md
├── data/
│   └── hotel_bookings.csv
├── powerbi/
│   └── hotel-booking-analysis.pbix
├── report/
│   └── hotel-booking-analysis.pdf
└── images/
    ├── hotel-booking-dashboard.png
    ├── booking-by-hotel.png
    ├── cancellation-rate.png
    ├── customer-type.png
    ├── market-segment.png
    ├── monthly-booking.png
    ├── adr-histogram.png
    └── lead-time-histogram.png
```

## Conclusion

Analisis menunjukkan bahwa volume booking tinggi tidak selalu diikuti cancellation rate yang rendah. City Hotel memiliki booking terbesar tetapi cancellation rate lebih tinggi, sedangkan Resort Hotel memiliki rata-rata lama menginap lebih panjang.

Transient merupakan customer type utama dan Online TA merupakan market segment terbesar. Groups memiliki cancellation rate tertinggi sehingga membutuhkan kebijakan booking yang lebih ketat.

Insight tersebut dapat digunakan untuk menyusun strategi promosi berdasarkan jenis hotel, customer type, market segment, dan periode booking.

## Author

**Ilham Juliandi**

Fresh Graduate — Informatics Engineering

Interested in **Data Analytics, Web Development, and Technology**.
