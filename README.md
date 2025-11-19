# Octocat
### 👋 Hi there, I'm Robinson P!

<a href="https://git.io/typing-svg"><img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=20&pause=1000&color=F700FF&center=true&vCenter=true&width=435&lines=Full-Stack+Developer;AI+%26+ML+Enthusiast;Open+Source+Contributor;Always+Learning+New+Things" alt="Typing SVG" /></a>
## 🔥 My GitHub Stats

[![Your GitHub Stats](https://github-readme-stats.vercel.app/api?username=robinsonkarunya&show_icons=true&theme=radical&hide_border=true)](https://github.com/anuraghazra/github-readme-stats)
## 💻 Top Languages

[![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=robinsonkarunya&layout=compact&theme=radical&hide_border=true)](https://github.com/anuraghazra/github-readme-stats)

name: Latest blog post workflow
on:
  schedule:
    - cron: '0 8 * * *' # Runs daily at 8:00 AM UTC
  workflow_dispatch:

jobs:
  update-readme-with-blog:
    name: Update this repo's README with latest blog posts
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: gautamkrishnar/blog-post-workflow@v1
        with:
          feed_url: 
          max_post_count: "5"
          date_format: "yyyy-mm-dd"
          comment_tag_name: "BLOG-POST-LIST"
          commit_message: "Update README with latest blog posts"
