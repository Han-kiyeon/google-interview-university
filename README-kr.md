# Google Interview University

Translations:
- [한국어 (in progress)] (README-kr.md) [Issues #1 https://github.com/daeseokyoun/google-interview-university/issues/1]
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
- [About Google](#about-google)
- [About Video Resources](#about-video-resources)
- [Interview Process & General Interview Prep](#interview-process--general-interview-prep)
- [Pick One Language for the Interview](#pick-one-language-for-the-interview)
- [Book List](#book-list)
- [Before you Get Started](#before-you-get-started)
- [What you Won't See Covered](#what-you-wont-see-covered)
- [Prerequisite Knowledge](#prerequisite-knowledge)
- [The Daily Plan](#the-daily-plan)
- [Algorithmic complexity / Big-O / Asymptotic analysis](#algorithmic-complexity--big-o--asymptotic-analysis)법
- [Data Structures](#data-structures)
    - [Arrays](#arrays)
    - [Linked Lists](#linked-lists)
    - [Stack](#stack)
    - [Queue](#queue)
    - [Hash table](#hash-table)
- [More Knowledge](#more-knowledge)
    - [Binary search](#binary-search)
    - [Bitwise operations](#bitwise-operations)
- [Trees](#trees)
    - [Trees - Notes & Background](#trees---notes--background)
    - [Binary search trees: BSTs](#binary-search-trees-bsts)
    - [Heap / Priority Queue / Binary Heap](#heap--priority-queue--binary-heap)
    - balanced search trees (general concept, not details)
    - traversals: preorder, inorder, postorder, BFS, DFS
- [Sorting](#sorting)
    - selection
    - insertion
    - heapsort
    - quicksort
    - merge sort
- [Graphs](#graphs)
    - directed
    - undirected
    - adjacency matrix
    - adjacency list
    - traversals: BFS, DFS
- [Even More Knowledge](#even-more-knowledge)
    - [Recursion](#recursion)
    - [Object-Oriented Programming](#object-oriented-programming)
    - [Design Patterns](#design-patterns)
    - [Combinatorics (n choose k) & Probability](#combinatorics-n-choose-k--probability)
    - [NP, NP-Complete and Approximation Algorithms](#np-np-complete-and-approximation-algorithms)
    - [Caches](#caches)
    - [Processes and Threads](#processes-and-threads)
    - [Papers](#papers)
    - [Testing](#testing)
    - [Scheduling](#scheduling)
    - [Implement system routines](#implement-system-routines)
    - [String searching & manipulations](#string-searching--manipulations)
- [System Design, Scalability, Data Handling](#system-design-scalability-data-handling) (if you have 4+ years experience)
- [Final Review](#final-review)
- [Coding Question Practice](#coding-question-practice)
- [Coding exercises/challenges](#coding-exerciseschallenges)
- [Once you're closer to the interview](#once-youre-closer-to-the-interview)
- [Your Resume](#your-resume)
- [Be thinking of for when the interview comes](#be-thinking-of-for-when-the-interview-comes)
- [Have questions for the interviewer](#have-questions-for-the-interviewer)
- [Once You've Got The Job](#once-youve-got-the-job)

---------------- Everything below this point is optional ----------------

- [Additional Books](#additional-books)
- [Additional Learning](#additional-learning)
    - [Dynamic Programming](#dynamic-programming)
    - [Compilers](#compilers)
    - [Floating Point Numbers](#floating-point-numbers)
    - [Unicode](#unicode)
    - [Endianness](#endianness)
    - [Emacs and vi(m)](#emacs-and-vim)
    - [Unix command line tools](#unix-command-line-tools)
    - [Information theory](#information-theory)
    - [Parity & Hamming Code](#parity--hamming-code)
    - [Entropy](#entropy)
    - [Cryptography](#cryptography)
    - [Compression](#compression)
    - [Networking](#networking) (if you have networking experience or want to be a systems engineer, expect questions)
    - [Computer Security](#computer-security)
    - [Garbage collection](#garbage-collection)
    - [Parallel Programming](#parallel-programming)
    - [Messaging, Serialization, and Queueing Systems](#messaging-serialization-and-queueing-systems)
    - [Fast Fourier Transform](#fast-fourier-transform)
    - [Bloom Filter](#bloom-filter)
    - [HyperLogLog](#hyperloglog)
    - [Locality-Sensitive Hashing](#locality-sensitive-hashing)
    - [van Emde Boas Trees](#van-emde-boas-trees)
    - [Augmented Data Structures](#augmented-data-structures)
    - [Tries](#tries)
    - [N-ary (K-ary, M-ary) trees](#n-ary-k-ary-m-ary-trees)
    - [Balanced search trees](#balanced-search-trees)
        - AVL trees
        - Splay trees
        - Red/black trees
        - 2-3 search trees
        - 2-3-4 Trees (aka 2-4 trees)
        - N-ary (K-ary, M-ary) trees
        - B-Trees
    - [k-D Trees](#k-d-trees)
    - [Skip lists](#skip-lists)
    - [Network Flows](#network-flows)
    - [Disjoint Sets & Union Find](#disjoint-sets--union-find)
    - [Math for Fast Processing](#math-for-fast-processing)
    - [Treap](#treap)
    - [Linear Programming](#linear-programming)
    - [Geometry, Convex hull](#geometry-convex-hull)
    - [Discrete math](#discrete-math)
    - [Machine Learning](#machine-learning)
    - [Go](#go)
- [Additional Detail on Some Subjects](#additional-detail-on-some-subjects)
- [Video Series](#video-series)
- [Computer Science Courses](#computer-science-courses)

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
- [The myth of the Genius Programmer](https://www.youtube.com/watch?v=0SARbwvhupQ)
- [It's Dangerous to Go Alone: Battling the Invisible Monsters in Tech](https://www.youtube.com/watch?v=1i8ylq4j_EY)

## About Google

- [x] For students - [Google Careers: Technical Development Guide](https://www.google.com/about/careers/students/guide-to-technical-development.html)
- [ ] 구글에서 일거리 찾기:
    - [ ] [The Evolution of Search (video)](https://www.youtube.com/watch?v=mTBShTwCnD4)
    - [ ] [How Search Works - the story](https://www.google.com/insidesearch/howsearchworks/thestory/)
    - [ ] [How Search Works](https://www.google.com/insidesearch/howsearchworks/)
    - [ ] [How Search Works - Matt Cutts (video)](https://www.youtube.com/watch?v=BNHR6IQJGZs)
    - [ ] [How Google makes improvements to its search algorithm (video)](https://www.youtube.com/watch?v=J5RZOU6vK4Q)
- [ ] 시리즈들:
    - [ ] [How Google Search Dealt With Mobile](https://backchannel.com/how-google-search-dealt-with-mobile-33bc09852dc9)
    - [ ] [Google's Secret Study To Find Out Our Needs](https://backchannel.com/googles-secret-study-to-find-out-our-needs-eba8700263bf)
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
        - [ ] [게리 엘 멕도웰 지음, 이병준 옮김 - http://www.kyobobook.co.kr/product/detailViewKor.laf?mallGb=KOR&barcode=9788966260485]
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

## Book List

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

## System Design, Scalability, Data Handling
- **You can expect system design questions if you have 4+ years of experience.**
- Scalability and System Design are very large topics with many topics and resources, since
      there is a lot to consider when designing a software/hardware system that can scale.
      Expect to spend quite a bit of time on this.
- Considerations from Yegge:
    - scalability
        - Distill large data sets to single values
        - Transform one data set to another
        - Handling obscenely large amounts of data
    - system design
        - features sets
        - interfaces
        - class hierarchies
        - designing a system under certain constraints
        - simplicity and robustness
        - tradeoffs
        - performance analysis and optimization
- [ ] **START HERE**: [System Design from HiredInTech](http://www.hiredintech.com/system-design/)
- [ ] [How Do I Prepare To Answer Design Questions In A Technical Inverview?](https://www.quora.com/How-do-I-prepare-to-answer-design-questions-in-a-technical-interview?redirected_qid=1500023)
- [ ] [8 Things You Need to Know Before a System Design Interview](http://blog.gainlo.co/index.php/2015/10/22/8-things-you-need-to-know-before-system-design-interviews/)
- [ ] [Algorithm design](http://www.hiredintech.com/algorithm-design/)
- [ ] [Database Normalization - 1NF, 2NF, 3NF and 4NF (video)](https://www.youtube.com/watch?v=UrYLYV7WSHM)
- [ ] [System Design Interview](https://github.com/checkcheckzz/system-design-interview) - There are a lot of resources in this one. Look through the articles and examples. I put some of them below.
- [ ] [How to ace a systems design interview](http://www.palantir.com/2011/10/how-to-rock-a-systems-design-interview/)
- [ ] [Numbers Everyone Should Know](http://everythingisdata.wordpress.com/2009/10/17/numbers-everyone-should-know/)
- [ ] [How long does it take to make a context switch?](http://blog.tsunanet.net/2010/11/how-long-does-it-take-to-make-context.html)
- [ ] [Transactions Across Datacenters (video)](https://www.youtube.com/watch?v=srOgpXECblk)
- [ ] [A plain English introduction to CAP Theorem](http://ksat.me/a-plain-english-introduction-to-cap-theorem/)
- [ ] Paxos Consensus algorithm:
    - [short video](https://www.youtube.com/watch?v=s8JqcZtvnsM)
    - [extended video with use case and multi-paxos](https://www.youtube.com/watch?v=JEpsBg0AO6o)
    - [paper](http://research.microsoft.com/en-us/um/people/lamport/pubs/paxos-simple.pdf)
- [ ] [Consistent Hashing](http://www.tom-e-white.com/2007/11/consistent-hashing.html)
- [ ] [NoSQL Patterns](http://horicky.blogspot.com/2009/11/nosql-patterns.html)
- [ ] Scalability:
    - [ ] [Great overview (video)](https://www.youtube.com/watch?v=-W9F__D3oY4)
    - [ ] Short series:
        - [Clones](http://www.lecloud.net/post/7295452622/scalability-for-dummies-part-1-clones)
        - [Database](http://www.lecloud.net/post/7994751381/scalability-for-dummies-part-2-database)
        - [Cache](http://www.lecloud.net/post/9246290032/scalability-for-dummies-part-3-cache)
        - [Asynchronism](http://www.lecloud.net/post/9699762917/scalability-for-dummies-part-4-asynchronism)
    - [ ] [Scalable Web Architecture and Distributed Systems](http://www.aosabook.org/en/distsys.html)
    - [ ] [Fallacies of Distributed Computing Explained](https://pages.cs.wisc.edu/~zuyu/files/fallacies.pdf)
    - [ ] [Pragmatic Programming Techniques](http://horicky.blogspot.com/2010/10/scalable-system-design-patterns.html)
        - [extra: Google Pregel Graph Processing](http://horicky.blogspot.com/2010/07/google-pregel-graph-processing.html)
    - [ ] [Jeff Dean - Building Software Systems At Google and Lessons Learned (video)](https://www.youtube.com/watch?v=modXC5IWTJI)
    - [ ] [Introduction to Architecting Systems for Scale](http://lethain.com/introduction-to-architecting-systems-for-scale/)
    - [ ] [Scaling mobile games to a global audience using App Engine and Cloud Datastore (video)](https://www.youtube.com/watch?v=9nWyWwY2Onc)
    - [ ] [How Google Does Planet-Scale Engineering for Planet-Scale Infra (video)](https://www.youtube.com/watch?v=H4vMcD7zKM0)
    - [ ] [The Importance of Algorithms](https://www.topcoder.com/community/data-science/data-science-tutorials/the-importance-of-algorithms/)
    - [ ] [Sharding](http://highscalability.com/blog/2009/8/6/an-unorthodox-approach-to-database-design-the-coming-of-the.html)
    - [ ] [Scale at Facebook (2009)](https://www.infoq.com/presentations/Scale-at-Facebook)
    - [ ] [Scale at Facebook (2012), "Building for a Billion Users" (video)](https://www.youtube.com/watch?v=oodS71YtkGU)
    - [ ] [Engineering for the Long Game - Astrid Atkinson Keynote(video)](https://www.youtube.com/watch?v=p0jGmgIrf_M&list=PLRXxvay_m8gqVlExPC5DG3TGWJTaBgqSA&index=4)
    - [ ] [7 Years Of YouTube Scalability Lessons In 30 Minutes](http://highscalability.com/blog/2012/3/26/7-years-of-youtube-scalability-lessons-in-30-minutes.html)
        - [video](https://www.youtube.com/watch?v=G-lGCC4KKok)
    - [ ] [How PayPal Scaled To Billions Of Transactions Daily Using Just 8VMs](http://highscalability.com/blog/2016/8/15/how-paypal-scaled-to-billions-of-transactions-daily-using-ju.html)
    - [ ] [How to Remove Duplicates in Large Datasets](https://blog.clevertap.com/how-to-remove-duplicates-in-large-datasets/)
    - [ ] [A look inside Etsy's scale and engineering culture with Jon Cowie (video)](https://www.youtube.com/watch?v=3vV4YiqKm1o)
    - [ ] [What Led Amazon to its Own Microservices Architecture](http://thenewstack.io/led-amazon-microservices-architecture/)
    - [ ] [To Compress Or Not To Compress, That Was Uber's Question](https://eng.uber.com/trip-data-squeeze/)
    - [ ] [Asyncio Tarantool Queue, Get In The Queue](http://highscalability.com/blog/2016/3/3/asyncio-tarantool-queue-get-in-the-queue.html)
    - [ ] [When Should Approximate Query Processing Be Used?](http://highscalability.com/blog/2016/2/25/when-should-approximate-query-processing-be-used.html)
    - [ ] [Google's Transition From Single Datacenter, To Failover, To A Native Multihomed Architecture]( http://highscalability.com/blog/2016/2/23/googles-transition-from-single-datacenter-to-failover-to-a-n.html)
    - [ ] [Spanner](http://highscalability.com/blog/2012/9/24/google-spanners-most-surprising-revelation-nosql-is-out-and.html)
    - [ ] [Egnyte Architecture: Lessons Learned In Building And Scaling A Multi Petabyte Distributed System](http://highscalability.com/blog/2016/2/15/egnyte-architecture-lessons-learned-in-building-and-scaling.html)
    - [ ] [Machine Learning Driven Programming: A New Programming For A New World](http://highscalability.com/blog/2016/7/6/machine-learning-driven-programming-a-new-programming-for-a.html)
    - [ ] [The Image Optimization Technology That Serves Millions Of Requests Per Day](http://highscalability.com/blog/2016/6/15/the-image-optimization-technology-that-serves-millions-of-re.html)
    - [ ] [A Patreon Architecture Short](http://highscalability.com/blog/2016/2/1/a-patreon-architecture-short.html)
    - [ ] [Tinder: How Does One Of The Largest Recommendation Engines Decide Who You'll See Next?](http://highscalability.com/blog/2016/1/27/tinder-how-does-one-of-the-largest-recommendation-engines-de.html)
    - [ ] [Design Of A Modern Cache](http://highscalability.com/blog/2016/1/25/design-of-a-modern-cache.html)
    - [ ] [Live Video Streaming At Facebook Scale](http://highscalability.com/blog/2016/1/13/live-video-streaming-at-facebook-scale.html)
    - [ ] [A Beginner's Guide To Scaling To 11 Million+ Users On Amazon's AWS](http://highscalability.com/blog/2016/1/11/a-beginners-guide-to-scaling-to-11-million-users-on-amazons.html)
    - [ ] [How Does The Use Of Docker Effect Latency?](http://highscalability.com/blog/2015/12/16/how-does-the-use-of-docker-effect-latency.html)
    - [ ] [Does AMP Counter An Existential Threat To Google?](http://highscalability.com/blog/2015/12/14/does-amp-counter-an-existential-threat-to-google.html)
    - [ ] [A 360 Degree View Of The Entire Netflix Stack](http://highscalability.com/blog/2015/11/9/a-360-degree-view-of-the-entire-netflix-stack.html)
    - [ ] [Latency Is Everywhere And It Costs You Sales - How To Crush It](http://highscalability.com/latency-everywhere-and-it-costs-you-sales-how-crush-it)
    - [ ] [Serverless (very long, just need the gist)](http://martinfowler.com/articles/serverless.html)
    - [ ] [What Powers Instagram: Hundreds of Instances, Dozens of Technologies](http://instagram-engineering.tumblr.com/post/13649370142/what-powers-instagram-hundreds-of-instances)
    - [ ] [Cinchcast Architecture - Producing 1,500 Hours Of Audio Every Day](http://highscalability.com/blog/2012/7/16/cinchcast-architecture-producing-1500-hours-of-audio-every-d.html)
    - [ ] [Justin.Tv's Live Video Broadcasting Architecture](http://highscalability.com/blog/2010/3/16/justintvs-live-video-broadcasting-architecture.html)
    - [ ] [Playfish's Social Gaming Architecture - 50 Million Monthly Users And Growing](http://highscalability.com/blog/2010/9/21/playfishs-social-gaming-architecture-50-million-monthly-user.html)
    - [ ] [TripAdvisor Architecture - 40M Visitors, 200M Dynamic Page Views, 30TB Data](http://highscalability.com/blog/2011/6/27/tripadvisor-architecture-40m-visitors-200m-dynamic-page-view.html)
    - [ ] [PlentyOfFish Architecture](http://highscalability.com/plentyoffish-architecture)
    - [ ] [Salesforce Architecture - How They Handle 1.3 Billion Transactions A Day](http://highscalability.com/blog/2013/9/23/salesforce-architecture-how-they-handle-13-billion-transacti.html)
    - [ ] [ESPN's Architecture At Scale - Operating At 100,000 Duh Nuh Nuhs Per Second](http://highscalability.com/blog/2013/11/4/espns-architecture-at-scale-operating-at-100000-duh-nuh-nuhs.html)
    - [ ] See "Messaging, Serialization, and Queueing Systems" way below for info on some of the technologies that can glue services together
    - [ ] Twitter:
        - [O'Reilly MySQL CE 2011: Jeremy Cole, "Big and Small Data at @Twitter" (video)](https://www.youtube.com/watch?v=5cKTP36HVgI)
        - [Timelines at Scale](https://www.infoq.com/presentations/Twitter-Timeline-Scalability)
    - For even more, see "Mining Massive Datasets" video series in the Video Series section.
- [ ] Practicing the system design process: Here are some ideas to try working through on paper, each with some documentation on how it was handled in the real world:
    - review: [System Design from HiredInTech](http://www.hiredintech.com/system-design/)
    - [cheat sheet](https://github.com/jwasham/google-interview-university/blob/master/extras/cheat%20sheets/system-design.pdf)
    - flow:
        1. Understand the problem and scope:
            - define the use cases, with interviewer's help
            - suggest additional features
            - remove items that interviewer deems out of scope
            - assume high availability is required, add as a use case
        2. Think about constraints:
            - ask how many requests per month
            - ask how many requests per second (they may volunteer it or make you do the math)
            - estimate reads vs. writes percentage
            - keep 80/20 rule in mind when estimating
            - how much data written per second
            - total storage required over 5 years
            - how much data read per second
        3. Abstract design:
            - layers (service, data, caching)
            - infrastructure: load balancing, messaging
            - rough overview of any key algorithm that drives the service
            - consider bottlenecks and determine solutions
    - Exercises:
        - [Design a CDN network: old article](http://repository.cmu.edu/cgi/viewcontent.cgi?article=2112&context=compsci)
        - [Design a random unique ID generation system](https://blog.twitter.com/2010/announcing-snowflake)
        - [Design an online multiplayer card game](http://www.indieflashblog.com/how-to-create-an-asynchronous-multiplayer-game.html)
        - [Design a key-value database](http://www.slideshare.net/dvirsky/introduction-to-redis)
        - [Design a function to return the top k requests during past time interval]( https://icmi.cs.ucsb.edu/research/tech_reports/reports/2005-23.pdf)
        - [Design a picture sharing system](http://highscalability.com/blog/2011/12/6/instagram-architecture-14-million-users-terabytes-of-photos.html)
        - [Design a recommendation system](http://ijcai13.org/files/tutorial_slides/td3.pdf)
        - [Design a URL-shortener system: copied from above](http://www.hiredintech.com/system-design/the-system-design-process/)
        - [Design a cache system](https://www.adayinthelifeof.nl/2011/02/06/memcache-internals/)

---

## Final Review

    This section will have shorter videos that can you watch pretty quickly to review most of the important concepts.
    It's nice if you want a refresher often.

- [ ] Series of 2-3 minutes short subject videos (23 videos)
    - [Videos](https://www.youtube.com/watch?v=r4r1DZcx1cM&list=PLmVb1OknmNJuC5POdcDv5oCS7_OUkDgpj&index=22)
- [ ] Series of 2-5 minutes short subject videos - Michael Sambol (18 videos):
    - [Videos](https://www.youtube.com/channel/UCzDJwLWoYCUQowF_nG3m5OQ)
- [ ] [Sedgewick Videos - Algorithms I](https://www.youtube.com/user/algorithmscourses/playlists?shelf_id=2&view=50&sort=dd)
    - [ ] [01. Union-Find](https://www.youtube.com/watch?v=8mYfZeHtdNc&list=PLe-ggMe31CTexoNYnMhbHaWhQ0dvcy43t)
    - [ ] [02. Analysis of Algorithms](https://www.youtube.com/watch?v=ZN-nFW0mEpg&list=PLe-ggMe31CTf0_bkOhh7sa5uqeppp3Sr0)
    - [ ] [03. Stacks and Queues](https://www.youtube.com/watch?v=TIC1gappbP8&list=PLe-ggMe31CTe-9jhnj3P_3mmrCh0A7iHh)
    - [ ] [04. Elementary Sorts](https://www.youtube.com/watch?v=CD2AL6VO0ak&list=PLe-ggMe31CTe_5WhGV0F--7CK8MoRUqBd)
    - [ ] [05. Mergesort](https://www.youtube.com/watch?v=4nKwesx_c8E&list=PLe-ggMe31CTeunC6GZHFBmQx7EKtjbGf9)
    - [ ] [06. Quicksort](https://www.youtube.com/watch?v=5M5A7qPWk84&list=PLe-ggMe31CTeE3x2-nF1-toca1QpuXwE1)
    - [ ] [07. Priority Queues](https://www.youtube.com/watch?v=G9TMe0KC0w0&list=PLe-ggMe31CTducy9LDiGVkdSv0NfiRwn5)
    - [ ] [08. Elementary Symbol Tables](https://www.youtube.com/watch?v=up_nlilw3ac&list=PLe-ggMe31CTc3a8nKRDxFZZrWrBvkc9SG)
    - [ ] [09. Balanced Search Trees](https://www.youtube.com/watch?v=qC1BLLPK_5w&list=PLe-ggMe31CTf7jHH_mFT50kayjCEA6Rhu)
    - [ ] [10. Geometric Applications of BST](https://www.youtube.com/watch?v=Wl30aGAp6TY&list=PLe-ggMe31CTdBsRIw0hXln0hilRs-DqAx)
    - [ ] [11. Hash Tables](https://www.youtube.com/watch?v=QA8fJGO-i9o&list=PLe-ggMe31CTcKxIRGqqThMts2eHtSrf11)
- [ ] [Sedgewick Videos - Algorithms II](https://www.youtube.com/user/algorithmscourses/playlists?flow=list&shelf_id=3&view=50)
    - [ ] [01. Undirected Graphs](https://www.youtube.com/watch?v=GmVhD-mmMBg&list=PLe-ggMe31CTc0zDzANxl4I2MhMoRVlbRM)
    - [ ] [02. Directed Graphs](https://www.youtube.com/watch?v=_z-JsVaUS40&list=PLe-ggMe31CTcEwaU8a1P1Gd95A77HV85K)
    - [ ] [03. Minimum Spanning Trees](https://www.youtube.com/watch?v=t8fNk9tfVYY&list=PLe-ggMe31CTceUZxDesGfHGLE7kcSafqj)
    - [ ] [04. Shortest Paths](https://www.youtube.com/watch?v=HoGSiB7tSeI&list=PLe-ggMe31CTePpG3jbeOTsnGUGZDKxgZD)
    - [ ] [05. Maximum Flow](https://www.youtube.com/watch?v=rYIKlFstBqE&list=PLe-ggMe31CTduQ68XQ-sVj32wYJIspTma)
    - [ ] [06. Radix Sorts](https://www.youtube.com/watch?v=HKPrVm5FWvg&list=PLe-ggMe31CTcNvUX9E3tQeM6ntrdR8e53)
    - [ ] [07. Tries](https://www.youtube.com/watch?v=00YaFPcC65g&list=PLe-ggMe31CTe9IyG9MB8vt5xUJeYgOYRQ)
    - [ ] [08. Substring Search](https://www.youtube.com/watch?v=QzI0p6zDjK4&list=PLe-ggMe31CTdAdjXB3lIuf2maubzo9t66)
    - [ ] [09. Regular Expressions](https://www.youtube.com/watch?v=TQWNQsJSPnk&list=PLe-ggMe31CTetTlJWouM42fyttyKPgSDh)
    - [ ] [10. Data Compression](https://www.youtube.com/watch?v=at9tjpxcBh8&list=PLe-ggMe31CTciifRRo6yY0Yt0mzgIXXVZ)
    - [ ] [11. Reductions](https://www.youtube.com/watch?v=Ow5x-ooMGv8&list=PLe-ggMe31CTe_yliW5vc3yO-dj1LSSDyF)
    - [ ] [12. Linear Programming](https://www.youtube.com/watch?v=rWhcLyiLZLA&list=PLe-ggMe31CTdy6dKzMgkWFuTTN1H8B-E1)
    - [ ] [13. Intractability](https://www.youtube.com/watch?v=6qcaaDp4cdQ&list=PLe-ggMe31CTcZCjluBHw53e_ek2k9Kn-S)

---

## Coding Question Practice

Now that you know all the computer science topics above, it's time to practice answering coding problems.

**Coding question practice is not about memorizing answers to programming problems.**

Why you need to practice doing programming problems:
- problem recognition, and where the right data structures and algorithms fit in
- gathering requirements for the problem
- talking your way through the problem like you will in the interview
- coding on a whiteboard or paper, not a computer
- coming up with time and space complexity for your solutions
- testing your solutions

There is a great intro for methodical, communicative problem solving in an interview. You'll get this from the programming
interview books, too, but I found this outstanding:
[Algorithm design canvas](http://www.hiredintech.com/algorithm-design/)

[My Process for Coding Interview (Book) Exercises](https://googleyasheck.com/my-process-for-coding-interview-exercises/)

No whiteboard at home? That makes sense. I'm a weirdo and have a big whiteboard. Instead of a whiteboard, pick up a
large drawing pad from an art store. You can sit on the couch and practice. This is my "sofa whiteboard".
I added the pen in the photo for scale. If you use a pen, you'll wish you could erase. Gets messy quick.

![my sofa whiteboard](https://dng5l3qzreal6.cloudfront.net/2016/Oct/art_board_sm_2-1476233630368.jpg)

Supplemental:

- [Mathematics for Topcoders](https://www.topcoder.com/community/data-science/data-science-tutorials/mathematics-for-topcoders/)
- [Dynamic Programming – From Novice to Advanced](https://www.topcoder.com/community/data-science/data-science-tutorials/dynamic-programming-from-novice-to-advanced/)
- [MIT Interview Materials](https://web.archive.org/web/20160906124824/http://courses.csail.mit.edu/iap/interview/materials.php)
- [Exercises for getting better at a given language](http://exercism.io/languages)

**Read and Do Programming Problems (in this order):**

- [ ] [Programming Interviews Exposed: Secrets to Landing Your Next Job, 2nd Edition](http://www.wiley.com/WileyCDA/WileyTitle/productCd-047012167X.html)
    - answers in C, C++ and Java
- [ ] [Cracking the Coding Interview, 6th Edition](http://www.amazon.com/Cracking-Coding-Interview-6th-Programming/dp/0984782850/)
    - answers in Java

See [Book List above](#book-list)

## Coding exercises/challenges

Once you've learned your brains out, put those brains to work.
Take coding challenges every day, as many as you can.

- [ ] [How to Find a Solution](https://www.topcoder.com/community/data-science/data-science-tutorials/how-to-find-a-solution/)
- [ ] [How to Dissect a Topcoder Problem Statement](https://www.topcoder.com/community/data-science/data-science-tutorials/how-to-dissect-a-topcoder-problem-statement/)

Challenge sites:
- [LeetCode](https://leetcode.com/)
- [TopCoder](https://www.topcoder.com/)
- [Project Euler (math-focused)](https://projecteuler.net/index.php?section=problems)
- [Codewars](http://www.codewars.com)
- [HackerRank](https://www.hackerrank.com/)
- [Codility](https://codility.com/programmers/)
- [InterviewCake](https://www.interviewcake.com/)
- [Geeks for Geeks](http://www.geeksforgeeks.org/)
- [InterviewBit](https://www.interviewbit.com/invite/icjf)

Maybe:
- [Mock interviewers from big companies](http://www.gainlo.co/)

## Once you're closer to the interview

- [ ] Cracking The Coding Interview Set 2 (videos):
    - [Cracking The Code Interview](https://www.youtube.com/watch?v=4NIb9l3imAo)
    - [Cracking the Coding Interview - Fullstack Speaker Series](https://www.youtube.com/watch?v=Eg5-tdAwclo)
    - [Ask Me Anything: Gayle Laakmann McDowell (author of Cracking the Coding Interview)](https://www.youtube.com/watch?v=1fqxMuPmGak)

## Your Resume

- [Ten Tips for a (Slightly) Less Awful Resume](http://steve-yegge.blogspot.co.uk/2007_09_01_archive.html)
- See Resume prep items in Cracking The Coding Interview and back of Programming Interviews Exposed


## Be thinking of for when the interview comes

Think of about 20 interview questions you'll get, along with the lines of the items below. Have 2-3 answers for each.
Have a story, not just data, about something you accomplished.

- Why do you want this job?
- What's a tough problem you've solved?
- Biggest challenges faced?
- Best/worst designs seen?
- Ideas for improving an existing Google product.
- How do you work best, as an individual and as part of a team?
- Which of your skills or experiences would be assets in the role and why?
- What did you most enjoy at [job x / project y]?
- What was the biggest challenge you faced at [job x / project y]?
- What was the hardest bug you faced at [job x / project y]?
- What did you learn at [job x / project y]?
- What would you have done better at [job x / project y]?

## Have questions for the interviewer

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

Congratulations!

- [10 things I wish I knew on my first day at Google](https://medium.com/@moonstorming/10-things-i-wish-i-knew-on-my-first-day-at-google-107581d87286#.livxn7clw)

Keep learning.

You're never really done.

---

    *****************************************************************************************************
    *****************************************************************************************************

    Everything below this point is optional. These are my recommendations, not Google's.
    By studying these, you'll get greater exposure to more CS concepts, and will be better prepared for
    any software engineering job. You'll be a much more well-rounded software engineer.

    *****************************************************************************************************
    *****************************************************************************************************

---

## Additional Books

- [ ] [The Unix Programming Environment](http://product.half.ebay.com/The-UNIX-Programming-Environment-by-Brian-W-Kernighan-and-Rob-Pike-1983-Other/54385&tg=info)
    - an oldie but a goodie
- [ ] [The Linux Command Line: A Complete Introduction](https://www.amazon.com/dp/1593273894/)
    - a modern option
- [ ] [TCP/IP Illustrated Series](https://en.wikipedia.org/wiki/TCP/IP_Illustrated)
- [ ] [Head First Design Patterns](https://www.amazon.com/gp/product/0596007124/)
    - a gentle introduction to design patterns
- [ ] [Design Patterns: Elements of Reusable Object-Oriente​d Software](https://www.amazon.com/Design-Patterns-Elements-Reusable-Object-Oriented/dp/0201633612)
    - aka the "Gang Of Four" book, or GOF
    - the canonical design patterns book
- [ ] [Site Reliability Engineering](https://landing.google.com/sre/book.html)
    - [Site Reliability Engineering: How Google Runs Production Systems](https://landing.google.com/sre/)
- [ ] [UNIX and Linux System Administration Handbook, 4th Edition](https://www.amazon.com/UNIX-Linux-System-Administration-Handbook/dp/0131480057/)

## Additional Learning

- ### Dynamic Programming
    - This subject can be pretty difficult, as each DP soluble problem must be defined as a recursion relation, and coming up with it can be tricky.
    - I suggest looking at many examples of DP problems until you have a solid understanding of the pattern involved.
    - [ ] Videos:
        - the Skiena videos can be hard to follow since he sometimes uses the whiteboard, which is too small to see
        - [ ] [Skiena: CSE373 2012 - Lecture 19 - Introduction to Dynamic Programming (video)](https://youtu.be/Qc2ieXRgR0k?list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b&t=1718)
        - [ ] [Skiena: CSE373 2012 - Lecture 20 - Edit Distance (video)](https://youtu.be/IsmMhMdyeGY?list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b&t=2749)
        - [ ] [Skiena: CSE373 2012 - Lecture 21 - Dynamic Programming Examples (video)](https://youtu.be/o0V9eYF4UI8?list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b&t=406)
        - [ ] [Skiena: CSE373 2012 - Lecture 22 - Applications of Dynamic Programming (video)](https://www.youtube.com/watch?v=dRbMC1Ltl3A&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b&index=22)
        - [ ] [Simonson: Dynamic Programming 0 (starts at 59:18) (video)](https://youtu.be/J5aJEcOr6Eo?list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&t=3558)
        - [ ] [Simonson: Dynamic Programming I - Lecture 11 (video)](https://www.youtube.com/watch?v=0EzHjQ_SOeU&index=11&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm)
        - [ ] [Simonson: Dynamic programming II - Lecture 12 (video)](https://www.youtube.com/watch?v=v1qiRwuJU7g&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&index=12)
        - [ ] List of individual DP problems (each is short):
            [Dynamic Programming (video)](https://www.youtube.com/playlist?list=PLrmLmBdmIlpsHaNTPP_jHHDx_os9ItYXr)
    - [ ] Yale Lecture notes:
        - [ ] [Dynamic Programming](http://www.cs.yale.edu/homes/aspnes/classes/223/notes.html#dynamicProgramming)
    - [ ] Coursera:
        - [ ] [The RNA secondary structure problem (video)](https://www.coursera.org/learn/algorithmic-thinking-2/lecture/80RrW/the-rna-secondary-structure-problem)
        - [ ] [A dynamic programming algorithm (video)](https://www.coursera.org/learn/algorithmic-thinking-2/lecture/PSonq/a-dynamic-programming-algorithm)
        - [ ] [Illustrating the DP algorithm (video)](https://www.coursera.org/learn/algorithmic-thinking-2/lecture/oUEK2/illustrating-the-dp-algorithm)
        - [ ] [Running time of the DP algorithm (video)](https://www.coursera.org/learn/algorithmic-thinking-2/lecture/nfK2r/running-time-of-the-dp-algorithm)
        - [ ] [DP vs. recursive implementation (video)](https://www.coursera.org/learn/algorithmic-thinking-2/lecture/M999a/dp-vs-recursive-implementation)
        - [ ] [Global pairwise sequence alignment (video)](https://www.coursera.org/learn/algorithmic-thinking-2/lecture/UZ7o6/global-pairwise-sequence-alignment)
        - [ ] [Local pairwise sequence alignment (video)](https://www.coursera.org/learn/algorithmic-thinking-2/lecture/WnNau/local-pairwise-sequence-alignment)

- ### Compilers
    - [ ] [How a Compiler Works in ~1 minute (video)](https://www.youtube.com/watch?v=IhC7sdYe-Jg)
    - [ ] [Harvard CS50 - Compilers (video)](https://www.youtube.com/watch?v=CSZLNYF4Klo)
    - [ ] [C++ (video)](https://www.youtube.com/watch?v=twodd1KFfGk)
    - [ ] [Understanding Compiler Optimization (C++) (video)](https://www.youtube.com/watch?v=FnGCDLhaxKU)

- ### Floating Point Numbers
    - [ ] simple 8-bit: [Representation of Floating Point Numbers - 1 (video - there is an error in calculations - see video description)](https://www.youtube.com/watch?v=ji3SfClm8TU)
    - [ ] 32 bit: [IEEE754 32-bit floating point binary (video)](https://www.youtube.com/watch?v=50ZYcZebIec)

- ### Unicode
    - [ ] [The Absolute Minimum Every Software Developer Absolutely, Positively Must Know About Unicode and Character Sets]( http://www.joelonsoftware.com/articles/Unicode.html)
    - [ ] [What Every Programmer Absolutely, Positively Needs To Know About Encodings And Character Sets To Work With Text](http://kunststube.net/encoding/)

- ### Endianness
    - [ ] [Big And Little Endian](https://www.cs.umd.edu/class/sum2003/cmsc311/Notes/Data/endian.html)
    - [ ] [Big Endian Vs Little Endian (video)](https://www.youtube.com/watch?v=JrNF0KRAlyo)
    - [ ] [Big And Little Endian Inside/Out (video)](https://www.youtube.com/watch?v=oBSuXP-1Tc0)
        - Very technical talk for kernel devs. Don't worry if most is over your head.
        - The first half is enough.

- ### Emacs and vi(m)
    - suggested by Yegge, from an old Amazon recruiting post: Familiarize yourself with a unix-based code editor
    - vi(m):
        - [Editing With vim 01 - Installation, Setup, and The Modes (video)](https://www.youtube.com/watch?v=5givLEMcINQ&index=1&list=PL13bz4SHGmRxlZVmWQ9DvXo1fEg4UdGkr)
        - [VIM Adventures](http://vim-adventures.com/)
        - set of 4 videos:
            - [The vi/vim editor - Lesson 1](https://www.youtube.com/watch?v=SI8TeVMX8pk)
            - [The vi/vim editor - Lesson 2](https://www.youtube.com/watch?v=F3OO7ZIOaJE)
            - [The vi/vim editor - Lesson 3](https://www.youtube.com/watch?v=ZYEccA_nMaI)
            - [The vi/vim editor - Lesson 4](https://www.youtube.com/watch?v=1lYD5gwgZIA)
        - [Using Vi Instead of Emacs](http://www.cs.yale.edu/homes/aspnes/classes/223/notes.html#Using_Vi_instead_of_Emacs)
    - emacs:
        - [Basics Emacs Tutorial (video)](https://www.youtube.com/watch?v=hbmV1bnQ-i0)
        - set of 3 (videos):
            - [Emacs Tutorial (Beginners) -Part 1- File commands, cut/copy/paste, cursor commands](https://www.youtube.com/watch?v=ujODL7MD04Q)
            - [Emacs Tutorial (Beginners) -Part 2- Buffer management, search, M-x grep and rgrep modes](https://www.youtube.com/watch?v=XWpsRupJ4II)
            - [Emacs Tutorial (Beginners) -Part 3- Expressions, Statements, ~/.emacs file and packages](https://www.youtube.com/watch?v=paSgzPso-yc)
        - [Evil Mode: Or, How I Learned to Stop Worrying and Love Emacs (video)](https://www.youtube.com/watch?v=JWD1Fpdd4Pc)
        - [Writing C Programs With Emacs](http://www.cs.yale.edu/homes/aspnes/classes/223/notes.html#Writing_C_programs_with_Emacs)
        - [(maybe) Org Mode In Depth: Managing Structure (video)](https://www.youtube.com/watch?v=nsGYet02bEk)

- ### Unix command line tools
    - suggested by Yegge, from an old Amazon recruiting post. I filled in the list below from good tools.
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

- ### Information theory (videos)
    - [ ] [Khan Academy](https://www.khanacademy.org/computing/computer-science/informationtheory)
    - [ ] more about Markov processes:
        - [ ] [Core Markov Text Generation](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/waxgx/core-markov-text-generation)
        - [ ] [Core Implementing Markov Text Generation](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/gZhiC/core-implementing-markov-text-generation)
        - [ ] [Project = Markov Text Generation Walk Through](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/EUjrq/project-markov-text-generation-walk-through)
    - See more in MIT 6.050J Information and Entropy series below.

- ### Parity & Hamming Code (videos)
    - [ ] [Intro](https://www.youtube.com/watch?v=q-3BctoUpHE)
    - [ ] [Parity](https://www.youtube.com/watch?v=DdMcAUlxh1M)
    - [ ] Hamming Code:
        - [Error detection](https://www.youtube.com/watch?v=1A_NcXxdoCc)
        - [Error correction](https://www.youtube.com/watch?v=JAMLuxdHH8o)
    - [ ] [Error Checking](https://www.youtube.com/watch?v=wbH2VxzmoZk)

- ### Entropy
    - also see videos below
    - make sure to watch information theory videos first
    - [ ] [Information Theory, Claude Shannon, Entropy, Redundancy, Data Compression & Bits (video)](https://youtu.be/JnJq3Py0dyM?t=176)

- ### Cryptography
    - also see videos below
    - make sure to watch information theory videos first
    - [ ] [Khan Academy Series](https://www.khanacademy.org/computing/computer-science/cryptography)
    - [ ] [Cryptography: Hash Functions](https://www.youtube.com/watch?v=KqqOXndnvic&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=30)
    - [ ] [Cryptography: Encryption](https://www.youtube.com/watch?v=9TNI2wHmaeI&index=31&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp)

- ### Compression
    - make sure to watch information theory videos first
    - [ ] Computerphile (videos):
        - [ ] [Compression](https://www.youtube.com/watch?v=Lto-ajuqW3w)
        - [ ] [Entropy in Compression](https://www.youtube.com/watch?v=M5c_RFKVkko)
        - [ ] [Upside Down Trees (Huffman Trees)](https://www.youtube.com/watch?v=umTbivyJoiI)
        - [ ] [EXTRA BITS/TRITS - Huffman Trees](https://www.youtube.com/watch?v=DV8efuB3h2g)
        - [ ] [Elegant Compression in Text (The LZ 77 Method)](https://www.youtube.com/watch?v=goOa3DGezUA)
        - [ ] [Text Compression Meets Probabilities](https://www.youtube.com/watch?v=cCDCfoHTsaU)
    - [ ] [Compressor Head videos](https://www.youtube.com/playlist?list=PLOU2XLYxmsIJGErt5rrCqaSGTMyyqNt2H)
    - [ ] [(optional) Google Developers Live: GZIP is not enough!](https://www.youtube.com/watch?v=whGwm0Lky2s)

- ### Networking
    - **if you have networking experience or want to be a systems engineer, expect questions**
    - otherwise, this is just good to know
    - [ ] [Khan Academy](https://www.khanacademy.org/computing/computer-science/internet-intro)
    - [ ] [UDP and TCP: Comparison of Transport Protocols](https://www.youtube.com/watch?v=Vdc8TCESIg8)
    - [ ] [TCP/IP and the OSI Model Explained!](https://www.youtube.com/watch?v=e5DEVa9eSN0)
    - [ ] [Packet Transmission across the Internet. Networking & TCP/IP tutorial.](https://www.youtube.com/watch?v=nomyRJehhnM)
    - [ ] [HTTP](https://www.youtube.com/watch?v=WGJrLqtX7As)
    - [ ] [SSL and HTTPS](https://www.youtube.com/watch?v=S2iBR2ZlZf0)
    - [ ] [SSL/TLS](https://www.youtube.com/watch?v=Rp3iZUvXWlM)
    - [ ] [HTTP 2.0](https://www.youtube.com/watch?v=E9FxNzv1Tr8)
    - [ ] [Video Series (21 videos)](https://www.youtube.com/playlist?list=PLEbnTDJUr_IegfoqO4iPnPYQui46QqT0j)
    - [ ] [Subnetting Demystified - Part 5 CIDR Notation](https://www.youtube.com/watch?v=t5xYI0jzOf4)

- ### Computer Security
    - [MIT (23 videos)](https://www.youtube.com/playlist?list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
        - [ ] [Introduction, Threat Models](https://www.youtube.com/watch?v=GqmQg-cszw4&index=1&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
        - [ ] [Control Hijacking Attacks](https://www.youtube.com/watch?v=6bwzNg5qQ0o&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh&index=2)
        - [ ] [Buffer Overflow Exploits and Defenses](https://www.youtube.com/watch?v=drQyrzRoRiA&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh&index=3)
        - [ ] [Privilege Separation](https://www.youtube.com/watch?v=6SIJmoE9L9g&index=4&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
        - [ ] [Capabilities](https://www.youtube.com/watch?v=8VqTSY-11F4&index=5&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
        - [ ] [Sandboxing Native Code](https://www.youtube.com/watch?v=VEV74hwASeU&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh&index=6)
        - [ ] [Web Security Model](https://www.youtube.com/watch?v=chkFBigodIw&index=7&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
        - [ ] [Securing Web Applications](https://www.youtube.com/watch?v=EBQIGy1ROLY&index=8&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
        - [ ] [Symbolic Execution](https://www.youtube.com/watch?v=yRVZPvHYHzw&index=9&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
        - [ ] [Network Security](https://www.youtube.com/watch?v=SIEVvk3NVuk&index=11&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
        - [ ] [Network Protocols](https://www.youtube.com/watch?v=QOtA76ga_fY&index=12&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)
        - [ ] [Side-Channel Attacks](https://www.youtube.com/watch?v=PuVMkSEcPiI&index=15&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)

- ### Garbage collection
    - [ ] [Garbage collection (Java); Augmenting data str (video)](https://www.youtube.com/watch?v=StdfeXaKGEc&list=PL-XXv-cvA_iAlnI-BQr9hjqADPBtujFJd&index=25)
    - [ ] [Compilers (video)](https://www.youtube.com/playlist?list=PLO9y7hOkmmSGTy5z6HZ-W4k2y8WXF7Bff)
    - [ ] [GC in Python (video)](https://www.youtube.com/watch?v=iHVs_HkjdmI)
    - [ ] [Deep Dive Java: Garbage Collection is Good!](https://www.infoq.com/presentations/garbage-collection-benefits)
    - [ ] [Deep Dive Python: Garbage Collection in CPython (video)](https://www.youtube.com/watch?v=P-8Z0-MhdQs&list=PLdzf4Clw0VbOEWOS_sLhT_9zaiQDrS5AR&index=3)

- ### Parallel Programming
    - [ ] [Coursera (Scala)](https://www.coursera.org/learn/parprog1/home/week/1)
    - [ ] [Efficient Python for High Performance Parallel Computing (video)](https://www.youtube.com/watch?v=uY85GkaYzBk)

- ### Messaging, Serialization, and Queueing Systems
    - [ ] [Thrift](https://thrift.apache.org/)
        - [Tutorial](http://thrift-tutorial.readthedocs.io/en/latest/intro.html)
    - [ ] [Protocol Buffers](https://developers.google.com/protocol-buffers/)
        - [Tutorials](https://developers.google.com/protocol-buffers/docs/tutorials)
    - [ ] [gRPC](http://www.grpc.io/)
        - [gRPC 101 for Java Developers (video)](https://www.youtube.com/watch?v=5tmPvSe7xXQ&list=PLcTqM9n_dieN0k1nSeN36Z_ppKnvMJoly&index=1)
    - [ ] [Redis](http://redis.io/)
        - [Tutorial](http://try.redis.io/)
    - [ ] [Amazon SQS (queue)](https://aws.amazon.com/sqs/)
    - [ ] [Amazon SNS (pub-sub)](https://aws.amazon.com/sns/)
    - [ ] [RabbitMQ](https://www.rabbitmq.com/)
        - [Get Started](https://www.rabbitmq.com/getstarted.html)
    - [ ] [Celery](http://www.celeryproject.org/)
        - [First Steps With Celery](http://docs.celeryproject.org/en/latest/getting-started/first-steps-with-celery.html)
    - [ ] [ZeroMQ](http://zeromq.org/)
        - [Intro - Read The Manual](http://zeromq.org/intro:read-the-manual)
    - [ ] [ActiveMQ](http://activemq.apache.org/)
    - [ ] [Kafka](http://kafka.apache.org/documentation.html#introduction)
    - [ ] [MessagePack](http://msgpack.org/index.html)
    - [ ] [Avro](https://avro.apache.org/)

- ### Fast Fourier Transform
    - [ ] [An Interactive Guide To The Fourier Transform](https://betterexplained.com/articles/an-interactive-guide-to-the-fourier-transform/)
    - [ ] [What is a Fourier transform? What is it used for?](http://www.askamathematician.com/2012/09/q-what-is-a-fourier-transform-what-is-it-used-for/)
    - [ ] [What is the Fourier Transform? (video)](https://www.youtube.com/watch?v=Xxut2PN-V8Q)
    - [ ] [Divide & Conquer: FFT (video)](https://www.youtube.com/watch?v=iTMn0Kt18tg&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=4)
    - [ ] [Understanding The FFT](http://jakevdp.github.io/blog/2013/08/28/understanding-the-fft/)

- ### Bloom Filter
    - Given a Bloom filter with m bits and k hashing functions, both insertion and membership testing are O(k)
    - [Bloom Filters](https://www.youtube.com/watch?v=-SuTGoFYjZs)
    - [Bloom Filters | Mining of Massive Datasets | Stanford University](https://www.youtube.com/watch?v=qBTdukbzc78)
    - [Tutorial](http://billmill.org/bloomfilter-tutorial/)
    - [How To Write A Bloom Filter App](http://blog.michaelschmatz.com/2016/04/11/how-to-write-a-bloom-filter-cpp/)

- ### HyperLogLog
    - [How To Count A Billion Distinct Objects Using Only 1.5KB Of Memory](http://highscalability.com/blog/2012/4/5/big-data-counting-how-to-count-a-billion-distinct-objects-us.html)

- ### Locality-Sensitive Hashing
    - used to determine the similarity of documents
    - the opposite of MD5 or SHA which are used to determine if 2 documents/strings are exactly the same.
    - [Simhashing (hopefully) made simple](http://ferd.ca/simhashing-hopefully-made-simple.html)

- ### van Emde Boas Trees
    - [ ] [Divide & Conquer: van Emde Boas Trees (video)](https://www.youtube.com/watch?v=hmReJCupbNU&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=6)
    - [ ] [MIT Lecture Notes](https://ocw.mit.edu/courses/electrical-engineering-and-computer-science/6-046j-design-and-analysis-of-algorithms-spring-2012/lecture-notes/MIT6_046JS12_lec15.pdf)

- ### Augmented Data Structures
    - [ ] [CS 61B Lecture 39: Augmenting Data Structures](https://youtu.be/zksIj9O8_jc?list=PL4BBB74C7D2A1049C&t=950)

- ### Tries
    - Note there are different kinds of tries. Some have prefixes, some don't, and some use string instead of bits
        to track the path.
    - I read through code, but will not implement.
    - [ ] [Sedgewick - Tries (3 videos)](https://www.youtube.com/playlist?list=PLe-ggMe31CTe9IyG9MB8vt5xUJeYgOYRQ)
        - [ ] [1. R Way Tries](https://www.youtube.com/watch?v=buq2bn8x3Vo&index=3&list=PLe-ggMe31CTe9IyG9MB8vt5xUJeYgOYRQ)
        - [ ] [2. Ternary Search Tries](https://www.youtube.com/watch?v=LelV-kkYMIg&index=2&list=PLe-ggMe31CTe9IyG9MB8vt5xUJeYgOYRQ)
        - [ ] [3. Character Based Operations](https://www.youtube.com/watch?v=00YaFPcC65g&list=PLe-ggMe31CTe9IyG9MB8vt5xUJeYgOYRQ&index=1)
    - [ ] [Notes on Data Structures and Programming Techniques](http://www.cs.yale.edu/homes/aspnes/classes/223/notes.html#Tries)
    - [ ] Short course videos:
        - [ ] [Introduction To Tries (video)](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/08Xyf/core-introduction-to-tries)
        - [ ] [Performance Of Tries (video)](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/PvlZW/core-performance-of-tries)
        - [ ] [Implementing A Trie (video)](https://www.coursera.org/learn/data-structures-optimizing-performance/lecture/DFvd3/core-implementing-a-trie)
    - [ ] [The Trie: A Neglected Data Structure](https://www.toptal.com/java/the-trie-a-neglected-data-structure)
    - [ ] [TopCoder - Using Tries](https://www.topcoder.com/community/data-science/data-science-tutorials/using-tries/)
    - [ ] [Stanford Lecture (real world use case) (video)](https://www.youtube.com/watch?v=TJ8SkcUSdbU)
    - [ ] [MIT, Advanced Data Structures, Strings (can get pretty obscure about halfway through)](https://www.youtube.com/watch?v=NinWEPPrkDQ&index=16&list=PLUl4u3cNGP61hsJNdULdudlRL493b-XZf)

- ### Balanced search trees
    - Know least one type of balanced binary tree (and know how it's implemented):
    - "Among balanced search trees, AVL and 2/3 trees are now passé, and red-black trees seem to be more popular.
        A particularly interesting self-organizing data structure is the splay tree, which uses rotations
        to move any accessed key to the root." - Skiena
    - Of these, I chose to implement a splay tree. From what I've read, you won't implement a
        balanced search tree in your interview. But I wanted exposure to coding one up
        and let's face it, splay trees are the bee's knees. I did read a lot of red-black tree code.
        - splay tree: insert, search, delete functions
        If you end up implementing red/black tree try just these:
        - search and insertion functions, skipping delete
    - I want to learn more about B-Tree since it's used so widely with very large data sets.
    - [ ] [Self-balancing binary search tree](https://en.wikipedia.org/wiki/Self-balancing_binary_search_tree)

    - [ ] **AVL trees**
        - In practice:
            From what I can tell, these aren't used much in practice, but I could see where they would be:
            The AVL tree is another structure supporting O(log n) search, insertion, and removal. It is more rigidly
            balanced than red–black trees, leading to slower insertion and removal but faster retrieval. This makes it
            attractive for data structures that may be built once and loaded without reconstruction, such as language
            dictionaries (or program dictionaries, such as the opcodes of an assembler or interpreter).
        - [ ] [MIT AVL Trees / AVL Sort (video)](https://www.youtube.com/watch?v=FNeL18KsWPc&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=6)
        - [ ] [AVL Trees (video)](https://www.coursera.org/learn/data-structures/lecture/Qq5E0/avl-trees)
        - [ ] [AVL Tree Implementation (video)](https://www.coursera.org/learn/data-structures/lecture/PKEBC/avl-tree-implementation)
        - [ ] [Split And Merge](https://www.coursera.org/learn/data-structures/lecture/22BgE/split-and-merge)

    - [ ] **Splay trees**
        - In practice:
            Splay trees are typically used in the implementation of caches, memory allocators, routers, garbage collectors,
            data compression, ropes (replacement of string used for long text strings), in Windows NT (in the virtual memory,
            networking and file system code) etc.
        - [ ] [CS 61B: Splay Trees (video)](https://www.youtube.com/watch?v=Najzh1rYQTo&index=23&list=PL-XXv-cvA_iAlnI-BQr9hjqADPBtujFJd)
        - [ ] MIT Lecture: Splay Trees:
            - Gets very mathy, but watch the last 10 minutes for sure.
            - [Video](https://www.youtube.com/watch?v=QnPl_Y6EqMo)

    - [ ] **Red/black trees**
        - these are a translation of a 2-3 tree (see below)
        - In practice:
            Red–black trees offer worst-case guarantees for insertion time, deletion time, and search time.
            Not only does this make them valuable in time-sensitive applications such as real-time applications,
            but it makes them valuable building blocks in other data structures which provide worst-case guarantees;
            for example, many data structures used in computational geometry can be based on red–black trees, and
            the Completely Fair Scheduler used in current Linux kernels uses red–black trees. In the version 8 of Java,
            the Collection HashMap has been modified such that instead of using a LinkedList to store identical elements with poor
            hashcodes, a Red-Black tree is used.
        - [ ] [Aduni - Algorithms - Lecture 4 (link jumps to starting point) (video)](https://youtu.be/1W3x0f_RmUo?list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&t=3871)
        - [ ] [Aduni - Algorithms - Lecture 5 (video)](https://www.youtube.com/watch?v=hm2GHwyKF1o&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&index=5)
        - [ ] [Black Tree](https://en.wikipedia.org/wiki/Red%E2%80%93black_tree)
        - [ ] [An Introduction To Binary Search And Red Black Tree](https://www.topcoder.com/community/data-science/data-science-tutorials/an-introduction-to-binary-search-and-red-black-trees/)

    - [ ] **2-3 search trees**
        - In practice:
            2-3 trees have faster inserts at the expense of slower searches (since height is more compared to AVL trees).
        - You would use 2-3 tree very rarely because its implementation involves different types of nodes. Instead, people use Red Black trees.
        - [ ] [23-Tree Intuition and Definition (video)](https://www.youtube.com/watch?v=C3SsdUqasD4&list=PLA5Lqm4uh9Bbq-E0ZnqTIa8LRaL77ica6&index=2)
        - [ ] [Binary View of 23-Tree](https://www.youtube.com/watch?v=iYvBtGKsqSg&index=3&list=PLA5Lqm4uh9Bbq-E0ZnqTIa8LRaL77ica6)
        - [ ] [2-3 Trees (student recitation) (video)](https://www.youtube.com/watch?v=TOb1tuEZ2X4&index=5&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp)

    - [ ] **2-3-4 Trees (aka 2-4 trees)**
        - In practice:
            For every 2-4 tree, there are corresponding red–black trees with data elements in the same order. The insertion and deletion
            operations on 2-4 trees are also equivalent to color-flipping and rotations in red–black trees. This makes 2-4 trees an
            important tool for understanding the logic behind red–black trees, and this is why many introductory algorithm texts introduce
            2-4 trees just before red–black trees, even though **2-4 trees are not often used in practice**.
        - [ ] [CS 61B Lecture 26: Balanced Search Trees (video)](https://www.youtube.com/watch?v=zqrqYXkth6Q&index=26&list=PL4BBB74C7D2A1049C)
        - [ ] [Bottom Up 234-Trees (video)](https://www.youtube.com/watch?v=DQdMYevEyE4&index=4&list=PLA5Lqm4uh9Bbq-E0ZnqTIa8LRaL77ica6)
        - [ ] [Top Down 234-Trees (video)](https://www.youtube.com/watch?v=2679VQ26Fp4&list=PLA5Lqm4uh9Bbq-E0ZnqTIa8LRaL77ica6&index=5)

    - [ ] **N-ary (K-ary, M-ary) trees**
        - note: the N or K is the branching factor (max branches)
        - binary trees are a 2-ary tree, with branching factor = 2
        - 2-3 trees are 3-ary
        - [ ] [K-Ary Tree](https://en.wikipedia.org/wiki/K-ary_tree)

    - [ ] **B-Trees**
        - fun fact: it's a mystery, but the B could stand for Boeing, Balanced, or Bayer (co-inventor)
        - In Practice:
            B-Trees are widely used in databases. Most modern filesystems use B-trees (or Variants). In addition to
            its use in databases, the B-tree is also used in filesystems to allow quick random access to an arbitrary
            block in a particular file. The basic problem is turning the file block i address into a disk block
            (or perhaps to a cylinder-head-sector) address.
        - [ ] [B-Tree](https://en.wikipedia.org/wiki/B-tree)
        - [ ] [Introduction to B-Trees (video)](https://www.youtube.com/watch?v=I22wEC1tTGo&list=PLA5Lqm4uh9Bbq-E0ZnqTIa8LRaL77ica6&index=6)
        - [ ] [B-Tree Definition and Insertion (video)](https://www.youtube.com/watch?v=s3bCdZGrgpA&index=7&list=PLA5Lqm4uh9Bbq-E0ZnqTIa8LRaL77ica6)
        - [ ] [B-Tree Deletion (video)](https://www.youtube.com/watch?v=svfnVhJOfMc&index=8&list=PLA5Lqm4uh9Bbq-E0ZnqTIa8LRaL77ica6)
        - [ ] [MIT 6.851 - Memory Hierarchy Models (video)](https://www.youtube.com/watch?v=V3omVLzI0WE&index=7&list=PLUl4u3cNGP61hsJNdULdudlRL493b-XZf)
                - covers cache-oblivious B-Trees, very interesting data structures
                - the first 37 minutes are very technical, may be skipped (B is block size, cache line size)


- ### k-D Trees
    - great for finding number of points in a rectangle or higher dimension object
    - a good fit for k-nearest neighbors
    - [ ] [Kd Trees (video)](https://www.youtube.com/watch?v=W94M9D_yXKk)
    - [ ] [kNN K-d tree algorithm (video)](https://www.youtube.com/watch?v=Y4ZgLlDfKDg)

- ### Skip lists
    - "These are somewhat of a cult data structure" - Skiena
    - [ ] [Randomization: Skip Lists (video)](https://www.youtube.com/watch?v=2g9OSRKJuzM&index=10&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp)
    - [ ] [For animations and a little more detail](https://en.wikipedia.org/wiki/Skip_list)

- ### Network Flows
    - [ ] [Ford-Fulkerson in 5 minutes (video)](https://www.youtube.com/watch?v=v1VgJmkEJW0)
    - [ ] [Ford-Fulkerson Algorithm (video)](https://www.youtube.com/watch?v=v1VgJmkEJW0)
    - [ ] [Network Flows (video)](https://www.youtube.com/watch?v=2vhN4Ice5jI)

- ### Disjoint Sets & Union Find
    - [ ] [UCB 61B - Disjoint Sets; Sorting & selection (video)](https://www.youtube.com/watch?v=MAEGXTwmUsI&list=PL-XXv-cvA_iAlnI-BQr9hjqADPBtujFJd&index=21)
    - [ ] [Sedgewick Algorithms - Union-Find (6 videos)](https://www.youtube.com/watch?v=8mYfZeHtdNc&list=PLe-ggMe31CTexoNYnMhbHaWhQ0dvcy43t)

- ### Math for Fast Processing
    - [ ] [Integer Arithmetic, Karatsuba Multiplication (video)](https://www.youtube.com/watch?v=eCaXlAaN2uE&index=11&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb)
    - [ ] [The Chinese Remainder Theorem (used in cryptography) (video)](https://www.youtube.com/watch?v=ru7mWZJlRQg)

- ### Treap
    - Combination of a binary search tree and a heap
    - [ ] [Treap](https://en.wikipedia.org/wiki/Treap)
    - [ ] [Data Structures: Treaps explained (video)](https://www.youtube.com/watch?v=6podLUYinH8)
    - [ ] [Applications in set operations](https://www.cs.cmu.edu/~scandal/papers/treaps-spaa98.pdf)

- ### Linear Programming (videos)
    - [ ] [Linear Programming](https://www.youtube.com/watch?v=M4K6HYLHREQ)
    - [ ] [Finding minimum cost](https://www.youtube.com/watch?v=2ACJ9ewUC6U)
    - [ ] [Finding maximum value](https://www.youtube.com/watch?v=8AA_81xI3ik)
    - [ ] [Solve Linear Equations with Python - Simplex Algorithm](https://www.youtube.com/watch?v=44pAWI7v5Zk)

- ### Geometry, Convex hull (videos)
    - [ ] [Graph Alg. IV: Intro to geometric algorithms - Lecture 9](https://youtu.be/XIAQRlNkJAw?list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&t=3164)
    - [ ] [Geometric Algorithms: Graham & Jarvis - Lecture 10](https://www.youtube.com/watch?v=J5aJEcOr6Eo&index=10&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm)
    - [ ] [Divide & Conquer: Convex Hull, Median Finding](https://www.youtube.com/watch?v=EzeYI7p9MjU&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=2)

- ### Discrete math
    - see videos below

- ### Machine Learning
    - [ ] Why ML?
        - [ ] [How Google Is Remaking Itself As A Machine Learning First Company](https://backchannel.com/how-google-is-remaking-itself-as-a-machine-learning-first-company-ada63defcb70)
        - [ ] [Large-Scale Deep Learning for Intelligent Computer Systems (video)](https://www.youtube.com/watch?v=QSaZGT4-6EY)
        - [ ] [Deep Learning and Understandability versus Software Engineering and Verification by Peter Norvig](https://www.youtube.com/watch?v=X769cyzBNVw)
    - [ ] [Google's Cloud Machine learning tools (video)](https://www.youtube.com/watch?v=Ja2hxBAwG_0)
    - [ ] [Google Developers' Machine Learning Recipes (Scikit Learn & Tensorflow) (video)](https://www.youtube.com/playlist?list=PLOU2XLYxmsIIuiBfYad6rFYQU_jL2ryal)
    - [ ] [Tensorflow (video)](https://www.youtube.com/watch?v=oZikw5k_2FM)
    - [ ] [Tensorflow Tutorials](https://www.tensorflow.org/versions/r0.11/tutorials/index.html)
    - [ ] [Practical Guide to implementing Neural Networks in Python (using Theano)](http://www.analyticsvidhya.com/blog/2016/04/neural-networks-python-theano/)
    - Courses:
        - [Great starter course: Machine Learning](https://www.coursera.org/learn/machine-learning)
              - [videos only](https://www.youtube.com/playlist?list=PLZ9qNFMHZ-A4rycgrgOYma6zxF4BZGGPW)
              - see videos 12-18 for a review of linear algebra (14 and 15 are duplicates)
        - [Neural Networks for Machine Learning](https://www.coursera.org/learn/neural-networks)
        - [Google's Deep Learning Nanodegree](https://www.udacity.com/course/deep-learning--ud730)
        - [Google/Kaggle Machine Learning Engineer Nanodegree](https://www.udacity.com/course/machine-learning-engineer-nanodegree-by-google--nd009)
        - [Self-Driving Car Engineer Nanodegree](https://www.udacity.com/drive)
        - [Metis Online Course ($99 for 2 months)](http://www.thisismetis.com/explore-data-science)
    - Resources:
        - Books:
            - [Python Machine Learning](https://www.amazon.com/Python-Machine-Learning-Sebastian-Raschka/dp/1783555130/)
            - [Data Science from Scratch: First Principles with Python](https://www.amazon.com/Data-Science-Scratch-Principles-Python/dp/149190142X)
            - [Introduction to Machine Learning with Python](https://www.amazon.com/Introduction-Machine-Learning-Python-Scientists/dp/1449369413/)
        - [Machine Learning for Software Engineers](https://github.com/ZuzooVn/machine-learning-for-software-engineers)
        - Data School: http://www.dataschool.io/

- ### Go
    - [ ] Videos:
        - [ ] [Why Learn Go?](https://www.youtube.com/watch?v=FTl0tl9BGdc)
        - [ ] [Go Programming](https://www.youtube.com/watch?v=CF9S4QZuV30)
        - [ ] [A Tour of Go](https://www.youtube.com/watch?v=ytEkHepK08c)
    - [ ] Books:
        - [ ] [An Introduction to Programming in Go (read free online)](https://www.golang-book.com/books/intro)
        - [ ] [The Go Programming Language (Donovan & Kernighan)](https://www.amazon.com/Programming-Language-Addison-Wesley-Professional-Computing/dp/0134190440)
    - [ ] [Bootcamp](https://www.golang-book.com/guides/bootcamp)

--

## Additional Detail on Some Subjects

    I added these to reinforce some ideas already presented above, but didn't want to include them
    above because it's just too much. It's easy to overdo it on a subject.
    You want to get hired in this century, right?

- [ ] **Union-Find**
    - [ ] [Overview](https://www.coursera.org/learn/data-structures/lecture/JssSY/overview)
    - [ ] [Naive Implementation](https://www.coursera.org/learn/data-structures/lecture/EM5D0/naive-implementations)
    - [ ] [Trees](https://www.coursera.org/learn/data-structures/lecture/Mxu0w/trees)
    - [ ] [Union By Rank](https://www.coursera.org/learn/data-structures/lecture/qb4c2/union-by-rank)
    - [ ] [Path Compression](https://www.coursera.org/learn/data-structures/lecture/Q9CVI/path-compression)
    - [ ] [Analysis Options](https://www.coursera.org/learn/data-structures/lecture/GQQLN/analysis-optional)

- [ ] **More Dynamic Programming** (videos)
    - [ ] [6.006: Dynamic Programming I: Fibonacci, Shortest Paths](https://www.youtube.com/watch?v=OQ5jsbhAv_M&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=19)
    - [ ] [6.006: Dynamic Programming II: Text Justification, Blackjack](https://www.youtube.com/watch?v=ENyox7kNKeY&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=20)
    - [ ] [6.006: DP III: Parenthesization, Edit Distance, Knapsack](https://www.youtube.com/watch?v=ocZMDMZwhCY&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=21)
    - [ ] [6.006: DP IV: Guitar Fingering, Tetris, Super Mario Bros.](https://www.youtube.com/watch?v=tp4_UXaVyx8&index=22&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb)
    - [ ] [6.046: Dynamic Programming & Advanced DP](https://www.youtube.com/watch?v=Tw1k46ywN6E&index=14&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp)
    - [ ] [6.046: Dynamic Programming: All-Pairs Shortest Paths](https://www.youtube.com/watch?v=NzgFUwOaoIw&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=15)
    - [ ] [6.046: Dynamic Programming (student recitation)](https://www.youtube.com/watch?v=krZI60lKPek&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=12)

- [ ] **Advanced Graph Processing** (videos)
    - [ ] [Synchronous Distributed Algorithms: Symmetry-Breaking. Shortest-Paths Spanning Trees](https://www.youtube.com/watch?v=mUBmcbbJNf4&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=27)
    - [ ] [Asynchronous Distributed Algorithms: Shortest-Paths Spanning Trees](https://www.youtube.com/watch?v=kQ-UQAzcnzA&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp&index=28)

- [ ] MIT **Probability** (mathy, and go slowly, which is good for mathy things) (videos):
    - [ ] [MIT 6.042J - Probability Introduction](https://www.youtube.com/watch?v=SmFwFdESMHI&index=18&list=PLB7540DEDD482705B)
    - [ ] [MIT 6.042J - Conditional Probability](https://www.youtube.com/watch?v=E6FbvM-FGZ8&index=19&list=PLB7540DEDD482705B)
    - [ ] [MIT 6.042J - Independence](https://www.youtube.com/watch?v=l1BCv3qqW4A&index=20&list=PLB7540DEDD482705B)
    - [ ] [MIT 6.042J - Random Variables](https://www.youtube.com/watch?v=MOfhhFaQdjw&list=PLB7540DEDD482705B&index=21)
    - [ ] [MIT 6.042J - Expectation I](https://www.youtube.com/watch?v=gGlMSe7uEkA&index=22&list=PLB7540DEDD482705B)
    - [ ] [MIT 6.042J - Expectation II](https://www.youtube.com/watch?v=oI9fMUqgfxY&index=23&list=PLB7540DEDD482705B)
    - [ ] [MIT 6.042J - Large Deviations](https://www.youtube.com/watch?v=q4mwO2qS2z4&index=24&list=PLB7540DEDD482705B)
    - [ ] [MIT 6.042J - Random Walks](https://www.youtube.com/watch?v=56iFMY8QW2k&list=PLB7540DEDD482705B&index=25)

- [ ] [Simonson: Approximation Algorithms (video)](https://www.youtube.com/watch?v=oDniZCmNmNw&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&index=19)

- [ ] **String Matching**
    - [ ] Rabin-Karp (videos):
        - [Rabin Karps Algorithm](https://www.coursera.org/learn/data-structures/lecture/c0Qkw/rabin-karps-algorithm)
        - [Precomputing](https://www.coursera.org/learn/data-structures/lecture/nYrc8/optimization-precomputation)
        - [Optimization: Implementation and Analysis](https://www.coursera.org/learn/data-structures/lecture/h4ZLc/optimization-implementation-and-analysis)
        - [Table Doubling, Karp-Rabin](https://www.youtube.com/watch?v=BRO7mVIFt08&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=9)
        - [Rolling Hashes, Amortized Analysis](https://www.youtube.com/watch?v=w6nuXg0BISo&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&index=32)
    - [ ] Knuth-Morris-Pratt (KMP):
        - [TThe Knuth-Morris-Pratt (KMP) String Matching Algorithm](https://www.youtube.com/watch?v=5i7oKodCRJo)
    - [ ] Boyer–Moore string search algorithm
        - [Boyer-Moore String Search Algorithm](https://en.wikipedia.org/wiki/Boyer%E2%80%93Moore_string_search_algorithm)
        - [Advanced String Searching Boyer-Moore-Horspool Algorithms (video)](https://www.youtube.com/watch?v=QDZpzctPf10)
    - [ ] [Coursera: Algorithms on Strings](https://www.coursera.org/learn/algorithms-on-strings/home/week/1)
        - starts off great, but by the time it gets past KMP it gets more complicated than it needs to be
        - nice explanation of tries
        - can be skipped

- [ ] **Sorting**

    - [ ] Stanford lectures on sorting:
        - [ ] [Lecture 15 | Programming Abstractions (video)](https://www.youtube.com/watch?v=ENp00xylP7c&index=15&list=PLFE6E58F856038C69)
        - [ ] [Lecture 16 | Programming Abstractions (video)](https://www.youtube.com/watch?v=y4M9IVgrVKo&index=16&list=PLFE6E58F856038C69)
    - [ ] Shai Simonson, [Aduni.org](http://www.aduni.org/):
        - [ ] [Algorithms - Sorting - Lecture 2 (video)](https://www.youtube.com/watch?v=odNJmw5TOEE&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&index=2)
        - [ ] [Algorithms - Sorting II - Lecture 3 (video)](https://www.youtube.com/watch?v=hj8YKFTFKEE&list=PLFDnELG9dpVxQCxuD-9BSy2E7BWY3t5Sm&index=3)
    - [ ] Steven Skiena lectures on sorting:
        - [ ] [lecture begins at 26:46 (video)](https://youtu.be/ute-pmMkyuk?list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b&t=1600)
        - [ ] [lecture begins at 27:40 (video)](https://www.youtube.com/watch?v=yLvp-pB8mak&index=8&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b)
        - [ ] [lecture begins at 35:00 (video)](https://www.youtube.com/watch?v=q7K9otnzlfE&index=9&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b)
        - [ ] [lecture begins at 23:50 (video)](https://www.youtube.com/watch?v=TvqIGu9Iupw&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b&index=10)

## Video Series

Sit back and enjoy. "Netflix and skill" :P

- [ ] [List of individual Dynamic Programming problems (each is short)](https://www.youtube.com/playlist?list=PLrmLmBdmIlpsHaNTPP_jHHDx_os9ItYXr)

- [ ] [x86 Architecture, Assembly, Applications (11 videos)](https://www.youtube.com/playlist?list=PL038BE01D3BAEFDB0)

- [ ] [MIT 18.06 Linear Algebra, Spring 2005 (35 videos)](https://www.youtube.com/playlist?list=PLE7DDD91010BC51F8)

- [ ] [Excellent - MIT Calculus Revisited: Single Variable Calculus](https://www.youtube.com/playlist?list=PL3B08AE665AB9002A)

- [ ] [Computer Science 70, 001 - Spring 2015 - Discrete Mathematics and Probability Theory](https://www.youtube.com/playlist?list=PL-XXv-cvA_iD8wQm8U0gG_Z1uHjImKXFy)

- [ ] [Discrete Mathematics by Shai Simonson (19 videos)](https://www.youtube.com/playlist?list=PL3o9D4Dl2FJ9q0_gtFXPh_H4POI5dK0yG)

- [ ] [Discrete Mathematics Part 1 by Sarada Herke (5 videos)](https://www.youtube.com/playlist?list=PLGxuz-nmYlQPOc4w1Kp2MZrdqOOm4Jxeo)

- [ ] CSE373 - Analysis of Algorithms (25 videos)
    - [Skiena lectures from Algorithm Design Manual](https://www.youtube.com/watch?v=ZFjhkohHdAA&list=PLOtl7M3yp-DV69F32zdK7YJcNXpTunF2b&index=1)

- [ ] [UC Berkeley 61B (Spring 2014): Data Structures (25 videos)](https://www.youtube.com/watch?v=mFPmKGIrQs4&list=PL-XXv-cvA_iAlnI-BQr9hjqADPBtujFJd)

- [ ] [UC Berkeley 61B (Fall 2006): Data Structures (39 videos)](https://www.youtube.com/playlist?list=PL4BBB74C7D2A1049C)

- [ ] [UC Berkeley 61C: Machine Structures (26 videos)](https://www.youtube.com/watch?v=gJJeUFyuvvg&list=PL-XXv-cvA_iCl2-D-FS5mk0jFF6cYSJs_)

- [ ] [OOSE: Software Dev Using UML and Java (21 videos)](https://www.youtube.com/playlist?list=PLJ9pm_Rc9HesnkwKlal_buSIHA-jTZMpO)

- [ ] [UC Berkeley CS 152: Computer Architecture and Engineering (20 videos)](https://www.youtube.com/watch?v=UH0QYvtP7Rk&index=20&list=PLkFD6_40KJIwEiwQx1dACXwh-2Fuo32qr)

- [ ] [MIT 6.004: Computation Structures (49 videos)](https://www.youtube.com/playlist?list=PLrRW1w6CGAcXbMtDFj205vALOGmiRc82-)

- [ ] [Carnegie Mellon - Computer Architecture Lectures (39 videos)](https://www.youtube.com/playlist?list=PL5PHm2jkkXmi5CxxI7b3JCL1TWybTDtKq)

- [ ] [MIT 6.006: Intro to Algorithms (47 videos)](https://www.youtube.com/watch?v=HtSuA80QTyo&list=PLUl4u3cNGP61Oq3tWYp6V_F-5jb5L2iHb&nohtml5=False)

- [ ] [MIT 6.033: Computer System Engineering (22 videos)](https://www.youtube.com/watch?v=zm2VP0kHl1M&list=PL6535748F59DCA484)

- [ ] [MIT 6.034 Artificial Intelligence, Fall 2010 (30 videos)](https://www.youtube.com/playlist?list=PLUl4u3cNGP63gFHB6xb-kVBiQHYe_4hSi)

- [ ] [MIT 6.042J: Mathematics for Computer Science, Fall 2010 (25 videos)](https://www.youtube.com/watch?v=L3LMbpZIKhQ&list=PLB7540DEDD482705B)

- [ ] [MIT 6.046: Design and Analysis of Algorithms (34 videos)](https://www.youtube.com/watch?v=2P-yW7LQr08&list=PLUl4u3cNGP6317WaSNfmCvGym2ucw3oGp)

- [ ] [MIT 6.050J: Information and Entropy, Spring 2008 (19 videos)](https://www.youtube.com/watch?v=phxsQrZQupo&list=PL_2Bwul6T-A7OldmhGODImZL8KEVE38X7)

- [ ] [MIT 6.851: Advanced Data Structures (22 videos)](https://www.youtube.com/watch?v=T0yzrZL1py0&list=PLUl4u3cNGP61hsJNdULdudlRL493b-XZf&index=1)

- [ ] [MIT 6.854: Advanced Algorithms, Spring 2016 (24 videos)](https://www.youtube.com/playlist?list=PL6ogFv-ieghdoGKGg2Bik3Gl1glBTEu8c)

- [ ] [Harvard COMPSCI 224: Advanced Algorithms (25 videos)](https://www.youtube.com/playlist?list=PL2SOU6wwxB0uP4rJgf5ayhHWgw7akUWSf)

- [ ] [MIT 6.858 Computer Systems Security, Fall 2014](https://www.youtube.com/watch?v=GqmQg-cszw4&index=1&list=PLUl4u3cNGP62K2DjQLRxDNRi0z2IRWnNh)

- [ ] [Stanford: Programming Paradigms (27 videos)](https://www.youtube.com/view_play_list?p=9D558D49CA734A02)

- [ ] [Introduction to Cryptography by Christof Paar](https://www.youtube.com/playlist?list=PL6N5qY2nvvJE8X75VkXglSrVhLv1tVcfy)
    - [Course Website along with Slides and Problem Sets](http://www.crypto-textbook.com/)

- [ ] [Mining Massive Datasets - Stanford University (94 videos)](https://www.youtube.com/playlist?list=PLLssT5z_DsK9JDLcT8T62VtzwyW9LNepV)

- [ ] [Graph Theory by Sarada Herke (67 videos)](https://www.youtube.com/user/DrSaradaHerke/playlists?shelf_id=5&view=50&sort=dd)

## Computer Science Courses

- [Directory of Online CS Courses](https://github.com/open-source-society/computer-science)
- [Directory of CS Courses (many with online lectures)](https://github.com/prakhar1989/awesome-courses)
