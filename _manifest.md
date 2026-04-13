# _manifest.md: SOC Strategic Alignment Simulator (soc-paradox-sim)

## Asset Inventory
| Path | Responsibility | Complexity |
| :--- | :--- | :--- |
| `index.html` | UI/UX, Game Mechanics, Firebase Logic | High (26KB Monolith) |
| `.github/workflows/deploy.yml` | CI/CD for GitHub Pages | Low |

## Debt & Constraints
- **Monolithic `index.html`:** For simplicity, all logic is in one file. This is acceptable for this scale but may require refactoring if features expand.
- **Firebase Keys:** Hardcoded in the client source (restricted in Firebase Console).

## Known Risks
- **Network Lag:** Simulator initialization requires active Firebase Auth.
- **Visual Performance:** High alert volumes (Protocol A) may cause lag on lower-end hardware (expected for study load).
