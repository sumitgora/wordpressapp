# wordpressapp
custom demo

## kubectl apply -f argocd/application.yaml

## For S3 bucket
create service account wp-gcsfuse-ksa
provide storage.admin permission

gcloud projects add-iam-policy-binding custom-bearing-463116-p0 \
    --member "principal://iam.googleapis.com/projects/130459338492/locations/global/workloadIdentityPools/custom-bearing-463116-p0.svc.id.goog/subject/ns/app/sa/wp-gcsfuse-ksa" \
    --role "roles/storage.admin"