# 캡스톤 디자인 ocr기술을 제공하는 웹 서비스(2021.03~2021.11)

> ## 개발환경

- os : ubuntu 20.04.3
- IDE : vscode
- DB : mysql
- test tool : pytest(unit test)
- framwork : flask(python)
- wsgi : gunicorn

> ## 구현한 기능(rest api)

- 회원가입, 로그인 기능(jwt를 이용하여 인증 구현)

- 이미지 전체를 ocr 하는 기능구현(tesseract에 추가로 학습해서 만든 모델 사용)

- 이미지에서 표만 인식해서 추출하는 기능구현(yolo v5로 직접 학습한 모델 사용)

- 추출된 표 이미지에서 각 셀을 인식후 ocr 하여 엑셀에 넣고 반환해주는 기능구현

- 이미지에서 원하는 부분만 추출해서 ocr할수 있는 템플릿 기능구현

  1. 원하는 부분의 좌표(템플릿)를 저장해둘 수 있는 기능 구현

  2. 저장해둔 템플릿 이름을 볼 수 있도록 전체 이름을 조회하는 기능 구현

  3. 특정 템플릿의 좌표를 볼 수 있도록 조회하는 기능 구현

  4. 템플릿정보를 수정할수 있는 기능구현

  5. 템플릿 정보를 삭제하는 기능 구현

  6. 템플릿 정보를 이용해서 추출된 이미지를 ocr 하는 기능 구현

  7. 템플릿 생성시에 저장한 좌표에 이름을 붙여서 저장할수 있게 하고, 해당이름과 ocr 한 결과를 받아서 엑셀(xlsx)로 만들어서 반환해주는 기능 구현

- 레이어드 아키텍쳐에 맞게 구현

  - presentation layer(디렉토리명 - view)

  - Business layer(디렉토리명 - service)

  - Persistence layer(디렉토리명 - models)

- pytest 라이브러리를 이용해서 단위 테스트 진행
