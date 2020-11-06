---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicefabric/new-azurermservicefabriccluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/New-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/New-AzureRmServiceFabricCluster.md
ms.openlocfilehash: 5da8d1f48a50cafc970278d59b99750f283a9414
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566900"
---
# <span data-ttu-id="76919-101">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="76919-101">New-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="76919-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="76919-102">SYNOPSIS</span></span>
<span data-ttu-id="76919-103">Эта команда использует сертификаты, предоставленные системой или автоматически подписанные сертификаты, для настройки нового кластера фабрики служб.</span><span class="sxs-lookup"><span data-stu-id="76919-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="76919-104">Он может использовать шаблон по умолчанию или настраиваемый шаблон, который вы предоставляете.</span><span class="sxs-lookup"><span data-stu-id="76919-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="76919-105">Вы можете указать папку для экспорта самозаверяющих сертификатов в хранилище ключей или их последующего получения из него.</span><span class="sxs-lookup"><span data-stu-id="76919-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76919-106">Максимальное</span><span class="sxs-lookup"><span data-stu-id="76919-106">SYNTAX</span></span>

### <span data-ttu-id="76919-107">ByDefaultArmTemplate (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="76919-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76919-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="76919-108">ByExistingKeyVault</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-VmPassword <SecureString>] -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76919-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="76919-109">ByNewPfxAndVaultName</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>]
 [-KeyVaultName <String>] [-CertificateSubjectName <String>] [-VmPassword <SecureString>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76919-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="76919-110">ByExistingPfxAndVaultName</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 [-VmPassword <SecureString>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="76919-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76919-111">DESCRIPTION</span></span>
<span data-ttu-id="76919-112">В команде **New-AzureRmServiceFabricCluster** используются сертификаты, предоставленные и созданные системой самостоятельно подписанные сертификаты для настройки нового кластера фабрики служб.</span><span class="sxs-lookup"><span data-stu-id="76919-112">The **New-AzureRmServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="76919-113">Используемый шаблон может быть шаблоном по умолчанию или настраиваемым шаблоном, который вы предоставляете.</span><span class="sxs-lookup"><span data-stu-id="76919-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="76919-114">Вы можете указать папку для экспорта самозаверяющих сертификатов или получить их позже из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="76919-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>

<span data-ttu-id="76919-115">Если вы указываете настраиваемый шаблон и файл параметров, вам не нужно предоставлять информацию о сертификате в файле параметров, система заполнит эти параметры.</span><span class="sxs-lookup"><span data-stu-id="76919-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>

<span data-ttu-id="76919-116">Четыре варианта описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="76919-116">The four options are detailed below.</span></span> <span data-ttu-id="76919-117">Прокрутите вниз, чтобы получить объяснения каждого из параметров.</span><span class="sxs-lookup"><span data-stu-id="76919-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="76919-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="76919-118">EXAMPLES</span></span>

### <span data-ttu-id="76919-119">Пример 1: указание только размера кластера, имени субъекта сертификата и операционной системы для развертывания кластера.</span><span class="sxs-lookup"><span data-stu-id="76919-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test01"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.cloudapp.azure.com" -f $RGname, $clusterloc
$pfxfolder="~\Documents"

Write-Output "Create cluster in '$clusterloc' with cert subject name '$subname' and cert output path '$pfxfolder'"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -Location $clusterloc -ClusterSize 3 -VmPassword $pass -CertificateSubjectName $subname -CertificateOutputFolder $pfxfolder -CertificatePassword $pass -OS WindowsServer2016Datacenter
```

<span data-ttu-id="76919-120">Эта команда задает только размер кластера, имя субъекта сертификата и операционную систему для развертывания кластера.</span><span class="sxs-lookup"><span data-stu-id="76919-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="76919-121">Пример 2: Указание существующего ресурса сертификата в хранилище ключей и настраиваемого шаблона для развертывания кластера</span><span class="sxs-lookup"><span data-stu-id="76919-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>
```
$RGname="test20"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secretId="https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -SecretIdentifier $secretId
```

<span data-ttu-id="76919-122">Эта команда задает существующий ресурс сертификата в хранилище ключей и настраиваемый шаблон для развертывания кластера.</span><span class="sxs-lookup"><span data-stu-id="76919-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="76919-123">Пример 3: создание нового кластера с помощью настраиваемого шаблона.</span><span class="sxs-lookup"><span data-stu-id="76919-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="76919-124">Укажите другое имя группы ресурсов для хранилища ключей и добавьте в систему новый сертификат.</span><span class="sxs-lookup"><span data-stu-id="76919-124">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.$clusterloc.cloudapp.azure.com" -f $RGName, $clusterloc
$pfxfolder="~\Documents"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateOutputFolder $pfxfolder -CertificatePassword $pass -KeyVaultResouceGroupName $keyVaultRG  -KeyVaultName $keyVault -CertificateSubjectName $subname
```

<span data-ttu-id="76919-125">Эта команда создает новый кластер с помощью настраиваемого шаблона.</span><span class="sxs-lookup"><span data-stu-id="76919-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="76919-126">Укажите другое имя группы ресурсов для хранилища ключей и добавьте в систему новый сертификат.</span><span class="sxs-lookup"><span data-stu-id="76919-126">Specify a different resource group name for the key vault and have the system upload a new certificate to it</span></span>

### <span data-ttu-id="76919-127">Пример 4: создание собственного сертификата и настраиваемого шаблона для создания нового кластера</span><span class="sxs-lookup"><span data-stu-id="76919-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$pfxsourcefile="c:\Mycertificates\my2017Prodcert.pfx"
$templateParmfile="~\Documents\GitHub\azure-quickstart-templates-parms\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="~\GitHub\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateFile $pfxsourcefile -CertificatePassword $pass -KeyVaultResouceGroupName $keyVaultRG -KeyVaultName $keyVault
```

<span data-ttu-id="76919-128">С помощью этой команды вы сможете настроить собственный сертификат и пользовательский шаблон и создать новый кластер.</span><span class="sxs-lookup"><span data-stu-id="76919-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="76919-129">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="76919-129">PARAMETERS</span></span>

### <span data-ttu-id="76919-130">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="76919-130">-CertificateFile</span></span>
<span data-ttu-id="76919-131">Существующий путь к файлу сертификата для основного сертификата кластера.</span><span class="sxs-lookup"><span data-stu-id="76919-131">The existing certificate file path for the primary cluster certificate.</span></span>

```yaml
Type: String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: Source

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76919-132">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="76919-132">-CertificateOutputFolder</span></span>
<span data-ttu-id="76919-133">Папка нового файла сертификата, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="76919-133">The folder of the new certificate file to be created.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName
Aliases: Destination

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76919-134">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="76919-134">-CertificatePassword</span></span>
<span data-ttu-id="76919-135">Пароль файла сертификата.</span><span class="sxs-lookup"><span data-stu-id="76919-135">The password of the certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: CertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76919-136">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="76919-136">-CertificateSubjectName</span></span>
<span data-ttu-id="76919-137">Имя субъекта создаваемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="76919-137">The subject name of the certificate to be created.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName
Aliases: Subject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76919-138">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="76919-138">-ClusterSize</span></span>
<span data-ttu-id="76919-139">Количество узлов в кластере.</span><span class="sxs-lookup"><span data-stu-id="76919-139">The number of nodes in the cluster.</span></span> <span data-ttu-id="76919-140">По умолчанию — 5 узлов.</span><span class="sxs-lookup"><span data-stu-id="76919-140">Default are 5 nodes.</span></span>

```yaml
Type: Int32
Parameter Sets: ByDefaultArmTemplate
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76919-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76919-141">-DefaultProfile</span></span>
<span data-ttu-id="76919-142">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="76919-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76919-143">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="76919-143">-KeyVaultName</span></span>
<span data-ttu-id="76919-144">Имя хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="76919-144">Azure key vault name.</span></span> <span data-ttu-id="76919-145">Если не задано, по умолчанию будет использоваться имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="76919-145">If not given, it will be defaulted to the resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76919-146">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="76919-146">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="76919-147">Имя группы ресурсов для хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="76919-147">Azure key vault resource group name.</span></span> <span data-ttu-id="76919-148">Если не задано, по умолчанию будет использоваться имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="76919-148">If not given, it will be defaulted to resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76919-149">-Location</span><span class="sxs-lookup"><span data-stu-id="76919-149">-Location</span></span>
<span data-ttu-id="76919-150">Расположение группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="76919-150">The resource group location.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76919-151">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="76919-151">-Name</span></span>
<span data-ttu-id="76919-152">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="76919-152">Specify the name of the cluster.</span></span> <span data-ttu-id="76919-153">Если не задано, оно будет совпадать с именем группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="76919-153">If not given, it will be same as resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate
Aliases: ClusterName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76919-154">-OS</span><span class="sxs-lookup"><span data-stu-id="76919-154">-OS</span></span>
<span data-ttu-id="76919-155">Операционная система виртуальных машин, образующих кластер.</span><span class="sxs-lookup"><span data-stu-id="76919-155">The Operating System of the VMs that make up the cluster.</span></span>

```yaml
Type: OperatingSystem
Parameter Sets: ByDefaultArmTemplate
Aliases: VmImage
Accepted values: WindowsServer2012R2Datacenter, WindowsServer2016Datacenter, WindowsServer2016DatacenterwithContainers, UbuntuServer1604

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76919-156">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="76919-156">-ParameterFile</span></span>
<span data-ttu-id="76919-157">Путь к файлу параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="76919-157">The path to the template parameter file.</span></span>

```yaml
Type: String
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76919-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76919-158">-ResourceGroupName</span></span>
<span data-ttu-id="76919-159">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="76919-159">Specify the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76919-160">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="76919-160">-SecondaryCertificateFile</span></span>
<span data-ttu-id="76919-161">Существующий путь к файлу сертификата для вторичного сертификата кластера.</span><span class="sxs-lookup"><span data-stu-id="76919-161">The existing certificate file path for the secondary cluster certificate.</span></span>

```yaml
Type: String
Parameter Sets: ByExistingPfxAndVaultName
Aliases: SecSource

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76919-162">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="76919-162">-SecondaryCertificatePassword</span></span>
<span data-ttu-id="76919-163">Пароль файла сертификата.</span><span class="sxs-lookup"><span data-stu-id="76919-163">The password of the certificate file.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByExistingPfxAndVaultName
Aliases: SecCertPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76919-164">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="76919-164">-SecretIdentifier</span></span>
<span data-ttu-id="76919-165">Существующий секретный URL-адрес хранилища ключей Azure, например: " https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f ".</span><span class="sxs-lookup"><span data-stu-id="76919-165">The existing Azure key vault secret URL, for example: 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'.</span></span>

```yaml
Type: String
Parameter Sets: ByExistingKeyVault
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76919-166">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="76919-166">-TemplateFile</span></span>
<span data-ttu-id="76919-167">Путь к файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="76919-167">The path to the template file.</span></span>

```yaml
Type: String
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76919-168">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="76919-168">-VmPassword</span></span>
<span data-ttu-id="76919-169">Пароль виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="76919-169">The password of the Vm.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByDefaultArmTemplate
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: SecureString
Parameter Sets: ByExistingKeyVault, ByNewPfxAndVaultName, ByExistingPfxAndVaultName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76919-170">-VmSku</span><span class="sxs-lookup"><span data-stu-id="76919-170">-VmSku</span></span>
<span data-ttu-id="76919-171">SKU виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="76919-171">The Vm Sku.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate
Aliases: Sku

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76919-172">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="76919-172">-VmUserName</span></span>
<span data-ttu-id="76919-173">Имя пользователя для ведения журнала на ВМ.</span><span class="sxs-lookup"><span data-stu-id="76919-173">The user name for logging to Vm.</span></span>

```yaml
Type: String
Parameter Sets: ByDefaultArmTemplate
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76919-174">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76919-174">-Confirm</span></span>
<span data-ttu-id="76919-175">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="76919-175">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76919-176">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76919-176">-WhatIf</span></span>
<span data-ttu-id="76919-177">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="76919-177">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="76919-178">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="76919-178">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76919-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76919-179">CommonParameters</span></span>
<span data-ttu-id="76919-180">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="76919-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76919-181">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76919-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76919-182">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="76919-182">INPUTS</span></span>

### <span data-ttu-id="76919-183">System. String</span><span class="sxs-lookup"><span data-stu-id="76919-183">System.String</span></span>
<span data-ttu-id="76919-184">System. Security. SecureString System. Int32 Microsoft. Azure. un, ServiceFabric. Models. для операционной системы</span><span class="sxs-lookup"><span data-stu-id="76919-184">System.Security.SecureString System.Int32 Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="76919-185">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="76919-185">OUTPUTS</span></span>

### <span data-ttu-id="76919-186">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="76919-186">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="76919-187">Пуск</span><span class="sxs-lookup"><span data-stu-id="76919-187">NOTES</span></span>

## <span data-ttu-id="76919-188">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76919-188">RELATED LINKS</span></span>

