# Sales and Customer Analysis Dashboard

1. OVERVIEW
 
   **Thông tin bộ dữ liệu**
Bộ dữ liệu gốc về thông tin bán hàng của một doanh nghiệp kinh doanh cây cảnh đa quốc gia tại Mỹ bao gồm các bảng dữ liệu:
  - Plant_Fact: Bản ghi các đơn đặt hàng từ ngày 01/01/2022 đến 14/042024 bao gồm thông tin về mã sản phẩm, mã khách hàng, dơn giá, doanh thu, chi phí,...
  - Accounts: Bảng dữ liệu thông tin khách hàng. Bao gồm thông tin về mã khách hàng, địa chỉ,...
  - Plant_Hierarchy: Bảng dữ liệu thông tin sản phẩm. Bao gồm thông tin nhóm sản phẩm, loại, kích cỡ sản phầm,...

   **Mục tiêu**
   - Báo cáo doanh thu, chi phí và lợi nhuận theo sản phẩm, quốc gia theo từng tháng, quý, năm
   - So sánh doanh thu năm nay với các năm trước
   - Xác định Retention rate, Churn rate, New customer rate theo thời gian và sản phẩm
     
   **Xử lý và làm sạch dữ liệu** 
   - Loại bỏ giá trị Duplicate
   - Format lại các trường dữ liệu
   - Tạo Relationship, tạo thêm bảng Dim_date,...

2.   Sales Performance Insights
        <img width="1449" height="820" alt="image" src="https://github.com/user-attachments/assets/9cde7e76-e39c-4773-a92f-131b44363ca7" />

_Về doanh thu và lợi nhuận qua thời gian_
- Doanh thu nhìn chung ổn định qua các năm, thường giảm nhẹ vào Quý 3 
- Tuy nhiên, lợi nhuận lại biến động theo thời gian. Nhìn chung thường giảm vào quý 4 và quý 1 sau đó tăng nhẹ vào quý 2 và tăng mạnh trong quý 3 (chi phí hoạt động trong quý 3 giảm mạnh)

_Về lợi nhuận và chi phí_
- Đa số khách hàng mang lại lợi nhuận bằng hoặc thậm chí thấp hơn chi phí mà doanh nghiệp bỏ ra. Lợi nhuận chi ở trong khoảng $0 - $20K nhưng chi phí bỏ ra đa số từ $20K - $40K.
- Một số đơn hàng (outlier) có lợi nhuận thấp nhưng lại có chi phí cao tới $60K
  > Cần lưu ý và loại bỏ các đơn hàng tương tự trong thời gian sau để giảm chi phí

_Về lợi nhuận các quốc gia_ 
  Nhóm khách hàng Trung Quốc mang lại doanh thu cao nhất do số lượng bán hàng cao. Tuy nhiên, % lợi nhuận của quốc gia này chỉ chiếm khoảng 39.1% doanh thu, không mang lại % lợi nhuận tương xứng với lượng bán hàng. Trong khi đó, France có doanh thu đứng thứ 7 nhưng lại có % lợi nhuận cao nhất, lên tới 43,1% doanh thu
  > Nên tập trung hơn vào thị trường Pháp, tăng số lượng đơn đặt hàng và lợi nhuận. Bên cạnh đó, giảm phụ thuộc vào thị trường Trung Quốc

3.  Customer analysis insights
        <img width="1210" height="679" alt="image" src="https://github.com/user-attachments/assets/4dfa4d6c-cba2-4d8e-868b-481f1c969890" />

Số lượng khách hàng sử dụng dịch vụ (active customer) không thay đỏi nhiều theo thời gian. Tuy nhiên, số lượng khách hàng mới lại biến động nhiều, đạt đỉnh vào Q1 năm 2022
Bên cạnh đó, Churn rate (tỷ lệ rời bỏ của khách hàng) ngày càng tăng mạnh, cho thấy doanh nghiệp đang quá tập trung vào việc thu hút khách hàng mới mà không để tâm tới việc giữ chân khách hàng
  > Doanh nghiệp cần tập trung cải thiện sản phẩm, dịch vụ chăm sóc khách hàng để giảm Churn rate hay tăng Retention rate, kết hợp duy trì các chiến lược thu hút khách hàng mới, từ đó tăng tệp khách hàng của doanh nghiệp 
