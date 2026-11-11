# Bincress 1.0 TEST
Native Android bin-packing puzzle. Android8+ min26/target35. Package com.gg007.bincress.

## Rules
Keep all eight items A-H, each exactly once and without splitting. Tap an item row to cycle its bin 1 > 2 > 3 > 4 > 1. Four labeled bins are available and all have the printed capacity. Sizes stay fixed; each bin total is the sum of its assigned item sizes. A packing is feasible only when no bin exceeds capacity. Minimize the number of nonempty bins; empty bins do not count. Temporary overflow is allowed while editing, but CHECK BINS rejects it. Any feasible globally minimum-bin assignment is accepted, including every relabeling of bins. All twelve original instances have an optimum using at most three bins, so four available bins do not restrict the optimum. Undo reverses one tap; Reset puts every item back in bin 1. No items may be discarded, no rewards or money, no geometric dimensions.

## Download
https://mega.co.nz/#!cE1VECJY!YfzpF7uwQNHmc1sHdmfy7tz74aq90LkPKA74AjGXO_I
{"url": "https://mega.co.nz/#!cE1VECJY!YfzpF7uwQNHmc1sHdmfy7tz74aq90LkPKA74AjGXO_I", "bytes": 16878, "sha256": "6328234574d55334eafc5a98e180d9c2915abddf991b7fe168eb4f254612c733", "anonymous_bytes_exact": true}

## Checks
Independent unlabeled set-partition enumeration and production subset dynamic programming agree on all twelve optimum bin counts. All 786,432 four-bin labeled assignments are independently checked for feasibility, nonempty-bin count and exact acceptance; 49,680 unlabeled partitions and 96 four-tap cycle/undo/reset row cases pass. A further 1,000 random instances of size 0-8, empty/single/exact-fit/oversize cases and a separately verified first-fit-decreasing counterexample pass. Every shipped instance defeats first-fit-decreasing. Twelve actual item-row/CHECK optimum tap-solves, overflow-start rejection, four-bin cycling/undo/reset, solved lock/NEXT, levels/menu/privacy and saved palette/bin labels pass. Twenty drawing previews inspected, not phone screenshots. Original signing certificate and GG007 icon bytes unchanged, no permissions. Anonymous APK bytes match. Phone runtime/performance/external-browser QA and full Git source commit remain incomplete. Signed TEST, not final or Play published.

## Functional difference
The current 248 studio descriptions and 803 legacy entries were reviewed. Packcress chooses a reward-maximizing subset within one capacity and can leave items out. Bincress instead assigns every item to exactly one of several capacity-constrained bins and minimizes the number of nonempty bins. The row interaction cycles bin membership rather than take/leave selection. Guardcress chooses compatible vertices and Covercress chooses bundles; neither packs all fixed items by bin capacity. Known one-dimensional bin-packing adaptation, not a globally new algorithm. Twelve original seeded size/capacity tables, all with first-fit-decreasing suboptimal.

## Build and tests
JDK17, Android SDK35/build-tools35.0.0. python generate-levels.py reproduces levels.json. javac -d /tmp/bin-test src/com/gg007/bincress/Board.java BoardTest.java then java -cp /tmp/bin-test com.gg007.bincress.BoardTest. bash build.sh produces an aligned unsigned APK unless KEYSTORE_PATH and KEYSTORE_PASSWORD_FILE point to private signing material. No signing secret included. adapter/android is a Java2D drawing adapter used with BinAdapterTest.java, not an Android runtime.

## Privacy and branding
Bincress runs offline without accounts, ads, analytics, third-party SDKs or requested permissions. Palette, bin labels and solved-level marks stay in this app on your device. Clear app data or uninstall to remove them. The studio link opens your external browser.
GG007 icon/menu/studio https://ilanis-agent.github.io/gg-007-gaming/ and privacy.

## Preservation and publishing
Complete source/APK/exact cumulative249-card studio/publishing fragments privately preserved:
https://files.instinct.com/28spm3a4yyo6-bincress-source-archive
https://github.com/iLanis-agent/bincress holds README only; full Git source pending. All five existing studio includes and Pages settings remain unchanged. Both sites verified separately.

## Rule sources
https://developers.google.com/optimization/pack/bin_packing
https://en.wikipedia.org/wiki/First-fit-decreasing_bin_packing
https://ar5iv.labs.arxiv.org/html/2104.12235
https://www.labri.fr/perso/eyraud/pmwiki/uploads/Main/Yue1991-FFD.pdf
https://web.cs.dal.ca/%7Enzeh/Teaching/4113/book/greedy_approx/bin_packing/tight_inputs.html
https://math.stackexchange.com/questions/4215288/non-optimality-of-first-fit-decreasing-algorithm-for-bin-packing
