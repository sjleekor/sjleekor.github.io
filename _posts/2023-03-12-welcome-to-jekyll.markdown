---
layout: post
title:  "Welcome to Jekyll!"
date:   2023-03-12 21:35:47 +0900
categories: jekyll update
---

jekyll 을 사용하면, markdown 으로 포스트를 _posts 밑에 작성해서 push 만 해놓으면 github 가 자동으

처음 셋팅은 [github pages jekyell 적용 공식문서][github-pages]부터 보기 시작하면 되는데 아쉽게도 한글 문서가 없습니다. 정확한 내용은 공식문서를 확인해주세요.

* sjleekor.github.io 라는 [레포][my-repo]를 만들었습니다. 레포 이름이 꼭 이런 식이야 하는 것은 아닌 것 같은데 확실하지 않습니다. 
* jekyll 을 사용하기 위해 ruby 와 jekyll 을 [jekyll 공식문서][jekyll-docs-install]를 보고 준비합니다. 한글화된 문서가 있어 좋습니다. 
* jekyll 문서에는 new 라는 명령어를 사용할 때 디렉터리 이름을 넣지만 레포를 클론해놓았으니 `.` 를 넘겨서 해당 디렉터리에 초기화합니다.
{% highlight bash %}
# 클론한 로컬 레포 루트로 이동합니다.
cd sjleekor.github.io
# jekyll 을 이용해 디렉터리를 초기화합니다. 
jekyll new .
{% endhighlight %}
* Gemfile 을 열어서 gem "jekyll" 로 시작하는 줄을 주석처리하고 gem "github-pages" 줄을 추가합니다. 228 은 github-pages 버전인데 [pages versions][github-pages-versions] 페이티를 참조해서 적습니다. 
{% highlight config %}
#gem "jekyll", "~> 4.3.2"
gem "github-pages", "~> 228", group: :jekyll_plugins
{% endhighlight %}
* 설치해줍시다.
{% highlight bash %}
bundle install
# ruby 최신버전에서는 webrick 을 설치해야 한다고 합니다.
bundle add webrick
{% endhighlight %}
* local 에서 실행해봅니다.
{% highlight bash %}
bundle exec jekyll serve
{% endhighlight %}
* [http://localhost:4000] 에 접근하면 화면을 확인할 수 있습니다.
* 이제 커밋하고 리모트에 푸쉬합니다. 
* 레포 셋팅 화면, Pages 메뉴에서 Source, Branch 를 설정하고 save 를 누르면 Your site is live at .... 상자가 나오며 접근할 수 있게 됩니다. 이 [블로그][deploy-pages] 설명이 되어 있습니다.

```go
type A struct {
	a string
}
```

[jekyll-docs]: https://jekyllrb-ko.github.io/
[jekyll-docs-install]: https://jekyllrb-ko.github.io/docs/
[my-repo]: https://github.com/sjleekor/sjleekor.github.io
[github-pages]: https://docs.github.com/ko/pages/setting-up-a-github-pages-site-with-jekyll/about-github-pages-and-jekyll 
[github-pages-versions]: https://pages.github.com/versions/
[deploy-pages]: https://fe-paradise.tistory.com/entry/Github-Pages-%EA%B9%83%ED%97%88%EB%B8%8C%EB%A1%9C-%EC%82%AC%EC%9D%B4%ED%8A%B8-%EB%B0%B0%ED%8F%AC%ED%95%98%EA%B8%B0-Github-Deploy