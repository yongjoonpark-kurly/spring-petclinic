### Ingress

- https://kubernetes-sigs.github.io/aws-load-balancer-controller/v2.3/guide/ingress/annotations/

**Public 인입(stg, prod)이 필요한 경우 SRE팀에 문의부탁드립니다.**

- 사내 정책으로 default value은 internal schema로 설정되어 있습니다.
- 8043 ingress에 있는 host로 들어오는 주소는 WAF를 경유하기 위한 목적이기에 반드시 public_elb(waf)로 인입점을 변경해야합니다.
- 또한 IS팀에 해당 rule 추가를 요청하셔야 합니다.
- 준비된 에러페이지가 없다면 https://www.kurly.com/shop/proc/HTTP_BAD_REQUEST.php 으로 전달됩니다.
