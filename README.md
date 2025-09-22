# prefetch_research

## Ref
- berti : https://github.com/agusnt/Berti-Artifact
- ChampSim : https://github.com/ChampSim/ChampSim

## private
- L1_only : https://github.com/seongho79-jeong/L1_only_prefetcher

## Traces
- gap : https://utexas.app.box.com/s/2k54kp8zvrqdfaa8cdhfquvcxwh7yn85/folder/132804598561
- cs : https://www.dropbox.com/scl/fo/8bae1cls8b6lxppq1dhsf/AIyWkFMiZiNQfMJ7S6hll-c/CRC2_trace?rlkey=v8tcfxldwv2jtywdehkwu5kob&e=1&subfolder_nav_tracking=1&dl=0

# 환경 설정
## download spec2k17
- berti의 script를 활용해서 설정

``` bash
prefetch_research/berti$ ./download_spec2k17.sh ../traces/
```

# berti 환경 설정
## Docker

```bash
docker build -t berti_sh -f Dockerfile.berti .

docker run -it \
  --name berti_sh \
  -v /home/seongho/workspace:/workspace \
  berti_sh
```

# L1_only 환경 설정
## Docker

```bash
docker build -t prefetch_sh -f Dockerfile.L1only .

docker run -it \
  --name prefetch_sh \
  -v /home/seongho/workspace:/workspace \
  prefetch_sh
```
