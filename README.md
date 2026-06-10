[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=24112951&assignment_repo_type=AssignmentRepo)
# Day 10 Lab: Data Pipeline & Data Observability

**Student ID:** 2A202600888
**Name:** Ho Duc Minh

---

## Mo ta

Bai lab xay dung mot ETL Pipeline tu dong doc du lieu JSON, kiem tra chat luong du lieu, chuan hoa va luu ket qua ra file CSV. Pipeline thuc hien 4 buoc chinh: Extract, Validate, Transform, Load. Ngoai ra, bai lab con thuc hien thi nghiem so sanh hieu qua xu ly giua du lieu sach va du lieu rac de danh gia tam quan trong cua Data Observability.

---

## Cach chay (How to Run)

### Prerequisites

```bash
pip install pandas pytest
```

### Chay ETL Pipeline

```bash
python solution.py
```

Sau khi chay, file `processed_data.csv` se duoc tao ra trong thu muc hien tai.

### Chay tests

```bash
python -m pytest tests/ -v
```

---

## Cau truc thu muc

```
├── solution.py              # ETL Pipeline script (Extract, Validate, Transform, Load)
├── raw_data.json            # Du lieu dau vao
├── processed_data.csv       # Output cua pipeline
├── experiment_report.md     # Bao cao thi nghiem Clean vs Garbage data
└── README.md                # File nay
```

---

## Ket qua

- **Tong records doc vao:** 5
- **Records hop le (valid):** 3
- **Records bi loai (dropped):** 2
  - 1 record bi loai do `price <= 0` (Mystery Box, gia = -10)
  - 1 record bi loai do `category` rong (Phone)
- **Output:** `processed_data.csv` voi cac cot `id`, `product`, `price`, `category`, `discounted_price`, `processed_at`
