pipeline{
 agent any
 stages{
  stage("dev-deploy"){
   when{
    branch "dev"
   }
   steps{
    echo"Deploy to Dev envt"
   }
  }
  stage("uat-deploy"){
   when{
    branch "uat"
   }
   steps{
    echo"Deploy to Uat envt"
   }
  }
  stage("prd-deploy"){
   when{
    branch "prd"
   }
   steps{
    echo"Deploy to prd envt"
   }
  }
 }
}
