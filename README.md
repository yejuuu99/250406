이전의 10초 카운트다운 타이머 업그레이드
 👉 _일시정지/재시작 기능 추가_


**추가적인 UX 개선 사항 적용**

✅ 타이머 종료 시 버튼 상태 초기화

타이머가 끝났을 때 '일시정지' 버튼이 '재시작'으로 바뀌도록 구성
:

if(timeLeft <= 0){
    clearInterval(timer);
    timer = null;
    displaynow.textContent = "타이머 종료!";
    prBtn.textContent = "일시정지"; // 추가한 부분
    isPaused = false; // **일시정지 검사 코드 - 이 상태도 초기화해줘야 재시작할 때 문제 없음
}
