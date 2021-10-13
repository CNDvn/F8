# HTML & CSS
## Vài tag phổ biến
1. h1 - h6 :heading
2. p :paragraph
3. img :image
4. a :achor
5. ul, li :unordered list, list item
6. table
7. input
8. button
9. div

## Đơn vị
1. Absolute units (Đơn vị tuyệt đối): kích thước cố định, không thay đổi khi các yếu tố xung quanh tác động vào, như thu nhỏ/phóng to trình duyệt
    - px
    - pt
    - cm
    - mm
    - inch
    - pc
2. Relative units (Đơn vị tương đối: phải có đứa để phụ thuộc vào): kích thước không cố định, bị thay đổi khi đối tượng mà nó phụ thuộc vào bị thay đổi
    - %: phụ thuộc vào thẻ chứa nó (mặc định 100% = 16px)
    - rem: phụ thuộc vào thẻ html
    - em: phụ thuộc vào thẻ gần nhất chứa nó (mặc định 1em = 16px)
    - vw(viewport width): phụ thuộc vào chiều ngang của trình duyệt (ex: 50vw = 50%vw)
    - vh(viewport height): phụ thuộc vào chiều dọc của trình duyệt (ex: 50vh = 50%vh)
    - vmin
    - vmax
    - ex
    - ch

## độ ưu tiên
1. Internal, External (thằng nào ở sau thì gọi apply thằng đó)
2. Inline - 1000
3. #id - 100
4. .class - 10
5. tag - 1
6. Equal specificity?
7. Universal selector and inherited

## Position (có thêm top left righ bottom khi dùng thuộc tính này)
1. Relative: tương đối
    - không bị phụ thuộc vào đối tượng nào khác cả, lấy chính vị trí đang đứng để làm gốc tọa độ => phụ thuộc vào chính nó
2. Absolute: tuyệt đối
    - phụ thuộc thẻ cha gần nhất có thuộc tính position để lấy cha đó làm gốc tọa độ
3. Fixed: phụ thuộc vào khung trình duyệt
    - vị trí phụ thuộc vào khung của trình duyệt
4. Sticky: bám dính phụ thuộc vào khung trình duyệt

## Breakpoints: là những điểm/vị trí mà bố cục website sẽ thay đổi - thích ứng để tạo nên giao diện responsive
- Mobile: width < 740px
- Tablet: width >= 740px and width < 1024px
- PC: width >= 1024px

## Flexbox
- display: flex|inline-flex - quyết định có sử dụng flex hay không
- flex-direction: row|column - thay đổi phương hướng của main axis
- flex-wrap: nowrap|wrap (xuống dòng) |wrap-reverse (nhẩy lên trên | đảo chiều cross start và cross end) - ...
- flex-basic:<lenght> - set kích thước cho main size
- justify-content: flex-start|flex-end|center|space-between(cách các flex item)|space-around(cách các flex item)|space-evenly - căn được những flex item theo phương main axis (dành cho cha nếu set cho cha thì con không cần dùng justify-self vì khi dùng thằng này ở cha thì ở con nó đã tự set justify-self rồi)
- justify-self: flex-start|flex-end|center
- align-content: flex-start|flex-end|center - giống justify-content nhưng theo phương cross axis
- align-self:flex-start|flex-end|center - tương tự justify-self
- flex-grow: <number> - thay đổi kích thước main size
- flex-shrink: <number> - ngược lại flex-grow (thu nhỏ lại)
- flex: <flex-grow>|<flex-shrink>|<flex-basic> - shorthand của flex-basic + flex-grow + flex-shrink
- flex-flow:<number>  - shorthand của flex-wrap + flex-direction
- order: <number> - quyết định thứ tự flex item được hiển thị xem thằng nào trước thằng nào sau
* tham khảo:
    https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Flexbox#the_flex_model
* Ôn luyện bằng: https://codepen.io/enxaneta/full/adLPwv/

## BEM
- là tiêu chuẩn đặt tên class khi viết CSS
### Ý nghĩa
- Viết tắt của: BLock Element Modifier
- Block: khối
- Element: thành phần của khối
- Modifier: Bổ sung ý nghĩa cho `Block` hoặc `Element`
### Tại sao dùng BEM
- Mỗi người đặt một kiểu
- Members đặt class trùng nhau, CSS đè lên nhau
### Cú pháp
- .block
- .block__element

- .block--modifier
- .block__element--modifier
### Trường hợp Block lồng Block
- Block con là thành phần dùng chung => là một block mới
- Block con chứa nhiều element

## Grid System
1. Xuất hiện từ đầu thế kỷ XX trong phong trào (Constructivism) nghệ thuật/kiến trúc
2. Tạo nên các khung nền, hỗ trợ việc sắp xếp bố cục theo trật tự/thống nhất/cân bằng
3. Hệ thống lưới thường gặp:
- Lưới nhiều cột (Mutilcolumn grid)
- Lưới một cột (Single column grid)
- Lưới module (Modular grid)
- Lưới đường cơ sở (Baseline grid)
4. Vai trò
- Tổ chức: có các đường căn gióng tiện lợi, dễ dàng sắp xếp các thành phần được ngăn nắp
- Cân bằng: Dù là đối xứng/Bất đối xứng, mang lại cái nhìn trực quan, đảm bảo sự cân bằng
- Tách biệt thành phần: Phân chia nội dung, tạo khoảng cách các phần hiệu quả
5. Ứng dụng
- Lưới trong thiết kế UI UX: vai trò đặc biệt quan trọng trong Responsive web design
- Lưới trong in ấn: Google "Grid system"
6. Responsive web design
- Grid: thành phần cha
- Row: Dòng
- Column: Cột
- Gutters: Khoảng cách 2 phía của column
7. Thành phần chính (lý thuyết)
- Column - Cột
    - Độ rộng sử dụng đơn vị % (tương đối) giúp linh động, dễ dàng tương thích với độ rộng khác nhau của các thiết bị. Số lượng cột trong grid system được xác định trước. (VD: PC 12|16 cột, tablet 8 cột, mobile 4 cột)
- Gutter - Đường ngăn cách (rãnh ngăn)
    - Là khoảng cách 2 phía của 1 cột, tạo nên rãnh ngăn giữa các cột. Độ rộng rãnh ngăn có thể thay đổi cho phù hợp với thiết kế hoặc độ rộng màn hình. (VD: PC/Tablet 24px, mobile 16px)
- Margin - Phần lề
    - Là khoảng cách 2 bên trái và phải của bố cục chính của website. Độ rộng phần lề thay đổi để phù hợp với các kích thước màn hình. VD: Phần lề lớn thích hợp cho màn hình lớn như PC, phần lề nhỏ thích hợp cho màn hình nhỏ như Tablet, mobile.
8. Thành phần chính (làm việc với CSS)
- Grid - Lưới (Thường là phần cha, chứa Row và Column)
- Row - Dòng (Dòng - chiều ngang, chứa Column)
- Column - Cột (chứa nội dung / thành phần trên website)

## Tạo thư viện Grid
### Tạo đối tượng Grid
1. Tạo class 
- grid: full-width, chiếm hết chiều ngang của đối tượng (cha)
- wide: chiều ngang tối đa 1200px
2. Đặt lại chiều rộng trên các thiết bị

- @media(min-width: 740px) and (max-width: 1023px){
    .wide{
        width: 644px;
    }
}
- @media (min-width: 1024px) and (max-width: 1239px){
    .wide{
        width: 984px;
    }
}
### Tạo đối tượng Row
1. Vai trò:
- Chứa các columns, giúp các columns nằm theo chiều ngang
- Khi tổng chiều ngang columns vượt quá kích thước Row, cho columns xuống hàng
- Loại bỏ khoảng thừa do gutters tạo ra ở 2 phía
2. CSS:
- @media (min-width: 740px){
    .row{
        margin-left: -8px;
        margin-right: -8px;
    }
}
- @media (min-width: 1113px){
    .row{
        margin-left: -12px;
        margin-right: -12px;
    }
}
- @media (min-width: 1024px) and (mã-width: 1239px){
    .wide .row{
        margin-left: -12px;
        margin-right: -12px;
    }
}
## Một vài thứ hay
### Reset CSS
- https://cdnjs.com/libraries/normalize trang tải cdn reset css