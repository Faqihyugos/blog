---
title: "Vscode Extensions Html"
date: 2021-06-08T12:48:16+07:00
draft: false
tags: [
  "Vscode Extensions",
  "Vscode",
  "HTML"
]
disqus_title: "vscode-extensions"
---

Mari kita lihat beberapa ekstensi untuk Kode VS yang membuat penulisan dan pengeditan HTML lebih baik. Anda mungkin tidak menyukai semuanya. Mungkin beberapa dari mereka tidak menarik bagi Anda, memecahkan masalah yang tidak Anda miliki, atau merasa lebih berantakan daripada yang Anda butuhkan. Tidak apa-apa. Ini hanya segelintir yang saya coba dan sukai sampai tingkat tertentu.

Saya akan mulai dengan Emmet di sini, meskipun secara teknis ini bukan ekstensi untuk Kode VS. Itu sudah terpasang. Anda harus mengetahuinya karena ini sangat berguna. Itu melakukan "HTML Expansions" seperti ini, yang saya gunakan hampir setiap hari dalam hidup saya:

## [HTML End Tag Labels](https://marketplace.visualstudio.com/items?itemName=anteprimorac.html-end-tag-labels)

Saya mendengar tentang ini dari Stefan Judis yang menulis blog tentangnya tempo hari dan inspirasi ide posting ini.

Ide keseluruhannya adalah daripada Anda meninggalkan komentar di HTML untuk menunjukkan elemen HTML apa yang ditutupnya (praktik yang agak umum, terutama untuk sebagian yang menutup elemen yang mungkin tidak dibuka di dokumen yang sama).

```html
<div class="main">


</div> <!-- / div.main -->

<?php /* / div.main */ ?>
<?php /* Sometimes I'd do it in a server side language so it didn't go over the wire. */ ?>
```

Ekstensi ini menunjukkan kepada Anda UI tentang HTML apa yang sedang ditutup:

![image](https://raw.githubusercontent.com/anteprimorac/vscode-html-end-tag-labels/master/images/screenshot-1.png)

## [Auto Close Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-close-tag)

Segera setelah Anda mengetik > dalam elemen HTML, seperti tanda kurung terakhir `<div>`, tag penutup secara otomatis dibuat untuk Anda.

Itu dapat dikonfigurasi untuk hanya menutup otomatis setelah Anda mengetik `/>` menunjukkan Anda akan menutup tag, yang merupakan default di Sublime Text 3. Omong-omong, jika Anda menginstal [Sublime Text Keymap](https://marketplace.visualstudio.com/items?itemName=ms-vscode.sublime-keybindings), Anda akan mendapatkannya secara otomatis, ditambah beberapa perintah kunci mewah lainnya.

## [Highlight Matching Tag](https://marketplace.visualstudio.com/items?itemName=vincaslt.highlight-matching-tag)

![image](https://images2.imgbox.com/71/2a/zIA1XCzK_o.gif)

Saya akan membuat video saya sendiri, tetapi saya menemukan bahwa meskipun saya menonaktifkan ekstensi ini, hal lain dalam vscode saya tetap menyoroti tag yang cocok. Saya tidak sepenuhnya yakin apa itu, yang membuat saya percaya itu mungkin fitur bawaan sekarang.

![image](https://i0.wp.com/css-tricks.com/wp-content/uploads/2021/05/Screen-Shot-2021-05-26-at-1.56.35-PM.png?w=1004&ssl=1)

Tidak khusus untuk HTML, tetapi jika seperti bantuan semacam ini dengan hal-hal yang cocok, Anda dapat mencoba [Bracket Pair Colorizer 2](https://marketplace.visualstudio.com/items?itemName=CoenraadS.bracket-pair-colorizer-2), yang bisa sangat bagus untuk CSS dan JavaScript.

## [Auto Rename Tag](https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag)

![image](https://github.com/formulahendry/vscode-auto-rename-tag/raw/master/images/usage.gif)

Saya percaya fungsi ini sebenarnya dibangun ke dalam canonical Emmet, tetapi sekali lagi, VS Code tidak menggunakan canonical Emmet sehingga fitur ini tidak ada, oleh karena itu perlunya plugin tambahan ini.

## [Better Comments](https://marketplace.visualstudio.com/items?itemName=aaron-bond.better-comments)

Saya meninggalkan komentar kode dengan cukup bebas, terutama ketika mengembangkan hal-hal baru. Sebuah konvensi yang saya suka adalah ketika komentar diawali (misalnya TODO) bahwa itu sangat penting dan membutuhkan perhatian. Better Comments memungkinkan mereka untuk terlihat berbeda secara visual.

![image](https://github.com/aaron-bond/better-comments/raw/master/images/better-comments.PNG)