# vimtutor
Mở terminal > nhập `vimtutor` để bắt đầu học về vim <br>
※Đừng quên cài đặt vim nhé.<br>
※Bạn cũng có thể cài đặt plugin vim trên VS code để thực hành <br>
## Bài 1 
1. Di chuyển con trỏ bằng các phím mũi tên hoặc phím `hjkl`.<br>
         h (trái) j (dưới) k (trên cùng) l (phải)

2. Để khởi chạy Vim, nhập `vim filename` <ENTER> tại dấu nhắc.<br>

3. Để thoát Vim, nhập `<ESC>: q! <ENTER>` (loại bỏ các thay đổi của bạn).<br>
               Hoặc nhập `<ESC>: wq <ENTER>` (lưu thay đổi). <br>
               `q` quite <br>
               `w` write <br>

4. Để xóa ký tự dưới con trỏ, nhập `x` ở chế độ bình thường. `x => xoá? ` <br>
      
5. Để chèn một ký tự ở vị trí con trỏ, nhập `i` ở chế độ bình thường. `i => insert` <br>
         i loại văn bản `<ESC>` được thêm vào vị trí con trỏ <br>
         Thêm văn bản `<ESC>` Thêm ở cuối dòng <br>

LƯU Ý: Nhấn phím `<ESC>` để chuyển sang chế độ bình thường. Tại thời điểm đó, bạn có thể hủy lệnh sai hoặc nhập một phần.

## Bài 2
1. Để xóa từ con trỏ đến cuối `một` từ, nhập `dw`. `dw => delete word`<br>
2. Để xóa từ con trỏ đến `cuối dòng`, nhập `d $`. <br>
3. Gõ `dd` để xóa toàn bộ dòng. <br>

4. Cho một số để lặp lại chuyển động: `2w` <br>
5. Định dạng của lệnh được sử dụng để thay đổi là <br>
                Toán tử [số] Motion <br>
                
      Mỗi:
        Toán tử - kiểu xóa `d`. <br>
        Số - bao nhiêu lần để lặp lại lệnh. <br>
        Motion - những gì hoạt động cho văn bản, chẳng hạn như `w` (word) hoặc `$` (cuối dòng) <br>

6. Thao tác với dòng <br>
    Sử dụng số `0` để di chuyển đến `đầu dòng`: 0 <br>
       ( cuối dòng `$` ) <br>
    [số] `dd` : xoá một số dòng ( 2dd -> xoá 2 dòng ) <br>
    
7. `Hoàn tác hành động cuối cùng`: `u` (chữ thường u) <br>
      `Hoàn tác` thay đổi cho `toàn bộ dòng`: `U` (chữ hoa U) <br>
      Hoàn tác hoàn tác: CTRL-R ?? ( chưa biết là gì ?? ) <br>
 
## Bài 3     
1. Để định vị lại văn bản đã bị xóa, hãy nhập `p`. `p => paste`  <br>
    Thao tác này sẽ chèn văn bản đã xóa sau con trỏ (nếu nó bị xóa từng dòng, nó sẽ được chèn ở dòng tiếp theo có con trỏ). <br>

2. Để thay thế ký tự dưới con trỏ, nhập `r` theo sau là ký tự thay thế nó. `r => rewrite viết lại` <br>

3. Lệnh thay đổi cho phép bạn thay đổi từ vị trí con trỏ đến điểm cuối được chỉ định bởi một chuyển động cụ thể.  <br>
    Ví dụ: cw thay đổi từ vị trí con trỏ đến cuối từ và c $ thay đổi từ cuối dòng.<br>
    `c` => change ( thay đổi ) <br> 
    `cw` => change work ( tính từ vị trí con trỏ đến hết từ) <br>
    `c$` => change to end of line ( tính từ vị trí con trỏ đến hết dòng ) <br>

4. Định dạng của lệnh thay đổi là <br>
      c [số] motion <br>

## Bài 4:
1. `CTRL-G` hiển thị vị trí nơi con trỏ đang đứng trong tệp và chi tiết của tệp. <br>
          `G` ( shift + g) di chuyển đến dòng dưới cùng của tập tin. <br>
          `[Số]G` di chuyển đến dòng đó. <br>
          `gg` di chuyển đến dòng đầu tiên. <br>

2. Nhập một từ sau / để tìm kiếm từ từ trên xuống dưới tính từ cont trỏ. <br>
     Nhập một từ sau? Để tìm kiếm từ từ dưới lên trên tính từ cont trỏ. <br>
     Sau khi tìm kiếm, `n` thực hiện tìm kiếm tiếp theo theo cùng một hướng và  `N` thực hiện tìm kiếm ngược lại. <br>
     `CTRL-O` di chuyển vị trí về phía trước, `CTRL-I` di chuyển vị trí tiếp theo. <br>

3. Với con trỏ trên (,), [,], {, hoặc}, nhập `%` để di chuyển đến ký tự tương ứng. <br>

4. Thay thế old ở đầu dòng hiện tại bằng new. :s/old/new <br>
     Thay thế tất cả old trong dòng hiện tại bằng new. : s/old/new/g  <br>
     Thay thế một cụm từ giữa hai #,# :#,#s/old/new/g <br>
     Thay thế tất cả các thuật ngữ tìm kiếm trong tập tin. :%s/old/new/g <br>
     Khi 'c' được thêm vào, cần có xác nhận cho mỗi lần thay thế. :%s/old/new/gc <br>
 
## Bài 5
1. Thực hiện một lệnh bên ngoài với :! Lệnh. <br>

      Các ví dụ thường được sử dụng: <br>
          (MS-DOS) (Unix) <br>
           :! dir:! ls-Xem danh sách trong thư mục. <br>
           :! del FILENAME:! rm FILENAME-Xóa một tệp. <br>

2. Một tệp được ghi vào đĩa bởi :w filename. <br>

3. v (chọn) motion ( ấn v + di chuyển con trỏ ) > :w FILENAME > dòng được chọn sẽ được lưu trong tệp. <br>

4. `:r FILENAME` để chèn nội dung FILENAME bên dưới vị trí con trỏ. <br>
5. `:r !dir` đọc đầu ra của lệnh dir bên dưới vị trí con trỏ. <br>
  
## Bài 6
1. Nhập o mở dòng bên dưới con trỏ và vào chế độ chèn. <br>
     Nhập O (chữ hoa) sẽ đưa bạn vào chế độ chèn tại dòng phía trên con trỏ. <br>

2. Nhập a để thêm văn bản sau ký tự trên con trỏ. <br>
     Nhập chữ hoa A để tự động chèn văn bản vào cuối dòng. <br>

3. Lệnh e di chuyển con trỏ cuối từ. <br>

4. Toán tử y (yanks) (bản sao) văn bản và p paste (dán) nó. <br>
     chon bằng v + di chuyển con trỏ  <br>
     j$ : di chuyển đến đầu dòng tiếp theo <br>
     
5. Nhập chữ hoa R để vào chế độ thay thế, nhấn <ESC> để thoát. <br>

6. Nhập ":set xxx" để đặt tùy chọn "xxx". <br>
        'ic' 'ignorecase' không phân biệt chữ hoa, chữ thường <br>
        'is' 'incsearch'  chỉ hiển thị nếu khớp hoàn toàn <br>
        'hls' 'hlsearch' làm nổi bật tất cả các kết quả <br>
     Bạn có thể sử dụng tên tùy chọn dài hoặc rút ngắn. <br>

7. Cho "no" để tắt tùy chọn :set noic <br>
  
## Bài 7
1. Để mở cửa sổ trợ giúp, nhập: trợ giúp hoặc nhấn <F1> hoặc <Trợ giúp>. <br>

2. Gõ: help cmd để tìm kiếm trợ giúp trên lệnh (cmd). <br>

3. Nhập CTRL-W CTRL-W để chuyển sang cửa sổ khác. <br>

4. Nhập: q để đóng cửa sổ trợ giúp. <br>

5. Tạo tập lệnh khởi động vimrc để giữ các cài đặt ưa thích của bạn. <br>

6.: Nhập CTRL-D để xem các hoàn thành có thể cho: lệnh. <br>
      Nhấn <TAB> để sử dụng hoàn tất. <br>

## Other
1. copy dòng : yy
