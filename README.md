# study-manifests (sunset)

GitBook 기반 study 앱(`idoyo7/study`, 이미지 `montkim9/my-gitbook`)의 Kubernetes 매니페스트 저장소였습니다.
**2026-08-02 부로 앱을 일몰**하면서 prod/stage 매니페스트를 모두 제거했습니다.

## 일몰 내역

| 대상 | 처리 |
|---|---|
| ArgoCD `study-app` (prod, stage) | `montstrap/{prod,stage}/apps/study.yaml` 삭제 → cascade delete |
| 매니페스트 | 이 저장소 `prod/`, `stage/` 삭제 |
| 중복 매니페스트 | `montstrap-manifest/{prod,stage}/study` 삭제 |
| `study.montkim.com` | 서비스 종료 (VirtualService 제거) |

## 후속 문서 사이트

study 콘텐츠는 아래 후계 사이트로 이관되었습니다.

- `idoyo7/study-hugo` — Hugo 기반, stage `study-hugo.makgol.com` / `docs.makgol.com`
- `idoyo7/study-nextra` — Nextra 기반, prod `nextra.montkim.com`
- `idoyo7/study-starlight` — Astro Starlight 기반, stage `study-starlight.makgol.com`

이 저장소는 이력 보존 목적으로만 남아 있습니다. 새 매니페스트를 추가하지 마세요.
