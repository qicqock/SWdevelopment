# Workflow
저희가 선택한 workflow 는 gitflow workflow 입니다.

## gitflow 개요
- 깃플로우(gitflow) 전략은 소프트웨의 소스코드를 관리하고 출시하기 위한 '브랜치 관리 전략(branch management strategy)'중 하나이다.
- 크게 항상 유지되는 메인 브랜치(master, develop)와 일정 기간 유지되는 보조 브랜치(feature, realease, hotfix)로 나뉜다.
- 규모가 큰 프로젝트에서는 브랜치 활용보다는 fork 기능을 사용한다. fork는 브랜치와 비슷하지만 프로젝트를 통째로 외부로 복제하여 개발하는 방식이다.
  - fork 방식은 브랜치처럼 바로 merge하는 방식이 아니라 pull request로 프로젝트 관리자에게 merge 요청을 보내고 관리자에 의해 merge되는 개발 방식이다.

## branch 설명
*gitflow workflow 이미지*
[이미지 출처](https://lucamezzalira.com/2014/03/10/git-flow-vs-github-flow/)
![gitflow workflow](https://i2.wp.com/lanziani.com/slides/gitflow/images/gitflow_1.png?zoom=2)

*우리팀이 gitflow를 이용하여 했던 실습 commit 구조*
![우리팀이 gitflow를 이용하여 했던 실습 commit 구조](https://i.imgur.com/sgfmrg9.png)
1. master branch - 모든 브랜치에 기준이 되며 상품으로 release하는 브랜치이다.
모든 브랜치에 기준이 되는 브랜치이며 결국 모든 변경사항은 master 브랜치에 병합되어야 한다.
master 브랜치를 직접 수정하기보다는 다른 브랜치의 변경사항을 병합하는 방법을 사용한다.


2. develop branch - 다음 출시 버전을 개발하는 브랜치
기능 개발을 위한 브랜치들을 병합하기 위해 사용. 즉, 모든 기능이 추가되고 버그가 수정되어 배포 가능한 안정적인 상태라면 develop 브랜치를 master브랜치에 merge한다. 평소에는 이 브랜치를 기반으로 개발을 진행한다.


3. hotfix branch - 출시 버전에서 발생한 버그를 수정 하는 브랜치
배포한 버전에 긴급하게 수정을 해야 할 필요가 있을 경우, ‘master’ 브랜치에서 분기하는 브랜치이다. ‘develop’ 브랜치에서 문제가 되는 부분을 수정하여 배포 가능한 버전을 만들기에는 시간도 많이 소요되고 안정성을 보장하기도 어려우므로 바로 배포가 가능한 ‘master’ 브랜치에서 직접 브랜치를 만들어 필요한 부분만을 수정한 후 다시 ‘master’브랜치에 병합하여 이를 배포해야 하는 것이다.



4. release branch - 이번 출시 버전을 준비하는 브랜치
배포를 위한 전용 브랜치를 사용함으로써 한 팀이 해당 배포를 준비하는 동안 다른 팀은 다음 배포를 위한 기능 개발을 계속할 수 있다. 즉, 딱딱 끊어지는 개발 단계를 정의하기에 아주 좋다.
예를 들어, ‘이번 주에 버전 1.3 배포를 목표로 한다!’라고 팀 구성원들과 쉽게 소통하고 합의할 수 있다는 말이다.


5. feature branch - 기능을 개발하는 브랜치
feature 브랜치는 새로운 기능 개발 및 버그 수정이 필요할 때마다 ‘develop’ 브랜치로부터 분기한다. feature 브랜치에서의 작업은 기본적으로 공유할 필요가 없기 때문에, 자신의 로컬 저장소에서 관리한다.
개발이 완료되면 ‘develop’ 브랜치로 병합(merge)하여 다른 사람들과 공유한다.



다 커밋메세지 뭐했는지+이름적기
그리고 다하면 언제든지 PR날리셈
ex) branch설명-민재

권태윤 : 팀원의 PR을 merge하여 전체 레포지토리 관리 및 총 정리

손홍일 : gitflow workflow와 forking workflow가 쓰이는 환경과 설명 추가

김기태 : gitflow workflow에 대한 이미지 추가 및 master branch의 역할 설명

이민재 : master branch 를 제외한 develop,hotfix,release,feature branch의 역할 설명

윤찬웅 : workflow.md 파일 작성을 위한 팀원의 역할 정리
