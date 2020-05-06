pipeline {
  environment {
    MSBUILD = "C:\Program Files (x86)\MSBuild\14.0\Bin"
    CONFIG = 'Release'
    PLATFORM = 'x64'
  }
  stages {
    stage('Build') {
      steps {
        bat "NuGet.exe restore your_project.sln"
        bat "\"${MSBUILD}\" BIM360GlueSDKSampleWebApp.sln /p:Configuration=${env.CONFIG};Platform=${env.PLATFORM} /maxcpucount:%NUMBER_OF_PROCESSORS% /nodeReuse:false"
      }
    }
  }
}
