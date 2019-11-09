https://www.acmicpc.net/problem/11946

## 문제
알고리즘 문제해결의 세계에 오신 것을 환영한다! 여러분들은 앞으로 열심히 공부하여 세계 최대의 대학생 프로그래밍 대회인 ACM-ICPC에 참여하게 될 것이다. 따라서 ACM-ICPC의 대회 방식을 잘 익혀두는 것이 좋을 것이다. 

ACM-ICPC는 세계에서 가장 큰 프로그래밍 대회이다. 3인이 1팀을 이루어 알고리즘 문제해결 능력을 겨루며 컴퓨터는 1대만 주어진다. 각 지역에서 Regional 대회를 통해 대표를 선발한 후 선발된 팀들은 최종적으로 World Finals에서 실력을 겨루게 된다. 대회에서는 대략 10개 내외로 문제가 주어지며 5시간동안 주어진 문제들을 최대한 많이 풀어서 통과해야 한다. 만약 틀린 답안을 제출했을 경우 다음과 같은 피드백을 준다.

run-time error

time-limit exceeded

wrong answer

다음은 등수 산정 방식을 설명한 것이다.

각 팀의 등수는 문제를 많이 푼 순으로 산정된다.

만약 푼 문제 수가 같을 경우 ‘총 시간’이 작은 순으로 산정된다.

‘총 시간’은 각 문제를 풀어서 통과했을 때의 시간 값을 더한 것이다. 각 문제를 풀어서 통과하면 대회 시작으로부터 통과할 때까지 걸린 분 수와 그 문제를 통과하기 이전의 틀린 답을 제출한 횟수에 20을 곱한 패널티를 더한다. 앙 패널띠~ 

통과하지 못한 문제에 대한 패널티는 계산하지 않는다.

만약 푼 문제 수와 총 시간까지 같을 경우, Regional 대회에서는 대표를 선발하기 위해 각 지역에서 세부적인 룰을 정할 수 있다. 그러나 이 문제에서는 그럴 경우 같은 등수로 처리하도록 하자. 또한, 이미 통과한 문제는 다시 제출해서 틀리거나 맞더라도 결과에 반영되지 않는다(즉 처음 통과할 때 ‘총 시간’을 적용하도록 한다).

당신은 이제 ICPC채점팀을 도와 일할 것이다. ICPC에 참가한 팀들의 채점 정보들이 주어지면 그 정보를 바탕으로 대회의 결과를 출력하여라.

## 입력
입력의 첫 줄에는 대회에 참가한 팀의 수를 나타내는 n과(1<=n<=100) 문제 수 m(1<=m<=15), 그리고 채점 로그의 개수 q가 주어진다(0<=q<=10000).

이후에 오는 q개의 줄에는 각 채점 정보가 주어진다. 채점 정보는 경과 시간(300이하의 음이 아닌 정수), 팀 번호(1부터 n까지의 자연수), 문제 번호(1부터 m까지의 자연수), 그리고 채점 결과로 이루어져 있다. 채점 결과는 “AC”, “RE”, “TLE”, “WA”중 하나이며 각각 “Accepted”, “Run-time Error”, “Time-limit Exceeded”, “Wrong Answer”를 의미한다(“Accepted”가 통과를 의미하며 나머지는 오답으로 간주된다). 채점 정보는 채점된 순서대로 입력된다. 즉 경과 시간 순으로 입력될 것이다.

## 출력
대회가 끝난 후 팀 별 성적을 순위에 따라 출력한다. 만약 순위가 같으면 팀 번호가 빠른 것을 먼저 출력한다. 각 팀마다 팀 번호, 푼 문제 수, 총 시간을 출력한다.