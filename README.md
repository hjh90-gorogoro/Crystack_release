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

Every download also holds the manual (`MANUAL_KO.html`, Korean) and a `samples` folder with example patterns, reference peaks and a 40-scan series for trying the heatmap.

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

## What it does

**Files**
- Opens two-column text patterns (`.xy`, `.xye`, `.dat`, `.chi`, `.csv`, `.txt`) with **Open…** or by dropping them on the window.
- Recognises Rigaku CrysAlis PowderGraph `.dat` files; for files with three or more columns it asks which column is x and which is the intensity.
- Reads the measured wavelength or energy from the file header, converts Q in 1/nm to 1/Å, and reads UTF-8 (with BOM) and UTF-16 files.

**Stack and axes**
- Shows the stack on a 2θ, d or Q axis at any wavelength (Cu, Co, Mo, Ag Kα1 presets, or type λ or keV). Patterns measured at different wavelengths line up on common d or Q.
- Gives every pattern its own scale and offset, with normalize, auto spacing, overlay and gradient colours.
- The pattern list is built for many files: filter, sort by name, value or file time, reorder by dragging, rename, and select several patterns to change at once.
- Optional Kα2 ticks for lab XRD.

**Reference peaks and unit cells**
- Imports reference peaks from `.jcpds` cards, `.cif` structures or a simple text list, drawn as tick rows under the plot.
- Makes a unit cell from any of the 230 space groups. Change the lattice parameters and the ticks follow at once, so you can fit them to measured peaks, e.g. to read a lattice parameter under pressure.
- hkl labels and guide lines on the ticks (keys **1** and **2**).

**Heatmap for series**
- Shows a temperature, time or pressure series as a heatmap, in stack order or at the real values read from file names, headers or a table file.
- Offers colormaps, linear / √ / log scaling, contrast and γ, normalisation, and difference maps against a chosen row.
- Follows a peak band through the series for its area, height, position, FWHM and cubic lattice parameter, with a profile beside the map and CSV export.

**Plot and export**
- Mouse: box zoom, right-click zoom out, middle-drag pan, double-click fit, and up to three markers showing 2θ, d and Q.
- Saves the whole workspace as a session file (`.crystack`).
- Exports figures as high-resolution PNG, SVG or PDF that match the screen, and data as `.xy` / `.dat` / `.chi`, one combined `.csv`, or a table of reference ticks.
- Ctrl+Z undoes a removal, a Clear or a session load.

See `MANUAL_KO.html` in the download for every option.

## Help

Open an issue at <https://github.com/hjh90-gorogoro/Crystack_release/issues> with the file type, your system and what happened.

## License

See [LICENSE](LICENSE). Third-party notices are inside every download (`THIRD_PARTY_LICENSES`).

---

# CryStack (한국어)

분말 X선 회절(XRD) 패턴을 쌓아서 2θ, d, Q 축으로 보고, 패턴마다 배율과 오프셋을 줄 수 있는 프로그램입니다. 개인·교육·연구 목적에는 무료입니다. 이 저장소에는 다운로드 파일만 있고 소스 코드는 공개하지 않습니다.

**다운로드:** [최신 릴리스](https://github.com/hjh90-gorogoro/Crystack_release/releases/latest)에서 사용하는 OS의 파일을 받으세요. Windows는 zip을 풀고 `CryStack.exe`를 실행하고, macOS는 zip을 풀어 `CryStack.app`을 응용 프로그램 폴더로 옮기고, Linux는 tar.gz를 풀고 `./install.sh`를 실행합니다. 받은 파일 안에 한국어 매뉴얼(`MANUAL_KO.html`)과 예제 파일(`samples` 폴더)이 들어 있습니다.

**처음 실행할 때 경고가 뜨는 경우:** 아직 유료 서명이 없어서 한 번 경고가 나옵니다. Windows는 "추가 정보 → 실행", macOS는 앱을 우클릭 → 열기를 누르세요. 그래도 막히면 터미널에서 `xattr -cr /Applications/CryStack.app`을 실행합니다.

**주요 기능**
- `.xy`, `.xye`, `.dat`, `.chi`, `.csv`, `.txt` 패턴 열기 (드래그 앤 드롭, CrysAlis `.dat` 자동 인식, 헤더의 파장 자동 읽기)
- 2θ / d / Q 축 전환과 파장 설정, 패턴별 배율·오프셋, 많은 파일을 다루기 위한 정렬·필터·다중 선택
- `.jcpds`, `.cif`, 텍스트 파일의 참조 피크 표시, 230개 공간군에서 단위격자를 만들어 격자상수를 바꾸며 피크 맞추기, hkl 라벨
- 온도·시간·압력 시리즈 히트맵: 컬러맵, 대비, 차이 지도, 피크 밴드 추적(면적, 위치, FWHM, 격자상수)과 CSV 저장
- 세션 저장, 화면과 같은 PNG / SVG / PDF 그림 내보내기, 데이터 `.xy` / `.csv` 내보내기

자세한 사용법은 다운로드 파일 안의 `MANUAL_KO.html`을 보세요.
