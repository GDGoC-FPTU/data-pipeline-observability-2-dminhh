# Experiment Report: Data Quality Impact on AI Agent

**Student ID:** 2A202600888
**Name:** Ho Duc Minh
**Date:** 2026-06-10

---

## 1. Ket qua thi nghiem

Chay ETL Pipeline voi 2 bo du lieu va ghi lai ket qua:

| Scenario | Records Input | Records Valid | Records Dropped | Output File |
|----------|--------------|---------------|-----------------|-------------|
| Clean Data (`raw_data.json`) | 5 | 3 | 2 | processed_data.csv |
| Garbage Data (gia tri am, category rong) | 5 | 1 | 4 | processed_data.csv |

| Scenario | Accuracy (1-10) | Notes |
|----------|-----------------|-------|
| Clean Data | 9 | Gia tri hop le, category dung dinh dang, tinh toan chinh xac |
| Garbage Data | 3 | Nhieu record bi loai do price <= 0 va category rong |

---

## 2. Phan tich & nhan xet

### Tai sao Agent tra loi sai khi dung Garbage Data?

Khi su dung du lieu "rac" (garbage data), pipeline ETL se loai bo nhieu record hon do vi pham cac quy tac validation. Cu the, cac record co gia tri price am hoac bang 0 se bi loai vi chung khong co y nghia trong thuc te kinh doanh. Tuong tu, cac record co truong category rong se bi bo qua vi khong the phan loai san pham.

Dieu nay dan den tap du lieu dau ra rat nho, thieu di nhieu thong tin quan trong. Neu mot AI Agent su dung du lieu nay de phan tich hoac du doan, no se dua ra ket qua sai lech hoac thieu chinh xac vi mau du lieu khong du lon va khong dai dien cho toan bo tap du lieu goc. Ngoai ra, outliers va gia tri khong hop le con lam sai lech cac phep tinh thong ke nhu gia trung binh, tong doanh thu, v.v.

Ket luan: chat luong du lieu dau vao anh huong truc tiep den chat luong ket qua phan tich va do chinh xac cua AI Agent.

---

## 3. Ket luan

**Quality Data > Quality Prompt?** Dong y.

Du prompt co duoc viet tot den dau, neu du lieu dau vao chua nhieu gia tri sai, thieu, hoac khong nhat quan, ket qua dau ra van se kem chinh xac. Du lieu sach la nen tang bat buoc de bat ky he thong AI nao hoat dong hieu qua va dang tin cay.
