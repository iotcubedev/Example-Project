# 래브라도 예제 프로젝트 

## 목차 
1. 래브라도 소개
    1. '래브라도랩스'와 '래브라도'
    1. 래브라도의 분석대상 소개
1. 분석방법
    1. **[소스코드]** Git 리포 분석
    1. **[소스코드]** 소스아카이브 분석
    1. **[소스코드]** 패키지 분석 
    1. **[컨테이너]** Docker 분석
1. 분석결과 확인
1. 검색기능 

---

## 1. 래브라도 소개
### 1-1. '래브라도랩스'와 '래브라도'
[▶ 래브라도 Brochure 보기](./img/LabradorOSS_Brochure_v1.0_ko.jpg)

**래브라도랩스:**
> 고려대 보안연구소(CSSA)에서 원천 기술을 갖고 분사한 회사로서, 고객 소프트웨어의 사용 리스크를 정확히 탐지하고 관리해주는 최고의 소프트웨어 안전관리 플랫폼 제공을 목표로 하고 있습니다.

**래브라도 OSS:**
> SBOM 기반의 OSS 공급망 안전 관리 솔루션. 
> * 래브라도 OSS v2.0 GS인증 1등급 획득 [▶ 뉴스 보기](https://www.boannews.com/media/view.asp?idx=109123&kind=)

### 1-2. 래브라도의 분석대상 소개

1. **오픈소스 소스파일**
    * ex1) github, gitlab 등 소스 리포지터리에 존재하는 프로젝트 소스 [▶ 예시: netty](https://github.com/netty/netty)
    * ex2) 버전 컨트롤을 사용하지 않는 프로젝트 소스 (.zip, .tar.gz) [▶ 예시: pcre](https://sourceforge.net/projects/pcre/files/pcre/)

2. **라이브러리**
    |Language|Package Manager|Package Manager File|Repository|
    |--|--|--|--|
    |Java|mvn, Gradle|pom.xml, build.gradle|[Maven Repository](https://mvnrepository.com/)|
    |Python|pip|requirements.txt|[PYPI](https://pypi.org/)|
    |Javascript|NPM, yarn|package.json|[NPM](https://www.npmjs.com/)|
    |Ruby|Ruby Bundler|Gemfile|[RubyGems](https://rubygems.org/)|
    |PHP|Composer|composer.json|[Packagist](https://packagist.org/)|
    |Swift, Objective-C|CocoaPods|Podfile|[CocoaPods](https://cocoapods.org/)|
    |Go|Go Modules|go.mod|[Go](https://pkg.go.dev/)|
    |.NET|Nuget, Paket|project.json|[NuGet Gallery](https://www.nuget.org/packages)|


3. **Docker Hub 의 컨테이너**
    * [Docker Hub](https://hub.docker.com/) 에 검색되는 컨테이너 ex) ubuntu:18.04


## 2. 분석방법

### 2-1. **[소스코드]** Git 리포 분석
**프로젝트 만들기 > 소스코드 > Source Repo**
>시연 테스트소스: https://github.com/iotcubedev/Java-Project

### 2-2. **[소스코드]** 소스아카이브 분석
**프로젝트 만들기 > 소스코드 > 아카이브 파일**
>시연 테스트소스: https://github.com/iotcubedev/Java-Project


### 2-3. **[소스코드]** 패키지 분석 
**프로젝트 만들기 > 소스코드 > 아카이브 파일**

    * 패키지매니저 파일로 분석 가능합니다.


|Language|리포지터리|예제 라이브러리|버전|패키지매니저파일|
|--|--|--|--|--|
|Java|[Maven Repository](https://mvnrepository.com/)|xerces:xercesImpl|2.6.2|pom.xml|
|Python|[PYPI](https://pypi.org/)|GDAL|1.7.1|requirements.txt|
|Javascript|[NPM](https://www.npmjs.com/)|jquery|1.8.2|package.json|
|Ruby|[RubyGems](https://rubygems.org/)|bundler|2.2.8|Gemfile|
|PHP|[Packagist](https://packagist.org/)|cnvs/canvas|v3.4.2|composer.json|
|Swift, Objective-C|[CocoaPods](https://cocoapods.org/)|nanopb|0.3.901|Podfile|
|Go|[Go](https://pkg.go.dev/)|github.com/ethereum/go-ethereum|v1.8.7|go.mod|
|.NET|[NuGet Gallery](https://www.nuget.org/packages)|FSharp.Core|4.3.3|project.json|



### 2-4. **[컨테이너]** Docker 분석
**프로젝트 만들기 > 컨테이너 > 이미지명**
>시연 컨테이너: ubuntu:18.04


---

## 3. 분석결과 확인
1. **SBOM**: 
    * **컴포넌트**: 파일매칭, 라이브러리매칭
1. **3-Layer 취약점**:
    * **함수 취약점**
    * **파일 취약점**
    * **컴포넌트 취약점**: 파일매칭, 라이브러리매칭
> 시연
---
## 4. 검색기능 
**우측상단 "DB 검색"**
> 시연