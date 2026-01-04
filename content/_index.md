---
# Leave the homepage title empty to use the site title
title: ''
summary: ''
date: 2022-10-24
type: landing

design:
  # Default section spacing
  spacing: '6rem'

sections:
  # 1. 个人简介板块 (Bio)
  - block: resume-biography-3
    content:
      # 重要：这里必须对应 content/authors/ 下的文件夹名
      # 如果你的文件夹是 admin，这里就填 admin
      username: admin
      text: ''
      # 这是一个下载简历的按钮，如果你没有 resume.pdf，可以把下面两行删掉
      button:
        text: Download CV
        url: uploads/resume.pdf
    design:
      background:
        gradient_mesh:
          enable: true
      name:
        size: lg
      avatar:
        size: xxl
        shape: circle

  # 2. 简短的研究介绍 (Markdown Text)
  - block: markdown
    content:
      title: '🔬 Research Focus'
      subtitle: ''
      text: |-
        Here you can introduce your research direction briefly. For example: I am focusing on Artificial Intelligence and Robotics.
        
        (You can edit this text in content/_index.md)
    design:
      columns: '1'

  # 3. 科研成果列表 (Publications)
  - block: collection
    id: publications
    content:
      title: Recent Publications
      text: ''
      filters:
        folders:
          - publications
        exclude_featured: false
    design:
      view: citation  # 引用格式展示，比较正式

  # 4. 思考文章 (Essays / Blog)
  - block: collection
    id: posts
    content:
      title: Essays & Thoughts
      subtitle: ''
      text: ''
      page_type: blog
      count: 5
      filters:
        folders:
          - blog    # 这里对应 content/blog 文件夹
    design:
      view: card    # 卡片式展示
      columns: 2

  # 5. 生活相册 (Gallery)
  # 注意：你需要创建一个相册文件夹才能显示图片
  # 路径：assets/media/albums/life
  - block: gallery
    id: gallery
    content:
      title: Life & Gallery
      text: ''
      gallery_item:
        - album: life  # 这里对应 assets/media/albums/ 下的文件夹名
    design:
      columns: 3
---