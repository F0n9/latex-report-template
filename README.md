# LaTeX Academic Report Template

[![Compiler](https://img.shields.io/badge/Compiler-pdfLaTeX-47A141?style=flat-square&logo=latex&logoColor=white)](https://www.latex-project.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-0d1117?style=flat-square)](LICENSE)
[![Format: A4](https://img.shields.io/badge/Format-A4-blue?style=flat-square)](main.pdf)
[![Institution](https://img.shields.io/badge/Style-HCMUS-00599C?style=flat-square)](https://hcmus.edu.vn)

A clean, modular, and publication-ready academic report template configured in LaTeX. Synchronized in layout, typography, palette, and metadata architecture with the modern Typst report template. Tailored for coursework, term projects, and technical theses at VNU-HCM University of Science (HCMUS) with out-of-the-box Vietnamese language and mathematical typesetting support.

## Features

- **Centralized Metadata:** All document and author credentials are decoupled into `metadata.tex`, matching `metadata.typ` 1:1.
- **Synchronized Visual Design:** Replicates the clean Typst cover page layout, full-bleed border frame, institutional branding, and boxed student credentials block.
- **Harmonized Color Palette:** Matches Typst theme tokens (`#1E3778` Navy headers, `#677CA6` slate header/footer lines, and `#F7F7F7` syntax blocks).
- **Vietnamese Language Support:** Built-in font encoding (T5, utf8) configured through standard LaTeX packages.
- **Modular Structure:** Clean chapter breakdown (`chapter/01_intro.tex`, `chapter/02_summary.tex`) for seamless writing and collaboration.
- **Reference Management:** Modern citation engine using BibLaTeX with centralized reference storage (`ref.bib`).

## Directory Structure

```text
latex-report-template/
├── assets/
│   ├── border.png
│   ├── logo.png
│   └── preview.png
├── chapter/
│   ├── 01_intro.tex
│   └── 02_summary.tex
├── style/
│   ├── config.tex
│   ├── cover_page.tex
│   └── header_footer.tex
├── metadata.tex
├── main.tex
├── ref.bib
├── main.pdf
├── .gitignore
└── LICENSE
```

## Getting Started

### Prerequisites

Use with any standard TeX distribution or cloud compiler:
- **Web (Recommended):** Import this repository directly into [Overleaf](https://www.overleaf.com/).
- **Windows:** [MiKTeX](https://miktex.org/) or [TeX Live](https://www.tug.org/texlive/)
- **Linux:** `sudo apt install texlive-full`
- **macOS:** [MacTeX](https://www.tug.org/mactex/)

### Compilation

Compile using `latexmk` or `pdflatex`:

```bash
latexmk -pdf main.tex
pdflatex main.tex
biber main
pdflatex main.tex
```

## Configuration

All report parameters are centralized in `metadata.tex`. You do not need to edit layout or formatting files to configure your report:

```latex
\newcommand{\university}{ĐẠI HỌC QUỐC GIA THÀNH PHỐ HỒ CHÍ MINH \\ TRƯỜNG ĐẠI HỌC KHOA HỌC TỰ NHIÊN}
\newcommand{\faculty}{KHOA CÔNG NGHỆ THÔNG TIN}
\newcommand{\department}{[Tên Bộ Môn / Chuyên Ngành]}
\newcommand{\course}{[Tên Học Phần / Môn Học]}

\newcommand{\projecttitle}{BÁO CÁO MÔN HỌC}
\newcommand{\projectsubtitle}{[Tên Đề Tài Báo Cáo]}

\newcommand{\classname}{[Lớp sinh hoạt / Mã lớp]}
\newcommand{\authorname}{[Họ và tên sinh viên]}
\newcommand{\authorid}{[Mã số sinh viên]}
\newcommand{\authoremail}{[Địa chỉ email]}
\newcommand{\instructorname}{[Họ và tên Giảng viên hướng dẫn]}

\newcommand{\submissiondate}{Thành phố Hồ Chí Minh, ngày [..] tháng [..] năm [..]}
```

## Preview

<p align="center">
  <img src="assets/preview.png" width="880" alt="Sample Template Preview" />
</p>

## License

This project is licensed under the [MIT License](LICENSE).
