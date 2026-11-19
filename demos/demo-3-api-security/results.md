# demo-3-api-security results

- summary: GREEN: 13 row(s), 0 failure(s), 0 error(s), 0 skipped
- pytest exit code of the run: 0
- media: the matrix rows and the redacted output tail rendered under
  media/evidence/ (see media/INDEX.md; listed with its sha256 in media/INDEX.md)
- the LAST 4000 CHARS of the (redacted) run log: .run-log.txt
- skipped rows make this pack RED, not green: a lane that half-ran is
  not a pass (a target-down run is refused at the door with exit 2)

## honest framing

This demo is the SECURITY story: one committed run of the authorization
matrix against the authorized local stack, with its CONFIRMED findings
in the row list. The confirmed BOLA row (order status crosses
identities) is a real vulnerability class demonstrated on the practice
target - the demo shows the framework finding and pinning it, not a
clean bill of health. No live traffic leaves the loopback; no third
party is touched (working agreement 7).
