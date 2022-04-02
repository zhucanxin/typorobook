# typorobook

关于git gpg。
为了双向都不再需要每次输入密码，本地端通过gpg-keygen 制作公钥，网络端通过setting-develop选项制作token，并将token记录下来，然后互相交换。可以有很多个。
1.在本地  gpg --list-keys,查看所有的密码，明确code
2. gpg --armor --export pub 44C40A5C2914A739207688479595B2C27CE47EA0，得出一串代码，将此代码粘贴到网页里面的位置。这样就可以pull不要密码了。
3. 将这个密钥加入到本地的git里面去。git remote set-url origin https://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@github.com/zhucanxin/zhucanxin.git
4.推送git push origin
