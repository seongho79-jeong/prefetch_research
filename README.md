# prefetch_research

## Ref
- berti : https://github.com/agusnt/Berti-Artifact
- ChampSim : https://github.com/ChampSim/ChampSim

## private
- L1_only : https://github.com/seongho79-jeong/L1_only_prefetcher

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
