---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceFabric.dll-Help.xml
Module Name: Az.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric/new-azservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/New-AzServiceFabricCluster.md
ms.openlocfilehash: 9e5ba2d2ee228da30a887c0c7b318dd9d270d763
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326188"
---
# <span data-ttu-id="f804f-101">New-AzServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="f804f-101">New-AzServiceFabricCluster</span></span>

## <span data-ttu-id="f804f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f804f-102">SYNOPSIS</span></span>

<span data-ttu-id="f804f-103">В этой команде используются сертификаты, которые вы предоставляете, или системные самозаверяемые сертификаты для настроить новый кластер тканью службы.</span><span class="sxs-lookup"><span data-stu-id="f804f-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="f804f-104">Он может использовать шаблон по умолчанию или настраиваемый шаблон, который вы предоставляете.</span><span class="sxs-lookup"><span data-stu-id="f804f-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="f804f-105">Вы можете указать папку для экспорта самозаверяющих сертификатов или их позднего получения из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="f804f-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span>

## <span data-ttu-id="f804f-106">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f804f-106">SYNTAX</span></span>

### <span data-ttu-id="f804f-107">ByDefaultArmTemplate (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f804f-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f804f-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="f804f-108">ByExistingKeyVault</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 -SecretIdentifier <String> [-Thumbprint <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f804f-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="f804f-109">ByNewPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>]
 [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>] [-CertificateSubjectName <String>]
 [-VmPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f804f-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="f804f-110">ByExistingPfxAndVaultName</span></span>
```
New-AzServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResourceGroupName <String>] [-KeyVaultName <String>]
 [-CertificateCommonName <String>] [-CertificateIssuerThumbprint <String>] [-VmPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f804f-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f804f-111">DESCRIPTION</span></span>

<span data-ttu-id="f804f-112">Команда **New-AzServiceFabricCluster** использует сертификаты, которые вы предоставляете, или системные самозаверяемые сертификаты для настроить новый кластер с тканью службы.</span><span class="sxs-lookup"><span data-stu-id="f804f-112">The **New-AzServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="f804f-113">Используемый шаблон может быть шаблоном по умолчанию или пользовательским шаблоном, который вы предоставляете.</span><span class="sxs-lookup"><span data-stu-id="f804f-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="f804f-114">Вы можете указать папку для экспорта самозаверяющих сертификатов или их позднего получения из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="f804f-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>
<span data-ttu-id="f804f-115">Если вы указываете настраиваемый файл шаблона и параметра, вам не нужно указывать сведения о сертификате в файле параметров, система заполнит эти параметры.</span><span class="sxs-lookup"><span data-stu-id="f804f-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>
<span data-ttu-id="f804f-116">Ниже описаны четыре варианта.</span><span class="sxs-lookup"><span data-stu-id="f804f-116">The four options are detailed below.</span></span> <span data-ttu-id="f804f-117">Прокрутите страницу вниз, чтобы просмотреть пояснения к каждому из параметров.</span><span class="sxs-lookup"><span data-stu-id="f804f-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="f804f-118">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f804f-118">EXAMPLES</span></span>

### <span data-ttu-id="f804f-119">Пример 1. Укажите только размер кластера, название темы сертификации и оси для развертывания кластера.</span><span class="sxs-lookup"><span data-stu-id="f804f-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "quickstart-sf-group"
$azureRegion = "southcentralus"
$clusterDnsName = "{0}.{1}.cloudapp.azure.com" -f $resourceGroupName, $azureRegion
$localCertificateFolder = "c:\certs"

Write-Output "Create cluster in '$azureRegion' with cert subject name '$clusterDnsName' and cert output path '$localCertificateFolder'"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -Location $azureRegion -ClusterSize 5 -VmPassword $password -CertificateSubjectName $clusterDnsName -CertificateOutputFolder $localCertificateFolder -CertificatePassword $pass -OS WindowsServer2016Datacenter
```

<span data-ttu-id="f804f-120">Эта команда определяет только размер кластера, имя темы сертификации и оси для развертывания кластера.</span><span class="sxs-lookup"><span data-stu-id="f804f-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="f804f-121">Пример 2. Указание существующего ресурса сертификата в хранилище ключа и настраиваемого шаблона для развертывания кластера</span><span class="sxs-lookup"><span data-stu-id="f804f-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>

```powershell
$resourceGroupName = "test20"
$templateParameterFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secretId = "https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -SecretIdentifier $secretId
```

<span data-ttu-id="f804f-122">Эта команда определяет существующий ресурс сертификата в хранилище ключа и настраиваемый шаблон для развертывания кластера.</span><span class="sxs-lookup"><span data-stu-id="f804f-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="f804f-123">Пример 3. Создание нового кластера с помощью настраиваемой шаблона.</span><span class="sxs-lookup"><span data-stu-id="f804f-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="f804f-124">Указание другого имени группы ресурсов для хранилища ключа и отправка системой нового сертификата в него</span><span class="sxs-lookup"><span data-stu-id="f804f-124">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "quickstart-sf-group"
$keyVaultResourceGroupName = " quickstart-kv-group"
$keyVaultName = "quickstart-kv"
$azureRegion = "southcentralus"
$clusterDnsName = "{0}.{1}.cloudapp.azure.com" -F $resourceGroupName, $azureRegion
$localCertificateFolder = "~\Documents"
$templateParameterFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -CertificateOutputFolder $localCertificateFolder -CertificatePassword $password -KeyVaultResourceGroupName $keyVaultResourceGroupName  -KeyVaultName $keyVaultName -CertificateSubjectName $clusterDnsName
```

<span data-ttu-id="f804f-125">Эта команда создает новый кластер с использованием настраиваемой шаблона.</span><span class="sxs-lookup"><span data-stu-id="f804f-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="f804f-126">Указание другого имени группы ресурсов для хранилища ключа и отправка системой нового сертификата в него</span><span class="sxs-lookup"><span data-stu-id="f804f-126">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

### <span data-ttu-id="f804f-127">Пример 4. Создание собственного сертификата и настраиваемго шаблона и создание нового кластера</span><span class="sxs-lookup"><span data-stu-id="f804f-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>

```powershell
$password = "Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$resourceGroupName = "test20"
$keyVaultResourceGroupName = "test20kvrg"
$keyVaultName = "test20kv"
$localCertificateFile = "c:\Mycertificates\my2017Prodcert.pfx"
$templateParameterFile = "~\Documents\GitHub\azure-quickstart-templates-parms\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile = "~\GitHub\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzServiceFabricCluster -ResourceGroupName $resourceGroupName -TemplateFile $templateFile -ParameterFile $templateParameterFile -CertificateFile $localCertificateFile -CertificatePassword $password -KeyVaultResourceGroupName $keyVaultResourceGroupName -KeyVaultName $keyVaultName
```

<span data-ttu-id="f804f-128">Эта команда позволит вам создать собственный сертификат и настраиваемый шаблон и создать новый кластер.</span><span class="sxs-lookup"><span data-stu-id="f804f-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="f804f-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f804f-129">PARAMETERS</span></span>

### <span data-ttu-id="f804f-130">-CertificateCommonName</span><span class="sxs-lookup"><span data-stu-id="f804f-130">-CertificateCommonName</span></span>

<span data-ttu-id="f804f-131">Общее имя сертификата</span><span class="sxs-lookup"><span data-stu-id="f804f-131">Certificate common name</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByExistingPfxAndVaultName
Aliases: CertCommonName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f804f-132">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="f804f-132">-CertificateFile</span></span>

<span data-ttu-id="f804f-133">Путь к существующему файлу сертификата для основного сертификата кластера</span><span class="sxs-lookup"><span data-stu-id="f804f-133">The existing certificate file path for the primary cluster certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: Source

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f804f-134">-CertificateIssuerThumbprint</span><span class="sxs-lookup"><span data-stu-id="f804f-134">-CertificateIssuerThumbprint</span></span>

<span data-ttu-id="f804f-135">Thumbprint issuer Certificate, separated by запятые, если их несколько</span><span class="sxs-lookup"><span data-stu-id="f804f-135">Certificate issuer thumbprint, separated by commas if more than one</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByExistingPfxAndVaultName
Aliases: CertIssuerThumbprint

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f804f-136">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="f804f-136">-CertificateOutputFolder</span></span>

<span data-ttu-id="f804f-137">Папка нового файла сертификата, который нужно создать</span><span class="sxs-lookup"><span data-stu-id="f804f-137">The folder of the new certificate file to be created</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName
Aliases: Destination

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f804f-138">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="f804f-138">-CertificatePassword</span></span>

<span data-ttu-id="f804f-139">Пароль файла сертификата</span><span class="sxs-lookup"><span data-stu-id="f804f-139">The password of the certificate file</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: CertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f804f-140">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="f804f-140">-CertificateSubjectName</span></span>

<span data-ttu-id="f804f-141">Имя темы создаемого сертификата</span><span class="sxs-lookup"><span data-stu-id="f804f-141">The subject name of the certificate to be created</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName
Aliases: Subject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f804f-142">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="f804f-142">-ClusterSize</span></span>

<span data-ttu-id="f804f-143">Количество узлов в кластере.</span><span class="sxs-lookup"><span data-stu-id="f804f-143">The number of nodes in the cluster.</span></span>
<span data-ttu-id="f804f-144">По умолчанию 5 узлов</span><span class="sxs-lookup"><span data-stu-id="f804f-144">Default are 5 nodes</span></span>

```yaml
Type: System.Int32
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f804f-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f804f-145">-DefaultProfile</span></span>

<span data-ttu-id="f804f-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f804f-146">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f804f-147">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="f804f-147">-KeyVaultName</span></span>

<span data-ttu-id="f804f-148">Имя ключа хранилища Azure, если его не сделать, будет по умолчанию задано имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f804f-148">Azure key vault name, if not given it will be defaulted to the resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f804f-149">-KeyVaultResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f804f-149">-KeyVaultResourceGroupName</span></span>

<span data-ttu-id="f804f-150">Имя группы ресурсов в ключевых хранилищах Azure, если не задано, будет по умолчанию задано имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f804f-150">Azure key vault resource group name, if not given it will be defaulted to resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: KeyVaultResouceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f804f-151">-Location</span><span class="sxs-lookup"><span data-stu-id="f804f-151">-Location</span></span>

<span data-ttu-id="f804f-152">Расположение группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="f804f-152">The resource group location</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f804f-153">-Name</span><span class="sxs-lookup"><span data-stu-id="f804f-153">-Name</span></span>

<span data-ttu-id="f804f-154">Укажите имя кластера, если он не задан, будет иметь такое же имя, как имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f804f-154">Specify the name of the cluster, if not given it will be same as resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases: ClusterName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f804f-155">-OS</span><span class="sxs-lookup"><span data-stu-id="f804f-155">-OS</span></span>

<span data-ttu-id="f804f-156">Операционная система ВМ-карт, которые составляют кластер.</span><span class="sxs-lookup"><span data-stu-id="f804f-156">The Operating System of the VMs that make up the cluster.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem
Parameter Sets: ByDefaultArmTemplate
Aliases: VmImage
Accepted values: WindowsServer2012R2Datacenter, WindowsServer2016Datacenter, WindowsServer2016DatacenterwithContainers, UbuntuServer1604

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f804f-157">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="f804f-157">-ParameterFile</span></span>

<span data-ttu-id="f804f-158">Путь к файлу параметра шаблона.</span><span class="sxs-lookup"><span data-stu-id="f804f-158">The path to the template parameter file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f804f-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f804f-159">-ResourceGroupName</span></span>

<span data-ttu-id="f804f-160">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f804f-160">Specify the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f804f-161">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="f804f-161">-SecondaryCertificateFile</span></span>

<span data-ttu-id="f804f-162">Путь к существующему файлу сертификата для дополнительного сертификата кластера</span><span class="sxs-lookup"><span data-stu-id="f804f-162">The existing certificate file path for the secondary cluster certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: SecSource

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f804f-163">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="f804f-163">-SecondaryCertificatePassword</span></span>

<span data-ttu-id="f804f-164">Пароль файла сертификата</span><span class="sxs-lookup"><span data-stu-id="f804f-164">The password of the certificate file</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByExistingPfxAndVaultName
Aliases: SecCertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f804f-165">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="f804f-165">-SecretIdentifier</span></span>

<span data-ttu-id="f804f-166">Существующий секретный URL-адрес хранилища ключей Azure, например https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f '</span><span class="sxs-lookup"><span data-stu-id="f804f-166">The existing Azure key vault secret URL, for example 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f804f-167">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="f804f-167">-TemplateFile</span></span>

<span data-ttu-id="f804f-168">Путь к файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="f804f-168">The path to the template file.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f804f-169">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="f804f-169">-Thumbprint</span></span>
<span data-ttu-id="f804f-170">The thumbprint for the certificate correspoinding to the SecretIdentifier.</span><span class="sxs-lookup"><span data-stu-id="f804f-170">The thumbprint for the certificate correspoinding to the SecretIdentifier.</span></span> <span data-ttu-id="f804f-171">Используйте этот способ, если управление сертификатом не производится, так как хранилище ключей будет храниться только как секретный сертификат и вы не сможете отодрить его.</span><span class="sxs-lookup"><span data-stu-id="f804f-171">Use this if the certificate is not managed as the key vault would only have the certificate stored as a secret and the cmdlet is unable to retreive the thumbprint.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExistingKeyVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f804f-172">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="f804f-172">-VmPassword</span></span>

<span data-ttu-id="f804f-173">Пароль VM-записи.</span><span class="sxs-lookup"><span data-stu-id="f804f-173">The password of the Vm.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f804f-174">-VmSku</span><span class="sxs-lookup"><span data-stu-id="f804f-174">-VmSku</span></span>

<span data-ttu-id="f804f-175">The Vm Sku</span><span class="sxs-lookup"><span data-stu-id="f804f-175">The Vm Sku</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases: Sku

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f804f-176">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="f804f-176">-VmUserName</span></span>

<span data-ttu-id="f804f-177">Имя пользователя для ведения журнала на VM</span><span class="sxs-lookup"><span data-stu-id="f804f-177">The user name for logging to Vm</span></span>

```yaml
Type: System.String
Parameter Sets: ByDefaultArmTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f804f-178">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f804f-178">-Confirm</span></span>

<span data-ttu-id="f804f-179">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f804f-179">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f804f-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f804f-180">-WhatIf</span></span>

<span data-ttu-id="f804f-181">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f804f-181">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f804f-182">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f804f-182">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f804f-183">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f804f-183">CommonParameters</span></span>
<span data-ttu-id="f804f-184">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f804f-184">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f804f-185">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f804f-185">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f804f-186">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f804f-186">INPUTS</span></span>

### <span data-ttu-id="f804f-187">System.String</span><span class="sxs-lookup"><span data-stu-id="f804f-187">System.String</span></span>

### <span data-ttu-id="f804f-188">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="f804f-188">System.Security.SecureString</span></span>

### <span data-ttu-id="f804f-189">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f804f-189">System.Int32</span></span>

### <span data-ttu-id="f804f-190">Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="f804f-190">Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="f804f-191">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f804f-191">OUTPUTS</span></span>

### <span data-ttu-id="f804f-192">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="f804f-192">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="f804f-193">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f804f-193">NOTES</span></span>

## <span data-ttu-id="f804f-194">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f804f-194">RELATED LINKS</span></span>
