# cg-compare

```
$ docker images
REPOSITORY   TAG       IMAGE ID       CREATED          SIZE
gdl-sem      latest    b7175db001b7   35 seconds ago   470MB
rf-sem       latest    ec0a545556f0   2 hours ago      2.07GB
vf-sem       latest    f563bfe4b139   2 hours ago      315MB
cg-sem       latest    a331dfa3caec   2 hours ago      349MB
```

google distroless images scan by Trivy
```
$ trivy image gdl-sem
2025-09-16T09:35:14Z    INFO    [vuln] Vulnerability scanning is enabled
2025-09-16T09:35:14Z    INFO    [secret] Secret scanning is enabled
2025-09-16T09:35:14Z    INFO    [secret] If your scanning is slow, please try '--scanners vuln' to disable secret scanning
2025-09-16T09:35:14Z    INFO    [secret] Please see https://trivy.dev/v0.66/docs/scanner/secret#recommendation for faster secret detection
2025-09-16T09:35:21Z    INFO    [python] Licenses acquired from one or more METADATA files may be subject to additional terms. Use `--debug` flag to see all affected packages.
2025-09-16T09:35:21Z    INFO    Detected OS     family="debian" version="12.12"
2025-09-16T09:35:21Z    INFO    [debian] Detecting vulnerabilities...   os_version="12" pkg_num=34
2025-09-16T09:35:21Z    INFO    Number of language-specific files       num=1
2025-09-16T09:35:21Z    INFO    [python-pkg] Detecting vulnerabilities...
2025-09-16T09:35:21Z    WARN    Using severities from other vendors for some vulnerabilities. Read https://trivy.dev/v0.66/docs/scanner/vulnerability#severity-selection for details.
2025-09-16T09:35:21Z    INFO    Table result includes only package filenames. Use '--format json' option to get the full path to the package file.

Report Summary

┌──────────────────────────────────────────────────────────────────────────────────┬────────────┬─────────────────┬─────────┐
│                                      Target                                      │    Type    │ Vulnerabilities │ Secrets │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ gdl-sem (debian 12.12)                                                           │   debian   │       46        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/Deprecated-1.2.18.dist-info/METADATA       │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/attrs-25.3.0.dist-info/METADATA            │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/boltons-21.0.0.dist-info/METADATA          │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/bracex-2.6.dist-info/METADATA              │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/certifi-2025.8.3.dist-info/METADATA        │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/charset_normalizer-3.4.3.dist-info/METADA- │ python-pkg │        0        │    -    │
│ TA                                                                               │            │                 │         │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/click-8.1.8.dist-info/METADATA             │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/click_option_group-0.5.7.dist-info/METADA- │ python-pkg │        0        │    -    │
│ TA                                                                               │            │                 │         │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/colorama-0.4.6.dist-info/METADATA          │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/defusedxml-0.7.1.dist-info/METADATA        │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/exceptiongroup-1.2.2.dist-info/METADATA    │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/face-24.0.0.dist-info/METADATA             │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/glom-22.1.0.dist-info/METADATA             │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/googleapis_common_protos-1.70.0.dist-info- │ python-pkg │        0        │    -    │
│ /METADATA                                                                        │            │                 │         │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/idna-3.10.dist-info/METADATA               │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/importlib_metadata-7.1.0.dist-info/METADA- │ python-pkg │        0        │    -    │
│ TA                                                                               │            │                 │         │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/jsonschema-4.25.1.dist-info/METADATA       │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/jsonschema_specifications-2025.9.1.dist-i- │ python-pkg │        0        │    -    │
│ nfo/METADATA                                                                     │            │                 │         │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/markdown_it_py-3.0.0.dist-info/METADATA    │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/mdurl-0.1.2.dist-info/METADATA             │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/opentelemetry_api-1.25.0.dist-info/METADA- │ python-pkg │        0        │    -    │
│ TA                                                                               │            │                 │         │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/opentelemetry_exporter_otlp_proto_common-- │ python-pkg │        0        │    -    │
│ 1.25.0.dist-info/METADATA                                                        │            │                 │         │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/opentelemetry_exporter_otlp_proto_http-1.- │ python-pkg │        0        │    -    │
│ 25.0.dist-info/METADATA                                                          │            │                 │         │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/opentelemetry_instrumentation-0.46b0.dist- │ python-pkg │        0        │    -    │
│ -info/METADATA                                                                   │            │                 │         │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/opentelemetry_instrumentation_requests-0.- │ python-pkg │        0        │    -    │
│ 46b0.dist-info/METADATA                                                          │            │                 │         │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/opentelemetry_proto-1.25.0.dist-info/META- │ python-pkg │        0        │    -    │
│ DATA                                                                             │            │                 │         │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/opentelemetry_sdk-1.25.0.dist-info/METADA- │ python-pkg │        0        │    -    │
│ TA                                                                               │            │                 │         │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/opentelemetry_semantic_conventions-0.46b0- │ python-pkg │        0        │    -    │
│ .dist-info/METADATA                                                              │            │                 │         │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/opentelemetry_util_http-0.46b0.dist-info/- │ python-pkg │        0        │    -    │
│ METADATA                                                                         │            │                 │         │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/packaging-25.0.dist-info/METADATA          │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/peewee-3.18.2.dist-info/METADATA           │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/pip-23.0.1.dist-info/METADATA              │ python-pkg │        1        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/protobuf-4.25.8.dist-info/METADATA         │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/pygments-2.19.2.dist-info/METADATA         │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/referencing-0.36.2.dist-info/METADATA      │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/requests-2.32.5.dist-info/METADATA         │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/rich-13.5.3.dist-info/METADATA             │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/rpds_py-0.27.1.dist-info/METADATA          │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/ruamel.yaml-0.18.15.dist-info/METADATA     │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/ruamel.yaml.clib-0.2.12.dist-info/METADATA │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/semgrep-1.136.0.dist-info/METADATA         │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/setuptools-58.1.0.dist-info/METADATA       │ python-pkg │        3        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/tomli-2.0.2.dist-info/METADATA             │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/typing_extensions-4.15.0.dist-info/METADA- │ python-pkg │        0        │    -    │
│ TA                                                                               │            │                 │         │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/urllib3-2.5.0.dist-info/METADATA           │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/wcmatch-8.5.2.dist-info/METADATA           │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/wheel-0.45.1.dist-info/METADATA            │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/wrapt-1.17.3.dist-info/METADATA            │ python-pkg │        0        │    -    │
├──────────────────────────────────────────────────────────────────────────────────┼────────────┼─────────────────┼─────────┤
│ usr/local/lib/python3.9/site-packages/zipp-3.23.0.dist-info/METADATA             │ python-pkg │        0        │    -    │
└──────────────────────────────────────────────────────────────────────────────────┴────────────┴─────────────────┴─────────┘
Legend:
- '-': Not scanned
- '0': Clean (no security findings detected)


gdl-sem (debian 12.12)

Total: 46 (UNKNOWN: 0, LOW: 30, MEDIUM: 10, HIGH: 4, CRITICAL: 2)

┌───────────────────────┬──────────────────┬──────────┬──────────────┬───────────────────┬───────────────┬─────────────────────────────────────────────────────────────┐
│        Library        │  Vulnerability   │ Severity │    Status    │ Installed Version │ Fixed Version │                            Title                            │
├───────────────────────┼──────────────────┼──────────┼──────────────┼───────────────────┼───────────────┼─────────────────────────────────────────────────────────────┤
│ gcc-12-base           │ CVE-2022-27943   │ LOW      │ affected     │ 12.2.0-14+deb12u1 │               │ binutils: libiberty/rust-demangle.c in GNU GCC 11.2 allows  │
│                       │                  │          │              │                   │               │ stack exhaustion in demangle_const                          │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2022-27943                  │
├───────────────────────┼──────────────────┤          │              ├───────────────────┼───────────────┼─────────────────────────────────────────────────────────────┤
│ libc6                 │ CVE-2010-4756    │          │              │ 2.36-9+deb12u13   │               │ glibc: glob implementation can cause excessive CPU and      │
│                       │                  │          │              │                   │               │ memory consumption due to...                                │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2010-4756                   │
│                       ├──────────────────┤          │              │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│                       │ CVE-2018-20796   │          │              │                   │               │ glibc: uncontrolled recursion in function                   │
│                       │                  │          │              │                   │               │ check_dst_limits_calc_pos_1 in posix/regexec.c              │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2018-20796                  │
│                       ├──────────────────┤          │              │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│                       │ CVE-2019-1010022 │          │              │                   │               │ glibc: stack guard protection bypass                        │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2019-1010022                │
│                       ├──────────────────┤          │              │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│                       │ CVE-2019-1010023 │          │              │                   │               │ glibc: running ldd on malicious ELF leads to code execution │
│                       │                  │          │              │                   │               │ because of...                                               │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2019-1010023                │
│                       ├──────────────────┤          │              │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│                       │ CVE-2019-1010024 │          │              │                   │               │ glibc: ASLR bypass using cache of thread stack and heap     │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2019-1010024                │
│                       ├──────────────────┤          │              │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│                       │ CVE-2019-1010025 │          │              │                   │               │ glibc: information disclosure of heap addresses of          │
│                       │                  │          │              │                   │               │ pthread_created thread                                      │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2019-1010025                │
│                       ├──────────────────┤          │              │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│                       │ CVE-2019-9192    │          │              │                   │               │ glibc: uncontrolled recursion in function                   │
│                       │                  │          │              │                   │               │ check_dst_limits_calc_pos_1 in posix/regexec.c              │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2019-9192                   │
├───────────────────────┼──────────────────┼──────────┤              ├───────────────────┼───────────────┼─────────────────────────────────────────────────────────────┤
│ libexpat1             │ CVE-2025-59375   │ HIGH     │              │ 2.5.0-1+deb12u2   │               │ expat: libexpat in Expat allows attackers to trigger large  │
│                       │                  │          │              │                   │               │ dynamic memory allocations...                               │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2025-59375                  │
│                       ├──────────────────┼──────────┤              │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│                       │ CVE-2023-52426   │ LOW      │              │                   │               │ expat: recursive XML entity expansion vulnerability         │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2023-52426                  │
│                       ├──────────────────┤          │              │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│                       │ CVE-2024-28757   │          │              │                   │               │ expat: XML Entity Expansion                                 │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2024-28757                  │
├───────────────────────┼──────────────────┤          │              ├───────────────────┼───────────────┼─────────────────────────────────────────────────────────────┤
│ libgcc-s1             │ CVE-2022-27943   │          │              │ 12.2.0-14+deb12u1 │               │ binutils: libiberty/rust-demangle.c in GNU GCC 11.2 allows  │
│                       │                  │          │              │                   │               │ stack exhaustion in demangle_const                          │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2022-27943                  │
├───────────────────────┤                  │          │              │                   ├───────────────┤                                                             │
│ libgomp1              │                  │          │              │                   │               │                                                             │
│                       │                  │          │              │                   │               │                                                             │
│                       │                  │          │              │                   │               │                                                             │
├───────────────────────┼──────────────────┤          │              ├───────────────────┼───────────────┼─────────────────────────────────────────────────────────────┤
│ libgssapi-krb5-2      │ CVE-2018-5709    │          │              │ 1.20.1-2+deb12u4  │               │ krb5: integer overflow in dbentry->n_key_data in            │
│                       │                  │          │              │                   │               │ kadmin/dbutil/dump.c                                        │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2018-5709                   │
│                       ├──────────────────┤          │              │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│                       │ CVE-2024-26458   │          │              │                   │               │ krb5: Memory leak at /krb5/src/lib/rpc/pmap_rmt.c           │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2024-26458                  │
│                       ├──────────────────┤          │              │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│                       │ CVE-2024-26461   │          │              │                   │               │ krb5: Memory leak at /krb5/src/lib/gssapi/krb5/k5sealv3.c   │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2024-26461                  │
├───────────────────────┼──────────────────┤          │              │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│ libk5crypto3          │ CVE-2018-5709    │          │              │                   │               │ krb5: integer overflow in dbentry->n_key_data in            │
│                       │                  │          │              │                   │               │ kadmin/dbutil/dump.c                                        │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2018-5709                   │
│                       ├──────────────────┤          │              │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│                       │ CVE-2024-26458   │          │              │                   │               │ krb5: Memory leak at /krb5/src/lib/rpc/pmap_rmt.c           │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2024-26458                  │
│                       ├──────────────────┤          │              │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│                       │ CVE-2024-26461   │          │              │                   │               │ krb5: Memory leak at /krb5/src/lib/gssapi/krb5/k5sealv3.c   │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2024-26461                  │
├───────────────────────┼──────────────────┤          │              │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│ libkrb5-3             │ CVE-2018-5709    │          │              │                   │               │ krb5: integer overflow in dbentry->n_key_data in            │
│                       │                  │          │              │                   │               │ kadmin/dbutil/dump.c                                        │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2018-5709                   │
│                       ├──────────────────┤          │              │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│                       │ CVE-2024-26458   │          │              │                   │               │ krb5: Memory leak at /krb5/src/lib/rpc/pmap_rmt.c           │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2024-26458                  │
│                       ├──────────────────┤          │              │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│                       │ CVE-2024-26461   │          │              │                   │               │ krb5: Memory leak at /krb5/src/lib/gssapi/krb5/k5sealv3.c   │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2024-26461                  │
├───────────────────────┼──────────────────┤          │              │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│ libkrb5support0       │ CVE-2018-5709    │          │              │                   │               │ krb5: integer overflow in dbentry->n_key_data in            │
│                       │                  │          │              │                   │               │ kadmin/dbutil/dump.c                                        │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2018-5709                   │
│                       ├──────────────────┤          │              │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│                       │ CVE-2024-26458   │          │              │                   │               │ krb5: Memory leak at /krb5/src/lib/rpc/pmap_rmt.c           │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2024-26458                  │
│                       ├──────────────────┤          │              │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│                       │ CVE-2024-26461   │          │              │                   │               │ krb5: Memory leak at /krb5/src/lib/gssapi/krb5/k5sealv3.c   │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2024-26461                  │
├───────────────────────┼──────────────────┼──────────┤              ├───────────────────┼───────────────┼─────────────────────────────────────────────────────────────┤
│ libncursesw6          │ CVE-2023-50495   │ MEDIUM   │              │ 6.4-4             │               │ ncurses: segmentation fault via _nc_wrap_entry()            │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2023-50495                  │
│                       ├──────────────────┼──────────┤              │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│                       │ CVE-2025-6141    │ LOW      │              │                   │               │ gnu-ncurses: ncurses Stack Buffer Overflow                  │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2025-6141                   │
├───────────────────────┼──────────────────┼──────────┤              ├───────────────────┼───────────────┼─────────────────────────────────────────────────────────────┤
│ libpython3.11-minimal │ CVE-2025-8194    │ HIGH     │              │ 3.11.2-6+deb12u6  │               │ cpython: Cpython infinite loop when parsing a tarfile       │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2025-8194                   │
│                       ├──────────────────┼──────────┤              │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│                       │ CVE-2025-4516    │ MEDIUM   │              │                   │               │ cpython: python: CPython DecodeError Handling Vulnerability │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2025-4516                   │
│                       ├──────────────────┤          │              │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│                       │ CVE-2025-6069    │          │              │                   │               │ cpython: Python HTMLParser quadratic complexity             │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2025-6069                   │
├───────────────────────┼──────────────────┼──────────┤              │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│ libpython3.11-stdlib  │ CVE-2025-8194    │ HIGH     │              │                   │               │ cpython: Cpython infinite loop when parsing a tarfile       │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2025-8194                   │
│                       ├──────────────────┼──────────┤              │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│                       │ CVE-2025-4516    │ MEDIUM   │              │                   │               │ cpython: python: CPython DecodeError Handling Vulnerability │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2025-4516                   │
│                       ├──────────────────┤          │              │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│                       │ CVE-2025-6069    │          │              │                   │               │ cpython: Python HTMLParser quadratic complexity             │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2025-6069                   │
├───────────────────────┼──────────────────┼──────────┤              ├───────────────────┼───────────────┼─────────────────────────────────────────────────────────────┤
│ libsqlite3-0          │ CVE-2025-7458    │ CRITICAL │              │ 3.40.1-2+deb12u2  │               │ sqlite: SQLite integer overflow                             │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2025-7458                   │
│                       ├──────────────────┼──────────┤              │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│                       │ CVE-2025-29088   │ MEDIUM   │              │                   │               │ sqlite: Denial of Service in SQLite                         │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2025-29088                  │
│                       ├──────────────────┤          │              │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│                       │ CVE-2025-7709    │          │              │                   │               │ An integer overflow exists in the FTS5                      │
│                       │                  │          │              │                   │               │ https://sqlite.org/fts5.html e ...                          │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2025-7709                   │
│                       ├──────────────────┼──────────┤              │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│                       │ CVE-2021-45346   │ LOW      │              │                   │               │ sqlite: crafted SQL query allows a malicious user to obtain │
│                       │                  │          │              │                   │               │ sensitive information...                                    │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2021-45346                  │
├───────────────────────┼──────────────────┤          │              ├───────────────────┼───────────────┼─────────────────────────────────────────────────────────────┤
│ libssl3               │ CVE-2025-27587   │          │              │ 3.0.17-1~deb12u2  │               │ OpenSSL 3.0.0 through 3.3.2 on the PowerPC architecture is  │
│                       │                  │          │              │                   │               │ vulnerable ......                                           │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2025-27587                  │
├───────────────────────┼──────────────────┤          │              ├───────────────────┼───────────────┼─────────────────────────────────────────────────────────────┤
│ libstdc++6            │ CVE-2022-27943   │          │              │ 12.2.0-14+deb12u1 │               │ binutils: libiberty/rust-demangle.c in GNU GCC 11.2 allows  │
│                       │                  │          │              │                   │               │ stack exhaustion in demangle_const                          │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2022-27943                  │
├───────────────────────┼──────────────────┼──────────┤              ├───────────────────┼───────────────┼─────────────────────────────────────────────────────────────┤
│ libtinfo6             │ CVE-2023-50495   │ MEDIUM   │              │ 6.4-4             │               │ ncurses: segmentation fault via _nc_wrap_entry()            │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2023-50495                  │
│                       ├──────────────────┼──────────┤              │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│                       │ CVE-2025-6141    │ LOW      │              │                   │               │ gnu-ncurses: ncurses Stack Buffer Overflow                  │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2025-6141                   │
├───────────────────────┼──────────────────┤          │              ├───────────────────┼───────────────┼─────────────────────────────────────────────────────────────┤
│ libuuid1              │ CVE-2022-0563    │          │              │ 2.38.1-5+deb12u3  │               │ util-linux: partial disclosure of arbitrary files in chfn   │
│                       │                  │          │              │                   │               │ and chsh when compiled...                                   │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2022-0563                   │
├───────────────────────┼──────────────────┼──────────┤              ├───────────────────┼───────────────┼─────────────────────────────────────────────────────────────┤
│ python3.11-minimal    │ CVE-2025-8194    │ HIGH     │              │ 3.11.2-6+deb12u6  │               │ cpython: Cpython infinite loop when parsing a tarfile       │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2025-8194                   │
│                       ├──────────────────┼──────────┤              │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│                       │ CVE-2025-4516    │ MEDIUM   │              │                   │               │ cpython: python: CPython DecodeError Handling Vulnerability │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2025-4516                   │
│                       ├──────────────────┤          │              │                   ├───────────────┼─────────────────────────────────────────────────────────────┤
│                       │ CVE-2025-6069    │          │              │                   │               │ cpython: Python HTMLParser quadratic complexity             │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2025-6069                   │
├───────────────────────┼──────────────────┼──────────┼──────────────┼───────────────────┼───────────────┼─────────────────────────────────────────────────────────────┤
│ zlib1g                │ CVE-2023-45853   │ CRITICAL │ will_not_fix │ 1:1.2.13.dfsg-1   │               │ zlib: integer overflow and resultant heap-based buffer      │
│                       │                  │          │              │                   │               │ overflow in zipOpenNewFileInZip4_6                          │
│                       │                  │          │              │                   │               │ https://avd.aquasec.com/nvd/cve-2023-45853                  │
└───────────────────────┴──────────────────┴──────────┴──────────────┴───────────────────┴───────────────┴─────────────────────────────────────────────────────────────┘

Python (python-pkg)

Total: 4 (UNKNOWN: 0, LOW: 0, MEDIUM: 1, HIGH: 3, CRITICAL: 0)

┌───────────────────────┬────────────────┬──────────┬────────┬───────────────────┬───────────────┬──────────────────────────────────────────────────────────┐
│        Library        │ Vulnerability  │ Severity │ Status │ Installed Version │ Fixed Version │                          Title                           │
├───────────────────────┼────────────────┼──────────┼────────┼───────────────────┼───────────────┼──────────────────────────────────────────────────────────┤
│ pip (METADATA)        │ CVE-2023-5752  │ MEDIUM   │ fixed  │ 23.0.1            │ 23.3          │ pip: Mercurial configuration injectable in repo revision │
│                       │                │          │        │                   │               │ when installing via pip                                  │
│                       │                │          │        │                   │               │ https://avd.aquasec.com/nvd/cve-2023-5752                │
├───────────────────────┼────────────────┼──────────┤        ├───────────────────┼───────────────┼──────────────────────────────────────────────────────────┤
│ setuptools (METADATA) │ CVE-2022-40897 │ HIGH     │        │ 58.1.0            │ 65.5.1        │ pypa-setuptools: Regular Expression Denial of Service    │
│                       │                │          │        │                   │               │ (ReDoS) in package_index.py                              │
│                       │                │          │        │                   │               │ https://avd.aquasec.com/nvd/cve-2022-40897               │
│                       ├────────────────┤          │        │                   ├───────────────┼──────────────────────────────────────────────────────────┤
│                       │ CVE-2024-6345  │          │        │                   │ 70.0.0        │ pypa/setuptools: Remote code execution via download      │
│                       │                │          │        │                   │               │ functions in the package_index module in...              │
│                       │                │          │        │                   │               │ https://avd.aquasec.com/nvd/cve-2024-6345                │
│                       ├────────────────┤          │        │                   ├───────────────┼──────────────────────────────────────────────────────────┤
│                       │ CVE-2025-47273 │          │        │                   │ 78.1.1        │ setuptools: Path Traversal Vulnerability in setuptools   │
│                       │                │          │        │                   │               │ PackageIndex                                             │
│                       │                │          │        │                   │               │ https://avd.aquasec.com/nvd/cve-2025-47273               │
└───────────────────────┴────────────────┴──────────┴────────┴───────────────────┴───────────────┴──────────────────────────────────────────────────────────┘

```
