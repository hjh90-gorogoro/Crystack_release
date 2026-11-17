# CryStack

Stack powder X-ray diffraction patterns and view them in 2θ, d-spacing or Q, with a scale and an offset for every pattern. Open `.xy`, `.xye`, `.dat`, `.chi` and `.csv` files, line up a series as a stack or a heatmap, overlay reference peaks from `.cif`, `.jcpds` or a space group, and export figures as PNG, SVG or PDF.

Free for personal, educational and research use. This repository only holds the downloads; the source code is not published.

## Download

Get the file for your system from the **[latest release](https://github.com/hjh90-gorogoro/Crystack_release/releases/latest)**.

| System | File | Notes |
| --- | --- | --- |
| Windows 10 / 11 (64-bit) | `CryStack-<version>-windows-x86_64.zip` | Unzip and run `CryStack.exe`. |
| macOS 11 or later | `CryStack-<version>-macos-universal.zip` | Unzip and move `CryStack.app` to Applications. |
| Linux (64-bit) | `CryStack-<version>-linux-x86_64.tar.gz` | `tar -xzf` the file and run `./install.sh`. |

Each release lists a SHA-256 checksum for every file. Check it after downloading:

```
shasum -a 256 <file>        # macOS / Linux
certutil -hashfile <file> SHA256   # Windows
```

## First start

CryStack is not signed with a paid certificate yet, so your system warns once.

- **Windows:** if "Windows protected your PC" appears, choose **More info → Run anyway**.
- **macOS:** right-click `CryStack.app` and choose **Open**, then **Open** again. If that is refused, run `xattr -cr /Applications/CryStack.app` in Terminal and try again.
- **Linux:** needs a graphical desktop. For Korean file names install a Hangul font, e.g. `sudo apt install fonts-nanum`.

## Help

Open an issue at <https://github.com/hjh90-gorogoro/Crystack_release/issues> with the file type, your system and what happened.

## License

See [LICENSE](LICENSE). Third-party notices are inside every download (`THIRD_PARTY_LICENSES`).

---

# CryStack (한국어)

분말 X선 회절(XRD) 패턴을 쌓아서 2θ, d, Q 축으로 보고, 패턴마다 배율과 오프셋을 줄 수 있는 프로그램입니다. 개인·교육·연구 목적에는 무료입니다. 이 저장소에는 다운로드 파일만 있고 소스 코드는 공개하지 않습니다.

**다운로드:** [최신 릴리스](https://github.com/hjh90-gorogoro/Crystack_release/releases/latest)에서 사용하는 OS의 파일을 받으세요. Windows는 zip을 풀고 `CryStack.exe`, macOS는 zip을 풀어 `CryStack.app`을 응용 프로그램 폴더로, Linux는 tar.gz를 풀고 `./install.sh`를 실행합니다.

**처음 실행할 때 경고가 뜨는 경우:** 아직 유료 서명이 없어서 한 번 경고가 나옵니다. Windows는 "추가 정보 → 실행", macOS는 앱을 우클릭 → 열기를 누르세요. 그래도 막히면 터미널에서 `xattr -cr /Applications/CryStack.app`을 실행합니다.
