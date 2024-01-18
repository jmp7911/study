# Travis CI

지속적 통합(Continuous Integration)을 제공하는 platform이다. 코드의 빌드와 테스트를 자동화하여 유닛단위로 프로젝트를 관리할 수 있도록 한다.

### Builds, Stages, Jobs and Phases 

- Build: 순서대로 실행되는 Job을 하나 이상 포함하고 있다. 예를 들어, Build에는 두 개의 Job이 있을 수 있으며, 각각 다른 프로그래밍 언어로 프로젝트를 테스트 합니다. 테스트가 끝나면 빌드를 완료합니다.
- Stages: 여러 단계로 구성된 순차적 Build 프로세스의 일부로, 병렬로 실행되는 Job의 그룹이다.
- Job: Repository를 가상환경에 clone 한 다음, 컴파일이나 테스트코드의 실행과 같은 phase를 수행하는 자동화된 프로세스 이다.
- Phase: Job의 순차적 단계 입니다. install, script 등이 있다.
### Jobs Life Cycle

1. install: 필요한 종속성을 설치
2. script: 빌드 스크립트를 실행

- 사용자 지정 명령
    1. before_install- install 단계 전에
    2. before_script- script 단계 전에
    3. after_script- script 단계 이후.
    4. after_success - when the build succeeds (e.g. building documentation), the result is in TRAVIS_TEST_RESULT environment variable
    5. after_failure - when the build fails (e.g. uploading log files), the result is in TRAVIS_TEST_RESULT environment variable
