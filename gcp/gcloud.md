## cliから自分のアカウントにログイン
```
gcloud auth login
# URLコピペ、ブラウザから認証
# ログイン後のコードをターミナルにコピペして認証完了

gcloud projects list

gcloud config set project {プロジェクトID}
```

## 適応されている認証情報の確認
```
gcloud config configurations list
```

## プロジェクト一覧表示
```
gcloud projects list
```

## プロジェクト切替
```
gcloud config set project {プロジェクトID}
```

## アカウントに権限を付与
```
gcloud projects add-iam-policy-binding {プロジェクト名} --member {serviceAccount:{アカウントのARN}} --role {付与するロール}
```

### アカウントの認証情報取得(account.json)
```
gcloud iam service-accounts keys create {保存するパス}/account.json \
  --iam-account terraform-serviceaccount@{プロジェクト_ID}.iam.gserviceaccount.com
```

### サーバーの環境変数にaccount.jsonを読み込ませる
```
export GOOGLE_CLOUD_KEYFILE_JSON=account.json
```

## プロジェクトに参加している全メンバーの権限確認
```
gcloud projects get-iam-policy {プロジェクト名}
```

## gcloud container clusters update  NAME（--complete-credential-rotation  
```  
| --complete-ip-rotation    
|  --enable-autoscaling     | --enable-legacy-authorization    
| --enable-master-authorized-networks |- -enable-network-policy    
| --generate-password | --logging-service = LOGGING_SERVICE    
| --maintenance-window = MAINTENANCE_WINDOW    
| --monitoring-service = MONITORING_SERVICE    
| --node-locations = ZONE、[ZONE、…]    
| --remove-labels = [KEY、…] | --set-password    
| --start-credential-rotation | --start-ip-rotation    
| --update-addons = [ADDON = ENABLED | DISABLED、…]    
| --update-labels = [KEY = VALUE、…]    
| --password = PASSWORD --enable-basic-auth    
| --username = USERNAME、-u USERNAME）[--async] 
[--master-authorized-networks = NETWORK、[NETWORK、…]] 
[--node-pool = NODE_POOL] 
[--max-nodes = MAX_NODES- -min-nodes = MIN_NODES] 
[--region = REGION    
| --zone = ZONE、-z ZONE] [GCLOUD_WIDE_FLAG…]
```

## gcloud container clusters resize NAME
```
 (--num-nodes=NUM_NODES | --size=NUM_NODES) 
[--async] 
[--node-pool=NODE_POOL] 
[--region=REGION  | --zone=ZONE, -z ZONE] 
[GCLOUD_WIDE_FLAG …]
```

## モニタリング アラートポリシー一覧表示
```
gcloud alpha monitoring policies list
```
- 既に作成されているポリシーを参考にterrafomr化する場合におすすめな出力形式
```
gcloud alpha monitoring policies describe projects/{プロジェクト名}/alertPolicies/{参考にしたいポリシーid} --format json
```
