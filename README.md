# enformer_tutorial

## 🔐 SSH 접속

```bash
ssh moonwonchoi@147.47.200.131 -p 22555
```
## 📁 디렉토리 이동
```bash
cd /media/leelabsg-storage1/moonwon/enformer_tutorial
```
```bash
mkdir /media/leelabsg-storage1/moonwon/enformer_tutorial/{폴더_이름}
```
## 🐍 Conda 환경 활성화
```bash
conda activate personalized_enformer
```
## 🧬 참조 유전체의 gene sequence에서 SNP 변경
먼저 작업할 디렉토리로 이동합니다:
```bash
mv {폴더_이름}
```
그 다음, bcftools를 사용해 개인화된 유전체로 변환합니다:
```bash
bcftools consensus -s MW00105 \
  -f /media/leelabsg-storage1/moonwon/enformer_tutorial/ENSG00000001630.fa \
  -I -H 2pIu \
  /media/leelabsg-storage1/moonwon/enformer_tutorial/tutorial.vcf.gz \
  > ./ENSG00000001630.fa
```
