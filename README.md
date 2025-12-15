# DH-Inspect-AI
AI-based tablet visual inspection system for pharmaceutical QC (normal vs defect classification and inspection log automation)
DH Inspect AI

AI-based Tablet Visual Inspection System for Pharmaceutical QC

⸻

Project Overview

DH Inspect AI는 제약 품질관리(QC) 현장에서 수행되는 정제 외관검사(깨짐, 이물, 결손 등)를
AI 기반 이미지 판정으로 보조하고, 검사 결과를 자동으로 기록하는 것을 목표로 하는 프로젝트이다.

본 프로젝트는 대규모 자동화 설비 도입이 어려운 중소 제약사를 주요 대상으로 하며,
QC 실무 흐름과 GMP 환경을 고려한 경량 외관검사 AI 시스템 개발을 지향한다.

⸻

Background and Problem Statement

현재 많은 제약 현장에서는 외관검사가 검사자의 육안에 의존하여 수행되고 있으며,
다음과 같은 한계가 존재한다.
	•	검사자 숙련도에 따른 판정 편차 발생
	•	장시간 검사로 인한 피로 누적 및 오류 가능성
	•	불량 판정 이력의 수기 기록 및 관리 한계
	•	GMP 실사 대응을 위한 데이터 정리 부담

⸻

Proposed Solution

DH Inspect AI는 다음과 같은 기능을 통해 외관검사 업무를 보조한다.
	•	정제 이미지 기반 정상/불량 판정
	•	QC 관점에서 정의된 외관 불량 기준 로직 적용
	•	검사 결과의 자동 기록 및 데이터화
	•	향후 불량률 분석 및 리포트 자동화 확장 가능

⸻

MVP Specification

Input
	•	정제 이미지 1장 (JPEG 또는 PNG)

Output
	•	판정 결과: 정상 또는 불량
	•	검사 일시 정보
	•	이미지 식별 정보

Data Logging
	•	검사 결과를 CSV 형식으로 자동 저장
	•	날짜, 시간, 이미지 ID, 판정 결과 기록

⸻

Development Plan

Phase 1: Image Processing Basics
	•	Grayscale 변환
	•	Thresholding 및 이진화
	•	Contour 검출
	•	정상 정제와 불량 정제의 외관 특징 정의

Phase 2: MVP AI Model
	•	기본적인 분류 모델 적용
	•	단일 이미지 입력 기반 판정 구현

Phase 3: QC-Oriented Expansion
	•	불량 유형 세분화
	•	일·주·월 단위 불량률 통계
	•	GMP 대응 외관검사 이력 리포트 포맷 설계

⸻

Target Users
	•	중소 제약사 품질관리(QC) 부서
	•	자동 외관검사 설비 미보유 업체
	•	수작업 외관검사 비중이 높은 제조 현장

⸻

Current Status
	•	프로젝트 기획 및 외관검사 QC 로직 설계 단계
	•	MVP 구현을 위한 기초 이미지 처리 학습 진행 중

⸻

Developer

Donghee (DH)
Major: Bio-Pharmaceutical Analysis
Interest: Pharmaceutical Quality Control, AI-based Inspection Systems, QC Automation
