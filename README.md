# Guestbook Final Project - Kubernetes, Autoscaling, Rolling Updates

Containerized Go guestbook app built with Docker, pushed to IBM Cloud Container Registry,
deployed to Kubernetes/OpenShift in the Skills Network lab, autoscaled with a Horizontal Pod
Autoscaler, then rolled to v2 and rolled back.

Folders:
- `answers/` - the text submitted for each graded question
- `screenshots/` - proof-of-work terminal screenshots, named by question

| Q | Task | Answer file | Proof screenshots |
|---|------|-------------|-------------------|
| 1 | Completed Dockerfile (COPY + EXPOSE) | `q1_Dockerfile.txt` | `q1_*` |
| 2 | v1 image in IBM Cloud Container Registry | `q2_crimages.txt` | `q2_*` |
| 3 | index.html (v1) | `q3_index_v1.html.txt` | `q3_*` |
| 4 | HPA created | `q4_hpa.txt` | `q4_*` |
| 5 | HPA scaled to 10 replicas under load | `q5_hpa2.txt` | `q5_*` |
| 6 | Docker push of the v2 image | `q6_upguestbook.txt` | `q6_*` |
| 7 | Deployment updated to v2 | `q7_deployment.txt` | `q7_*` |
| 8 | index.html (v2) | `q8_up-app.txt` | `q6_q8_*` |
| 9 | Rollout history, revision 3 (CPU limits/requests) | `q9_rev.txt` | `q9_*` |
| 10 | ReplicaSets after rollback | `q10_rs.txt` | `q10_*` |

Notes
- A first deploy failed with `InvalidImageName` because `deployment.yml` still held the
  `<your sn labs namespace>` placeholder. Replacing it fixed the pod and let the HPA read CPU
  metrics (`q5_03`, `q5_04`).
- Setup screenshots are prefixed `00_`.
