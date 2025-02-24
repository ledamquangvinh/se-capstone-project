# Database Design

## 1 - Database Diagram
![database diagram](../image/img-db-diagram.png)

## 2 - Database Specification

### 2.1 - List of Tables

| No     | Table Name            | Description                                  |
| :----: | :-------------------- | :------------------------------------------- |
| 1      | loaitaikhoan          | Thong tin phan quyen cua tai khoan           |
| 2      | taikhoan              | Thong tin tai khoan                          |
| 3      | hangsanxuat           | Thong tin hang san xuat                      | 
| 4      | loaisanpham           | Danh muc san pham                            |
| 5      | sanpham               | Thong tin san pham                           |
| 6      | tinhtrang             | Tinh trang don hang                          |
| 7      | dondathang            | Thong tin don dat hang                       |
| 8      | chitietdonhang        | Thong tin chi tiet don dat hang              |              

## 2.2 - Table Structure

2.2.1 - Table: ***loaitaikhoan***
| No     | Field Name            | Data Type    | Key(PK/FK)    | Description                                   |
| :----: | :-------------------- | :----------: | :--------:    |:--------------------------------------------- |
| 1      | maloaitaikhoan        | int          | PK            | Ma loai tai khoan                             |
| 2      | tenloaitaikhoan       | varchar(45)  |               | Ten loai tai khoan                            |

2.2.2 - Table: ***taikhoan***
| No    | Field Name            | Data Type     | Key(PK/FK)    | Description                                   |
| :---: | :-------------------  | :----------:  | :--------:    |:--------------------------------------------- |
| 1     | mataikhoan            | int           | PK            | Ma tai khoan                                  |
| 2     | tendangnhap           | varchar(20)   |               | Ten dang nhap                                 |
| 3     | matkhau               | varchar(20)   |               | Mat khau                                      |
| 4     | tenhienthi            | varchar(64)   |               | Ten hien thi                                  |
| 5     | diachi                | varchar(256)  |               | Dia chi                                       |
| 6     | dienthoai             | varchar(11)   |               | So dien thoai                                 |
| 7     | email                 | varchar(30)   |               | Email nguoi dung                              |
| 8     | bixoa                 | bool          |               | Tai khoan co bi xoa khong                     |
| 9     | maloaitaikhoan        | int           | FK            | Ma loai tai khoan                             |      

2.2.3 - Table: ***hangsanxuat***
| No    | Field Name            | Data Type     | Key(PK/FK)    | Description                                   |
| :---: | :-------------------  | :----------:  | :--------:    |:--------------------------------------------- |
| 1     | mahangsanxuat         | int           | PK            | Ma hang san xuat                              |
| 2     | tenhangsanxuat        | varchar(64)   |               | Ten hang san xuat                             |
| 3     | logourl               | varchar(45)   |               | Duong dan cho logo                            |
| 4     | bixoa                 | bool          |               | Hang san xuat co bi xoa khong                 |

2.2.4 - Table: ***loaisanpham***
| No    | Field Name            | Data Type     | Key(PK/FK)    | Description                                   |
| :---: | :-------------------  | :----------:  | :--------:    |:--------------------------------------------- |
| 1     | maloaisanpham         | int           | PK            | Ma loai san pham                              |
| 2     | tenloaisanpham        | varchar(64)   |               | Ten loai san pham                             |
| 3     | bixoa                 | bool          |               | Loai san pham co bi xoa khong                 |

2.2.5 - Table: ***sanpham***
| No    | Field Name            | Data Type     | Key(PK/FK)    | Description                                   |
| :---: | :-------------------  | :----------:  | :--------:    |:--------------------------------------------- |
| 1     | masanpham             | int           | PK            | Ma San Pham                                   |
| 2     | tensanpham            | varchar(45)   |               | Ten san pham                                  |
| 3     | hinhurl               | varchar(45)   |               | Duong dan cua hinh                            |
| 4     | giasanpham            | int           |               | Gia san pham                                  |
| 5     | ngaynhap              | datetime      |               | Ngay nhap san pham                            |
| 6     | soluongton            | int           |               | So luong hang ton                             |
| 7     | soluongban            | int           |               | So luong san pham da ban                      |
| 8     | soluocxem             | int           |               | So luong luoc xem                             |
| 9     | mota                  | text          |               | Mo ta san pham                                |
| 10    | bixoa                 | bool          |               | San pham co bi xoa khong                      |
| 11    | maloaisanpham         | int           | FK            | Ma loai san pham                              |
| 12    | mahangsanxuat         | int           | FK            | Ma hang san xuat                              |

2.2.6 - Table: ***tinhtrang**
| No    | Field Name            | Data Type     | Key(PK/FK)    | Description                                   |
| :---: | :-------------------  | :----------:  | :--------:    |:--------------------------------------------- |
| 1     | matinhtrang           | int           | PK            | Ma tinh trang                                 |
| 2     | tentinhtrang          | varchar(45)   |               | Ten tinh trang                                |

2.2.7 - Table: ***dondathang***
| No    | Field Name            | Data Type     | Key(PK/FK)    | Description                                   |
| :---: | :-------------------  | :----------:  | :--------:    |:--------------------------------------------- |
| 1     | madondathang          | varchar(9)    | PK            | Ma don dat hang                               |
| 2     | ngaylap               | datetime      |               | Ngay lap don dat hang                         |
| 3     | tongthanhtien         | int           |               | Tong thanh tien cua don dat hang              |
| 4     | mataikhoan            | int           | FK            | Ma tai khoan                                  |
| 5     | matinhtrang           | int           | FK            | ma tinh trang cua don dat hang                |

2.2.8 - Table: ***chitietdonhang***
| No    | Field Name            | Data Type     | Key(PK/FK)    | Description                                   |
| :---: | :-------------------  | :----------:  | :--------:    |:--------------------------------------------- |
| 1     | machitietdondathang   | varchar(11)   | PK            | Ma chi tiet don dat hang                      |
| 2     | soluong               | int           |               | So luong                                      |
| 3     | madondathang          | varchar(9)    | FK            | Ma don dat hang                               |
| 4     | masanpham             | int           | FK            | Ma san pham
