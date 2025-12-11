# tommipontinen76/scoop-bucket

Just my own Scoop bucket for portable software that are not in winget, scoop or chocolatey.


You can add this bucket to Scoop so you can install the programs it contains:

```powershell
scoop bucket add tommipontinen76 https://github.com/tommipontinen76/scoop-bucket.git
```

Check that the bucket was added:

```powershell
scoop bucket list
```


## Search and install programs

After adding the bucket, search for available apps:

```powershell
scoop search <app-name>
```

Install an app from this bucket:

```powershell
scoop install <app-name>
```

If two buckets provide the same app name, you can force a bucket-qualified install:

```powershell
scoop install tommipontinen76/<app-name>
```

Alternative: install directly from a raw manifest URL (no need to add the bucket):

```powershell
scoop install https://raw.githubusercontent.com/tommipontinen76/scoop-bucket/main/<app-name>.json
```

---

## Update & remove

Update manifests (buckets) and upgrade installed apps:

```powershell
scoop update
scoop update <app-name>
```

Update just this bucket's manifests:

```powershell
scoop bucket rm tommipontinen76    # removes the bucket if you no longer want it
scoop bucket add tommipontinen76 https://github.com/tommipontinen76/scoop-bucket.git
```

Uninstall an app:

```powershell
scoop uninstall <app-name>
```

---

## Troubleshooting

- If a download fails, try again — network/CDN issues sometimes occur.
- If manifests change, run `scoop update` before `scoop install`.
- Ensure PowerShell execution policy and TLS 1.2 are enabled on older Windows versions.

---


## License & Disclaimer

This bucket contains third-party software manifests. Use at your own risk. Check each application's upstream license and source before installing.

If you find anything broken or missing, open an issue or a PR in this repo.

Enjoy!
