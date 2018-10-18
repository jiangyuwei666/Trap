# pip安装出现红色错误的结局办法
```
C:\Users\Jiangyuwei>pip install -i https://pypi.tuna.tsinghua.edu.cn/simple mitmproxy
Looking in indexes: https://pypi.tuna.tsinghua.edu.cn/simple
Collecting mitmproxy
  Retrying (Retry(total=4, connect=None, read=None, redirect=None, status=None)) after connection broken by 'SSLError(SSLError(1, '[SSL: CERTIFICATE_VERIFY_FAILED] certificate verify failed (_ssl.c:777)'),)': /simple/mitmproxy/
  Retrying (Retry(total=3, connect=None, read=None, redirect=None, status=None)) after connection broken by 'SSLError(SSLError(1, '[SSL: CERTIFICATE_VERIFY_FAILED] certificate verify failed (_ssl.c:777)'),)': /simple/mitmproxy/
  Retrying (Retry(total=2, connect=None, read=None, redirect=None, status=None)) after connection broken by 'SSLError(SSLError(1, '[SSL: CERTIFICATE_VERIFY_FAILED] certificate verify failed (_ssl.c:777)'),)': /simple/mitmproxy/
  Retrying (Retry(total=1, connect=None, read=None, redirect=None, status=None)) after connection broken by 'SSLError(SSLError(1, '[SSL: CERTIFICATE_VERIFY_FAILED] certificate verify failed (_ssl.c:777)'),)': /simple/mitmproxy/
  Retrying (Retry(total=0, connect=None, read=None, redirect=None, status=None)) after connection broken by 'SSLError(SSLError(1, '[SSL: CERTIFICATE_VERIFY_FAILED] certificate verify failed (_ssl.c:777)'),)': /simple/mitmproxy/
  Could not fetch URL https://pypi.tuna.tsinghua.edu.cn/simple/mitmproxy/: There was a problem confirming the ssl certificate: HTTPSConnectionPool(host='pypi.tuna.tsinghua.edu.cn', port=443): Max retries exceeded with url: /simple/mitmproxy/ (Caused by SSLError(SSLError(1, '[SSL: CERTIFICATE_VERIFY_FAILED] certificate verify failed (_ssl.c:777)'),)) - skipping
  Could not find a version that satisfies the requirement mitmproxy (from versions: )
No matching distribution found for mitmproxy
```
![如图](http://ww1.sinaimg.cn/large/006BhB5Ogy1fwcokorjqkj30xz0hrq40.jpg)

解决办法如下：
1. 安装时加入 `--trusted-host pypi.python.org`参数：
    
    比如`pip --trusted-host pypi.python.org install requests`
2. 在pip.conf中加入trusted-host选项，该方法是一劳永逸

    [global]
    timeout = 6000
    index-url = http://pypi.douban.com/simple/ 
    [install]
    use-mirrors = true
    mirrors = http://pypi.douban.com/simple/ 
    trusted-host = pypi.douban.com