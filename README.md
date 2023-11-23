<a name="readme-top"></a>
<!-- PROJECT LOGO -->
<div align="center">
  <a href="https://daylaioto.net">
    <img src="images/1024_t.png" alt="Logo" width="240" height="240">
  </a>
<!-- 
  <h3 align="center"><span style="color:green">DAYLAIOTO</span><span style="color:red">.NET</span>
</h3>
----------------------------------------------------------------
function Alias(text) {
  return text.toLowerCase().replace(/ /g, "-");
}
result = Alias('aaaa');
----------------------------------------------------------------
 -->

</div>
<!-- TABLE OF CONTENTS -->

 ## :bookmark_tabs: <span style="color:red">Menu</span>
  <ol>
    <li>
      <a href="#setup-ssh-github">Setup SSH Github</a>
      <ul>
        <li><a href="#windows-generate-new-ssh-key">Windows generate new SSH key</a></li>
        <li><a href="#linux-generate-new-ssh-key">Linux generate new SSH key</a></li>
      </ul>  
  </ol>


<!-- Settup SSH -->

## Setup SSH Github

Bạn có thể tạo key SSH mới trên máy của mình. Sau khi tạo key, bạn có thể thêm public vào tài khoản của mình trên GitHub.com để bật xác thực cho các hoạt động Git qua SSH.

### Windows generate new SSH key
1. Open Git Bash.
2. Copy và dán văn bản bên dưới, thay thế email được sử dụng trong ví dụ bằng địa chỉ email GitHub của bạn.

    ```sh
      ssh-keygen -t rsa -b 4096 -C "your_email@gmail.com"
    ```
3. Open file `id_rsa.pub` trong folder _(đổi YOU thành user hiện tại trên máy của bạn)_ :
    ```sh 
      /c/Users/YOU/.ssh/
    ```
4. Copy toàn bộ nội dung key bên trong file trên.
5. Open Github -> User -> Setting -> SSH keys and GPG keys -> New SSH key -> paste key, Add new title
6. Quay lại repositories bạn muốn clone về.
7. Chọn `Code` -> chọn tab `SSH` -> click button copy link ssh.
8. Bây giờ nếu muốn clone thì git clone và paste link vào.
9. Muốn push data lên Github thì : 
    ```sh 
      git add . && git commit -m "add new" && git push -u origin main
    ```
10. MULTIPLE Github Account Key SSH
      - Open .git -> config in project
      - Add :
  
        ```
        [core]
          ...
          sshCommand = ssh -i ~/.ssh/key_name
        [remote "origin"]
          ...
        ```



<p align="right">(<a href="#readme-top">back to top</a>)</p>


* ### Linux generate new SSH key

<p align="right">(<a href="#readme-top">back to top</a>)</p>
