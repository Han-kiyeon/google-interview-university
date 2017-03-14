# Google Interview University

Translations:
- [한국어](README-kr.md)
- [中文版本](README-cn.md)
- [Español (in progress)](README-es.md) [Issue #80](https://github.com/jwasham/google-interview-university/issues/80)
- [हिन्दी (in progress)](README-hn.md) [Issue #81](https://github.com/jwasham/google-interview-university/issues/81)
- [עברית (in progress)](README-he.md) [Issue #82](https://github.com/jwasham/google-interview-university/issues/82)


## 문서 소개

이 문서는 구글 Software 개발자가 되기 위한 계획적인 접근 방식을 제공한다.
이 문서의 최초 작성자는 John Washam 이며, 그 분의 git repository forking 하여 문서 번역 진행했습니다. 또한 이문서의 "나는" 이라는 것은 최초 작성자입니다.

![Coding at the whiteboard - from HBO's Silicon Valley](https://dng5l3qzreal6.cloudfront.net/2016/Aug/coding_board_small-1470866369118.jpg)

아래 긴 리스트의 내용은 **Google 의 코칭 노트** 에서 참고 및 확장 했으니, 꼭 알고 있어야 하는 사항이니 명심하자.

인터뷰에서 나왔던 내용이나 문제를 푸는데 도움이 될 만한 것들을 문서 아래에 추가했다. 많은 내용들이 Steve Yegge's Blog "[Get that job at Google](http://steve-yegge.blogspot.com/2008/03/get-that-job-at-google.html)" 에서 가져왔고, 때로는 Google 의 코칭 노트에서 단어 하나 하나를 반영했다.

나는 Yegge 가 권하는 방법에서 부터 당신이 알아야 할 것을 정리 드립니다. 그리고 새로이 software engineer 가 되고 싶다면(이 문서에는 web development 와 software engineer 에 차이가 있으며, 그 차이는 computer science 관련 지식등의 더 많은 것을 알고 있어야 하는 것으로 보입니다.) 만약, 당신이 computer science(컴퓨터 과학)에 지식과 경력이 있다면 interview 는 더욱더 힘들 것입니다.(더 어려운 문제가 주어진다는 의미로 생각됩니다.) [Read more here](https://googleyasheck.com/what-you-need-to-know-for-your-google-interview-and-what-you-dont/)

만약, system engineer 와 관련된 일을 했다면, networking 이나 security 관련된 지식을 조금 더 알아야 한다.

---

## Table of Contents

- [문서 소개](#문서-소개)
- [문서 소개2](#문서-소개2)
- [문서 사용법](#문서-사용법)
- [Get in a Googley Mood](#get-in-a-googley-mood)
- [Follow Along with Me](#follow-along-with-me)
- [Don't feel you aren't smart enough](#dont-feel-you-arent-smart-enough)
- [구글에 대해](#구글에-대해)
- [About Video Resources](#about-video-resources)
- [Interview Process & General Interview Prep](#interview-process--general-interview-prep)
- [Pick One Language for the Interview](#pick-one-language-for-the-interview)
- [책 목록](#책-목록)
- [시작하기 전에](#시작하기-전에)
- [여기서 다루지 않는 것들](#여기서-다루지-않는-것들)
- [선행 지식](#선행-지식)
- [일일 계획](#일일-계획)
- [알고리즘 복잡도 / Big-O / 점근 분석](#알고리즘-복잡도--Big-O--점근-분석)
- [자료 구조](#자료-구조)
    - [배열](#배열)
    - [연결 리스트](#연결-리스트)
    - [스택](#스택)
    - [큐](#큐)
    - [해쉬 테이블](#해쉬-테이블)
- [추가 자료 구조](#추가-자료-구조)
    - [이진 검색](#이진-트리)
    - [비트 연산](#비트-연산)
- [트리](#트리---Tree)
    - [트리 - 노트 & 배경 지식](#트리---노트--배경-지식)
    - [이진 검색 트리: BSTs](#이진-검색-트리-bsts)
    - [힙 / 우선순위 큐 / 이진 힙](#힙--우선순위-큐--이진-힙)
    - 균형 잡힌 이진 트리 (기본 컨셉, 자세히는 아님)
    - 트리 순방: preorder, inorder, postorder, BFS, DFS
- [정렬](#정렬)
    - selection
    - insertion
    - heapsort
    - quicksort
    - merge sort
- [그래프](#그래프)
    - directed
    - undirected
    - adjacency matrix
    - adjacency list
    - traversals: BFS, DFS
- [더 많은 지식](#더-많은-지식)
    - [재귀](#recursion)
    - [객체지향적 프로그래밍](#객체지향적-프로그래밍)
    - [디자인 패턴](#디자인-패턴)
    - [조합(n 개중에 k) 와 확률](#조합-n-개중에-k-와-확률)
    - [NP, NP-Complete 과 근사 알고리즘](#np-np-complete-과-근사-알고리즘)
    - [캐쉬](#캐쉬)
    - [프로세스와 쓰레드](#프로세스와-쓰레드)
    - [논문](#논문)
    - [테스팅](#테스팅)
    - [스케줄링](#스케줄링)
    - [시스템 루틴 구현](#시스템-루틴-구현)
    - [문자열 검색 & 조작](#문자열-검색--조작)
- [시스템 설계, 확장, 자료 처리 (System Design, Scalability, Data Handling)](#시스템-설계-확장-자료-처리) (4년 이상 경력자)
- [마지막 리뷰](#마지막-리뷰)
- [코딩 문제 연습](#코딩-문제-연습)
- [코딩 연습/도전](#코딩-연습도전)
- [일단 당신이 인터뷰에 가까이 갔다.](#일단-당신이-인터뷰에-가까이-갔다.)
- [이력서](#이력서)
- [인터뷰가 다가올 때쯤 생각해볼 만한 것들](#인터뷰가-다가올-때쯤-생각해볼-만한-것들)
- [Have questions for the interviewer](#have-questions-for-the-interviewer)
- [Once You've Got The Job](#once-youve-got-the-job)

---------------- Everything below this point is optional ----------------

- [추가적인 책](#추가적인-책)
- [추가적인 배움](#추가적인-배움)
    - [동적 프로그래밍](#동적-프로그래밍)
    - [컴파일러](#컴파일러)
    - [Floating Point Numbers](#floating-point-numbers)
    - [유니코드](#유니코드)
    - [엔디안](#엔디안)
    - [Emacs 와 vi(m)](#emacs-와-vim)
    - [유닉스 커맨드 라인 툴](#유닉스-커맨드-라인-툴)
    - [정보 이론 (영상)](#정보-이론-영상)
    - [패러티 & 해밍 코드 (영상)](#패러티--해밍-코드-영상)
    - [엔트로피](#엔트로피)
    - [암호학](#암호학)
    - [압축](#압축)
    - [네트워킹](#네트워킹)
    - [컴퓨터 보안](#컴퓨터-보안)
    - [가비지 컬렉션](#가비지-컬렉션)
    - [병렬 프로그래밍](#병렬-프로그래밍)
    - [메세징, 직렬화, 그리고 대기(큐) 시스템](#메세징-직렬화-그리고-대기큐-시스템)
    - [Fast Fourier Transform 빠른 푸리에 변환](#fast-fourier-transform-빠른-푸리에-변환)
    - [Bloom Filter 블룸 필터](#bloom-filter-블룸-필터)
    - [HyperLogLog](#hyperloglog)
    - [Locality-Sensitive Hashing](#locality-sensitive-hashing)
    - [van Emde Boas Trees 반 엠데 보아스 트리](#van-emde-boas-trees-반-엠데-보아스-트리)
    - [Augmented Data Structures 증강된 자료 구조들](#augmented-data-structures-증강된-자료-구조들)
    - [Tries 트라이(Prefix tree)](#tries-트라이Prefix-tree)
    - [N-ary (K-ary, M-ary) trees](#n-ary-k-ary-m-ary-trees)
    - [Balanced search trees 균형 잡힌 이진 트리](#balanced-search-trees-균형-잡힌-이진-트리)
        - AVL trees
        - Splay trees
        - Red/black trees
        - 2-3 search trees
        - 2-3-4 Trees (aka 2-4 trees)
        - N-ary (K-ary, M-ary) trees
        - B-Trees
    - [k-D 트리](#k-d-트리)
    - [Skip lists](#skip-lists)
    - [네트웍 흐름](#네트웍-흐름)
    - [Disjoint Sets & Union Find 분리된 셋 & 유니온 찾기](#disjoint-sets--union-find-분리된-셋--유니온-찾기)
    - [빠른 처리를 위한 수학 Math for Fast Processing](#빠른-처리를-위한-수학-math-for-fast-processing)
    - [Treap](#treap)
    - [선형 프로그래밍 (영상)](#선형-프로그래밍-영상)
    - [기하학, Convex hull 볼록 선체 (영상)](#기하학-Convex-hull-볼록-선체-영상)
    - [이산 수학](#이산-수학)
    - [머신 러닝](#머신-러닝)
    - [Go](#go)
- [또다른 주제에 대한 상세](#또다른-주제에-대한-상세)
- [영상 시리즈](#영상-시리즈)
- [컴퓨터 과학](#컴퓨터-과학)

---

## 문서 소개2

나는 나의 구글 인터뷰 준비를 위해 이 문서와 같은 계획을 만들고 실행했다. 나는 web 과 관련된 startup 을 1997년 부터 해왔었다. 나는 경제학 학위는 있지만, computer science 는 없었다. 나의 경력은 매우 성공적이었지만, 나는 구글에서 일하기는 원한다. 컴퓨터 시스템, 알고리즘 효율성, 데이터 구조 성능, 저수준 언어등이 어떻게 동작하는지 알고 싶고 만약 당신이 이중 어떤 것도 알기를 원치 않다면 구글은 당신을 고용하지 않을 것이다.

내가 이 프로젝트를 시작했을 때, 나는 stack, heap, Big-O, tree 와 graph 탐색 같은 것은 알지 못했다. 만약 내가 정렬(sorting) 알고리즘을 구현해야 했다면, 나는 그것을 하기 어렵다고 말했을 것입니다. 데이터 구조(Data Structure)는 사용한 적도, 어떻게 내부적으로 수행되는지도 알지 못했다. 또한 나는 "out of memory" error 를 보아도 메모리 관리를 해야하는 것도 몰라고, 다차원 배열은 몇번 써본 정도이다. 데이터 구조는 처음부터 생성해본적이 절대 없다.

하지만 이 공부를 시작하고 나서는 내가 고용(구글에)될 것이라는 강한 자신감을 갖게 되었고, 이것은 길게 보고 계획을 만들었다. 당연히 이것은 몇개월이라는 시간을 투자해야 한다. 만약 당신이 위에서 언급한 내용에 대해 친숙하다면 시간을 많이 단축할 수 있을 것이다.

**[번역자] 모든 링크된 문서나 영상은 영어로 되어있다. 비슷한 참고할 만한 본인이 찾은 좋은 문서가 있다면 같이 링크하도록 하겠다.**

## 문서 사용법

아래에 나오는 모든 내용은 개요이고, 당신은 여기서 부터 순차적으로 하나씩 접근해야 합니다.

나는 Github 의 markdown 을 이용하여 check list 를 만들고 이용합니다.

- [x] 새로운 브랜치를 만들고 이 파일에 있는 선택 항목에 대해, 완료했다면 'x' 를 대괄호 호([]) 사이에 입력합니다.

    브랜치를 "Fork" 하고 아래의 command 를 입력하세요.
    `git clone https://your.github.com/...`

    `git checkout -b progress`

    계획된 일들이 완료되면 check box 를 선택(x 입력) 하고 저장한뒤,

    `git add . `

    `git commit -m "Marked x" `

    `git push origin progress`
    이렇게 하면, 새로운 브랜치 생성 및 자신의 계획 관리가 되는 md 파일이 된다.

[More about Github-flavored markdown](https://guides.github.com/features/mastering-markdown/#GitHub-flavored-markdown)

[Github 의 markdown 한글 문서](https://gist.github.com/ihoneymon/652be052a0727ad59601)

## Get in a Googley Mood

"[future Googler](https://github.com/jwasham/google-interview-university/blob/master/extras/future-googler.pdf)" 프린트 해서 잘보이는 곳에 두자.

[![future Googler sign](https://dng5l3qzreal6.cloudfront.net/2016/Oct/Screen_Shot_2016_10_04_at_10_13_24_AM-1475601104364.png)](https://github.com/jwasham/google-interview-university/blob/master/extras/future-googler.pdf)

## Follow Along with Me

My story: [구글 인터뷰 준비를 위해 왜 8 달 동안 공부를 했는지에 대한 나의 이야기](https://medium.com/@googleyasheck/why-i-studied-full-time-for-8-months-for-a-google-interview-cc662ce9bb13)

블로그 / 트위터 / Google+ / 링크드인:

- **Blog**: [GoogleyAsHeck.com](https://googleyasheck.com/)
- Twitter: [@googleyasheck](https://twitter.com/googleyasheck)
- Twitter: [@StartupNextDoor](https://twitter.com/StartupNextDoor)
- Google+: [+Googleyasheck](https://plus.google.com/+Googleyasheck)
- LinkedIn: [johnawasham](https://www.linkedin.com/in/johnawasham)

![John Washam - Google Interview University](https://dng5l3qzreal6.cloudfront.net/2016/Aug/book_stack_photo_resized_18_1469302751157-1472661280368.png)

## Don't feel you aren't smart enough
- 구글 엔지니어는 스마트 하다. 그러나 충분히 스마트 하지 않는(?) 사람도 있다. 아래의 Youtube 는 꼭 보자.
- [The myth of the Genius Programmer 천재 프로그래머에 대한 미신](https://www.youtube.com/watch?v=0SARbwvhupQ)
- [혼자 가는건 너무 위험해: 기술이라는 보이지 않는 괴물과 싸워야해](https://www.youtube.com/watch?v=1i8ylq4j_EY)

## 구글에 대해

- [x] For students - [Google Careers: 기술 개발 가이드](https://www.google.com/about/careers/students/guide-to-technical-development.html)
- [ ] 구글에서 일거리 찾기:
    - [ ] [검색의 진화 (영상)](https://www.youtube.com/watch?v=mTBShTwCnD4)
    - [ ] [검색이 동작하는 방법 - 이야기](https://www.google.com/insidesearch/howsearchworks/thestory/)
    - [ ] [검색 동작 방법](https://www.google.com/insidesearch/howsearchworks/)
    - [ ] [검색 동작 방법 - Matt Cutts (영상)](https://www.youtube.com/watch?v=BNHR6IQJGZs)
    - [ ] [어떻게 구굴은 검색 알고리즘을 향상시키는가? (영상)](https://www.youtube.com/watch?v=J5RZOU6vK4Q)
- [ ] 시리즈들:
    - [ ] [구글이 모바일 검색을 처리하는 방법](https://backchannel.com/how-google-search-dealt-with-mobile-33bc09852dc9)
    - [ ] [우리의 요구를 찾기 위한 구글의 비밀 스터디](https://backchannel.com/googles-secret-study-to-find-out-our-needs-eba8700263bf)
    - [ ] [Google Search Will Be Your Next Brain](https://backchannel.com/google-search-will-be-your-next-brain-5207c26e4523)
    - [ ] [The Deep Mind Of Demis Hassabis](https://backchannel.com/the-deep-mind-of-demis-hassabis-156112890d8a)
- [ ] [Book: How Google Works](https://www.amazon.com/How-Google-Works-Eric-Schmidt/dp/1455582344)
- [ ] [Made by Google announcement - Oct 2016 (video)](https://www.youtube.com/watch?v=q4y0KOeXViI)

## About Video Resources

어떤 영상들은 Coursera, EdX 나 Lynda.com 에서 enroll(등록)을 해야 볼수 있는 것들이 있다.(이를 MOOC 라 한다.) 때로는 몇달을 기다려야 그 강좌를
들을 수 있는 경우가 있고, Lynda.com의 경우 유료이다. (google 검색으로 coursera / Edx 를 검색하면 이용법등의 블로그들을 찾을 수 있을 것이다.)

## Interview Process & General Interview Prep

- [ ] 영상들:
    - [ ] [How to Work at Google: Prepare for an Engineering Interview (video)](https://www.youtube.com/watch?v=ko-KkSmp-Lk)
    - [ ] [How to Work at Google: Example Coding/Engineering Interview (video)](https://www.youtube.com/watch?v=XKu_SEDAykw)
    - [ ] [How to Work at Google - Candidate Coaching Session (video)](https://www.youtube.com/watch?v=oWbUtlUhwa8&feature=youtu.be)
    - [ ] [Google Recruiters Share Technical Interview Tips (video)](https://www.youtube.com/watch?v=qc1owf2-220&feature=youtu.be)
    - [ ] [How to Work at Google: Tech Resume Preparation (video)](https://www.youtube.com/watch?v=8npJLXkcmu8)

- [ ] 문서들:
    - [ ] [Becoming a Googler in Three Steps](http://www.google.com/about/careers/lifeatgoogle/hiringprocess/)
    - [ ] [Get That Job at Google](http://steve-yegge.blogspot.com/2008/03/get-that-job-at-google.html)
        - 그(?)가 말한 모든 내용은 아래 리스트에 나와있다.
    - [ ] _(아주 오래된 문서)_ [How To Get A Job At Google, Interview Questions, Hiring Process](http://dondodge.typepad.com/the_next_big_thing/2010/09/how-to-get-a-job-at-google-interview-questions-hiring-process.html)
    - [ ] [Phone Screen Questions](http://sites.google.com/site/steveyegge2/five-essential-phone-screen-questions)

- [ ] Prep Courses:
    - [ ] [Software Engineer Interview Unleashed (paid course)](https://www.udemy.com/software-engineer-interview-unleashed):
        - Learn how to make yourself ready for software engineer interviews from a former Google interviewer.

- [ ] Additional (not suggested by Google but I added):
    - [ ] [ABC: Always Be Coding](https://medium.com/always-be-coding/abc-always-be-coding-d5f8051afce2#.4heg8zvm4)
    - [ ] [Four Steps To Google Without A Degree](https://medium.com/always-be-coding/four-steps-to-google-without-a-degree-8f381aa6bd5e#.asalo1vfx)
    - [ ] [Whiteboarding](https://medium.com/@dpup/whiteboarding-4df873dbba2e#.hf6jn45g1)
    - [ ] [How Google Thinks About Hiring, Management And Culture](http://www.kpcb.com/blog/lessons-learned-how-google-thinks-about-hiring-management-and-culture)
    - [ ] [Effective Whiteboarding during Programming Interviews](http://www.coderust.com/blog/2014/04/10/effective-whiteboarding-during-programming-interviews/)
    - [ ] Cracking The Coding Interview Set 1:
        - [ ] [Gayle L McDowell - Cracking The Coding Interview (video)](https://www.youtube.com/watch?v=rEJzOhC5ZtQ)
        - [ ] [Cracking the Coding Interview with Author Gayle Laakmann McDowell (video)](https://www.youtube.com/watch?v=aClxtDcdpsQ)
    - [ ] Cracking The Coding Interview 한글 번역판:
        - [ ] [게리 엘 멕도웰 지음, 이병준 옮김](http://www.kyobobook.co.kr/product/detailViewKor.laf?mallGb=KOR&barcode=9788966260485)
    - [ ] How to Get a Job at the Big 4:
        - [ ] ['How to Get a Job at the Big 4 - Amazon, Facebook, Google & Microsoft' (video)](https://www.youtube.com/watch?v=YJZCUhxNCv8)
    - [ ] [Failing at Google Interviews](http://alexbowe.com/failing-at-google-interviews/)

## Pick One Language for the Interview

이와 관련된 짧은 글을 소개 한다.: [Important: Pick One Language for the Google Interview](https://googleyasheck.com/important-pick-one-language-for-the-google-interview/)

당신이 원하는 언어를 선택할 수 있지만, 아래의 언어를 우선 선택하는 것이 좋다.:

- C++
- Java
- Python

당신은 아래의 언어 또한 선택할 수 있지만, 약간의 손해(?) 사항이 있는 듯:

- JavaScript
- Ruby

당신은 선택한 언어에 매우 익숙하고 관련된 지식을 갖고 있어야 한다.

언어 선택에 있어 도움이 될 만한 글들:
- http://www.byte-by-byte.com/choose-the-right-language-for-your-coding-interview/
- http://blog.codingforinterviews.com/best-programming-language-jobs/
- https://www.quora.com/What-is-the-best-language-to-program-in-for-an-in-person-Google-interview

[See language resources here](programming-language-resources.md)

C / C++ / Python 을 배울 때, 도움이 될만한 책들이 아래에 리스트되어 있다.

## 책 목록

아래의 리스트는 내가 이용한 책의 양보다는 작다. 당신의 시간을 절약할 수 있길 기대한다.

### Interview Prep

- [ ] [Programming Interviews Exposed: Secrets to Landing Your Next Job, 2nd Edition](http://www.wiley.com/WileyCDA/WileyTitle/productCd-047012167X.html)
    - C++ / JAVA 로 답변
    - Google candidate 에게 코칭할때 사용됨.
    - 번역판 : [한빛 미디어, 프로그래밍 면접 이렇게 준비한다](http://www.hanbit.co.kr/store/books/look.php?p_code=B9005920688)
    - 이책은 Cracking Coding Interview 책을 보기전에 보면 좋다.
    - 너무 어렵지도 않고, 인터뷰에서 당신이 마주할 수 있는 많은 문제들을 쉽게 풀수 있도록 도와 준다.
- [ ] [Cracking the Coding Interview, 6th Edition](http://www.amazon.com/Cracking-Coding-Interview-6th-Programming/dp/0984782850/)
    - 번역판 :[게리 엘 멕도웰 지음, 이병준 옮김 - http://www.kyobobook.co.kr/product/detailViewKor.laf?mallGb=KOR&barcode=9788966260485]
    - JAVA 로 답변
    - [Google Careers site](https://www.google.com/about/careers/how-we-hire/interview/)에서 추천함
    - 만약 당신이 "The Google Resume" 에 참조를 했다면, "Cracking the Coding Interview" 책을 소개 했을 것이다.

당신이 정말 정말 시간이 많다면,

- [ ] [Elements of Programming Interviews](https://www.amazon.com/Elements-Programming-Interviews-Insiders-Guide/dp/1479274836)
    - C++ 로 인터뷰를 본다면 정말 좋은 책이다.
    - 일반적인 문제 해결을 위해 좋은 책이다.

### Computer Architecture

짧은 시간 안에:

- [ ] [Write Great Code: Volume 1: Understanding the Machine](https://www.amazon.com/Write-Great-Code-Understanding-Machine/dp/1593270038)
    - 이 책은 2004년에 출간되어, 바뀐 부분이 있지만 이 책은 computer 를 이해하는데 훌륭한 리소스다.
    - 저자는 HLA(80x86 프로세서를 위한 high level assembler 임) 를 개발goTrh, HLA 에 사용한 예제등을 사용했다.
    - 아래의 챕터를 읽어보면 기본기를 다지는데 좋다:
        - Chapter 2 - Numeric Representation (숫자 표현)
        - Chapter 3 - Binary Arithmetic and Bit Operations (이진 산술 및 비트 연산)
        - Chapter 4 - Floating-Point Representation (소수 표현)
        - Chapter 5 - Character Representation (문자 표현)
        - Chapter 6 - Memory Organization and Access (메모리 구성 및 접근)
        - Chapter 7 - Composite Data Types and Memory Objects (복합 데이터 유형 및 메모리 객체)
        - Chapter 9 - CPU Architecture (CPU 아키텍쳐)
        - Chapter 10 - Instruction Set Architecture (명령어 집합 구조)
        - Chapter 11 - Memory Architecture and Organization (메모리 아키텍쳐와 구성)

만약 당신이 조금더 시간이 있다면:

- [ ] [Computer Architecture, Fifth Edition: A Quantitative Approach](https://www.amazon.com/dp/012383872X/)
    - 더 풍부하고 최신의 내용이 있지만, 시간이 조금 더 많이 필요함.

### Language Specific

**당신은 꼭 인터뷰를 위한 선호하는(?) 언어를 선택해야 한다** 위에서 언급했던 추천하는 언어를 위해 공부할 수 있는 책을 소개 한다.

만약에 당신이 아래의 한가지 정도를 읽었다면, 알고리즘과 데이터 구조에 대한 지식을 얻게 된 것이다. 다음으로 코딩 문제를 풀어보는 것이 좋다.
또한 새로운 언어를 선택하고 기본적인 부분을 빠르게 확인 하고, 정리하려고 한다면 sololearn[https://www.sololearn.com/]을 확인 해보길 바란다.

[Additional language-specific resources here.](programming-language-resources.md)

### C++

나는 아래의 두 개를 읽지 않았지만, Sedgewick 이 쓴 것은 읽으면 정말 좋다.

- [ ] [Algorithms in C++, Parts 1-4: Fundamentals, Data Structure, Sorting, Searching](https://www.amazon.com/Algorithms-Parts-1-4-Fundamentals-Structure/dp/0201350882/)
- [ ] [Algorithms in C++ Part 5: Graph Algorithms](https://www.amazon.com/Algorithms-Part-Graph-3rd-Pt-5/dp/0201361183/)

만약, 더 나은 C++ 을 위한 책이 있다면 소개 바란다.

### Java

- [ ] [Algorithms (Sedgewick and Wayne)](https://www.amazon.com/Algorithms-4th-Robert-Sedgewick/dp/032157351X/)
    - 책과 연관된 영상이 youtube 에 있음. (and Sedgewick!):
        - [Algorithms I - 알고리즘 part 1](https://www.youtube.com/user/algorithmscourses/playlists?view=50&sort=dd&shelf_id=2)
        - [Algorithms II - 알고리즘 part 2](https://www.youtube.com/user/algorithmscourses/playlists?shelf_id=3&view=50&sort=dd)

OR:

- [ ] [Data Structures and Algorithms in Java](https://www.amazon.com/Data-Structures-Algorithms-Michael-Goodrich/dp/1118771338/)
    - 공저 Goodrich, Tamassia, Goldwasser
    - UC Berkeley 에서 CS 기초 코스의 부교제로 사용됨.
    - 아래 python 버전도 있다. 같은 주제를 다루었다.

### Python

- [ ] [Data Structures and Algorithms in Python](https://www.amazon.com/Structures-Algorithms-Python-Michael-Goodrich/dp/1118290275/)
    - 공저 Goodrich, Tamassia, Goldwasser
    - 좋은 책이고, 거의 모든 것을 알려준다.
    - 책 리뷰: https://googleyasheck.com/book-report-data-structures-and-algorithms-in-python/


### Optional Books

**어떤 사람들은 아래의 책을 추천했지만, 내 생각은 다년간 software engineering 경험이 있고 더 어려운 인터뷰가 기대된다면 봐야 할 것이다.**

- [ ] [Algorithm Design Manual](http://www.amazon.com/Algorithm-Design-Manual-Steven-Skiena/dp/1849967202) (Skiena)
    - 리뷰 및 문제 인식에 좋음.
    - 알고리즘 파트는 인터뷰에서 받을 어려움보다 훨씬 더 어렵다.
    - 이 책은 두 파트로 구성:
        - 자료 구조와 알고리즘
            - 장점:
                - 알고리즘 교과서로 좋은 리뷰를 받음.
                - 저자의 문제 풀이 경험으로 부터 나오는 좋은 이야기
                - C code 로 보여줌.
            - 단점:
                - 어떤 부분에서는 CLRS(Introduction to Algorithms) 보다 깊이가 있기도 하지만, 어떤 주제에 대해서는 CLRS 가 나음.
                - 챕터 7, 8, 9 는 이해하기가 정말로 어렵고, 게다가 어떤 부분은 자세히 설명도 안되있거나 이해하기 위해 노력을 많이 해야 한다.
                - 내가 틀린말을 하게 하지 마라: 나는 Skiena 의 가르치는 방식과 버릇(?)을 좋아하지만 뉴욕주립대의 교제가 될 수 없을 수도 있다.
                 (오역일수도 있어서 원문을 남깁니다. don't get me wrong: I like Skiena, his teaching style, and mannerisms, but I may not be Stony Brook material.)
        - 알고리즘:
            - 이책을 사야하는 진짜 이유는 이 파트에 있다.
            - about to get to this part. Will update here once I've made my way through it.
    - Yegge 말을 인용하면: "다른 어떤 책 보다 더 이 책은 Graph 가 얼마 평범하고 중요한지를 이해하는데 도움을 주었다 - 모든
         프로그래머의 툴킷에 포함되어야 할 것이다. 이 책은 또한, 자료 구조와 정렬 알고리즘을 다룬다. 그러나 진짜 좋은 부분은 이 책의 후반부에
         있는데, 그것은 유용한 문제들을 다양한 방법으로 너무 자세하지 않을 정도로 백과사전 처럼 구성을 해놓았다.
         모든 1-pager(아마 하나의 문제를 다루는 범위?)는 간단한 그림을 사용해 기억하기 쉽게 도운다. 이것은 수백의 문제를 풀고 기억하기 위해 좋은 방법이라 생각한다."
    - kindle 에서 대여 가능
    - 좋은 가격으로 Half.com 에서 살수 있다. 국내에 번역본이 없는 것으로 보인다.
    - 답변들을 정리해 놓은 사이트:
        - [Solutions](http://www.algorithm.cs.sunysb.edu/algowiki/index.php/The_Algorithms_Design_Manual_(Second_Edition))
        - [Solutions](http://blog.panictank.net/category/algorithmndesignmanualsolutions/page/2/)
    - [Errata](http://www3.cs.stonybrook.edu/~skiena/algorist/book/errata)

- [ ] [Introduction to Algorithms](https://www.amazon.com/Introduction-Algorithms-3rd-MIT-Press/dp/0262033844)
    - **중요:** 이 책을 읽는 것은 제한적인 가치를 가질 수 있다. 이 책은 알고리즘과 자료구조에 대한 좋은 리뷰를 갖고 있지만, 좋은 코드를 작성하는 방법을 알려주지는 않는다. 당신은 어지간한 문제는 효율적으로 코드를 구현할 수 있어야 한다.
    - Yegge 말을 인용: "만약 당신이 인터뷰를 받기를 원한다면, 이 책에 대해 당신의 방법대로 진행이 완료될 때까지 지원서 내는 것을 조금 뒤로 미루는 것도 고민해보라. "
    - 좋은 가격으로 Half.com 에서 살수 있다.
    - 저자 이름을 따서 CLR 또는 CLRS 라 불린다.(Stein 이란 사람이 늦게 합류해서 CLR 로도 불린다는..)
    - [번역판] http://www.kyobobook.co.kr/product/detailViewKor.laf?ejkGb=KOR&mallGb=KOR&barcode=9791156641131&orderClick=LEB&Kc=

- [ ] [Programming Pearls](http://www.amazon.com/Programming-Pearls-2nd-Jon-Bentley/dp/0201657880)
    - 첫 몇 챕터는 프로그래밍 문제에 대해 훌륭한 해결책을 보여주지만, 이것은 단지 소개정도일 뿐이다. 이 책은 프로그램의 디자인 및 설계에 대한 것이고 "Code complete" 보다 짧은 버전이다.

- ~~"Algorithms and Programming: Problems and Solutions" by Shen~~
    - A fine book, but after working through problems on several pages I got frustrated with the Pascal, do while loops, 1-indexed arrays, and unclear post-condition satisfaction results.
    - 다른 책이나 온라인 코딩 문제를 다루어 보는 것이 더 좋을 것 같다.


## 시작하기 전에

이 리스트들은 많은 달들이 지난, out-dated 된 내용 일 수 있다.

여기에 내가 한 실수들이 있다, 그로인해 당신이 더 나은 경험을 하길 바란다.
(번역자) 한글로 된 비슷한 자료나 참고가 있으면 링크를 남기도록 하겠다.

### 1. 아마 다 기억할 수 없을 꺼야..

나는 많은 시간을 들여 영상을 보면서 노트도 했지만 몇개월 뒤에는 기억이 잘 안났어. 나는 3일을 소비해서 나의 노트와 flash card를 이용해서
다시 확인 했어.

이걸 꼭 읽어봐야에 나중에 내가 한 실수를 하지 않으려면:
[Retaining Computer Science Knowledge](https://googleyasheck.com/retaining-computer-science-knowledge/)

### 2. Flashcard 를 이용하자.

기억이 안나는 문제를 해결하고자, 나는 작은 flashcard 사이트를 활용했다. 2가지 타입이 있는데, 일반적인 것과 코드를 구분해서 만들었고
각각은 서로 다른 포멧으로 만들어 졌다.

나는 처음 주로 이용한 것은 모바일 우선의 웹사이를 사용했다, 언제 어디서나 폰이나 타블릿으로 확인 할 수 있기 때문이다.

무료로 만들어 보자:

- [Flashcards 사이트 목록](https://github.com/jwasham/computer-science-flash-cards)
- [나의 flashcard 데이터 베이스](https://github.com/jwasham/computer-science-flash-cards/blob/master/cards-jwasham.db): 내가 모든 카드들(에셈블리, 파이선, 머신 러닝 그리고 통계등)을 갖고 다녀봤는데, google 에서 요구하는 것들은 너무나도 많다.

**Flashcard 를 위한 조언:**
처음에는 당신이 답을 충분히 인지 하겠지만, 이것을 안다고 확인(mark) 하지 말자. 당신은 같은 카드를 진짜(?) 알기 전까지 보고 또보자. 반복하는 것은 당신의 뇌의 깊은 곳에 지식으로 남게 해줄것이다.

다른 방법으로는 내가 사용하는 flashcard 사이트인 [Anki](http://ankisrs.net/) 를 사용하는 것이다. 이걸 사용하므로써 반복하게 되고 기억에 오래 남도록 도와 줄 것이다.
그것은 user-friendly 하고, cloud 를 통해 동기화 되며 모든 플랫폼서 사용가능 하다. iOS 에서는 25 $ 이지만 다른 플랫폼에서는 무료다.

나의 anki 를 위한 flashcard data 포멧: https://ankiweb.net/shared/info/25173560 (thanks [@xiewenya](https://github.com/xiewenya))

### 3. 리뷰, 리뷰, 또 리뷰

나는 ASCII, OSI 스택, Big-O 표기법 등에 대한 치트 시트를 가지고, 남는 시간에 그것들을 공부했다.

프로그래밍 문제를 풀다가 쉬는 30분에 flashcard 를 읽고 또 읽었다.

### 4. 집중

너의 값진 시간을 방해하는 요소들이 많이 있다. 집중하고 또 집중하자.

## 여기서 다루지 않는 것들

여기에 있는 많은 리스트된 것들은 구글 인터뷰 코칭 노트에서 나온 개인적인 to-do 리스트이다. 이것은 일반적인 내용을 담고 있으며, 아래 언급한 것은 다루지 않는다.:

- SQL
- Javascript
- HTML, CSS, 그리고 다른 프론트엔드 기술.

## 일일 계획

어떤 주제는 하루에 끝낼수 있고, 어떤 것들은 몇 일이 걸릴 수도 있다. 어떤 것들은 어떤 구현도 없는 내용이 있을 수도 있다.

매일 나는 아래의 리스트에서 하나를 선택해서 관련 주제의 영상을 보고 관련된 내용을 구현했다.:

- C - 함수의 인자로 struct * 를 넘겨 구현해노는 연습.
- C++ - 빌트인 type 을 사용하지 않고 구현
- C++ - 빌트인(built-in) type 을 사용하기(예, STL 의 std::list)
- Python - using built-in types (to keep practicing Python)
- 파이썬 - 빌트인 type 사용(지속적인 연습을 위해)
- 그리고 내가 제대로 구현했는지 확인하기 위해 test 를 작성하기. 대로는 간단히 assert 문을 사용한다.
- 당신은 JAVA 나 다른 언어를 사용할 수 있습니다. 위의 내용은 제가 했던 내용입니다.

당신은 위의 모든 언어를 연습할 필요가 없습니다. 하나만 선택하세요. [인터뷰를 위한 언어 선택](#pick-one-language-for-the-interview).

왜 이 모든 것들이 코드를 만드는 것인가?
- 지칠 때 까지, 연습, 연습, 또 연습하라. 그리고 문제 없이 진행 할 수 있도록 하라. (어떤 문제는 많은 [Edge cases](https://en.wikipedia.org/wiki/Edge_case) 들이 있으니 기억 할 수 있도록 기록 해두자.)
/**번역하면서 정확하게 "raw constraints" 에 대한 내용을 모르겠다.**/
- Work within the raw constraints (allocating/freeing memory without help of garbage collection (except Python))
- 가비지 컬렉션(garbage collection)과 같은 도움없이 메모리 할당/해제와 같은 것을 연습해보자.(파이썬은 제외)
- 빌트인 type 들을 사용하는 연습을 많이 하자(실제로는 내가 구현한 연결 리스트를 제품 만드는데는 사용하지 않을꺼니까.)

나는 모든 주제에 대해 연습할 시간이 없었지만, 시도 해볼 것이다.

아래 github page 에 내가 작성한 코드들을 올려놓았다:
 - [C] (https://github.com/jwasham/practice-c)
 - [C++] (https://github.com/jwasham/practice-cpp)
 - [Python] (https://github.com/jwasham/practice-python)

당신은 모든 알고리즘의 내용을 기억할 필요는 없다.

코드를 컴퓨터가 아닌 종이나 화이트 보드로 연습해보자. 샘플로 주어진 입력 값으로 테스트 해보자. 그다음에 컴퓨터로 코드를 만들어 테스트 하는 연습을 하는 것이다.

## 선행 지식

- [ ] **C 언어 배우기**
    - C 는 모든 곳(아마 배울 수 있는)에 있다. 너는 책, 강의, 영상과 같은 것을 통해 배울 수 있을 것이다.
    - [ ] [C Programming Language, Vol 2](https://www.amazon.com/Programming-Language-Brian-W-Kernighan/dp/0131103628)
        - This is a short book, but it will give you a great handle on the C language and if you practice it a little
            you'll quickly get proficient. Understanding C helps you understand how programs and memory work.
        - 이 책은 분량이 적지만, 만약 당신이 조금만 연습한다면 C 언어를 훌륭히 다룰수 있도록 해줄 것이다.
        - [문제들에 대한 답변 코드](https://github.com/lekkas/c-algorithms)

- [ ] **컴퓨터는 프로그램을 어떻게 실행시키는가:**
    - [ ] [CPU 가 어떻게 프로그램을 수행하는지 (영상)](https://www.youtube.com/watch?v=42KTvGYQYnA)
    - [ ] [머신 코드 명령어(영상)](https://www.youtube.com/watch?v=Mv2XQgpbTNE)

## 알고리즘 복잡도 / Big-O / 점근 분석
- 구현할 내용이 없다.
- [ ] [하버드 CS50 - 점근 표기 (영상)](https://www.youtube.com/watch?v=iOq5kSKqeR4)
- [ ] [Big O 표기 (빠른 접근 영상) (영상)](https://www.youtube.com/watch?v=V6mKVRU1evU)
- [ ] [Big O 표기 (and Omega and Theta) - 가장 좋은 수학적 접근 영상 (영상)](https://www.youtube.com/watch?v=ei-A_wy5Yxw&index=2&list=PL1BaGV1cIH4UhkL8a9bJGG356covJ76qN)
- [ ] Skiena:
    - [영상](https://www.youtube.com/watch?v=gSyDMtdPNpU&index=2&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b)
    - [슬라이드](http://www3.cs.stonybrook.edu/~algorith/video-lectures/2007/lecture2.pdf)
- [ ] [알고리즘 복잡도 좋은 설명](http://discrete.gr/complexity/)
- [ ] [논리적 사고 (영상)](https://class.coursera.org/algorithmicthink1-004/lecture/59)
- [ ] [점근식 (영상)](https://class.coursera.org/algorithmicthink1-004/lecture/61)
- [ ] [UC Berkeley Big O (영상)](https://youtu.be/VIS4YDpuP98)
- [ ] [UC Berkeley Big Omega (영상)](https://youtu.be/ca3e7UVmeUc)
- [ ] [Amortized Analysis (영상)](https://www.youtube.com/watch?v=B3SpQZaAZP4&index=10&list=PL1BaGV1cIH4UhkL8a9bJGG356covJ76qN)
- [ ] [논리적 사고 "Big O" (영상)](https://class.coursera.org/algorithmicthink1-004/lecture/63)
- [ ] TopCoder (includes recurrence relations and master theorem):
    - [계산 복잡도 1](https://www.topcoder.com/community/data-science/data-science-tutorials/computational-complexity-section-1/)
    - [계산 복잡도 2](https://www.topcoder.com/community/data-science/data-science-tutorials/computational-complexity-section-2/)
- [ ] [알고리즘 복잡도 치트 시트](http://bigocheatsheet.com/)

    만약, 어떤 강의 들은 너무 수학적(?)이라면, 구체적으로 수학에 대한 배경 지식을 위한 문서의 하단 부에 있는 것으로 확인해보자.

## 자료 구조

- ### 배열
    - 자동으로 vector 의 크기조정(resizing)을 해주는 과정을 구현해보자.
    - [ ] 설명:
        - [배열 (영상)](https://www.coursera.org/learn/data-structures/lecture/OsBSF/arrays)
        - [UCBerkley CS61B - 선형 및 다차원 배열 (영상)](https://youtu.be/Wp8oiO_CZZE?t=15m32s)
        - [기초 배열 (영상)](https://www.lynda.com/Developer-Programming-Foundations-tutorials/Basic-arrays/149042/177104-4.html)
        - [다차원 배열 (영상)](https://www.lynda.com/Developer-Programming-Foundations-tutorials/Multidimensional-arrays/149042/177105-4.html)
        - [동적 배열 (영상)](https://www.coursera.org/learn/data-structures/lecture/EwbnV/dynamic-arrays)
        - [Jagged Arrays-서로 다른 크기를 가지는 다차원 배열 (영상)](https://www.youtube.com/watch?v=1jtrQqYpt7g)
           /**https://en.wikipedia.org/wiki/Jagged_array**/
        - [Jagged Arrays (영상)](https://www.lynda.com/Developer-Programming-Foundations-tutorials/Jagged-arrays/149042/177106-4.html)
        - [크기 재조정 배열 (영상)](https://www.lynda.com/Developer-Programming-Foundations-tutorials/Resizable-arrays/149042/177108-4.html)
    - [ ] vector 구현 (자동 크기 조정을 통한 변하기 쉬운 배열):
        - [ ] 배열과 포인터를 사용해서 코딩 연습하고 숫자로 인텍싱하지 말고 포인터를 통해 접근 및 계산하도록 하자.
        - [ ] 할당된 메모리를 갖고 새로운 raw 데이터 배열
            - can allocate int array under the hood, just not use its features
            - start with 16, or if starting number is greater, use power of 2 - 16, 32, 64, 128
            - 아마 내부 feature 를 사용하지 않고 int array의 메모리를 할당 받아서 사용 할 수 있도록 하는 것일 텐데, 정확한 해석이 불가하여 원문을 남긴다.
        - [ ] size() - 배열의 크기를 반환
        - [ ] capacity() - vector 가 추가 공간 할당 없이 가질 수 있는 공간
        - [ ] is_empty() - 비어있는지 아닌지
        - [ ] at(index) - 주어진 index 의 값을 반환, 최대 인텍스를 넘어가면 안됨.
        - [ ] push(item) - vector 에 하나 추가
        - [ ] insert(index, item) - vector 에 아이템을 하나 추가하는데, index 로 들어온 곳에 추가 한다. index 이후의 데이터는 하나씩 오른쪽 쉬프트가 되어야 함.
        - [ ] prepend(item) - 인덱스 0 에 아이템 추가
        - [ ] pop() - 마지막에 있는 요소 제거함과 값을 반환
        - [ ] delete(index) - index 에 위치하는 요소 제거 및 모든 요소들은 왼쪽으로 쉬프트 되어야 함.
        - [ ] remove(item) - 값으로 요소를 찾아서 vector 에서 제거, 또한 같은 값의 여러 요소들이 제거 될 수 있다.
        - [ ] find(item) - 요소의 값으로 최초 일치하는 요소의 인덱스를 반환, 만약에 같은 요소가 없다면 -1을 반환
        - [ ] resize(new_capacity) // private 함수
            - 만약 vector 가 capacity() 를 넘어서면, 크기를 두배로 늘린다.
            - 요소들을 pop으로 빼내다가, 갖고 있는 요소의 개수가 capacity 의 1/4 이 되면, 크기를 반으로 재조정 한다.
    - [ ] 시간 복잡도
        - O(1) to add/remove at end (amortized for allocations for more space), index, or update 인텍스나 맨 마지막에 추가/삭제
        - O(n) : 어디에 위치하든 추가/삭제
    - [ ] 공간 복잡도
        - contiguous in memory, so proximity helps performance
        - 연속적인 메모리 공간은 성능에 좋게 작용?
        - space needed = (array capacity, which is >= n) * size of item, but even if 2n, still O(n)

- ### 연결 리스트
    - [ ] 설명:
        - [ ] [단순 연결 리스트 (영상)](https://www.coursera.org/learn/data-structures/lecture/kHhgK/singly-linked-lists)
        - [ ] [CS 61B - 연결 리스트 (영상)](https://www.youtube.com/watch?v=sJtJOtXCW_M&list=PL-XXv-cvA_iAlnI-BQr9hjqADPBtujFJd&index=5)
    - [ ] [C 코드 (영상)](https://www.youtube.com/watch?v=QN6FPiD0Gzo)
            - 전체 영상은 아니고, 노드 구조체와 메모리 할당 관련해서만 알려줌
    - [ ] 연결 리스트 vs 배열:
        - [Core 연결 리스트 Vs 배열 (영상)](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/rjBs9/core-linked-lists-vs-arrays)
        - [In The Real World Linked Lists Vs Arrays (영상)](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/QUaUd/in-the-real-world-lists-vs-arrays)
    - [ ] [연결 리스트를 피해야 하는 이유 (영상)](https://www.youtube.com/watch?v=YQs6IC-vgmo)
    - [ ] Gotcha: pointer to pointer 지식이 있어야 한다:
        (포인터를 함수에 인자로 넘길때 포인터의 포인팅을 변경할 수 있어야 한다. 즉, 포인터가 가리키는 값 뿐만 아니라 포이터 자체의 address 변경이 가능해야 할 것이다.) 아래의 링크는 단순이 pointer to pointer 에 대한 파악을 위한 것이다. 포인터에 대한 간략한 내용이니 확인 해보도록 하자.
        - [Pointers to Pointers](https://www.eskimo.com/~scs/cclass/int/sx8.html)
    - [ ] 구현 (나는 tail pointer 를 사용/사용하지 않음 둘다 구현함):
        - [ ] size() - 리스트에 있는 요소의 개수를 반환
        - [ ] empty() - 리스트가 비어 있으면 true 반환 아니면 false
        - [ ] value_at(index) - n번째 아이템의 값을 반환 (리스트의 인텍스는 0 부터 시작함.)
        - [ ] push_front(value) - 리스트의 맨 앞에 아이템 하나 추가
        - [ ] pop_front() - 맨 앞의 아이템 제거 및 그 아이템의 값을 반환
        - [ ] push_back(value) - 리스트의 맨 앞에 아이템 추가
        - [ ] pop_back() - 리스트의 맨 뒤의 아이템 제거 및 값 반환
        - [ ] front() - 리스트 맨 앞 아이템의 값 반환
        - [ ] back() - 리스트의 맨 뒤 아이템의 값 반환get value of end item
        - [ ] insert(index, value) - 주어진 index 의 위치에 값을 추가하기, 그래서 현재 그 인텍스의 아이템은 새로 추가된 아이템의 포인터에 의해 접근 된다.
        - [ ] erase(index) - 주어진 인덱스에 있는 노드 삭제
        - [ ] value_n_from_end(n) - 맨 뒤에서 n 번째에 있는 노드의 값을 반환 한다.
        - [ ] reverse() - 리스트의 순서 뒤집기
        - [ ] remove_value(value) - 주어진 value 를 처음 찾은 인텍스의 아이템 삭제
    - [ ] 이중 연결 리스트
        - [설명 (영상)](https://www.coursera.org/learn/data-structures/lecture/jpGKD/doubly-linked-lists)
        - 구현 할 사항은 없음.

- ### 스택
    - [ ] [스택 (영상)](https://www.coursera.org/learn/data-structures/lecture/UdKzQ/stacks)
    - [ ] [스택 / Last-In First-Out (영상)](https://www.lynda.com/Developer-Programming-Foundations-tutorials/Using-stacks-last-first-out/149042/177120-4.html)
    - [ ] 구현은 안할 것이다. 간단히 배열로 구현 해보면 좋을 듯.

- ### 큐
    - [ ] [큐 / First-In First-Out(영상)](https://www.lynda.com/Developer-Programming-Foundations-tutorials/Using-queues-first-first-out/149042/177122-4.html)
    - [ ] [큐 (video)](https://www.coursera.org/learn/data-structures/lecture/EShpq/queue)
    - [ ] [원형 큐/First-In First-Out](https://en.wikipedia.org/wiki/Circular_buffer)
    - [ ] [우선순위 큐 (영상)](https://www.lynda.com/Developer-Programming-Foundations-tutorials/Priority-queues-deques/149042/177123-4.html)
    - [ ] 연결 리스트를 이용하여 구현하자(tail 포인터 사용):
        - enqueue(value) - tail 포인터가 가리키고 있는 위치에 값 넣기
        - dequeue() - 값을 반환하고 맨 앞의 추가된지 가장 오래된 아이템 삭제 (front)
        - empty() - 비어있는지 확인, 비어있으면 true 반환
    - [ ] 고정 크기 배열로 구현:
        - enqueue(value) - 가용한 공간의 맨 마지막에 값을 추가
        - dequeue() - 가장 추가된지 오래된 요소의 값을 반환 하고 삭제
        - empty() - 비어 있는지 확인
        - full() - 가용한 공간에 요소들이 가득차 있는지 확인.
    - [ ] 복잡도:
        - a bad implementation using linked list where you enqueue at head and dequeue at tail would be O(n)
        - enqueue 를 head 포인터가 있는 곳에 하고, dequeue를 tail 이 가르키는 곳으로 하는 나쁜(?) 구현으로 하면 O(n) 임
            because you'd need the next to last element, causing a full traversal each dequeue. (번역이 애매함)
        - enqueue: O(1) (amortized, linked list and array [probing])
        - dequeue: O(1) (linked list and array)
        - empty: O(1) (linked list and array)

- ### 해쉬 테이블
    - [ ] 영상:
        - [ ] [Chaining(체이닝)의 해슁 (video)](https://www.youtube.com/watch?v=0M_kIqhwbFo&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=8)
        - [ ] [Table Doubling, Karp-Rabin (video)](https://www.youtube.com/watch?v=BRO7mVIFt08&index=9&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb)
        - [ ] [오픈 어드레싱, 암호법의 해슁 (video)](https://www.youtube.com/watch?v=rvdJDijO2Ro&index=10&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb)
        - [ ] [PyCon 2010: 강력한 Dictionary (영상)](https://www.youtube.com/watch?v=C4Kc8xzcA68)
        - [ ] [(Advanced) Randomization: Universal & Perfect Hashing (video)](https://www.youtube.com/watch?v=z0lJ2k0sl1g&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=11)
        - [ ] [(Advanced) 완벽한 해슁 (video)](https://www.youtube.com/watch?v=N0COwN14gt0&list=PL2B4EEwhKD-NbwZ4ezj7gyc_3yNrojKM9&index=4)

    - [ ] 온라인 강좌:
        - [ ] [해쉬 함수의 이해 (video)](https://www.lynda.com/Developer-Programming-Foundations-tutorials/Understanding-hash-functions/149042/177126-4.html)
        - [ ] [해쉬 테이블의 이용 (영상)](https://www.lynda.com/Developer-Programming-Foundations-tutorials/Using-hash-tables/149042/177127-4.html)
        - [ ] [해슁 지원 함수 (영상)](https://www.lynda.com/Developer-Programming-Foundations-tutorials/Supporting-hashing/149042/177128-4.html)
        - [ ] [Language Support Hash Tables (영상)](https://www.lynda.com/Developer-Programming-Foundations-tutorials/Language-support-hash-tables/149042/177129-4.html)
        - [ ] [Core Hash Tables (영상)](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/m7UuP/core-hash-tables)
        - [ ] [자료구조 (영상)](https://www.coursera.org/learn/data-structures/home/week/3)
        - [ ] [전화번호부 문제 (영상)](https://www.coursera.org/learn/data-structures/lecture/NYZZP/phone-book-problem)
        - [ ] 분산 처리된(Distributed) 해쉬 테이블:
            - [Dropbox 에서 저장공간 최적화 및 즉각적인 업로드) (영상)](https://www.coursera.org/learn/data-structures/lecture/DvaIb/instant-uploads-and-storage-optimization-in-dropbox)
            - [분산 처리된 해쉬테이블 (video)](https://www.coursera.org/learn/data-structures/lecture/tvH8H/distributed-hash-tables)

    - [ ] 선형 탐색을 통한 배열로 구현
        - hash(k, m) - m 은 해쉬 테이블의 크기
        - add(key, value) - 만약 key 가 있다면, 값을 업데이트
        - exists(key) - key 가 있는지 확인
        - get(key) - key 에 대응된 값을 반환
        - remove(key) - key / value 값 제거

## 추가 자료 구조

- ### 이전 트리(Binary Tree)
    - [ ] [Binary Search (영상)](https://www.youtube.com/watch?v=D5SrAga1pno)
    - [ ] [Binary Search (영상)](https://www.khanacademy.org/computing/computer-science/algorithms/binary-search/a/binary-search)
    - [ ] [조금 더 자세히](https://www.topcoder.com/community/data-science/data-science-tutorials/binary-search/)
    - [ ] 구현:
        - binary search (정렬된 정수형 배열로)
        - binary search using recursion(재귀로 구현)

- ### 비트 연산
    - [ ] [비트 연산 치트 시트](https://github.com/jwasham/google-interview-university/blob/master/extras/cheat%20sheets/bits-cheat-cheet.pdf) - 너는 2의 승수에 관련된 값을 알고 있어야 한다. (2^1 부터 2^16 까지 그리고 2^32 값)
    - [ ] &(AND), | (OR), ^(XOR), ~(NOT), >> (Right shift), << (Left shift) 와 같은 비트 조작 연산을 이해하는 것은 중요하다.
        - [ ] [words](https://en.wikipedia.org/wiki/Word_(computer_architecture))
        - [ ] 소개 영상:
            [비트 조작 (영상)](https://www.youtube.com/watch?v=7jkIUgLC29I)
        - [ ] [C 프로그래밍 연습 2-10: 비트 연산 (영상)](https://www.youtube.com/watch?v=d0AwjSpNXR0)
        - [ ] [비트 조작](https://en.wikipedia.org/wiki/Bit_manipulation)
        - [ ] [비트 연산](https://en.wikipedia.org/wiki/Bitwise_operation)
        - [ ] [Bithacks](https://graphics.stanford.edu/~seander/bithacks.html)
        - [ ] [The Bit Twiddler - 컴퓨터 광](http://bits.stephan-brumme.com/)
        - [ ] [The Bit Twiddler Interactive](http://bits.stephan-brumme.com/interactive.html)
    - [ ] 1과 2의 보수
        - [이진: 더하기 & 빼기 (왜 2의 보수를 써야 하는가?) (영상)](https://www.youtube.com/watch?v=lKTsv6iVxV4)
        - [1의 보수](https://en.wikipedia.org/wiki/Ones%27_complement)
        - [2의 보수](https://en.wikipedia.org/wiki/Two%27s_complement)
    - [ ] bit 세기
        - [바이트 내에 bit 를 세는 4가지 방법(영상)](https://youtu.be/Hzuzo9NJrlc)
        - [비트 세기](https://graphics.stanford.edu/~seander/bithacks.html#CountBitsSetKernighan)
        - [32비트 정수에서 1로 설정된 비트의 개수 세기](http://stackoverflow.com/questions/109023/how-to-count-the-number-of-set-bits-in-a-32-bit-integer)
    - [ ] round to next power of 2:
        - [Round Up To Next Power Of Two](http://bits.stephan-brumme.com/roundUpToNextPowerOfTwo.html)
    - [ ] 값 교환:
        - [교환-Swap](http://bits.stephan-brumme.com/swap.html)
    - [ ] 절대값:
        - [절대값](http://bits.stephan-brumme.com/absInteger.html)

## 트리 - Tree

- ### 트리 - 노트 & 배경 지식
    - [ ] [트리 종류별 설명 (영상)](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/ovovP/core-trees)
    - [ ] [Series: Trees (video)](https://www.coursera.org/learn/data-structures/lecture/95qda/trees)
    - 기본 트리 생성
    - traversal(순방)
    - 조작 알고리즘(manipulation algorithms)
    - BFS (breadth-first search) 너비 우선 탐색
        - [MIT (영상)](https://www.youtube.com/watch?v=s-CYnVz-uh4&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=13)
        - level order (BFS, using queue)
            시간 복잡도: O(n)
            공간 복잡도: 최선: O(1), 최악: O(n/2)=O(n)
    - DFS (depth-first search) - 깊이 우선 탐색
        - [MIT (영상)](https://www.youtube.com/watch?v=AfSk24UTFS8&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=14)
        - notes:
            시간 복잡도: O(n)
            공간 복잡도:
                최선: O(log n) - 평균적으로 트리의 높이
                최악: O(n)
        - inorder (DFS: left, self, right) - 왼쪽 -> 자신 -> 오른쪽 노드 순으로 탐방
        - postorder (DFS: left, right, self) -> 왼쪽 -> 오른쪽 -> 자신 순으로
        - preorder (DFS: self, left, right) -> 자신 -> 왼쪽 -> 오른쪽

- ### 이진 탐색 트리: BSTs
    - [ ] [이진 탐색 트리 리뷰 (영상)](https://www.youtube.com/watch?v=x6At0nzX92o&index=1&list=PLA5Lqm4uh9Bbq-E0ZnqTIa8LRaL77ica6)
    - [ ] [Series (영상)](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/p82sw/core-introduction-to-binary-search-trees)
        - starts with symbol table and goes through BST applications
    - [ ] [소개 (영상)](https://www.coursera.org/learn/data-structures/lecture/E7cXP/introduction)
    - [ ] [MIT (영상)](https://www.youtube.com/watch?v=9Jry5-82I68)
    - C/C++:
        - [ ] [이진 탐색 트리 - C/C++ 로 구현 (영상)](https://www.youtube.com/watch?v=COZK7NATh4k&list=PL2_aWCzGMAwI3W_JlcBbtYTwiQSsOTa6P&index=28)
        - [ ] [BST 구현 - 스택과 힙에서 메모리 할당 ()](https://www.youtube.com/watch?v=hWokyBoo0aI&list=PL2_aWCzGMAwI3W_JlcBbtYTwiQSsOTa6P&index=29)
        - [ ] [이진 트리에서 min/max 요소 찾기 (영상)](https://www.youtube.com/watch?v=Ut90klNN264&index=30&list=PL2_aWCzGMAwI3W_JlcBbtYTwiQSsOTa6P)
        - [ ] [이진 트리의 높이 찾기 (영상)](https://www.youtube.com/watch?v=_pnqMz5nrRs&list=PL2_aWCzGMAwI3W_JlcBbtYTwiQSsOTa6P&index=31)
        - [ ] [이진 트리 탐방 - breadth-first(너비 우선) and depth-first(깊이 우선) 전략 (영상)](https://www.youtube.com/watch?v=9RHO6jU--GU&list=PL2_aWCzGMAwI3W_JlcBbtYTwiQSsOTa6P&index=32)
        - [ ] [이진 트리: Level Order Traversal (영상)](https://www.youtube.com/watch?v=86g8jAQug04&index=33&list=PL2_aWCzGMAwI3W_JlcBbtYTwiQSsOTa6P)
        - [ ] [이진 트리 순방: Preorder, Inorder, Postorder (영상)](https://www.youtube.com/watch?v=gm8DUJJhmY4&index=34&list=PL2_aWCzGMAwI3W_JlcBbtYTwiQSsOTa6P)
        - [ ] [이진 트리가 맞는지 아닌지 확인 (영상)](https://www.youtube.com/watch?v=yEwSGhSsT0U&index=35&list=PL2_aWCzGMAwI3W_JlcBbtYTwiQSsOTa6P)
        - [ ] [이진트리에서 노느 삭제 (영상)](https://www.youtube.com/watch?v=gcULXE7ViZw&list=PL2_aWCzGMAwI3W_JlcBbtYTwiQSsOTa6P&index=36)
        - [ ] [Inorder Successor in a binary search tree (영상)](https://www.youtube.com/watch?v=5cPbNCrdotA&index=37&list=PL2_aWCzGMAwI3W_JlcBbtYTwiQSsOTa6P)
    - [ ] 구현:
        - [ ] insert    // 트리에 값 삽입
        - [ ] get_node_count // 값이 저장된 개수 반환
        - [ ] print_values // 제일 작은 값에서 큰 값의 순서대로 트리에 있는 모든 값 출력
        - [ ] delete_tree // 트리 지우기
        - [ ] is_in_tree // 트리에 주어진 값이 있는지 확인(있으면 true)
        - [ ] get_height // 트리의 높이 확인 (노드가 하나 있는 트리는 높이가 1임)
        - [ ] get_min   // 트리에 저장된 제일 작은 값 반환
        - [ ] get_max   // 트리에 저장된 가장 큰 값 반환
        - [ ] is_binary_search_tree // 이진 트리인지 아닌지
        - [ ] delete_value // 값 삭제
        - [ ] get_successor // 트리에 주어진 값보다 다음으로 가장 높은 값을 전달, 없으면 -1

- ### 힙 / 우선순위 큐 / 이진 힙
    - 트리의 형태로 보여질 것이나 실제로 저장될 때는 연결 리스트나 배열인 선형적으로 저장됨.
    - [ ] [힙](https://en.wikipedia.org/wiki/Heap_(data_structure))
    - [ ] [소개 (영상)](https://www.coursera.org/learn/data-structures/lecture/2OpTs/introduction)
    - [ ] [곧이 곧대로 구현 (영상)](https://www.coursera.org/learn/data-structures/lecture/z3l9N/naive-implementations)
    - [ ] [이진 트리 (영상)](https://www.coursera.org/learn/data-structures/lecture/GRV2q/binary-trees)
    - [ ] [트리 높이에 주목 (영상)](https://www.coursera.org/learn/data-structures/supplement/S5xxz/tree-height-remark)
    - [ ] [기본 연산 (영상)](https://www.coursera.org/learn/data-structures/lecture/0g1dl/basic-operations)
    - [ ] [Complete Binary Trees(이진 트리) (영상)](https://www.coursera.org/learn/data-structures/lecture/gl5Ni/complete-binary-trees)
    - [ ] [의사코드 (영상)](https://www.coursera.org/learn/data-structures/lecture/HxQo9/pseudocode)
    - [ ] [힙 정렬 - 시작하기 (영상)](https://youtu.be/odNJmw5TOEE?list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&t=3291)
    - [ ] [힙 정렬 (영상)](https://www.coursera.org/learn/data-structures/lecture/hSzMO/heap-sort)
    - [ ] [힙 만들기 (영상)](https://www.coursera.org/learn/data-structures/lecture/dwrOS/building-a-heap)
    - [ ] [MIT: 힙 과 힙정렬 (영상)](https://www.youtube.com/watch?v=B7hVxCmfPtM&index=4&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb)
    - [ ] [CS 61B Lecture 24: 우선 순위 큐 (영상)](https://www.youtube.com/watch?v=yIUFT6AKBGE&index=24&list=PL4BBB74C7D2A1049C)
    - [ ] [선형 시간 힙 생성 - Linear Time BuildHeap (최대 힙)](https://www.youtube.com/watch?v=MiyLo8adrWw)
    - [ ] 최대 힙 구현:
        - [ ] insert - 노드 추가
        - [ ] sift_up - 추가 할때 사용
        - [ ] get_max - 가장 큰 값 반환, 노드 제거 안함
        - [ ] get_size() - 노드 개수 반환
        - [ ] is_empty() - 힙 트리가 비어있는지 확인
        - [ ] extract_max - 가장 큰 값 반환 및 제거
        - [ ] sift_down - 제거할 때 사용
        - [ ] remove(i) - 인덱스 i 에 있는 노드 삭제
        - [ ] heapify - 배열의 요소를 가지고 힙을 만든다, heap_sort 에 필요함
        - [ ] heap_sort() - 정렬되지 않는 배열을 인자로 받아 최대 힙을 사용하여 정렬된 배열로 만들어 준다.
            - 노트 : 저장 하는 과정 대신에 최소 힙이 사용될 수 있는데, 공간이 배로 늘어간다.(in-place 로 할 수 없음)

## 정렬

- [ ] 노트:
    - 정렬을 구현 & best/worst 그리고 평균적인 복잡도를 알아본다:
        - 버블 정렬은 안함 - O(n^2), n 이 16 보다 작은 경우를 제외 함
    - [ ] 정렬 알고리즘의 안정성(stability in sorting algorithms ("퀵 정렬은 안정적이야?"))
        - 참고: 안정적이라 하면, 복잡도가 best/worst 그리고 평균적인 것이 차이가 많이 안난다는 얘기인듯.
        - [정렬 알고리즘의 안정성](https://en.wikipedia.org/wiki/Sorting_algorithm#Stability)
        - [정렬 알고리즘의 안정성](http://stackoverflow.com/questions/1517793/stability-in-sorting-algorithms)
        - [정렬 알고리즘의 안정성](http://www.geeksforgeeks.org/stability-in-sorting-algorithms/)
        - [정렬 알고리즘 - 안정성](http://homepages.math.uic.edu/~leon/cs-mcs401-s08/handouts/stability.pdf)
    - [ ] 연결리스트를 사용하는 알고리즘은 뭔지? 배열은? 아님 둘다?
        - 나는 정렬을 연결 리스트로 구현하는 것은 추천하지 않지만, 병합정렬은 가능하다고 봐
        - [연결리스트로 구현한 병합정렬](http://www.geeksforgeeks.org/merge-sort-for-linked-list/)

- For heapsort, see Heap data structure above. Heap sort is great, but not stable.
- 힙 정렬을 위해서는 위에서 언급한 힙 자료 구조에서 설명했어. 힙정렬 정말 좋지만 안정적으로 하진 못해.

- [ ] [Sedgewick - 병합정렬 (5 영상)](https://www.youtube.com/watch?v=4nKwesx_c8E&list=PLe-ggMe31CTeunC6GZHFBmQx7EKtjbGf9)
    - [ ] [1. Mergesort 병합정렬](https://www.youtube.com/watch?v=4nKwesx_c8E&list=PLe-ggMe31CTeunC6GZHFBmQx7EKtjbGf9&index=1)
    - [ ] [2. Bottom up Mergesort](https://www.youtube.com/watch?v=HGOIGUYjeyk&list=PLe-ggMe31CTeunC6GZHFBmQx7EKtjbGf9&index=2)
    - [ ] [3. Sorting Complexity 정렬 복잡도](https://www.youtube.com/watch?v=WvU_mIWo0Ac&index=3&list=PLe-ggMe31CTeunC6GZHFBmQx7EKtjbGf9)
    - [ ] [4. Comparators 비교](https://www.youtube.com/watch?v=7MvC1kmBza0&index=4&list=PLe-ggMe31CTeunC6GZHFBmQx7EKtjbGf9)
    - [ ] [5. Stability 안정성](https://www.youtube.com/watch?v=XD_5iINB5GI&index=5&list=PLe-ggMe31CTeunC6GZHFBmQx7EKtjbGf9)

- [ ] [Sedgewick - 퀵 정렬 (4 videos)](https://www.youtube.com/playlist?list=PLe-ggMe31CTeE3x2-nF1-toca1QpuXwE1)
    - [ ] [1. Quicksort 퀵 정렬](https://www.youtube.com/watch?v=5M5A7qPWk84&index=1&list=PLe-ggMe31CTeE3x2-nF1-toca1QpuXwE1)
    - [ ] [2. Selection 선택](https://www.youtube.com/watch?v=CgVYfSyct_M&index=2&list=PLe-ggMe31CTeE3x2-nF1-toca1QpuXwE1)
    - [ ] [3. Duplicate Keys 중복 키](https://www.youtube.com/watch?v=WBFzOYJ5ybM&index=3&list=PLe-ggMe31CTeE3x2-nF1-toca1QpuXwE1)
    - [ ] [4. System Sorts 시스템 정렬](https://www.youtube.com/watch?v=rejpZ2htBjE&index=4&list=PLe-ggMe31CTeE3x2-nF1-toca1QpuXwE1)

- [ ] UC Berkeley:
    - [ ] [CS 61B Lecture 29: Sorting I 정렬 1(영상)](https://www.youtube.com/watch?v=EiUvYS2DT6I&list=PL4BBB74C7D2A1049C&index=29)
    - [ ] [CS 61B Lecture 30: Sorting II 정렬 2(영상)](https://www.youtube.com/watch?v=2hTY3t80Qsk&list=PL4BBB74C7D2A1049C&index=30)
    - [ ] [CS 61B Lecture 32: Sorting III 정렬 3(영상)](https://www.youtube.com/watch?v=Y6LOLpxg6Dc&index=32&list=PL4BBB74C7D2A1049C)
    - [ ] [CS 61B Lecture 33: Sorting V 정렬 4(영상)](https://www.youtube.com/watch?v=qNMQ4ly43p4&index=33&list=PL4BBB74C7D2A1049C)

- [ ] [버블 정렬 (영상)](https://www.youtube.com/watch?v=P00xJgWzz2c&index=1&list=PL89B61F78B552C1AB)
- [ ] [버블 정렬 분석 (영상)](https://www.youtube.com/watch?v=ni_zk257Nqo&index=7&list=PL89B61F78B552C1AB)
- [ ] [삽입 정렬, 병합 정렬 (영상)](https://www.youtube.com/watch?v=Kg4bqzAqRBM&index=3&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb)
- [ ] [삽입 정렬 (영상)](https://www.youtube.com/watch?v=c4BRHC7kTaQ&index=2&list=PL89B61F78B552C1AB)
- [ ] [병합 정렬 (영상)](https://www.youtube.com/watch?v=GCae1WNvnZM&index=3&list=PL89B61F78B552C1AB)
- [ ] [퀵 정렬 (영상)](https://www.youtube.com/watch?v=y_G9BkAm6B8&index=4&list=PL89B61F78B552C1AB)
- [ ] [선택 정렬 (영상)](https://www.youtube.com/watch?v=6nDMgr0-Yyo&index=8&list=PL89B61F78B552C1AB)

- [ ] 병합 정렬 코드:
    - [ ] [추가 배열 이용 (C)](http://www.cs.yale.edu/homes/aspnes/classes/223/examples/sorting/mergesort.c)
    - [ ] [추가 배열 이용 (Python)](https://github.com/jwasham/practice-python/blob/master/merge_sort/merge_sort.py)
    - [ ] [배열 없이 (C++)](https://github.com/jwasham/practice-cpp/blob/master/merge_sort/merge_sort.cc)
- [ ] 퀵 정렬 코드:
    - [ ] [구현 (C)](http://www.cs.yale.edu/homes/aspnes/classes/223/examples/randomization/quick.c)
    - [ ] [구현 (C)](https://github.com/jwasham/practice-c/blob/master/quick_sort/quick_sort.c)
    - [ ] [구현 (Python)](https://github.com/jwasham/practice-python/blob/master/quick_sort/quick_sort.py)

- [ ] 구현:
    - [ ] 병합 정렬: O(n log n) 평균/최악
    - [ ] 퀵 정렬: O(n log n) 평균
    - 선택 정렬과 삽입 정렬은 모두 평균/최악으 경우 O(n^2) 임.
    - 힙 정렬은, 앞서 설명한 힙 자료 구조에서 살펴봐

- [ ] 필수는 아니지만, 내가 추천하는 것들임: Radix 정렬 관련이고 번역이 애매해서 냅둠
    - [ ] [Sedgewick - Radix Sorts (6 영상)](https://www.youtube.com/playlist?list=PLe-ggMe31CTcNvUX9E3tQeM6ntrdR8e53)
        - [ ] [1. Strings in Java](https://www.youtube.com/watch?v=zRzU-FWsjNU&list=PLe-ggMe31CTcNvUX9E3tQeM6ntrdR8e53&index=6)
        - [ ] [2. Key Indexed Counting](https://www.youtube.com/watch?v=CtgKYmXs62w&list=PLe-ggMe31CTcNvUX9E3tQeM6ntrdR8e53&index=5)
        - [ ] [3. Least Significant Digit First String Radix Sort](https://www.youtube.com/watch?v=2pGVq_BwPKs&list=PLe-ggMe31CTcNvUX9E3tQeM6ntrdR8e53&index=4)
        - [ ] [4. Most Significant Digit First String Radix Sort](https://www.youtube.com/watch?v=M3cYNY90R6c&index=3&list=PLe-ggMe31CTcNvUX9E3tQeM6ntrdR8e53)
        - [ ] [5. 3 Way Radix Quicksort](https://www.youtube.com/watch?v=YVl58kfE6i8&index=2&list=PLe-ggMe31CTcNvUX9E3tQeM6ntrdR8e53)
        - [ ] [6. Suffix Arrays](https://www.youtube.com/watch?v=HKPrVm5FWvg&list=PLe-ggMe31CTcNvUX9E3tQeM6ntrdR8e53&index=1)
    - [ ] [Radix Sort](http://www.cs.yale.edu/homes/aspnes/classes/223/notes.html#radixSort)
    - [ ] [Radix Sort (video)](https://www.youtube.com/watch?v=xhr26ia4k38)
    - [ ] [Radix Sort, Counting Sort (linear time given constraints) (video)](https://www.youtube.com/watch?v=Nz1KZXbghj8&index=7&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb)
    - [ ] [Randomization: Matrix Multiply, Quicksort, Freivalds' algorithm (video)](https://www.youtube.com/watch?v=cNB2lADK3_s&index=8&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp)
    - [ ] [Sorting in Linear Time (video)](https://www.youtube.com/watch?v=pOKy3RZbSws&list=PLUl4u3cNGP61hsJNdULdudlRL493b-XZf&index=14)

만약 당신이 이 주제에 대해 더 자세히 알고 싶다면 [Additional Detail on Some Subjects](#additional-detail-on-some-subjects) 에서 정렬 부분을 참조.

## 그래프

그래프는 컴퓨터 과학에서 많은 문제들을 표현할 수 있다. 그래서 그래프 섹션은 좀 많다.

- Yegge가 노트:
    - 그래프가 메모리에 표현되는 기본 3가지 방법:
        - objects and pointers 객체 및 포인터
        - matrix 매트릭스
        - adjacency list 근접 리스트
    - 위의 각 표현 및 장/단점에 익숙해질 때 까지 알아보고 연습해야 한다.
    - 너비 우선 탐색(BFS) 와 깊이 우선 탐색(DFS) - 각 계산 복잡도와 상충관계(tradeoffs) 그리고 실제 어떻게 구현하는지 알아두자
    - 알고리즘 문제를 볼때, 제일 먼저 그래프 기반의 해결책을 생각해보자, 아니면 다른 방법으로 넘어가고

- [ ] Skiena Lectures - 훌륭한 인트로:
    - [ ] [CSE373 2012 - Lecture 11 - 그래프 자료 구조 (영상)](https://www.youtube.com/watch?v=OiXxhDrFruw&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b&index=11)
    - [ ] [CSE373 2012 - Lecture 12 - Breadth-First Search 너비 우선 탐색 (영상)](https://www.youtube.com/watch?v=g5vF8jscteo&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b&index=12)
    - [ ] [CSE373 2012 - Lecture 13 - 그래프 알고리즘 (영상)](https://www.youtube.com/watch?v=S23W6eTcqdY&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b&index=13)
    - [ ] [CSE373 2012 - Lecture 14 - 그래프 알고리즘 (계속) (영상)](https://www.youtube.com/watch?v=WitPBKGV0HY&index=14&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b)
    - [ ] [CSE373 2012 - Lecture 15 - 그래프 알고리즘 (계속) (영상)](https://www.youtube.com/watch?v=ia1L30l7OIg&index=15&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b)
    - [ ] [CSE373 2012 - Lecture 16 - 그래프 알고리즘 (계속) (영상)](https://www.youtube.com/watch?v=jgDOQq6iWy8&index=16&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b)

- [ ] 그래프 (더 살펴보기):

    - [ ] [6.006 단순 최단 경로 (video)](https://www.youtube.com/watch?v=Aa2sqUhIn-E&index=15&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb)
    - [ ] [6.006 Dijkstra 다익스트라 (영상)](https://www.youtube.com/watch?v=2E7MmKv0Y24&index=16&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb)
    - [ ] [6.006 Bellman-Ford 벨만-포드(영상)](https://www.youtube.com/watch?v=ozsuci5pIso&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=17)
    - [ ] [6.006 다익스트라 속도 높이기 (영상)](https://www.youtube.com/watch?v=CHvQ3q_gJ7E&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=18)
    - [ ] [Aduni: 그래프 알고리즘 I - 위상(Topology) 정렬, 최소 스패닝 트리, 프림 알고리즘 -  강좌 6 (영상)]( https://www.youtube.com/watch?v=i_AQT_XfvD8&index=6&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm)
    - [ ] [Aduni: 그래프 알고리즘 II - DFS, BFS, 크러스컬 알고리즘, 서로소(Union Find) 자료구조 - 강좌 7 (영상)]( https://www.youtube.com/watch?v=ufj5_bppBsA&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&index=7)
    - [ ] [Aduni: 그래프 알고리즘 III: 최단 경로 - 강좌 8 (영상)](https://www.youtube.com/watch?v=DiedsPsMKXc&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&index=8)
    - [ ] [Aduni: 그래프 알고리즘 IV: 기하학 알고리즘 소개(geometric algorithms) - 강좌 9 (영상)](https://www.youtube.com/watch?v=XIAQRlNkJAw&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&index=9)
    - [ ] [CS 61B 2014 (starting at 58:09) (video)](https://youtu.be/dgjX4HdMI-Q?list=PL-XXv-cvA_iAlnI-BQr9hjqADPBtujFJd&t=3489)
    - [ ] [CS 61B 2014: 가중 그래프(Weighted graphs) (영상)](https://www.youtube.com/watch?v=aJjlQCFwylA&list=PL-XXv-cvA_iAlnI-BQr9hjqADPBtujFJd&index=19)
    - [ ] [그리디(Greedy Algorithms): 최소 스패닝 트리(Minimum Spanning Tree) (영상)](https://www.youtube.com/watch?v=tKwnms5iRBU&index=16&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp)
    - [ ] [Strongly Connected Components Kosaraju's Algorithm 그래프 알고리즘 (영상)](https://www.youtube.com/watch?v=RpgcYiky7uw)

- Full Coursera Course:
    - [ ] [그래프 알고리즘 (영상)](https://www.coursera.org/learn/algorithms-on-graphs/home/welcome)

- Yegge: 만약 기회가 있다면, 고급 알고리즘을 배워보라:
    - [ ] Dijkstra's algorithm 다익스트라 알고리즘 - 위에 - 6.006
    - [ ] A*
        - [ ] [A 정렬 알고리즘](https://en.wikipedia.org/wiki/A*_search_algorithm)
        - [ ] [A* 길찾기 기초 (영상)](https://www.youtube.com/watch?v=KNXfSOx4eEE)
        - [ ] [A* 길찾기 (E01: 알고리즘 설명) (영상)](https://www.youtube.com/watch?v=-L-WgKMFuhE)

- 구현:
    - [ ] DFS : adjacency list(인접리스트 + 재귀)
    - [ ] DFS : adjacency list(인접리스트 + 반복문 + 스택)
    - [ ] DFS : adjacency matrix(인접 매트릭스 + 재귀)
    - [ ] DFS : adjacency matrix(인접 매트릭스 + 반복문 + 스택)
    - [ ] BFS : adjacency list(인접리스트)
    - [ ] BFS : adjacency matrix(인접 매트릭스)
    - [ ] single-source shortest path 단순 최단 경로(다익스트라)
    - [ ] minimum spanning tree 최소 스패닝 트리
    - DFS-기반 알고리즘 (위의 Aduni 영상 참조):
        - [ ] 사이클 확인 check for cycle (위상(Topology) 정렬이 요구)
        - [ ] topological sort 위상 정렬
        - [ ] count connected components in a graph 그래프에서 요소들의 연결 개수
        - [ ] list strongly connected components
        - [ ] check for bipartite graph 이단(?) 그래프 확인

당신이 그래프 연습을 조금더 할 고 싶다면, 문서의 Skiena "책" 섹션을 참조해서 보도록 하자

## 더 많은 지식

- ### 재귀
    - [ ] 재귀 및 역추적(backtracking)에 대한 스탠포드 강의:
        - [ ] [Lecture 8 | 프로그래밍 추상화 (영상)](https://www.youtube.com/watch?v=gl3emqCuueQ&list=PLFE6E58F856038C69&index=8)
        - [ ] [Lecture 9 | 프로그래밍 추상화 (영상)](https://www.youtube.com/watch?v=uFJhEPrbycQ&list=PLFE6E58F856038C69&index=9)
        - [ ] [Lecture 10 | 프로그래밍 추상화 (영상)](https://www.youtube.com/watch?v=NdF1QDTRkck&index=10&list=PLFE6E58F856038C69)
        - [ ] [Lecture 11 | 프로그래밍 추상화 (영상)](https://www.youtube.com/watch?v=p-gpaIGRCQI&list=PLFE6E58F856038C69&index=11)
    - 이것을 언제 사용해야 적절한가?
    - 꼬리(tail) 재귀를 사용할 때와 아닐 때는 어떤게 더 나아?
        - [ ] [꼬리 재귀(Tail Recursion) 은 뭐고, 왜 나쁜가?](https://www.quora.com/What-is-tail-recursion-Why-is-it-so-bad)
        - [ ] [꼬리 재귀 (영상)](https://www.youtube.com/watch?v=L1jjXGfxozc)

- ### 객체지향적 프로그래밍
    - [ ] [선택: UML 2.0 시리즈 (video)](https://www.youtube.com/watch?v=OkC7HKtiZC0&list=PLGLfVvz_LVvQ5G-LdJ8RLqe-ndo7QITYc)
    - [ ] 객체 지향 소프트웨어 엔지리어링: UML과 자바로 소프트웨어 개발(21 영상들):
        - 만약 당신이 객체지향과 객체지향 디자인에 대해 잘 알고 있다면 그냥 넘어가도록 하자.
        - [OOSE:  UML과 자바로 소프트웨어 개발](https://www.youtube.com/playlist?list=PLJ9pm_Rc9HesnkwKlal_buSIHA-jTZMpO)
    - [ ] SOLID OOP Principles(SOLID 객체지향 프로그래밍 원칙):
        - [ ] [S.O.L.I.D 원칙-한글](https://ko.wikipedia.org/wiki/SOLID)
        - [ ] [Bob Martin(밥 마틴) 객체지향의 원칙과 애자일 디자인 (영상)](https://www.youtube.com/watch?v=TMuno5RZNeE)
        - [ ] [SOLID C# 디자인 패턴 (영상)](https://www.youtube.com/playlist?list=PL8m4NUhTQU48oiGCSgCP1FiJEcg_xJzyQ)
        - [ ] [SOLID 원칙 (영상)](https://www.youtube.com/playlist?list=PL4CE9F710017EA77A)
        - [ ] S - [Single Responsibility Principle 단일 책임 원칙](http://www.oodesign.com/single-responsibility-principle.html) | [Single responsibility to each Object 각 객체에 대한 단일 책임](http://www.javacodegeeks.com/2011/11/solid-single-responsibility-principle.html)
            - [더 많은 내용](https://docs.google.com/open?id=0ByOwmqah_nuGNHEtcU5OekdDMkk)
        - [ ] O - [Open/Closed Principal 개방/폐쇄 원칙](http://www.oodesign.com/open-close-principle.html)  | [On production level Objects are ready for extension for not for modification 확장에는 열려 있으나 변경에는 닫혀 있어야 한다](https://en.wikipedia.org/wiki/Open/closed_principle)
            - [더 많은 내용](http://docs.google.com/a/cleancoder.com/viewer?a=v&pid=explorer&chrome=true&srcid=0BwhCYaYDn8EgN2M5MTkwM2EtNWFkZC00ZTI3LWFjZTUtNTFhZGZiYmUzODc1&hl=en)
        - [ ] L - [Liskov Substitution Principal 리스코프 치환 원칙](http://www.oodesign.com/liskov-s-substitution-principle.html) | [Base Class and Derived class follow ‘IS A’ principal 프로그램의 정확성을 깨지 않않으면서 하위 타입의 인스턴스로 바꿀수 있어야 한다는 원칙](http://stackoverflow.com/questions/56860/what-is-the-liskov-substitution-principle)
            - [더 많은 내용](http://docs.google.com/a/cleancoder.com/viewer?a=v&pid=explorer&chrome=true&srcid=0BwhCYaYDn8EgNzAzZjA5ZmItNjU3NS00MzQ5LTkwYjMtMDJhNDU5ZTM0MTlh&hl=en)
        - [ ] I - [Interface segregation principle 인터페이스 분리 원칙](http://www.oodesign.com/interface-segregation-principle.html) | clients should not be forced to implement interfaces they don't use 특정 클라이언트를 위한 인터페이스 여러 개가 범용 인터페이스 하나 보다 낫다.
            - [5분만에 인터페이스 분리 원칙 보기(영상)](https://www.youtube.com/watch?v=3CtAfl7aXAQ)
            - [더 많은 내용](http://docs.google.com/a/cleancoder.com/viewer?a=v&pid=explorer&chrome=true&srcid=0BwhCYaYDn8EgOTViYjJhYzMtMzYxMC00MzFjLWJjMzYtOGJiMDc5N2JkYmJi&hl=en)
        - [ ] D -[Dependency Inversion principle 의존관계 역전 원칙](http://www.oodesign.com/dependency-inversion-principle.html) | Reduce the dependency In composition of objects. 구체화에 의존하기 보다 추상화에 의존.
            - [왜 의존관계 역전인지, 왜 중요한지 알아보자](http://stackoverflow.com/questions/62539/what-is-the-dependency-inversion-principle-and-why-is-it-important)
            - [더 많은 자료](http://docs.google.com/a/cleancoder.com/viewer?a=v&pid=explorer&chrome=true&srcid=0BwhCYaYDn8EgMjdlMWIzNGUtZTQ0NC00ZjQ5LTkwYzQtZjRhMDRlNTQ3ZGMz&hl=en)

- ### 디자인 패턴
    - [ ] [빠르게 UML 리뷰(영상)](https://www.youtube.com/watch?v=3cmzqZzwNDM&list=PLGLfVvz_LVvQ5G-LdJ8RLqe-ndo7QITYc&index=3)
    - [ ] 패턴들(굳이 번역을 하지 않음):
        - [한글 참조 블로그](http://wiki.gurubee.net/pages/viewpage.action?pageId=1507372)
        - [JAVA 한글 참조 블로그-링크모음](http://sdw8001.tistory.com/122) 코드와 설명이 간결함.
        - [ ] strategy
        - [ ] singleton
        - [ ] adapter
        - [ ] prototype
        - [ ] decorator
        - [ ] visitor
        - [ ] factory, abstract factory
        - [ ] facade
        - [ ] observer
        - [ ] proxy
        - [ ] delegate
        - [ ] command
        - [ ] state
        - [ ] memento
        - [ ] iterator
        - [ ] composite
        - [ ] flyweight
    - [ ] [Chapter 6 (Part 1) - 패턴들 (영상)](https://youtu.be/LAP2A80Ajrg?list=PLJ9pm_Rc9HesnkwKlal_buSIHA-jTZMpO&t=3344)
    - [ ] [Chapter 6 (Part 2) - Abstraction-Occurrence, General Hierarchy, Player-Role, Singleton , Observer , Delegation (영상)](https://www.youtube.com/watch?v=U8-PGsjvZc4&index=12&list=PLJ9pm_Rc9HesnkwKlal_buSIHA-jTZMpO)
    - [ ] [Chapter 6 (Part 3) - Adapter, Facade, Immutable, Read-Only Interface, Proxy (video)](https://www.youtube.com/watch?v=7sduBHuex4c&index=13&list=PLJ9pm_Rc9HesnkwKlal_buSIHA-jTZMpO)
    - [ ] [관련 영상 리스트 (27 영상)](https://www.youtube.com/playlist?list=PLF206E906175C7E07)
    - [ ] [Head First Design Patterns](https://www.amazon.com/Head-First-Design-Patterns-Freeman/dp/0596007124)
          [번역판-Head First Design Patterns](http://book.naver.com/bookdb/book_detail.nhn?bid=1882446)
        - 정식으로는 "Design Patterns: Elements of Reusable Object-Oriented Software" 책이지만, Head First 는 초보자에게 정말 좋은 책
    - [ ] [간편 참조: 101가지 디자인 패턴과 개발자를 위한 팁](https://sourcemaking.com/design-patterns-and-tips)

- ### 조합(n 개중에 k) 와 확률
    - [ ] [수학 스킬: 팩토리얼/순열(Permutation)/조합을 찾는 방법 (영상)](https://www.youtube.com/watch?v=8RRo6Ti9d0U)
    - [ ] [Make School: 확률 (영상)](https://www.youtube.com/watch?v=sZkAAk9Wwa4)
    - [ ] [Make School: 확률과 마트로브 연쇄 (영상)](https://www.youtube.com/watch?v=dNaJg-mLobQ)
    - [ ] 칸 아카데미:
        - [한글 칸아카데미 접근](https://ko.khanacademy.org/)
        - 기본 코스:
            - [ ] [이론적 확률 기초](https://www.khanacademy.org/math/probability/probability-and-combinatorics-topic)
        - 영상들 - 41 (각각은 간단하다.):
            - [ ] [확률 설명 (영상)](https://www.youtube.com/watch?v=uzkc-qNVoOk&list=PLC58778F28211FA19)

- ### NP, NP-Complete 과 근사 알고리즘
    - [NP, NP-complete 위키](https://namu.wiki/w/P-NP%20%EB%AC%B8%EC%A0%9C)
    - NP-Complete 문제에서 가장 유명한 외판원/배낭 문제를 알아두면 좋다.
    - [ ] [계산 복잡성 (영상)](https://www.youtube.com/watch?v=moPtwq_cVH8&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=23)
    - [ ] Simonson:
        - [ ] [그리디 알고리즘 II & NP Completeness 기초 (영상)](https://youtu.be/qcGnJ47Smlo?list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&t=2939)
        - [ ] [NP Completeness II & Reductions (영상)](https://www.youtube.com/watch?v=e0tGC6ZQdQE&index=16&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm)
        - [ ] [NP Completeness III (영상)](https://www.youtube.com/watch?v=fCX1BGT3wjE&index=17&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm)
        - [ ] [NP Completeness IV (영상)](https://www.youtube.com/watch?v=NKLDp3Rch3M&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&index=18)
    - [ ] Skiena:
        - [ ] [CSE373 2012 - Lecture 23 - NP-Completeness 소개 (영상)](https://youtu.be/KiK5TVgXbFg?list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b&t=1508)
        - [ ] [CSE373 2012 - Lecture 24 - NP-Completeness 증명 (영상)](https://www.youtube.com/watch?v=27Al52X3hd4&index=24&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b)
        - [ ] [CSE373 2012 - Lecture 25 - NP-Completeness 도전 (영상)](https://www.youtube.com/watch?v=xCPH4gwIIXM&index=25&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b)
    - [ ] [복잡도: P, NP, NP-completeness, Reductions (영상)](https://www.youtube.com/watch?v=eHZifpgyH_4&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=22)
    - [ ] [Complexity: 근접 알고리즘 (영상)](https://www.youtube.com/watch?v=MEz1J9wY2iM&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=24)
    - [ ] [Complexity: Fixed-Parameter Algorithms 고정 매개변수 알고리즘 (영상)](https://www.youtube.com/watch?v=4q-jmGrmxKs&index=25&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp)
    - 피터 노르빅(Peter Norvig) 은 외판원 문제에 대한 근접 최적 해법을 논의했다:
        - [Jupyter 노트](http://nbviewer.jupyter.org/url/norvig.com/ipython/TSP.ipynb)
    - 페이지 1048 - CLRS 는 1140(Introduction to Algorithms)

- ### 캐쉬
    - [ ] LRU 캐쉬:
        - [ ] [LRU 캐쉬의 마법 (100 Days of Google Dev) (영상)](https://www.youtube.com/watch?v=R5ON3iwx78M)
        - [ ] [LRU 구현 (영상)](https://www.youtube.com/watch?v=bq6N7Ym81iI)
        - [ ] [LeetCode - 146 LRU 캐쉬 (C++) (video)](https://www.youtube.com/watch?v=8-FZRAjR7qU)
    - [ ] CPU 캐쉬:
        - [ ] [MIT 6.004 L15: 메모리 계층 구조 (영상)](https://www.youtube.com/watch?v=vjYF_fAZI5E&list=PLrRW1w6CGAcXbMtDFj205vALOGmiRc82-&index=24)
        - [ ] [MIT 6.004 L16: 캐쉬 문제 (영상)](https://www.youtube.com/watch?v=ajgC3-pyGlk&index=25&list=PLrRW1w6CGAcXbMtDFj205vALOGmiRc82-)

- ### 프로세스와 쓰레드
    - [ ] 컴퓨터 과학 162 - 운영체제 (25 영상):
        - 아래 링크에서 프로세스와 쓰레드 관련된 영상은 영상 1에서 11까지임
        - [운영체제와 시스템 프로그래밍 (영상)](https://www.youtube.com/playlist?list=PL-XXv-cvA_iBDyz-ba4yDskqMDY6A1w_c)
    - [프로세스 A와 쓰레드 A는 무엇이 다른가?](https://www.quora.com/What-is-the-difference-between-a-process-and-a-thread)
    - 관련 내용:
        - 프로세트, 쓰레드, 동시성(Concurrency) 문제
            - difference between processes and threads (프로세스와 쓰레드의 차이점)
            - processes (프로세스)
            - threads (쓰레드)
            - locks (락)
            - mutexes (뮤텍스)
            - semaphores (세마포어)
            - monitors (모니터)
            - how they work (위의 것들이 어떻게 동작하니?)
            - deadlock (교착상태)
            - livelock (레이스 컨디션?)
        - CPU 활동, 인터럽트, 문맥교환(context switching)
        - 최근 멀티코어 프로세스와 함께 동시성(concurrency)를 봐야함.
        - 프로세스 자원 요구 (메모리: 코드, 정적 저장소, 스택, 힙과 파일 디스크립터, I/O)
        - Thread resource needs (shares above (minus stack) with other threads in the same process but each has its own pc, stack counter, registers, and stack)
        - 쓰레드 자원 요구 (프로세스에서 요구하는 자원 중 스택을 제외한 나머지는 다른 쓰레드(같은 프로세스 내에 있는)와 공유, 하지만 쓰레드 각각은 PC(program counter), SP(Stack pointer), 레지스터, 스택)
        - 프로세스 forking(생성)은 새로운 프로세스가 메모리에 쓰기하기 전까지는 COW(copy-on-write) 정책을 통해 메모리를 공유한다. 쓰기를 한다면 모든 메모리를 새로운 프로세스를 위해 복사 한다.
        - 문맥 교환(Context switching)
            - H/W 와 함께 운영체제에 의해 문맥교환(context switching)이 어떻게 일어나는지 파악
    - [ ] [C++ 쓰레드 (시리즈 - 10 영상들)](https://www.youtube.com/playlist?list=PL5jc9xFGsL8E12so1wlMS0r0hTQoJL74M)
    - [ ] 파이썬에서 동시성(concurrency) (영상):
        - [ ] [쓰레드에 대한 짧은 시리즈들](https://www.youtube.com/playlist?list=PL1H1sBF1VAKVMONJWJkmUh6_p8g4F2oy1)
        - [ ] [파이썬 쓰레드](https://www.youtube.com/watch?v=Bs7vPNbB9JM)
        - [ ] [파이썬 GIL 의 이해(2010)](https://www.youtube.com/watch?v=Obt-vMVdM8s)
            - [참고](http://www.dabeaz.com/GIL)
        - [ ] [David Beazley - 처음으로 접하는 파이썬 병렬성(Concurrency): LIVE! - PyCon 2015](https://www.youtube.com/watch?v=MCs5OvhV9S4)
        - [ ] [Keynote David Beazley - 재미있는 주제 (Python Asyncio)](https://www.youtube.com/watch?v=ZzfHjytDceU)
        - [ ] [파이썬 뮤텍스](https://www.youtube.com/watch?v=0zaPs8OtyKY)

- ### 논문
    - Google 논문과 잘 알려진 논문들이 있다.
    - 이 모든 논문을 다 읽는다는 것은 너가 가진 시간보다 더 많은 시간을 들여야 할 것이다. 나는 선택적으로 읽기를 권장한다.
    - [ ] [1978: 순차 프로세스 통신 Communicating Sequential Processes](http://spinroot.com/courses/summer/Papers/hoare_1978.pdf)
        - [Go 언어로 구현](https://godoc.org/github.com/thomas11/csp)
        - [오래된 논문??](https://www.cs.cmu.edu/~crary/819-f09/)
    - [ ] [2003: 구글 파일 시스템](http://static.googleusercontent.com/media/research.google.com/en//archive/gfs-sosp2003.pdf)
    - [ ] [2004: MapReduce: 대형 클러스터에서 간략화된 데이터 처리]( http://static.googleusercontent.com/media/research.google.com/en//archive/mapreduce-osdi04.pdf)
    - [ ] [2007: 모든 프로그래머가 알아야하는 메모리 (매우 내용이 많음, 그리고 저자가 몇몇 섹션은 건너뛰게 권유함)](https://www.akkadia.org/drepper/cpumemory.pdf)
    - [ ] [2012: Google's Colossus](https://www.wired.com/2012/07/google-colossus/)
        - 지금은 논문은 볼수 없음.
    - [ ] 2012: AddressSanitizer: 빠른 어드레스 안전 검사기:
        - [논문](http://static.googleusercontent.com/media/research.google.com/en//pubs/archive/37752.pdf)
        - [영상](https://www.usenix.org/conference/atc12/technical-sessions/presentation/serebryany)
    - [ ] 2013: Spanner: Google’s Globally-Distributed Database 구글의 전세계적인 분산 데이터 베이스:
        - [논문](http://static.googleusercontent.com/media/research.google.com/en//archive/spanner-osdi2012.pdf)
        - [영상](https://www.usenix.org/node/170855)
    - [ ] [2014: 머신 러닝: The High-Interest Credit Card of Technical Debt](http://static.googleusercontent.com/media/research.google.com/en//pubs/archive/43146.pdf)
    - [ ] [2015: 연속적인 파이프 라인](http://static.googleusercontent.com/media/research.google.com/en//pubs/archive/43790.pdf)
    - [ ] [2015: High-Availability at Massive Scale: Building Google’s Data Infrastructure for Ads](https://static.googleusercontent.com/media/research.google.com/en//pubs/archive/44686.pdf)
    - [ ] [2015: 텐서 플로우: 이기종의 분산 시스템의 대규모 머신 러닝](http://download.tensorflow.org/paper/whitepaper2015.pdf )
    - [ ] [2015: 개발자가 코드를 찾는 방법 케이스 스터터디](http://static.googleusercontent.com/media/research.google.com/en//pubs/archive/43835.pdf)
    - [ ] [2016: Borg, Omega, and Kubernetes](http://static.googleusercontent.com/media/research.google.com/en//pubs/archive/44843.pdf)

- ### 테스팅
    - 여기서 보여주는 내용:
        - how unit testing works 유닛 테스트 방법
        - what are mock objects mock 객체는 무엇?
        - what is integration testing 통합 테스팅?
        - what is dependency injection 의존 주입은 무엇?
    - [ ] [제임스 바흐(James Bach)와 함께 하는 애자일 소프트웨어 테스팅 (영상)](https://www.youtube.com/watch?v=SAhJf36_u5U)
    - [ ] [열린 강좌(James Bach) : 소프트웨어 테스팅 (영상)](https://www.youtube.com/watch?v=ILkT_HV9DVU)
    - [ ] [Steve Freeman - 테스팅 중심의 개발 (영상)](https://vimeo.com/83960706)
        - [슬라이드](http://gotocon.com/dl/goto-berlin-2013/slides/SteveFreeman_TestDrivenDevelopmentThatsNotWhatWeMeant.pdf)
    - [ ] [TDD 는 죽었다. 테스트여 영원하라](http://david.heinemeierhansson.com/2014/tdd-is-dead-long-live-testing.html)
    - [ ] [TDD 가 죽었어? (영상)](https://www.youtube.com/watch?v=z9quxZsLcfo)
    - [ ] [영상 시리즈 (152 영상들) - 모두 필요하진 않아 (영상)](https://www.youtube.com/watch?v=nzJapzxH_rE&list=PLAwxTw4SYaPkWVHeC_8aSIbSxE_NXI76g)
    - [ ] [파이썬으로 하는 테스트 중심의 웹 개발](http://www.obeythetestinggoat.com/pages/book.html#toc)
    - [ ] Dependency injection 의존 주입:
        - [ ] [영상](https://www.youtube.com/watch?v=IKD2-MAkXyQ)
        - [ ] [Tao Of Testing](http://jasonpolites.github.io/tao-of-testing/ch3-1.1.html)
    - [ ] [테스트코드는 어떻게?](http://jasonpolites.github.io/tao-of-testing/ch4-1.1.html)

- ### 스케줄링
    - OS 에서 어떻게 동작하는지 확인
    - 운영체제 관련 영상으로 부터 알아 볼 수 있다

- ### 시스템 루틴 구현
    - 당신이 사용하는 프로그래밍 API 아래는 어떻게 구현이 되었는지 이해
    - 구현 할 수 있나?

- ### 문자열 검색 & 조작
    - [ ] [Sedgewick - 접미사 배열 (영상)](https://www.youtube.com/watch?v=HKPrVm5FWvg)
    - [ ] [Sedgewick - 내부문자열(Substring) 검색 (영상)](https://www.youtube.com/watch?v=2LvvVFCEIv8&list=PLe-ggMe31CTdAdjXB3lIuf2maubzo9t66&index=5)
        - [ ] [1. SubString 검색 소개](https://www.youtube.com/watch?v=2LvvVFCEIv8&list=PLe-ggMe31CTdAdjXB3lIuf2maubzo9t66&index=5)
        - [ ] [2. Brute-Force Substring 검색](https://www.youtube.com/watch?v=CcDXwIGEXYU&list=PLe-ggMe31CTdAdjXB3lIuf2maubzo9t66&index=4)
        - [ ] [3. Knuth-Morris Pratt KMP 알고리즘](https://www.youtube.com/watch?v=n-7n-FDEWzc&index=3&list=PLe-ggMe31CTdAdjXB3lIuf2maubzo9t66)
        - [ ] [4. Boyer-Moore](https://www.youtube.com/watch?v=fI7Ch6pZXfM&list=PLe-ggMe31CTdAdjXB3lIuf2maubzo9t66&index=2)
        - [ ] [5. Rabin-Karp](https://www.youtube.com/watch?v=QzI0p6zDjK4&index=1&list=PLe-ggMe31CTdAdjXB3lIuf2maubzo9t66)
    - [ ] [텍스트에서 패턴 찾기 (영상)](https://www.coursera.org/learn/data-structures/lecture/tAfHI/search-pattern-in-text)

    더 자세히 보고 싶다면 아래 [Additional Detail on Some Subjects](#additional-detail-on-some-subjects) 에서 "문자열 매칭" 섹션을 보기 바란다

---

## 시스템 설계, 확장, 자료 처리 (System Design, Scalability, Data Handling)
- **4년 이상의 경험을 갖고 있다면 시스템 디자인 질문에 대한 준비를 해야 한다.**
- 확장 가능한 소프트웨어/하드웨어를 설계하는 데는 많은 고민이 필요하기 때문에 시스템 확장 및 설계는 매우 많은 주제와 자원(자료)들이 필요하다.
- Yegge 가 얘기하는 고려들:
    - 확장성
        - 큰 데이터 세트를 하나의 값으로 증류(Distill)
        - Transform one data set to another 하나의 자료 세트에서 다른 자료로 변경
        - Handling obscenely large amounts of data  엄청 많은 양의 데이터 처리
    - 시스템 설계
        - features sets 설계 특징
        - interfaces 인터페이스
        - class hierarchies 클래스 계층
        - designing a system under certain constraints 시스템 제약 사항하에 설계
        - simplicity and robustness 단순하고 견고하게
        - tradeoffs 상충 관계
        - performance analysis and optimization 성능 분석 및 최적화
- [ ] **여기서 부터 시작하자**: [HiredInTech 의 시스템 설계](http://www.hiredintech.com/system-design/)
- [ ] [기술 명접에서 설계관련 질문은 어떻게 대답할까?](https://www.quora.com/How-do-I-prepare-to-answer-design-questions-in-a-technical-interview?redirected_qid=1500023)
- [ ] [시스템 설계 인터뷰 보기전에 알아야 할 8가지](http://blog.gainlo.co/index.php/2015/10/22/8-things-you-need-to-know-before-system-design-interviews/)
- [ ] [알고리즘 설계](http://www.hiredintech.com/algorithm-design/)
- [ ] [데이터 베이스 표준화 Database Normalization - 1NF, 2NF, 3NF and 4NF (영상)](https://www.youtube.com/watch?v=UrYLYV7WSHM)
- [ ] [시스템 설계 인터뷰](https://github.com/checkcheckzz/system-design-interview) - 여기에 많은 내용들이 있다. 기사(articles) 와 예제도 있다.
- [ ] [시스템 디자인 인터뷰에서 잘하는 방법](http://www.palantir.com/2011/10/how-to-rock-a-systems-design-interview/)
- [ ] [모두가 알아야 하는 숫자(?) Numbers Everyone Should Know](http://everythingisdata.wordpress.com/2009/10/17/numbers-everyone-should-know/)
- [ ] [문맥 교환(context switch)에 얼마나 많은 시간이 걸릴까?](http://blog.tsunanet.net/2010/11/how-long-does-it-take-to-make-context.html)
- [ ] [데이터 센터간 트랜잭션 Transactions Across Datacenters (영상)](https://www.youtube.com/watch?v=srOgpXECblk)
- [ ] [평범한 영어로 CAP 이론을 소개](http://ksat.me/a-plain-english-introduction-to-cap-theorem/)
- [ ] Paxos Consensus 알고리즘:
    - [Paxos 알고리즘 소개 - 한글](http://zetawiki.com/wiki/Paxos_%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98)
    - [짧은 소개 영상](https://www.youtube.com/watch?v=s8JqcZtvnsM)
    - [다중-paxos 와 사용 예제와 함께 보여주는 영상](https://www.youtube.com/watch?v=JEpsBg0AO6o)
    - [논문](http://research.microsoft.com/en-us/um/people/lamport/pubs/paxos-simple.pdf)
- [ ] [일관된 해슁](http://www.tom-e-white.com/2007/11/consistent-hashing.html)
- [ ] [NoSQL 패턴들](http://horicky.blogspot.com/2009/11/nosql-patterns.html)
- [ ] 확장성:
    - [ ] [놀라운 개념 소개 (영상)](https://www.youtube.com/watch?v=-W9F__D3oY4)
    - [ ] 짧은 시리즈:
        - [클론](http://www.lecloud.net/post/7295452622/scalability-for-dummies-part-1-clones)
        - [데이터 베이스](http://www.lecloud.net/post/7994751381/scalability-for-dummies-part-2-database)
        - [캐쉬](http://www.lecloud.net/post/9246290032/scalability-for-dummies-part-3-cache)
        - [비동기](http://www.lecloud.net/post/9699762917/scalability-for-dummies-part-4-asynchronism)
    - [ ] [확장 가능한 웹 아키텍쳐와 분산 시스템](http://www.aosabook.org/en/distsys.html)
        - [이 사이트의 번역 블로그](http://d2.naver.com/helloworld/206816)
    - [ ] [분산 컴퓨팅의 오류에 대한 설명](https://pages.cs.wisc.edu/~zuyu/files/fallacies.pdf)
    - [ ] [실용적인 프로그래밍 기법](http://horicky.blogspot.com/2010/10/scalable-system-design-patterns.html)
        - [추가: 구글 Pregel 그래프 처리](http://horicky.blogspot.com/2010/07/google-pregel-graph-processing.html)
    - [ ] [Jeff Dean - 구글에서 소프트웨어 시스템 빌딩과 교훈 (영상)](https://www.youtube.com/watch?v=modXC5IWTJI)
    - [ ] [확장을 위한 시스템 아키텍처링 소개](http://lethain.com/introduction-to-architecting-systems-for-scale/)
    - [ ] [앱 엔진과 클라우드 데이터 저장소를 사용해서 모바일 게임을 모든 잠재 고객에게 확장 (영상)](https://www.youtube.com/watch?v=9nWyWwY2Onc)
    - [ ] [How Google Does Planet-Scale Engineering for Planet-Scale Infra (영상)](https://www.youtube.com/watch?v=H4vMcD7zKM0)
    - [ ] [알고리즘의 중요성](https://www.topcoder.com/community/data-science/data-science-tutorials/the-importance-of-algorithms/)
    - [ ] [Sharding](http://highscalability.com/blog/2009/8/6/an-unorthodox-approach-to-database-design-the-coming-of-the.html)
          - 추가 설명 : [데이터베이스의 샤딩 - 한글](http://yeoubi.net/blog/database-sharding/)
    - [ ] [페이스북에서 확장 (2009)](https://www.infoq.com/presentations/Scale-at-Facebook)
    - [ ] [페이스북에서 확장 (2012), "10억 사용자를 위한 구축" (영상)](https://www.youtube.com/watch?v=oodS71YtkGU)
    - [ ] [Long(?) 게임을 위한 엔지니어링 - Astrid Atkinson 키노트(영상)](https://www.youtube.com/watch?v=p0jGmgIrf_M&list=PLRXxvay_m8gqVlExPC5DG3TGWJTaBgqSA&index=4)
    - [ ] [30분에 보는 7년동안 Youtube 확장성 배움들](http://highscalability.com/blog/2012/3/26/7-years-of-youtube-scalability-lessons-in-30-minutes.html)
        - [영상](https://www.youtube.com/watch?v=G-lGCC4KKok)
    - [ ] [8 개의 가상 머신으로 매일 10억 트랜젝션을 어떻게 PayPal 을 확장한 건가?](http://highscalability.com/blog/2016/8/15/how-paypal-scaled-to-billions-of-transactions-daily-using-ju.html)
    - [ ] [대량 데이터 셋에서 중복된 값을 제거하는 방법](https://blog.clevertap.com/how-to-remove-duplicates-in-large-datasets/)
    - [ ] [A look inside Etsy's scale and engineering culture with Jon Cowie (video)](https://www.youtube.com/watch?v=3vV4YiqKm1o)
    - [ ] [무엇이 아마존을 자신만의 마이크로 서비스 아키텍쳐로 이끌게 하는가?](http://thenewstack.io/led-amazon-microservices-architecture/)
    - [ ] [압축하지 않거나 압축하거나, 그것이 Uber 의 질문이었다.](https://eng.uber.com/trip-data-squeeze/)
    - [ ] [Asyncio Tarantool Queue, Get In The Queue](http://highscalability.com/blog/2016/3/3/asyncio-tarantool-queue-get-in-the-queue.html)
    - [ ] [대략적으로 쿼리의 처리는 언제 처리해야 하나?](http://highscalability.com/blog/2016/2/25/when-should-approximate-query-processing-be-used.html)
    - [ ] [장애 조치를 위한, 네이티브 멀티홈 아키텍처를 위한 하나의 데이터 센터에서 구글의 트랜잭션 처리 Google's Transition From Single Datacenter, To Failover, To A Native Multihomed Architecture]( http://highscalability.com/blog/2016/2/23/googles-transition-from-single-datacenter-to-failover-to-a-n.html)
    - [ ] [Spanner 스패너](http://highscalability.com/blog/2012/9/24/google-spanners-most-surprising-revelation-nosql-is-out-and.html)
    - [ ] [Egnyte 건축술: 다중 분산된 페타 바이트 구축 및 확장을 위한 교훈](http://highscalability.com/blog/2016/2/15/egnyte-architecture-lessons-learned-in-building-and-scaling.html)
    - [ ] [기술 학습 주도 프로그래밍: 새로운 세계를 위한 새로운 프로그래밍](http://highscalability.com/blog/2016/7/6/machine-learning-driven-programming-a-new-programming-for-a.html)
    - [ ] [하루 당 수백만의 요청을 처리하는 이미지 최적화 기술](http://highscalability.com/blog/2016/6/15/the-image-optimization-technology-that-serves-millions-of-re.html)
    - [ ] [짧은 Patreon 아키텍쳐](http://highscalability.com/blog/2016/2/1/a-patreon-architecture-short.html)
    - [ ] [Tinder: 가장 큰 추천 엔진이 어떻게 다음 볼 사람을 결정할까?](http://highscalability.com/blog/2016/1/27/tinder-how-does-one-of-the-largest-recommendation-engines-de.html)
    - [ ] [현대의 캐쉬의 설계](http://highscalability.com/blog/2016/1/25/design-of-a-modern-cache.html)
    - [ ] [페이스북 규모에서 라이브 비디오 스트리밍 Live Video Streaming At Facebook Scale](http://highscalability.com/blog/2016/1/13/live-video-streaming-at-facebook-scale.html)
    - [ ] [아마존 AWS 에서 11 백만이상의 사용자를 위해 초보자 확장 가이드](http://highscalability.com/blog/2016/1/11/a-beginners-guide-to-scaling-to-11-million-users-on-amazons.html)
    - [ ] [어떻게 Docker 효과 지연을 어떻게 사용? How Does The Use Of Docker Effect Latency?](http://highscalability.com/blog/2015/12/16/how-does-the-use-of-docker-effect-latency.html)
       - Docker 를 위한 책 [아마존 웹 서비스를 다루는 기술](http://pyrasis.com/book/TheArtOfAmazonWebServices)
    - [ ] [구글에서 AMP는 잠재적인 위협 요소가 될까?](http://highscalability.com/blog/2015/12/14/does-amp-counter-an-existential-threat-to-google.html)
       - AMP(Accelerated Mobile Page) 가속화된 모바일 페이지
    - [ ] [Netflix 스택의 360 도 시각](http://highscalability.com/blog/2015/11/9/a-360-degree-view-of-the-entire-netflix-stack.html)
    - [ ] [지연은 어디서나 발생하며, 그것은 언제나 비용을 발생시킨다. - 어떻게 그것을 줄일수 있지?](http://highscalability.com/latency-everywhere-and-it-costs-you-sales-how-crush-it)
    - [ ] [Serverless (매우 김, 요점만 보도록)](http://martinfowler.com/articles/serverless.html)
    - [ ] [인스타그램의 힘: 수백개의 인스턴스들, 여러 기술들](http://instagram-engineering.tumblr.com/post/13649370142/what-powers-instagram-hundreds-of-instances)
    - [ ] [Cinchcast 아키텍쳐 - 매일 1500 시간의 오디오를 생산하는 아키텍쳐](http://highscalability.com/blog/2012/7/16/cinchcast-architecture-producing-1500-hours-of-audio-every-d.html)
    - [ ] [Justin.Tv's 라이브 비디오 방송 아키텍쳐](http://highscalability.com/blog/2010/3/16/justintvs-live-video-broadcasting-architecture.html)
    - [ ] [Payfish의 소셜 게임 아키텍쳐 - 5억만명의 매월 사용자와 성장](http://highscalability.com/blog/2010/9/21/playfishs-social-gaming-architecture-50-million-monthly-user.html)
    - [ ] [TripAdvisor 아키텍쳐 - 4억만 방문자, 20억 동적 페이지 뷰들, 30TB Data](http://highscalability.com/blog/2011/6/27/tripadvisor-architecture-40m-visitors-200m-dynamic-page-view.html)
    - [ ] [PlentyOfFish 아키텍쳐](http://highscalability.com/plentyoffish-architecture)
    - [ ] [Salesforce 아키텍쳐 - 하루에 13억 트랜잭션을 처리하는가?](http://highscalability.com/blog/2013/9/23/salesforce-architecture-how-they-handle-13-billion-transacti.html)
    - [ ] [ESPN 규모에 따른 아키텍쳐 - 초당 100,000 Duh Nuh Nuhs 를 수행](http://highscalability.com/blog/2013/11/4/espns-architecture-at-scale-operating-at-100000-duh-nuh-nuhs.html)
    - [ ] 서비스들 서로 잘 붙을 수 있는 몇 가지 기술에 대한 정보는 아래의 "메세징, 직렬화, 대기(큐) 시스템"에서 확인 가능하다.
    - [ ] 트위터:
        - [O'Reilly MySQL CE 2011: Jeremy Cole, "크고 작은 데이터 @Twitter" (영상)](https://www.youtube.com/watch?v=5cKTP36HVgI)
        - [규모의 일정 Timelines at Scale](https://www.infoq.com/presentations/Twitter-Timeline-Scalability)
    - 더 많이 보기 위해, "Mining Massive Datasets" 비디오 시리즈들을 참고 바란다.
- [ ] 시스템 설계 프로세스 연습: 여기에 몇 가지 논문이나 실상에서 어떻게 처리되고 있는지에 대한 몇몇 문서들을 통해 시도해 볼 수 있을 것이다.:
    - 리뷰: [HiredInTech로 부터 시스템 설계](http://www.hiredintech.com/system-design/)
    - [치트 시트](https://github.com/jwasham/google-interview-university/blob/master/extras/cheat%20sheets/system-design.pdf)
    - flow 흐름:
        1. 문제와 범위 이해:
            - 인터뷰하는 사람의 도움을 받아 유스 케이스(use case) 를 정의하자.
            - 추가적인 feature(특징)을 제안하자
            - 범위에서 벗어나는 요소는 제거하자
            - 높은 유효성(availability) 가 필요하다고 가정하면, use case들을 추가하자.
        2. 제약에 대해 고려하자:
            - 한달에 얼마나 많은 요청이 있는지 물어보자.
            - 초당 얼마나 많은 요청이 있는지 물어보자 (그들은 지원자에게 수학적인 것을 하도록 만들 것이다.)
            - estimate reads vs. writes percentage (평가를 읽기 vs. 비율을 쓰기)
            - 평가를 할 때, 80 대 20 법칙을 항상 마음에 담아두자
            - 초당 얼마나 많은 데이터를 쓰는지?
            - 5년동안 필요한 총 저장소 크기
            - 얼마나 많은 데이터를 초당 읽는지
        3. 추상 설계:
            - 레이어 layers (서비스, 데이타, 캐슁)
            - 하부 구조 infrastructure: load balancing, messaging (로드 밸런싱, 메세징)
            - 서비스를 시작하기 위한 중요한 알고리즘의 간단한 리뷰
            - 병목현상에 대한 고려 및 해결책을 결정
    - 연습들:
        - [CDN 네트웍 설계: 오래된 문서](http://repository.cmu.edu/cgi/viewcontent.cgi?article=2112&context=compsci)
        - [랜덤 고유 ID 를 생성하는 시스템의 설계](https://blog.twitter.com/2010/announcing-snowflake)
        - [온라인 다중 사용자 카드 게임 설계](http://www.indieflashblog.com/how-to-create-an-asynchronous-multiplayer-game.html)
        - [키-값 데이터 베이스 설계](http://www.slideshare.net/dvirsky/introduction-to-redis)
        - [과거 시간 간격동안 top K 요청을 반환하는 함수 설계]( https://icmi.cs.ucsb.edu/research/tech_reports/reports/2005-23.pdf)
        - [사진 공유 시스템 설계](http://highscalability.com/blog/2011/12/6/instagram-architecture-14-million-users-terabytes-of-photos.html)
        - [추천 시스템 설계](http://ijcai13.org/files/tutorial_slides/td3.pdf)
        - [URL-shortener 시스템 설계](http://www.hiredintech.com/system-design/the-system-design-process/)
        - [캐쉬 시스템 설계](https://www.adayinthelifeof.nl/2011/02/06/memcache-internals/)

---

## 마지막 리뷰

    이 섹션은 중요한 컨셉에 대해 빠르게 리뷰하기 위한 짧은 영상들로 구성했다.
    이것은 당신이 지식을 상기 시키는데 아주 훌륭하다.

- [ ] 2-3분짜리 여러 주제에 대한 시리즈 영상 (23 영상들):
    - [영상들](https://www.youtube.com/watch?v=r4r1DZcx1cM&list=PLmVb1OknmNJuC5POdcDv5oCS7_OUkDgpj&index=22)
- [ ] 2-5분짜리 여러 주제에 대한 시리즈 영상 (18 영상들):
    - [영상들](https://www.youtube.com/channel/UCzDJwLWoYCUQowF_nG3m5OQ)
- [ ] [Sedgewick Videos - 알고리즘 I](https://www.youtube.com/user/algorithmscourses/playlists?shelf_id=2&view=50&sort=dd)
    - [ ] [01. Union-Find 유니온 찾기](https://www.youtube.com/watch?v=8mYfZeHtdNc&list=PLe-ggMe31CTexoNYnMhbHaWhQ0dvcy43t)
    - [ ] [02. 알고리즘 분석](https://www.youtube.com/watch?v=ZN-nFW0mEpg&list=PLe-ggMe31CTf0_bkOhh7sa5uqeppp3Sr0)
    - [ ] [03. 스택과 큐](https://www.youtube.com/watch?v=TIC1gappbP8&list=PLe-ggMe31CTe-9jhnj3P_3mmrCh0A7iHh)
    - [ ] [04. 기본 정렬](https://www.youtube.com/watch?v=CD2AL6VO0ak&list=PLe-ggMe31CTe_5WhGV0F--7CK8MoRUqBd)
    - [ ] [05. Mergesort 병합정렬](https://www.youtube.com/watch?v=4nKwesx_c8E&list=PLe-ggMe31CTeunC6GZHFBmQx7EKtjbGf9)
    - [ ] [06. Quicksort 퀵 정렬](https://www.youtube.com/watch?v=5M5A7qPWk84&list=PLe-ggMe31CTeE3x2-nF1-toca1QpuXwE1)
    - [ ] [07. Priority Queues 우선순위 큐](https://www.youtube.com/watch?v=G9TMe0KC0w0&list=PLe-ggMe31CTducy9LDiGVkdSv0NfiRwn5)
    - [ ] [08. Elementary Symbol Tables 기본 심볼 테이블](https://www.youtube.com/watch?v=up_nlilw3ac&list=PLe-ggMe31CTc3a8nKRDxFZZrWrBvkc9SG)
    - [ ] [09. Balanced Search Trees 균등 검색 트리](https://www.youtube.com/watch?v=qC1BLLPK_5w&list=PLe-ggMe31CTf7jHH_mFT50kayjCEA6Rhu)
    - [ ] [10. Geometric Applications of BST BST 의 기하학적 으용](https://www.youtube.com/watch?v=Wl30aGAp6TY&list=PLe-ggMe31CTdBsRIw0hXln0hilRs-DqAx)
    - [ ] [11. 해쉬 테이블](https://www.youtube.com/watch?v=QA8fJGO-i9o&list=PLe-ggMe31CTcKxIRGqqThMts2eHtSrf11)
- [ ] [Sedgewick Videos - 알고리즘 II](https://www.youtube.com/user/algorithmscourses/playlists?flow=list&shelf_id=3&view=50)
    - [ ] [01. Undirected Graphs 방향이 지정되지 않은 그래프](https://www.youtube.com/watch?v=GmVhD-mmMBg&list=PLe-ggMe31CTc0zDzANxl4I2MhMoRVlbRM)
    - [ ] [02. Directed Graphs 방향이 있는 그래프](https://www.youtube.com/watch?v=_z-JsVaUS40&list=PLe-ggMe31CTcEwaU8a1P1Gd95A77HV85K)
    - [ ] [03. Minimum Spanning Trees 최소 스패닝 트리](https://www.youtube.com/watch?v=t8fNk9tfVYY&list=PLe-ggMe31CTceUZxDesGfHGLE7kcSafqj)
    - [ ] [04. Shortest Paths 최단 경로](https://www.youtube.com/watch?v=HoGSiB7tSeI&list=PLe-ggMe31CTePpG3jbeOTsnGUGZDKxgZD)
    - [ ] [05. Maximum Flow 최대 흐름](https://www.youtube.com/watch?v=rYIKlFstBqE&list=PLe-ggMe31CTduQ68XQ-sVj32wYJIspTma)
    - [ ] [06. Radix Sorts Radix 정렬](https://www.youtube.com/watch?v=HKPrVm5FWvg&list=PLe-ggMe31CTcNvUX9E3tQeM6ntrdR8e53)
    - [ ] [07. Tries](https://www.youtube.com/watch?v=00YaFPcC65g&list=PLe-ggMe31CTe9IyG9MB8vt5xUJeYgOYRQ)
    - [ ] [08. Substring Search subString 검색](https://www.youtube.com/watch?v=QzI0p6zDjK4&list=PLe-ggMe31CTdAdjXB3lIuf2maubzo9t66)
    - [ ] [09. Regular Expressions 정규 표현](https://www.youtube.com/watch?v=TQWNQsJSPnk&list=PLe-ggMe31CTetTlJWouM42fyttyKPgSDh)
    - [ ] [10. Data Compression 데이터 압축](https://www.youtube.com/watch?v=at9tjpxcBh8&list=PLe-ggMe31CTciifRRo6yY0Yt0mzgIXXVZ)
    - [ ] [11. Reductions 감축](https://www.youtube.com/watch?v=Ow5x-ooMGv8&list=PLe-ggMe31CTe_yliW5vc3yO-dj1LSSDyF)
    - [ ] [12. Linear Programming 선형 프로그래밍](https://www.youtube.com/watch?v=rWhcLyiLZLA&list=PLe-ggMe31CTdy6dKzMgkWFuTTN1H8B-E1)
    - [ ] [13. Intractability 다루기 힘든 문제](https://www.youtube.com/watch?v=6qcaaDp4cdQ&list=PLe-ggMe31CTcZCjluBHw53e_ek2k9Kn-S)

---

## 코딩 문제 연습

이제 당신은 컴퓨터 과학 주제를 위에서 모두 살펴보았다, 이제는 코딩 문제에 답변하기 위해 연습해야 한다.

**코딩 문제연습은 문제를 프로그래밍을 위해 외어야 하는 것들은 없다. 연습을 많이 하란 얘긴듯**

왜 당신은 프로래밍 문제를 풀기 위해 연습이 필요한가:
- 문제 인지(recognition), 그리고 알맞은 자료 구조 및 알고리즘을 찾아야 함
- 문제로 부터 요구사항을 모아야함
- 인터뷰를 받는 것을 대비해서 니가 어떻게 풀것인지 말해보자
- 코딩을 컴퓨터가 아닌 화이트 보드나 종이에 해보자
- 너의 코드에 대한 시간/공간 복잡도를 생각해보자
- 테스트

이것을 위해 훌륭한 진입방법을 알려줄 사이트를 소개한다. 물론, 관련 책들을 봐도 무방하지만, 내가 찾은 사이트는 정말 대단하다.:
[Algorithm design canvas](http://www.hiredintech.com/algorithm-design/)

[코딩 인터뷰 연습을 위한 나만의 프로세스](https://googleyasheck.com/my-process-for-coding-interview-exercises/)

집에 화이트 보드가 없다고? 그럴수도 있다. 나는 이상한 사람이라 큰 화이트 보드가 있다. 화이트보드 대신, 미술용품점에서 큰 드로잉 패드를 사자. 그러면 당신은 소파에 앉아 연습을 할 수 있다. 이것은 나의 "소파 화이트 보드"이다. 나는 사진에 펜도 같이 넣었다. 당신이 펜을 사용하면, 또한 지울수도 있다. 그러면 빨리 지저분해진다.

![나의 소파 화이트 보다](https://dng5l3qzreal6.cloudfront.net/2016/Oct/art_board_sm_2-1476233630368.jpg)

보충:

- [TopCoders 를 위한 수학](https://www.topcoder.com/community/data-science/data-science-tutorials/mathematics-for-topcoders/)
- [Dynamic Programming 동적프로그래밍– 초보에서 고급으로](https://www.topcoder.com/community/data-science/data-science-tutorials/dynamic-programming-from-novice-to-advanced/)
- [MIT 인터뷰 자료](https://web.archive.org/web/20160906124824/http://courses.csail.mit.edu/iap/interview/materials.php)
- [언어(JAVA/C++ 등) 사용을 더 잘 할 수 있는 연습을 도와줌](http://exercism.io/languages)

**프로그래밍 문제를 읽고 풀어보자(순서대로):**

- [ ] [Programming Interviews Exposed: Secrets to Landing Your Next Job, 2nd Edition](http://www.wiley.com/WileyCDA/WileyTitle/productCd-047012167X.html)
    - 답변은 C++ / C / JAVA 로 됨
    - 번역판 : [한빛 미디어, 프로그래밍 면접 이렇게 준비한다](http://www.hanbit.co.kr/store/books/look.php?p_code=B9005920688)
- [ ] [Cracking the Coding Interview, 6th Edition](http://www.amazon.com/Cracking-Coding-Interview-6th-Programming/dp/0984782850/)
    - 답변은 JAVA 로만
    - [번역 게리 엘 멕도웰 지음, 이병준 옮김](http://www.kyobobook.co.kr/product/detailViewKor.laf?mallGb=KOR&barcode=9788966260485)


위의 [책 리스트](#book-list)

## 코딩 연습/도전

일단, 당신의 두뇌를 배우게 했다면, 그 두뇌를 일하게 하세요.
코딩 문제를 당신이 할 수 있는 한 많이 해보세요

- [ ] [해결책을 찾는 방법](https://www.topcoder.com/community/data-science/data-science-tutorials/how-to-find-a-solution/)
- [ ] [Topcoder 문제를 해독하는 방법](https://www.topcoder.com/community/data-science/data-science-tutorials/how-to-dissect-a-topcoder-problem-statement/)

문제 제공 사이트:
- [LeetCode](https://leetcode.com/)
- [TopCoder](https://www.topcoder.com/)
- [Project Euler (math-focused)](https://projecteuler.net/index.php?section=problems)
- [Codewars](http://www.codewars.com)
- [HackerRank](https://www.hackerrank.com/)
- [Codility](https://codility.com/programmers/)
- [InterviewCake](https://www.interviewcake.com/)
- [Geeks for Geeks](http://www.geeksforgeeks.org/)
- [InterviewBit](https://www.interviewbit.com/invite/icjf)

아마도:
- [큰 회사로 부터 가상의 인터뷰보는 사람들](http://www.gainlo.co/)

## 일단 당신이 인터뷰에 가까이 갔다.

- [ ] Cracking The Coding Interview 세트 2 (videos):
    - [Cracking The Code Interview 영상](https://www.youtube.com/watch?v=4NIb9l3imAo)
    - [Cracking the Coding Interview - Fullstack Speaker Series](https://www.youtube.com/watch?v=Eg5-tdAwclo)
    - [무엇이든 물어보세요: Gayle Laakmann McDowell (저자)](https://www.youtube.com/watch?v=1fqxMuPmGak)

## 이력서

- [나쁘지 않는 이력서를 만들기 위한 10가지 팁](http://steve-yegge.blogspot.co.uk/2007_09_01_archive.html)
- See Resume prep items in Cracking The Coding Interview and back of Programming Interviews Exposed
- Cracking The Coding Interview 에 이력서 준비 챕터를 보고, "프로그래밍 면접 이렇게 준비한다"책을 보자.


## 인터뷰가 다가올 때쯤 생각해볼 만한 것들

당신이 받을 20가지 인터뷰 문제를 생각해보자. 각각 2-3개의 답변을 준비하자. 당신이 성취한 것에 대한 내용을 스토리로 만들자.

- Why do you want this job? 왜 이 일을 원하는가?
- What's a tough problem you've solved? 당신이 해결한 어려운 문제는?
- Biggest challenges faced? 당면한 문제중 가장 도전적인 것들?
- Best/worst designs seen? 당신이 본 최고/최악 설계
- Ideas for improving an existing Google product. 현존하는 구글 제품중 향상시킬 만한 아이디어
- How do you work best, as an individual and as part of a team? 개인으로 또는 팀의 구성원으로 어떻게 최선을 다했나?
- Which of your skills or experiences would be assets in the role and why? 당신의 기술이나 경험 중 어느 것이 그 역할에 자산이 될 것이며 그 이유는 무엇입니까?
- What did you most enjoy at [job x / project y]? 일이나 프로젝트 중 가장 재미있게 했던 것은?
- What was the biggest challenge you faced at [job x / project y]? 가장 도전적인 것?
- What was the hardest bug you faced at [job x / project y]? 당면한 버그 중 가장 어려웠던 것?
- What did you learn at [job x / project y]? 그 프로젝트로 부터 무엇을 배웠나
- What would you have done better at [job x / project y]? 그 프로젝트에서 무엇을 더 잘할 수 있었나?

## Have questions for the interviewer (번역안함.)

    Some of mine (I already may know answer to but want their opinion or team perspective):

- How large is your team?
- What does your dev cycle look like? Do you do waterfall/sprints/agile?
- Are rushes to deadlines common? Or is there flexibility?
- How are decisions made in your team?
- How many meetings do you have per week?
- Do you feel your work environment helps you concentrate?
- What are you working on?
- What do you like about it?
- What is the work life like?

## Once You've Got The Job

Congratulations! 축하합니다.

- [10 things I wish I knew on my first day at Google](https://medium.com/@moonstorming/10-things-i-wish-i-knew-on-my-first-day-at-google-107581d87286#.livxn7clw)

Keep learning. 계속 배우세요

You're never really done. 여기서 끝내면 안됩니다.

---

    *****************************************************************************************************
    *****************************************************************************************************

    추가적인 것들은 아래에 있습니다. 이것은 저의 단순 추천입니다. 이것들을 공부하면, CS 개념에 대해 더 많은 것을
    배우게 되고 다른 소프트웨어 엔지니어링 개발 일을 얻을 수 있을 겁니다.
    당신은 훨씬 더 균형 잡힌 소프트웨어 엔지니어가 될 것입니다.

    *****************************************************************************************************
    *****************************************************************************************************

---

## 추가적인 책

- [ ] [UNIX 프로그래밍 환경](http://product.half.ebay.com/The-UNIX-Programming-Environment-by-Brian-W-Kernighan-and-Rob-Pike-1983-Other/54385&tg=info)
    - 옛것이지만 좋은 책
- [ ] [리눅스 커멘드 라인: 완벽 소개](https://www.amazon.com/dp/1593273894/)
    - 최근 추가됨.
- [ ] [TCP/IP 일러스트 시리즈](https://en.wikipedia.org/wiki/TCP/IP_Illustrated)
- [ ] [Head First Design Patterns](https://www.amazon.com/gp/product/0596007124/)
    - [번역판-Head First Design Patterns](http://book.naver.com/bookdb/book_detail.nhn?bid=1882446)
- [ ] [디자인 패턴: 객체 지향 소프트웨어 재사용의 요소](https://www.amazon.com/Design-Patterns-Elements-Reusable-Object-Oriented/dp/0201633612)
- [ ] [Site 신뢰성 엔지니어링](https://landing.google.com/sre/book.html)
    - [Site 신뢰성 엔지니어링: 구글이 생산 시스템을 돌리는 방법](https://landing.google.com/sre/)
- [ ] [UNIX 와 리눅스의 관리자 핸드북 4th](https://www.amazon.com/UNIX-Linux-System-Administration-Handbook/dp/0131480057/)

## 추가적인 배움

- ### 동적 프로그래밍
    - 이 주제는 꽤나 어렵다. DP 는 재귀와 많은 연관이 되어 있다.
    - 나는 이런 문제들의 패턴을 이해할 수 있을 때까지 가능한한 많은 예제들을 보는 것을 추천한다.
    - [ ] 영상들:
        - Skiena 영상은 때때로 화이트보드를 사용하는데 글자가 너무 작아서 따라가기가 힘들수도 있다.
        - [ ] [Skiena: CSE373 2012 - Lecture 19 - 동적 프로그래밍 소개 (영상)](https://youtu.be/Qc2ieXRgR0k?list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b&t=1718)
        - [ ] [Skiena: CSE373 2012 - Lecture 20 - 거리 수정 (영상)](https://youtu.be/IsmMhMdyeGY?list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b&t=2749)
        - [ ] [Skiena: CSE373 2012 - Lecture 21 - 동적 프로그래밍 예제 (영상)](https://youtu.be/o0V9eYF4UI8?list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b&t=406)
        - [ ] [Skiena: CSE373 2012 - Lecture 22 - 동적 프로그래밍 응용 (영상)](https://www.youtube.com/watch?v=dRbMC1Ltl3A&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b&index=22)
        - [ ] [Simonson: 동적 프로그래밍 0 (59:18 에서 시작) (video)](https://youtu.be/J5aJEcOr6Eo?list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&t=3558)
        - [ ] [Simonson: 동적 프로그래밍 I - Lecture 11 (video)](https://www.youtube.com/watch?v=0EzHjQ_SOeU&index=11&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm)
        - [ ] [Simonson: 동적 프로그래밍 II - Lecture 12 (video)](https://www.youtube.com/watch?v=v1qiRwuJU7g&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&index=12)
        - [ ] 개인적으로 찾은? DP 문제들:
            [동적 프로그래밍 (영상)](https://www.youtube.com/playlist?list=PLrmLmBdmIlpsHaNTPP_jHHDx_os9ItYXr)
    - [ ] Yale 강의 노트:
        - [ ] [동적 프로그래밍](http://www.cs.yale.edu/homes/aspnes/classes/223/notes.html#dynamicProgramming)
    - [ ] Coursera:
        - [ ] [The RNA secondary structure problem (영상)](https://www.coursera.org/learn/algorithmic-thinking-2/lecture/80RrW/the-rna-secondary-structure-problem)
        - [ ] [동적 프로그래밍 알고리즘 (영상)](https://www.coursera.org/learn/algorithmic-thinking-2/lecture/PSonq/a-dynamic-programming-algorithm)
        - [ ] [DP 알고리즘의 일러스트 (영상)](https://www.coursera.org/learn/algorithmic-thinking-2/lecture/oUEK2/illustrating-the-dp-algorithm)
        - [ ] [DP 알고리즘의 수행시간 (영상)](https://www.coursera.org/learn/algorithmic-thinking-2/lecture/nfK2r/running-time-of-the-dp-algorithm)
        - [ ] [DP vs. 재귀 구현 (영상)](https://www.coursera.org/learn/algorithmic-thinking-2/lecture/M999a/dp-vs-recursive-implementation)
        - [ ] [Global pairwise sequence alignment 전역 양방향 순서 정렬 (video)](https://www.coursera.org/learn/algorithmic-thinking-2/lecture/UZ7o6/global-pairwise-sequence-alignment)
        - [ ] [Local pairwise sequence alignment 지역 양방향 순서 정렬 (video)](https://www.coursera.org/learn/algorithmic-thinking-2/lecture/WnNau/local-pairwise-sequence-alignment)

- ### 컴파일러
    - [ ] [1분안에 알아보는 컴파일러의 동작 방법 (영상)](https://www.youtube.com/watch?v=IhC7sdYe-Jg)
    - [ ] [Harvard CS50 - 컴파일러 (영상)](https://www.youtube.com/watch?v=CSZLNYF4Klo)
    - [ ] [C++ (영상)](https://www.youtube.com/watch?v=twodd1KFfGk)
    - [ ] [컴파일러 최적화의 이해 (C++) (영상)](https://www.youtube.com/watch?v=FnGCDLhaxKU)

- ### Floating Point Numbers
    - [ ] 단순 8-bit: [Floating Point 숫자의 표현 - 1 (영상 - 여기에 하나의 계산의 오류가 있음)](https://www.youtube.com/watch?v=ji3SfClm8TU)
    - [ ] 32 bit: [IEEE754 32-bit floating point binary (video)](https://www.youtube.com/watch?v=50ZYcZebIec)

- ### 유니코드
    - [ ] [모든 소프트웨어 개발자가 최소한으로 알아야 할 유니코드와 캐랙터 셑]( http://www.joelonsoftware.com/articles/Unicode.html)
    - [ ] [모든 프로그래머가 알아야 하는 텍스트 인코딩과 캐랙터 셑](http://kunststube.net/encoding/)
    - [ ] [한글 인코딩의 이해 1편: 한글 인코딩의 역사와 유니코드](http://d2.naver.com/helloworld/19187)
    - [ ] [한글 인코딩의 이해 2편: 유니코드와 Java를 이용한 한글 처리](http://d2.naver.com/helloworld/76650)

- ### 엔디안
    - [ ] [빅 / 리틀 엔디안](https://www.cs.umd.edu/class/sum2003/cmsc311/Notes/Data/endian.html)
    - [ ] [빅 엔디안 Vs 리틀 엔디안 (영상)](https://www.youtube.com/watch?v=JrNF0KRAlyo)
    - [ ] [빅/리틀 엔디안 내외부 (video)](https://www.youtube.com/watch?v=oBSuXP-1Tc0)
        - 커널 개발을 위한 매우 기술적 이야기.
        - 앞부분 반정도만 봐

- ### Emacs 와 vi(m)
    - 예전 아마존 리쿠르팅 포스트에서 Yegge 가 제안, unix 기반 코드 에디터에 익숙해져라
    - vi(m):
        - [vim 연습 01 - 설치, 설정 그리고 모드 (영상)](https://www.youtube.com/watch?v=5givLEMcINQ&index=1&list=PL13bz4SHGmRxlZVmWQ9DvXo1fEg4UdGkr)
        - [VIM 고급](http://vim-adventures.com/)
        - 4개의 시리즈 영상:
            - [vi/vim 에디터 - Lesson 1](https://www.youtube.com/watch?v=SI8TeVMX8pk)
            - [vi/vim 에디터 - Lesson 2](https://www.youtube.com/watch?v=F3OO7ZIOaJE)
            - [vi/vim 에디터 - Lesson 3](https://www.youtube.com/watch?v=ZYEccA_nMaI)
            - [vi/vim 에디터 - Lesson 4](https://www.youtube.com/watch?v=1lYD5gwgZIA)
        - [Emacs 대신에 Vi 쓰자](http://www.cs.yale.edu/homes/aspnes/classes/223/notes.html#Using_Vi_instead_of_Emacs)
    - emacs:
        - [기본 Emacs (영상)](https://www.youtube.com/watch?v=hbmV1bnQ-i0)
        - 3 개의 영상 (영상들):
            - [Emacs 소개 (초보) -Part 1- 파일 명령어, cut/copy/paste, 커서 커맨드](https://www.youtube.com/watch?v=ujODL7MD04Q)
            - [Emacs 소개 (초보) -Part 2- 버퍼 관리, 검색, M-x grep 과 rgrep 모드](https://www.youtube.com/watch?v=XWpsRupJ4II)
            - [Emacs 소개 (초보) -Part 3- 표현, 기술, ~/.emacs 파일 그리고 패키지](https://www.youtube.com/watch?v=paSgzPso-yc)
        - [알마 모드: 또는, 걱정하지 않고 Emacs 를 사랑하는 방법 (영상)](https://www.youtube.com/watch?v=JWD1Fpdd4Pc)
        - [C 프로그램 작성하기](http://www.cs.yale.edu/homes/aspnes/classes/223/notes.html#Writing_C_programs_with_Emacs)
        - [(maybe) 깊이 있는 Org 모드: 구조 관리 (영상)](https://www.youtube.com/watch?v=nsGYet02bEk)

- ### 유닉스 커맨드 라인 툴
    - 예전 아마존 리쿠르팅 포스트에서 Yegge 가 제안.
    - [ ] bash
    - [ ] cat
    - [ ] grep
    - [ ] sed
    - [ ] awk
    - [ ] curl or wget
    - [ ] sort
    - [ ] tr
    - [ ] uniq
    - [ ] [strace](https://en.wikipedia.org/wiki/Strace)
    - [ ] [tcpdump](https://danielmiessler.com/study/tcpdump/)

- ### 정보 이론 (영상)
    - [ ] [Khan Academy](https://www.khanacademy.org/computing/computer-science/informationtheory)
       - ko.khanacademy.org 로 접속하면 한글 사이트로 나옴.
    - [ ] Markov 프로세스:
        - [ ] [Core Markov 텍스트 생성](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/waxgx/core-markov-text-generation)
        - [ ] [Core Markov 텍스트 생성 구현](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/gZhiC/core-implementing-markov-text-generation)
        - [ ] [Project = Markov Text Generation Walk Through](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/EUjrq/project-markov-text-generation-walk-through)

- ### 패러티 & 해밍 코드 (영상)
    - [ ] [소개](https://www.youtube.com/watch?v=q-3BctoUpHE)
    - [ ] [패러티](https://www.youtube.com/watch?v=DdMcAUlxh1M)
    - [ ] 해밍 코드:
        - [에러 발견](https://www.youtube.com/watch?v=1A_NcXxdoCc)
        - [에러 수정](https://www.youtube.com/watch?v=JAMLuxdHH8o)
    - [ ] [에러 확인](https://www.youtube.com/watch?v=wbH2VxzmoZk)

- ### 엔트로피
    - 위에도 관련 영상 있음
    - 정보 이론 영상을 먼전 보고 아래의 것을 볼 수 있도록 하자
    - [ ] [Information Theory, Claude Shannon, Entropy, Redundancy, Data Compression & Bits (video)](https://youtu.be/JnJq3Py0dyM?t=176)

- ### 암호학
    - 이것도 위에 보면 영상
    - 정보 이론 영상을 먼전 보고 아래의 것을 볼 수 있도록 하자
    - [ ] [Khan Academy 시리즈](https://www.khanacademy.org/computing/computer-science/cryptography)
    - [ ] [암호: 해쉬 함수](https://www.youtube.com/watch?v=KqqOXndnvic&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=30)
    - [ ] [암호: 암호화](https://www.youtube.com/watch?v=9TNI2wHmaeI&index=31&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp)

- ### 압축
    - 정보 이론 영상을 먼전 보고 아래의 것을 볼 수 있도록 하자
    - [ ] 컴퓨터 애호가 (영상들):
        - [ ] [압축](https://www.youtube.com/watch?v=Lto-ajuqW3w)
        - [ ] [엔트로피 압축](https://www.youtube.com/watch?v=M5c_RFKVkko)
        - [ ] [트리 뒤집기 (허프만 트리)](https://www.youtube.com/watch?v=umTbivyJoiI)
        - [ ] [EXTRA BITS/TRITS - 허프만 트리](https://www.youtube.com/watch?v=DV8efuB3h2g)
        - [ ] [멋진 텍스트 압축 (LZ 77 방법)](https://www.youtube.com/watch?v=goOa3DGezUA)
        - [ ] [텍스트 압축이 확률을 만나다.](https://www.youtube.com/watch?v=cCDCfoHTsaU)
    - [ ] [Compressor Head 영상](https://www.youtube.com/playlist?list=PLOU2XLYxmsIJGErt5rrCqaSGTMyyqNt2H)
    - [ ] [(옵션) 구글 개발자: GZIP 은 충분치 않아!](https://www.youtube.com/watch?v=whGwm0Lky2s)

- ### 네트워킹
    - **만약, 당신이 네트워킹관련 경험이 있거나 시스템 엔지니어가 되고자 한다면, 아래의 질문들을 살펴보자**
    - 알아두면 좋은 것들이다.
    - [ ] [Khan Academy](https://www.khanacademy.org/computing/computer-science/internet-intro)
      - ko.khanacademy.org 로 접속하면 한글 사이트로 나옴.
    - [ ] [UDP 와 TCP: Transport Protocols 비교](https://www.youtube.com/watch?v=Vdc8TCESIg8)
    - [ ] [TCP/IP 와 OSI Model 설명!](https://www.youtube.com/watch?v=e5DEVa9eSN0)
    - [ ] [패킷이 인터넷을 통해 전송. 네트워킹 & TCP/IP 소개.](https://www.youtube.com/watch?v=nomyRJehhnM)
    - [ ] [HTTP](https://www.youtube.com/watch?v=WGJrLqtX7As)
    - [ ] [SSL 와 HTTPS](https://www.youtube.com/watch?v=S2iBR2ZlZf0)
    - [ ] [SSL/TLS](https://www.youtube.com/watch?v=Rp3iZUvXWlM)
    - [ ] [HTTP 2.0](https://www.youtube.com/watch?v=E9FxNzv1Tr8)
    - [ ] [영상 시리즈 (21 영상들)](https://www.youtube.com/playlist?list=PLEbnTDJUr_IegfoqO4iPnPYQui46QqT0j)
    - [ ] [Subnetting Demystified - Part 5 CIDR Notation](https://www.youtube.com/watch?v=t5xYI0jzOf4)

- ### 컴퓨터 보안
    - [MIT (23 영상들)](https://www.youtube.com/playlist?list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
        - [ ] [소개, 위협 모델](https://www.youtube.com/watch?v=GqmQg-cszw4&index=1&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
        - [ ] [Hijacking 공격에 대한 컨트롤](https://www.youtube.com/watch?v=6bwzNg5qQ0o&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh&index=2)
        - [ ] [버퍼 오버플로우 공격 및 방어](https://www.youtube.com/watch?v=drQyrzRoRiA&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh&index=3)
        - [ ] [특권 분리 Privilege Separation](https://www.youtube.com/watch?v=6SIJmoE9L9g&index=4&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
        - [ ] [기능들 Capabilities](https://www.youtube.com/watch?v=8VqTSY-11F4&index=5&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
        - [ ] [Sandboxing Native Code](https://www.youtube.com/watch?v=VEV74hwASeU&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh&index=6)
        - [ ] [Web 보안 모델](https://www.youtube.com/watch?v=chkFBigodIw&index=7&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
        - [ ] [웹 응용 프로그램의 보안](https://www.youtube.com/watch?v=EBQIGy1ROLY&index=8&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
        - [ ] [Symbolic Execution](https://www.youtube.com/watch?v=yRVZPvHYHzw&index=9&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
        - [ ] [네트웍 보안](https://www.youtube.com/watch?v=SIEVvk3NVuk&index=11&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
        - [ ] [네트웍 프로토콜](https://www.youtube.com/watch?v=QOtA76ga_fY&index=12&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
        - [ ] [Side-Channel Attacks](https://www.youtube.com/watch?v=PuVMkSEcPiI&index=15&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)

- ### 가비지 컬렉션
    - [ ] [가비지 컬렉션 (Java); Augmenting data str (영상)](https://www.youtube.com/watch?v=StdfeXaKGEc&list=PL-XXv-cvA_iAlnI-BQr9hjqADPBtujFJd&index=25)
    - [ ] [컴파일러 (영상)](https://www.youtube.com/playlist?list=PLO9y7hOkmmSGTy5z6HZ-W4k2y8WXF7Bff)
    - [ ] [파이썬 GC (영상)](https://www.youtube.com/watch?v=iHVs_HkjdmI)
    - [ ] [Deep Dive Java: 가비지 컬렉션은 좋아!](https://www.infoq.com/presentations/garbage-collection-benefits)
    - [ ] [Deep Dive Python: CPython 에서 가비지 컬렉션 (영상)](https://www.youtube.com/watch?v=P-8Z0-MhdQs&list=PLdzf4Clw0VbOEWOS_sLhT_9zaiQDrS5AR&index=3)

- ### 병렬 프로그래밍
    - [ ] [Coursera (Scala)](https://www.coursera.org/learn/parprog1/home/week/1)
    - [ ] [좋은 성능을 내는 병렬 컴퓨팅을 위한 효과적인 파이썬 (영상)](https://www.youtube.com/watch?v=uY85GkaYzBk)

- ### 메세징, 직렬화, 그리고 대기(큐) 시스템
    - [ ] [Thrift 절약](https://thrift.apache.org/)
        - [Tutorial 소개](http://thrift-tutorial.readthedocs.io/en/latest/intro.html)
    - [ ] [Protocol Buffers 프로토콜 버퍼들](https://developers.google.com/protocol-buffers/)
        - [Tutorials 소개](https://developers.google.com/protocol-buffers/docs/tutorials)
    - [ ] [gRPC](http://www.grpc.io/)
        - [gRPC 101 for Java Developers (영상)](https://www.youtube.com/watch?v=5tmPvSe7xXQ&list=PLcTqM9n_dieN0k1nSeN36Z_ppKnvMJoly&index=1)
    - [ ] [Redis](http://redis.io/)
        - [소개](http://try.redis.io/)
    - [ ] [Amazon SQS (큐)](https://aws.amazon.com/sqs/)
    - [ ] [Amazon SNS (pub-sub)](https://aws.amazon.com/sns/)
    - [ ] [RabbitMQ](https://www.rabbitmq.com/)
        - [시작하기](https://www.rabbitmq.com/getstarted.html)
    - [ ] [Celery](http://www.celeryproject.org/)
        - [Celery 시작하기](http://docs.celeryproject.org/en/latest/getting-started/first-steps-with-celery.html)
    - [ ] [ZeroMQ](http://zeromq.org/)
        - [소개 - 메뉴얼을 읽자](http://zeromq.org/intro:read-the-manual)
    - [ ] [ActiveMQ](http://activemq.apache.org/)
    - [ ] [Kafka](http://kafka.apache.org/documentation.html#introduction)
    - [ ] [MessagePack](http://msgpack.org/index.html)
    - [ ] [Avro](https://avro.apache.org/)

- ### Fast Fourier Transform 빠른 푸리에 변환
    - [ ] [푸리에 변환을 위한 대화식 가이드 An Interactive Guide To The Fourier Transform](https://betterexplained.com/articles/an-interactive-guide-to-the-fourier-transform/)
    - [ ] [푸리에 변환은 무엇인가? 무엇을 위해 쓰이는가?](http://www.askamathematician.com/2012/09/q-what-is-a-fourier-transform-what-is-it-used-for/)
    - [ ] [푸리에 변환은 무엇인가? (영상)](https://www.youtube.com/watch?v=Xxut2PN-V8Q)
    - [ ] [분할 & 정복 Divide & Conquer: FFT (영상)](https://www.youtube.com/watch?v=iTMn0Kt18tg&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=4)
    - [ ] [FFT의 이해](http://jakevdp.github.io/blog/2013/08/28/understanding-the-fft/)

- ### Bloom Filter 블룸 필터
    - [블룸 필터-한글 위키](https://ko.wikipedia.org/wiki/%EB%B8%94%EB%A3%B8_%ED%95%84%ED%84%B0)
    - 주어진 m 비트와 함께 주어진 블룸필터와 K 해쉬 함수, 삽입과 관련 테스팅은 O(k) 이다.
    - [블룸 필터](https://www.youtube.com/watch?v=-SuTGoFYjZs)
    - [블룸 필터 | Mining of Massive Datasets | Stanford University](https://www.youtube.com/watch?v=qBTdukbzc78)
    - [소개](http://billmill.org/bloomfilter-tutorial/)
    - [블룸 필터 앱만드는 방법](http://blog.michaelschmatz.com/2016/04/11/how-to-write-a-bloom-filter-cpp/)

- ### HyperLogLog
    - [확률적 자료구조를 이용한 추정 - 유일한 원소 개수 추정과 HyperLogLog (한글)](http://d2.naver.com/helloworld/711301)
    - [단지 1.5 KB 의 메모리로 10억개의 분명한(?) 객체를 세는 방법](http://highscalability.com/blog/2012/4/5/big-data-counting-how-to-count-a-billion-distinct-objects-us.html)

- ### Locality-Sensitive Hashing
    - [소개 한글](http://blog.daum.net/jchern/13627840)
    - MD5나 SHA 의 반대말로 두 문서나 문자열이 정확히 같은지 결정하는데 사용된다.
    - [Simhashing (hopefully) made simple](http://ferd.ca/simhashing-hopefully-made-simple.html)

- ### van Emde Boas Trees 반 엠데 보아스 트리
    - [ ] [분할 정복: van Emde Boas Trees (영상)](https://www.youtube.com/watch?v=hmReJCupbNU&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=6)
    - [ ] [MIT 강의노트](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-046j-design-and-analysis-of-algorithms-spring-2012/lecture-notes/MIT6_046JS12_lec15.pdf)

- ### Augmented Data Structures 증강된 자료 구조들
    - [ ] [CS 61B Lecture 39: 증강된 자료 구조들](https://youtu.be/zksIj9O8_jc?list=PL4BBB74C7D2A1049C&t=950)

- ### Tries 트라이(Prefix tree)
    - [트라이 간략 설명 및 코드(자바)](http://m.blog.naver.com/javaking75/140211950640)
    - Note there are different kinds of tries. Some have prefixes, some don't, and some use string instead of bits
        to track the path. (몇몇 종류의 트라이가 있다. 몇몇은 접두어가 있고, 다른 몇몇은 없는데, 경로를 찾기위해 비트를 사용하는 대신 문자열을 사용.)
    - 코드를 보았지만, 구현해보진 못했다.
    - [ ] [Sedgewick - 트라이 (3 videos)](https://www.youtube.com/playlist?list=PLe-ggMe31CTe9IyG9MB8vt5xUJeYgOYRQ)
        - [ ] [1. R Way Tries](https://www.youtube.com/watch?v=buq2bn8x3Vo&index=3&list=PLe-ggMe31CTe9IyG9MB8vt5xUJeYgOYRQ)
        - [ ] [2. Ternary Search Tries](https://www.youtube.com/watch?v=LelV-kkYMIg&index=2&list=PLe-ggMe31CTe9IyG9MB8vt5xUJeYgOYRQ)
        - [ ] [3. Character Based Operations](https://www.youtube.com/watch?v=00YaFPcC65g&list=PLe-ggMe31CTe9IyG9MB8vt5xUJeYgOYRQ&index=1)
    - [ ] [자료 구조와 프로그래밍 기술의 노트](http://www.cs.yale.edu/homes/aspnes/classes/223/notes.html#Tries)
    - [ ] 짧은 영상:
        - [ ] [트라이 소개 (영상)](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/08Xyf/core-introduction-to-tries)
        - [ ] [트라이 성능 (영상)](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/PvlZW/core-performance-of-tries)
        - [ ] [트라이 구현 (영상)](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/DFvd3/core-implementing-a-trie)
    - [ ] [트라이: 소홀하게 된 자료 구조](https://www.toptal.com/java/the-trie-a-neglected-data-structure)
    - [ ] [TopCoder - 트라이를 사용하자](https://www.topcoder.com/community/data-science/data-science-tutorials/using-tries/)
    - [ ] [Stanford Lecture (실생활 케이스) (video)](https://www.youtube.com/watch?v=TJ8SkcUSdbU)
    - [ ] [MIT, 고급 자료 구조, 문자열](https://www.youtube.com/watch?v=NinWEPPrkDQ&index=16&list=PLUl4u3cNGP61hsJNdULdudlRL493b-XZf)

- ### Balanced search trees 균형 잡힌 이진 트리
    - 균형잡힌 이진 트리의 최소 한가지 형태는 알아야 함 (구현도 할 수 있어야 해):
    - "균형 잡힌 이진트리 중에, AVL 과 2/3 트리들은 조금 오래 됬고, red-black(레드 블랙) 트리는 요즘 인기 인듯.
        특히 흥미로운 자체 구성 자료 구조는 회전을 이용하여 루트에서 다른 접근 가능한 키로 옮겨 갈 수 있는 스플레이 트리(splay tree) 이다." - Skiena
    - 물론, 나는 splay 트리 구현을 선택했다. 내가 읽어 온 내용을 보면, 당신은 인터뷰 중에는 균형잡힌 이진 트리 구현을 할 필요는 없다. 그러나 나는 코딩을 일단 해보고 그것을 격어보았다. 나는 레드 블랙트리 코드도 많이 읽었었다.
        - splay 트리: insert, search, delete 함수
        만약 당신이 레드-블랙 트리를 구현하고 싶다면:
        - search / insertion 함수, delete 는 안해도 될 듯.
    - 나는 매우 많은 자료 셋을 다룰 때 사용하는 B-트리도 더 많이 배우고 싶었다.
    - [ ] [자체 균형 이진 검색 트리](https://en.wikipedia.org/wiki/Self-balancing_binary_search_tree)

    - [ ] **AVL 트리**
        - 실제로:
            저의 생각은 AVL 트리는 많이 사용되지 않는 것이지만, 나는 어디에 사용되는지 봤습니다.:
            AVL 트리는 O(log n) 검색, 삽입 그리고 삭제를 지원하는 자료 구조이다. 이것은 레드 블랙 트리 보다 더 완벽한 균형잡힌 이진 트리 이고 느린 삽입 / 삭제 연산이지만, 검색은 더 빠릅니다. 한번 구축 되어 재구성 없이 로드 될 수 있는 데이터 구조에 매력적입니다. (언어 사전, 어셈블리어의 opcode 나 인터프리터가 사용하는 프로그램 사전)
        - [ ] [MIT AVL 트리 / AVL 정렬 (영상)](https://www.youtube.com/watch?v=FNeL18KsWPc&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=6)
        - [ ] [AVL 트리 (영상)](https://www.coursera.org/learn/data-structures/lecture/Qq5E0/avl-trees)
        - [ ] [AVL 트리 구현 (video)](https://www.coursera.org/learn/data-structures/lecture/PKEBC/avl-tree-implementation)
        - [ ] [분리 및 병합](https://www.coursera.org/learn/data-structures/lecture/22BgE/split-and-merge)

    - [ ] **스플레이 트리 Splay trees**
        - 실제로:
            Splay 트리는 캐쉬, 메모리 할당, 라우터, 가비지 컬렉션, 데이터 압축, ropes (replacement of string used for long text strings - 긴 텍스트를 위해 사용되는 문자열 치환), 윈도우즈 NT(가상 메모리, 네트워킹 그리고 파일 시스템) 등
        - [ ] [CS 61B: 스플레이 트리 (영상)](https://www.youtube.com/watch?v=Najzh1rYQTo&index=23&list=PL-XXv-cvA_iAlnI-BQr9hjqADPBtujFJd)
        - [ ] MIT Lecture: Splay Trees:
            - 굉장히 수학적이지만, 마지막 10분은 꼭 보도록 하세요
            - [영상](https://www.youtube.com/watch?v=QnPl_Y6EqMo)

    - [ ] **레드-블랙 트리 Red/black trees**
        - 2-3 트리의 변환 (아래)
        - 실제로:
            레드-블랙 트리는 삽입 시간, 제거 시간 그리고 검색 시간의 worst-case 를 보장한다. 이것은 Real-time 응용 프로그램과 같이 수행 시간에 민감한 것에게 좋을 뿐만 아니라, 최악(worst-case) 보장을 제공하는 다른 자료구조에서도 가치 있는 블럭을 생성할 수 있도록 한다. 예를 들면, 계산 기하학에서 사용되는 많은 자료 구조에서 레드 블랙 트리가 기반이 될 수 있고, 현 리눅스 커널에서 스케줄러로 사용되는 CFS(Completely Fair Scheduler)에도 사용된다. JAVA 버전 8 에서는 해쉬맵에서 부족한 해쉬 코드로 인해 같은 해쉬값을 가지는 요소를 저장하기 위해 연결 리스트를 사용하는 대신 레드 블랙 트리(같은 해쉬 값 요소가 8개 이상이면)를 사용한다.
        - [ ] [Aduni - 알고리즘 - Lecture 4 (아래 링크는 처음부터 시작함) (영상)](https://youtu.be/1W3x0f_RmUo?list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&t=3871)
        - [ ] [Aduni - 알고리즘 - Lecture 5 (영상)](https://www.youtube.com/watch?v=hm2GHwyKF1o&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&index=5)
        - [ ] [블랙 트리](https://en.wikipedia.org/wiki/Red%E2%80%93black_tree)
        - [ ] [이진 검색 및 레드 블랙 트리 소개](https://www.topcoder.com/community/data-science/data-science-tutorials/an-introduction-to-binary-search-and-red-black-trees/)

    - [ ] **2-3 검색 트리**
        - 실제로:
            2-3 트리는 삽입은 빠르지만, 검색은 느리다.(높이는 AVL 트리보다 더 높음.)
        - 당신은 2-3 트리는 서로 다른 타입의 노드가 포함되어 구현되어 야 하기 때문에 거의 사용할 일 은 없다. 대신 사람들은 레드 블랙 트리를 사용한다.
        - [ ] [2-3 트리 직감과 정의 (영상)](https://www.youtube.com/watch?v=C3SsdUqasD4&list=PLA5Lqm4uh9Bbq-E0ZnqTIa8LRaL77ica6&index=2)
        - [ ] [2-3 트리의 이진 뷰](https://www.youtube.com/watch?v=iYvBtGKsqSg&index=3&list=PLA5Lqm4uh9Bbq-E0ZnqTIa8LRaL77ica6)
        - [ ] [2-3 트리 (영상)](https://www.youtube.com/watch?v=TOb1tuEZ2X4&index=5&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp)

    - [ ] **2-3-4 트리 (일명 2-4 트리)**
        - 실제로:
            모든 2-4 트리는, 동일한 순서를 가지는 레드 블랙 트리의 데이터 요소들과 대응된다. 2-4 트리에서 삽입 및 삭제 수행은 레드 블랙 트리에서 회전과 반전(color-flipping)과 동일합니다. 이것은 2-4 트리를 레드-블랙 트리 로직을 이해하는데 중요하다는 것을 알 수 있고, 교과서(?)에 레드 블랙 트리 전에 2-4 트리를 많이 소개되는지 알수 있다. **2-4 트리는 실제로 잘 쓰여지지 않음에도 말이다.**
        - [ ] [CS 61B Lecture 26: 이진 검색 트리 (video)](https://www.youtube.com/watch?v=zqrqYXkth6Q&index=26&list=PL4BBB74C7D2A1049C)
        - [ ] [Bottom Up 234-Trees (video)](https://www.youtube.com/watch?v=DQdMYevEyE4&index=4&list=PLA5Lqm4uh9Bbq-E0ZnqTIa8LRaL77ica6)
        - [ ] [Top Down 234-Trees (video)](https://www.youtube.com/watch?v=2679VQ26Fp4&list=PLA5Lqm4uh9Bbq-E0ZnqTIa8LRaL77ica6&index=5)

    - [ ] **N-ary (K-ary, M-ary) 트리**
        - note: N 또는 K는 분기 인자 이다. (최대 분기)
        - 이진 트리는 분기 인자 2를 가지는 2-ary 트리이다.
        - 2-3 트리는 3-ary 임
        - [ ] [K-Ary 트리](https://en.wikipedia.org/wiki/K-ary_tree)

    - [ ] **B-트리**
        - 재밌는 사실: 이것은 미스테리지만, B 트리는 Boeing, Balanced 또는 Bayer(공동 발명가)의 약자이다.
        - 실제로:
            B-트리는 데이터베이스에서 널리 사용된다. 최근 파일 시스템들은 B-트리를 사용한다. 데이터 베이스에서 사용 외에도, B-트리는 특정 파일의 빠른 랜덤 접근을 허용기 위해 파일시스템에서도 사용된다. 기본적인 문제는 파일 블락 i 주소를 디스크 블럭 주소로 변환하는 작업이다.
        - [ ] [B-트리](https://en.wikipedia.org/wiki/B-tree)
        - [ ] [B-트리 소개 (영상)](https://www.youtube.com/watch?v=I22wEC1tTGo&list=PLA5Lqm4uh9Bbq-E0ZnqTIa8LRaL77ica6&index=6)
        - [ ] [B-트리 정의 및 삽입 (영상)](https://www.youtube.com/watch?v=s3bCdZGrgpA&index=7&list=PLA5Lqm4uh9Bbq-E0ZnqTIa8LRaL77ica6)
        - [ ] [B-트리 삭제 (영상)](https://www.youtube.com/watch?v=svfnVhJOfMc&index=8&list=PLA5Lqm4uh9Bbq-E0ZnqTIa8LRaL77ica6)
        - [ ] [MIT 6.851 - 메모리 계층 모델 (영상)](https://www.youtube.com/watch?v=V3omVLzI0WE&index=7&list=PLUl4u3cNGP61hsJNdULdudlRL493b-XZf)
                - covers cache-oblivious B-Trees, very interesting data structures
                - 처음 37분은 매우 기술적인 내용이다, 스킵해도 될 듯.

- ### k-D 트리
    - 사각형이나 더 높은 차원의 객체 내에서 점의 수를 찾는데 효과적
    - k-nearest 이웃을 위해 좋음.
    - [ ] [Kd 트리 (영상)](https://www.youtube.com/watch?v=W94M9D_yXKk)
    - [ ] [kNN K-d 트리 알고리즘 (영상)](https://www.youtube.com/watch?v=Y4ZgLlDfKDg)

- ### Skip Lists
    - "이것은 약간 컬트 자료 구조이다" - Skiena
    - [ ] [랜덤: Skip Lists (video)](https://www.youtube.com/watch?v=2g9OSRKJuzM&index=10&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp)
    - [ ] [애니매이션과 조금더 상세](https://en.wikipedia.org/wiki/Skip_list)

- ### 네트웍 흐름
    - [ ] [5분안에 보는 Ford-Fulkerson (영상)](https://www.youtube.com/watch?v=v1VgJmkEJW0)
    - [ ] [Ford-Fulkerson 알고리즘 (영상)](https://www.youtube.com/watch?v=v1VgJmkEJW0)
    - [ ] [네트웍 흐름 (영상)](https://www.youtube.com/watch?v=2vhN4Ice5jI)

- ### Disjoint Sets & Union Find 분리된 셋 & 유니온 찾기
    - [ ] [UCB 61B - Disjoint Sets; Sorting & selection (영상)](https://www.youtube.com/watch?v=MAEGXTwmUsI&list=PL-XXv-cvA_iAlnI-BQr9hjqADPBtujFJd&index=21)
    - [ ] [Sedgewick Algorithms - Union-Find (6 영상)](https://www.youtube.com/watch?v=8mYfZeHtdNc&list=PLe-ggMe31CTexoNYnMhbHaWhQ0dvcy43t)

- ### 빠른 처리를 위한 수학 Math for Fast Processing
    - [ ] [정수 산술, Karatsuba 곱 (영상)](https://www.youtube.com/watch?v=eCaXlAaN2uE&index=11&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb)
    - [ ] [중국 나머지 정리 (암호에서 사용됨) (영상)](https://www.youtube.com/watch?v=ru7mWZJlRQg)

- ### Treap
    - 이진 검색 트리 및 힙의 조합
    - [ ] [Treap](https://en.wikipedia.org/wiki/Treap)
    - [ ] [자료 구조: Treaps 설명 (영상)](https://www.youtube.com/watch?v=6podLUYinH8)
    - [ ] [Applications in set operations](https://www.cs.cmu.edu/~scandal/papers/treaps-spaa98.pdf)

- ### 선형 프로그래밍 (영상)
    - [ ] [선형 프로그래밍](https://www.youtube.com/watch?v=M4K6HYLHREQ)
    - [ ] [최소 비용 찾기](https://www.youtube.com/watch?v=2ACJ9ewUC6U)
    - [ ] [최대 값 찾기](https://www.youtube.com/watch?v=8AA_81xI3ik)
    - [ ] [파이썬으로 선형 방정식 풀기 - Simplex 알고리즘](https://www.youtube.com/watch?v=44pAWI7v5Zk)

- ### 기하학, Convex hull 볼록 선체 (영상)
    - [ ] [그래프 알고리즘 IV: 기하학 알고리즘 소개 - Lecture 9](https://youtu.be/XIAQRlNkJAw?list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&t=3164)
    - [ ] [기하학 알고리즘: Graham & Jarvis - Lecture 10](https://www.youtube.com/watch?v=J5aJEcOr6Eo&index=10&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm)
    - [ ] [분할 & 정복: Convex Hull, 중간값 찾기](https://www.youtube.com/watch?v=EzeYI7p9MjU&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=2)

- ### 이산 수학
    - 아래 비디오를 보자

- ### 머신 러닝
    - [ ] 왜 머신 러닝인가?
        - [ ] [구글이 머신 러닝을 처음 적용한 회사로 재조명 되는 방법](https://backchannel.com/how-google-is-remaking-itself-as-a-machine-learning-first-company-ada63defcb70)
        - [ ] [지능형 컴퓨팅 시스템을 위한 대형 규모의 딥 러닝 (영상)](https://www.youtube.com/watch?v=QSaZGT4-6EY)
        - [ ] [딥러닝 그리고 이해 가능성 vs. 소프트웨어 엔지니어링과 검증by Peter Norvig](https://www.youtube.com/watch?v=X769cyzBNVw)
    - [ ] [구글 클라우드 머신 러닝 툴 (영상)](https://www.youtube.com/watch?v=Ja2hxBAwG_0)
    - [ ] [구글 개발자들의 머신 러닝 요리법 (Scikit Learn & Tensorflow) (영상)](https://www.youtube.com/playlist?list=PLOU2XLYxmsIIuiBfYad6rFYQU_jL2ryal)
    - [ ] [Tensorflow (영상)](https://www.youtube.com/watch?v=oZikw5k_2FM)
    - [ ] [Tensorflow 소개](https://www.tensorflow.org/versions/r0.11/tutorials/index.html)
    - [ ] [파이썬으로 신경망 구현을 위한 실용 가이드(Theano 사용)](http://www.analyticsvidhya.com/blog/2016/04/neural-networks-python-theano/)
    - 강좌:
        - [시작을 위한 좋은 강좌: 머신 러닝](https://www.coursera.org/learn/machine-learning)
              - [영상](https://www.youtube.com/playlist?list=PLZ9qNFMHZ-A4rycgrgOYma6zxF4BZGGPW)
              - see videos 12-18 for a review of linear algebra (14 and 15 are duplicates)
              - 선형 대수학의 리뷰를 위한 12-18 비디오를 보자(14/15는 중복)
        - [머신러닝을 위한 신경망](https://www.coursera.org/learn/neural-networks)
        - [구글 딥 러닝 Nanodegree](https://www.udacity.com/course/deep-learning--ud730)
        - [구글 머신 러닝 엔지니어 Nanodegree](https://www.udacity.com/course/machine-learning-engineer-nanodegree-by-google--nd009)
        - [자율주행 자동자 엔지니어 Nanodegree](https://www.udacity.com/drive)
        - [Metis Online Course (2달동안 10만원)](http://www.thisismetis.com/explore-data-science)
    - 자료:
        - 책:
            - [파이썬 머신 러닝](https://www.amazon.com/Python-Machine-Learning-Sebastian-Raschka/dp/1783555130/)
            - [데이터 과학 시작하기: 파이썬과 함께 하는 첫 원칙](https://www.amazon.com/Data-Science-Scratch-Principles-Python/dp/149190142X)
            - [파이썬과 함께 하는 머신 러닝 소개](https://www.amazon.com/Introduction-Machine-Learning-Python-Scientists/dp/1449369413/)
        - [소프트웨어 엔지니어를 위한 머신 러닝](https://github.com/ZuzooVn/machine-learning-for-software-engineers)
        - Data School: http://www.dataschool.io/

- ### Go
    - [ ] 영상:
        - [ ] [왜 Go를 배워야해?](https://www.youtube.com/watch?v=FTl0tl9BGdc)
        - [ ] [Go 프로그래밍](https://www.youtube.com/watch?v=CF9S4QZuV30)
        - [ ] [Go 소개](https://www.youtube.com/watch?v=ytEkHepK08c)
    - [ ] 책:
        - [ ] [Go 로 하는 프로그래밍 소개(online 에서는 꽁짜)](https://www.golang-book.com/books/intro)
        - [ ] [Go 프로그래밍 언어 (Donovan & Kernighan)](https://www.amazon.com/Programming-Language-Addison-Wesley-Professional-Computing/dp/0134190440)
    - [ ] [부트 캠프](https://www.golang-book.com/guides/bootcamp)

--

## 또다른 주제에 대한 상세

    나는 특정 주제에 대해 조금더 상세히 설명하려고 한다. 하지만, 이것들을 원치 않는다면, 포함하지 않아도 된다. (너무 많거든)

- [ ] **Union-Find 유니온 찾기**
    - [ ] [Overview](https://www.coursera.org/learn/data-structures/lecture/JssSY/overview)
    - [ ] [순진하게 구현](https://www.coursera.org/learn/data-structures/lecture/EM5D0/naive-implementations)
    - [ ] [트리](https://www.coursera.org/learn/data-structures/lecture/Mxu0w/trees)
    - [ ] [랭크에 의한 유니온 Union By Rank](https://www.coursera.org/learn/data-structures/lecture/qb4c2/union-by-rank)
    - [ ] [경로 압축](https://www.coursera.org/learn/data-structures/lecture/Q9CVI/path-compression)
    - [ ] [옵션 분석](https://www.coursera.org/learn/data-structures/lecture/GQQLN/analysis-optional)

- [ ] **동적 프로그래밍** (videos)
    - [ ] [6.006: 동적 프로그래밍 I: 피보나치, 최단 경로](https://www.youtube.com/watch?v=OQ5jsbhAv_M&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=19)
    - [ ] [6.006: 동적 프로그래밍 II: 텍스트 양쪽 맞춤, 블랙잭](https://www.youtube.com/watch?v=ENyox7kNKeY&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=20)
    - [ ] [6.006: DP III: 괄호, 거리 수정, 배낭문제](https://www.youtube.com/watch?v=ocZMDMZwhCY&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=21)
    - [ ] [6.006: DP IV: Guitar Fingering, 테트리스, 슈퍼 마리오 Bros.](https://www.youtube.com/watch?v=tp4_UXaVyx8&index=22&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb)
    - [ ] [6.046: 동적 프로그래밍 고급](https://www.youtube.com/watch?v=Tw1k46ywN6E&index=14&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp)
    - [ ] [6.046: 동적 프로그래밍: 모든 쌍의 최단 경로](https://www.youtube.com/watch?v=NzgFUwOaoIw&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=15)
    - [ ] [6.046: 동적 프로그래밍](https://www.youtube.com/watch?v=krZI60lKPek&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=12)

- [ ] **그래프 처리** (videos)
    - [ ] [동기화된 분산 알고리즘: Symmetry-Breaking. 최단 경로 스패닝 트리 ](https://www.youtube.com/watch?v=mUBmcbbJNf4&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=27)
    - [ ] [동기화된 분산 알고리즘: 최단 경로 스패닝 트리](https://www.youtube.com/watch?v=kQ-UQAzcnzA&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=28)

- [ ] MIT **확률** (mathy, and go slowly, which is good for mathy things) (videos):
    - [ ] [MIT 6.042J - 확률 소개](https://www.youtube.com/watch?v=SmFwFdESMHI&index=18&list=PLB7540DEDD482705B)
    - [ ] [MIT 6.042J - 조건부 확률](https://www.youtube.com/watch?v=E6FbvM-FGZ8&index=19&list=PLB7540DEDD482705B)
    - [ ] [MIT 6.042J - Independence 독립](https://www.youtube.com/watch?v=l1BCv3qqW4A&index=20&list=PLB7540DEDD482705B)
    - [ ] [MIT 6.042J - Random Variables 랜덤 값](https://www.youtube.com/watch?v=MOfhhFaQdjw&list=PLB7540DEDD482705B&index=21)
    - [ ] [MIT 6.042J - 기대값 I](https://www.youtube.com/watch?v=gGlMSe7uEkA&index=22&list=PLB7540DEDD482705B)
    - [ ] [MIT 6.042J - 기대값 II](https://www.youtube.com/watch?v=oI9fMUqgfxY&index=23&list=PLB7540DEDD482705B)
    - [ ] [MIT 6.042J - Large Deviations 큰 편](https://www.youtube.com/watch?v=q4mwO2qS2z4&index=24&list=PLB7540DEDD482705B)
    - [ ] [MIT 6.042J - Random Walks 랜덤 워크](https://www.youtube.com/watch?v=56iFMY8QW2k&list=PLB7540DEDD482705B&index=25)

- [ ] [Simonson: Approximation Algorithms 근사 알고리즘 (영상)](https://www.youtube.com/watch?v=oDniZCmNmNw&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&index=19)

- [ ] **문자열 일치**
    - [ ] Rabin-Karp (영상):
        - [Rabin Karps 알고리즘](https://www.coursera.org/learn/data-structures/lecture/c0Qkw/rabin-karps-algorithm)
        - [사전 계산](https://www.coursera.org/learn/data-structures/lecture/nYrc8/optimization-precomputation)
        - [최적화: 구현 및 분석](https://www.coursera.org/learn/data-structures/lecture/h4ZLc/optimization-implementation-and-analysis)
        - [표 이중화 Table Doubling, Karp-Rabin](https://www.youtube.com/watch?v=BRO7mVIFt08&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=9)
        - [Rolling Hashes, Amortized Analysis](https://www.youtube.com/watch?v=w6nuXg0BISo&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=32)
    - [ ] Knuth-Morris-Pratt (KMP):
        - [Knuth-Morris-Pratt (KMP) 문자열 찾기 알고리즘](https://www.youtube.com/watch?v=5i7oKodCRJo)
    - [ ] Boyer–Moore 문자열 찾기 알고리즘
        - [Boyer-Moore 문자열 찾기 알고리즘m](https://en.wikipedia.org/wiki/Boyer%E2%80%93Moore_string_search_algorithm)
        - [고급 문자열 검색 Boyer-Moore-Horspool 알고리즘 (영상)](https://www.youtube.com/watch?v=QDZpzctPf10)
    - [ ] [Coursera: 문자열에 대한 알고리즘](https://www.coursera.org/learn/algorithms-on-strings/home/week/1)
        - 출발은 좋지만, KMP 에 대한 내용이 갈수록 복잡해짐
        - 트리에 대한 설명 좋음
        - 이건 안봐도 무방

- [ ] **정렬**

    - [ ] Stanford 정렬에 대한 강좌:
        - [ ] [Lecture 15 | 프로그래밍 추상화 (영상)](https://www.youtube.com/watch?v=ENp00xylP7c&index=15&list=PLFE6E58F856038C69)
        - [ ] [Lecture 16 | 프로그래밍 추상화 (영상)](https://www.youtube.com/watch?v=y4M9IVgrVKo&index=16&list=PLFE6E58F856038C69)
    - [ ] Shai Simonson, [Aduni.org](http://www.aduni.org/):
        - [ ] [알고리즘 - 정렬 - Lecture 2 (영상)](https://www.youtube.com/watch?v=odNJmw5TOEE&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&index=2)
        - [ ] [알고리즘 - 정렬 II - Lecture 3 (video)](https://www.youtube.com/watch?v=hj8YKFTFKEE&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&index=3)
    - [ ] Steven Skiena lectures on sorting:
        - [ ] [lecture 시작지점 26:46 (영상)](https://youtu.be/ute-pmMkyuk?list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b&t=1600)
        - [ ] [lecture 시작지점 27:40 (영상)](https://www.youtube.com/watch?v=yLvp-pB8mak&index=8&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b)
        - [ ] [lecture 시작지점 35:00 (영상)](https://www.youtube.com/watch?v=q7K9otnzlfE&index=9&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b)
        - [ ] [lecture 시작지점 23:50 (영상)](https://www.youtube.com/watch?v=TvqIGu9Iupw&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b&index=10)

## 영상 시리즈

앉아서 그냥 즐겨. "넷플릭스와 기술" :P

- [ ] [개별 동적 프로그래밍 문제 리스트 (각각은 짧음)](https://www.youtube.com/playlist?list=PLrmLmBdmIlpsHaNTPP_jHHDx_os9ItYXr)

- [ ] [x86 아키텍쳐, 어셈블리, 응용프로그램 (11 영상)](https://www.youtube.com/playlist?list=PL038BE01D3BAEFDB0)

- [ ] [MIT 18.06 선형 대수학, Spring 2005 (35 영상)](https://www.youtube.com/playlist?list=PLE7DDD91010BC51F8)

- [ ] [훌륭 - MIT 미적분: 단일 변수 미적분학](https://www.youtube.com/playlist?list=PL3B08AE665AB9002A)

- [ ] [Computer Science 70, 001 - Spring 2015 - 이산 수학과 확률 이론](https://www.youtube.com/playlist?list=PL-XXv-cvA_iD8wQm8U0gG_Z1uHjImKXFy)

- [ ] [이산 수학 by Shai Simonson (19 영상)](https://www.youtube.com/playlist?list=PL3o9D4Dl2FJ9q0_gtFXPh_H4POI5dK0yG)

- [ ] [이산 수학 Part 1 by Sarada Herke (5 영상)](https://www.youtube.com/playlist?list=PLGxuz-nmYlQPOc4w1Kp2MZrdqOOm4Jxeo)

- [ ] CSE373 - 알고리즘 분석 (25 영상)
    - [Skiena lectures 알고리즘 설계 메뉴얼](https://www.youtube.com/watch?v=ZFjhkohHdAA&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b&index=1)

- [ ] [UC Berkeley 61B (Spring 2014): 자료 구조 (25 영상)](https://www.youtube.com/watch?v=mFPmKGIrQs4&list=PL-XXv-cvA_iAlnI-BQr9hjqADPBtujFJd)

- [ ] [UC Berkeley 61B (Fall 2006): 자료 구조 (39 영상)](https://www.youtube.com/playlist?list=PL4BBB74C7D2A1049C)

- [ ] [UC Berkeley 61C: 기계 구조 (26 영상)](https://www.youtube.com/watch?v=gJJeUFyuvvg&list=PL-XXv-cvA_iCl2-D-FS5mk0jFF6cYSJs_)

- [ ] [OOSE: UML 과 JAVA로 하는 소프트웨어 개발 (21 영상)](https://www.youtube.com/playlist?list=PLJ9pm_Rc9HesnkwKlal_buSIHA-jTZMpO)

- [ ] [UC Berkeley CS 152: 컴퓨터 아키텍쳐와 엔지니어링 (20 영상)](https://www.youtube.com/watch?v=UH0QYvtP7Rk&index=20&list=PLkFD6_40KJIwEiwQx1dACXwh-2Fuo32qr)

- [ ] [MIT 6.004: 계산 구조 (49 영상)](https://www.youtube.com/playlist?list=PLrRW1w6CGAcXbMtDFj205vALOGmiRc82-)

- [ ] [Carnegie Mellon - 컴퓨터 아키텍쳐 (39 영상)](https://www.youtube.com/playlist?list=PL5PHm2jkkXmi5CxxI7b3JCL1TWybTDtKq)

- [ ] [MIT 6.006: 알고리즘 소개 (47 영상)](https://www.youtube.com/watch?v=HtSuA80QTyo&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&nohtml5=False)

- [ ] [MIT 6.033: 컴퓨터 시스템 엔지니어링 (22 영상)](https://www.youtube.com/watch?v=zm2VP0kHl1M&list=PL6535748F59DCA484)

- [ ] [MIT 6.034 인공지는, Fall 2010 (30 영상)](https://www.youtube.com/playlist?list=PLUl4u3cNGP63gFHB6xb-kVBiQHYe_4hSi)

- [ ] [MIT 6.042J: 컴퓨터 과학을 위한 수학, Fall 2010 (25 영상)](https://www.youtube.com/watch?v=L3LMbpZIKhQ&list=PLB7540DEDD482705B)

- [ ] [MIT 6.046: 알고리즘 설계와 분석 (34 영상)](https://www.youtube.com/watch?v=2P-yW7LQr08&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp)

- [ ] [MIT 6.050J: 정보와 엔트로피, Spring 2008 (19 영상)](https://www.youtube.com/watch?v=phxsQrZQupo&list=PL_2Bwul6T-A7OldmhGODImZL8KEVE38X7)

- [ ] [MIT 6.851: 고급 자료 구조 (22 영상)](https://www.youtube.com/watch?v=T0yzrZL1py0&list=PLUl4u3cNGP61hsJNdULdudlRL493b-XZf&index=1)

- [ ] [MIT 6.854: 고급 알고리즘, Spring 2016 (24 영상)](https://www.youtube.com/playlist?list=PL6ogFv-ieghdoGKGg2Bik3Gl1glBTEu8c)

- [ ] [Harvard COMPSCI 224: 고급 알고리즘 (25 영상)](https://www.youtube.com/playlist?list=PL2SOU6wwxB0uP4rJgf5ayhHWgw7akUWSf)

- [ ] [MIT 6.858 컴퓨터 시스템 보안, Fall 2014 (영상)](https://www.youtube.com/watch?v=GqmQg-cszw4&index=1&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)

- [ ] [Stanford: 프로그래밍 패러다임 (27 영상)](https://www.youtube.com/view_play_list?p=9D558D49CA734A02)

- [ ] [암호학 소개 by Christof Paar](https://www.youtube.com/playlist?list=PL6N5qY2nvvJE8X75VkXglSrVhLv1tVcfy)
    - [강좌를 위한 웹사이트에 슬라이드와 문제들이 있다](http://www.crypto-textbook.com/)

- [ ] [Mining 대규모 데이터 셋 - Stanford University (94 영상들)](https://www.youtube.com/playlist?list=PLLssT5z_DsK9JDLcT8T62VtzwyW9LNepV)

- [ ] [그래프 이론 by Sarada Herke (67 영상들)](https://www.youtube.com/user/DrSaradaHerke/playlists?shelf_id=5&view=50&sort=dd)

## 컴퓨터 과학

- [Directory of Online CS Courses](https://github.com/open-source-society/computer-science)
- [Directory of CS Courses (many with online lectures)](https://github.com/prakhar1989/awesome-courses)
