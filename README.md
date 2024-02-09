# Core 200 Marlin Firware 2.1.2.1
제 코어 200용 마린 펌웨어 설정입니다

## 오리지날 core 200(24v)과 다른점
- e3d revo 6 핫엔드
- 500w 파워
- 12v 전용 알루미늄 베드(온도 센서 내장) 214m x 214mm
- 챔버 온도 센서 추가
- BLTouch
- Z축 TM 스크류 피치2 리드4(베어링이 고장나서 그냥 교체)

입니다

## Configuration.h
소스 순서대로 나열했어요
- e3d revo6 적용: 센서 5번
- 베드/챔버 온도 센서: 100k옴 1번
- 챔버 온도 센서 핀 15번
- PID 값 적용
- PID 메뉴 활성화
- Mechanical/Endstop Settings
- core200에서 가져온 Movement Settings(TM 스크류 DEFAULT_AXIS_STEPS_PER_UNIT 제외; core200 800 -> 400)
- BLTouch 활성화, 오프셋 
- 좌표: 가로 X, 세로 Y 그리고 원점은 왼쪽전면쪽
- Bed Leveling: 그리드 포인트 4개, 베드 레벨링 메뉴 활성화
- 기타 EEPROM 설정, SD카드 그리고 LCD

핫엔드와 베드 PID값 그리고 프로브 오프셋은 제 프린터 측정치이므로 새로 측정해서 쓰세요. PID는 Configuration->Advanced Settings->Temperature' 메뉴에서 측정하면 됩니다.

## Configuration_adv.h
- BABYSTEPPING 활성화

## 참조
- [알루미늄 베드](https://nasspop.com/product/detail.html?product_no=638&cate_no=201&display_group=1)
- [NTC100K 챔버 온도 센서](https://nasspop.com/product/detail.html?product_no=23&cate_no=226&display_group=1)
- [BLTouch 브라켓](https://nasspop.com/product/detail.html?product_no=594&cate_no=213&display_group=1)
- XY 좌표 스왑: [Marlin 1.1.8 Core200 펌에어입니다](https://cafe.naver.com/makingtool/4370)(자유계시판, 크라이브 위우진)

----
----
[Configurations 2.1.2.1](https://github.com/MarlinFirmware/Configurations/tree/release-2.1.2.1)
README.md 원본입니다

# Configurations
Pre-tested Configurations for Marlin Firmware 2.1.2.1

Marlin Firmware is configured using two files:

- `Configuration.h` contains core configuration options like machine geometry.
- `Configuration_adv.h` contains optional settings for advanced and low level features.

For Graphical LCD these files may also be included:

- `_Bootscreen.h` provides the bitmap for a custom Boot Screen.
- `_Statusscreen.h` provides bitmaps to customize the Status Screen.

See the [Configuration page](https://marlinfw.org/docs/configuration/configuration.html) for more information about configuration and individual configuration options.
