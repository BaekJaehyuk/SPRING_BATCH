# Spring Batch 학습 
Spring Batch 5를 기반으로 대량 데이터를 처리할 수 있는 환경을 구축하는 것을 학습 목표로 합니다.

대용량 데이터 배치 처리를 위해 **스프링 배치 5의 프레임워크**를 활용하여 데이터를 효율적으로 배치 처리를 예제를 통해 구현하였으며, 스프링 배치의 작업을 기록하기 위해 메타 데이터용 DB를 설정하여 배치 환경 구성하였습니다.


# 📌 배치란? (Batch Processing)
배치 처리란, 주어진 데이터를 한 번에 일괄 처리하는 방식입니다.

### 1. 배치 처리의 주요 개념

**1-1. Reader (읽기)**

→ 데이터베이스, CSV, JSON 등의 데이터를 읽어옴

**1-2. Processor (처리)**

→ 데이터를 가공 및 변환

**1-3. Writer (쓰기)**

→ 처리된 데이터를 저장소(DB, 파일 등)에 저장.

# 📊 배치 처리 흐름

### 배치 데이터 흐름

  `[메타데이터 DB] → Reader → Processor → Writer → [데이터 소스 DB]`
  
  - 메타데이터 DB : 배치 실행 이력을 저장하여 중복 실행을 방지
  
  - 데이터 소스 DB : 처리된 데이터가 저장

### 스프링 배치의 내부 구조

  `[JobLauncher] → [Job] → [Step] → [ItemReader] → [ItemProcessor] → [ItemWriter]`
  
  - 각 단계에서 데이터를 읽고, 가공한 후 최종 저장하는 방식으로 동작합니다.

## 📚 참고 자료
- [유튜브 - 개발자 유미](https://www.youtube.com/watch?v=MNzPsOQ3NJk&list=PLJkjrxxiBSFCaxkvfuZaK5FzqQWJwmTfR)
- [Spring Batch 공식 문서](https://spring.io/projects/spring-batch)
