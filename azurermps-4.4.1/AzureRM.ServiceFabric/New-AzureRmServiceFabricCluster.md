---
external help file: Microsoft.Azure.Commands.ServiceFabric.dll-Help.xml
Module Name: AzureRM.ServiceFabric
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/New-AzureRmServiceFabricCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceFabric/Commands.ServiceFabric/help/New-AzureRmServiceFabricCluster.md
ms.openlocfilehash: c1f6dea6c4fb103107a052d64a82ad81eafdb8c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569191"
---
# <span data-ttu-id="411fc-101">New-AzureRmServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="411fc-101">New-AzureRmServiceFabricCluster</span></span>

## <span data-ttu-id="411fc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="411fc-102">SYNOPSIS</span></span>
<span data-ttu-id="411fc-103">Эта команда использует сертификаты, предоставленные системой или автоматически подписанные сертификаты, для настройки нового кластера фабрики служб.</span><span class="sxs-lookup"><span data-stu-id="411fc-103">This command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="411fc-104">Он может использовать шаблон по умолчанию или настраиваемый шаблон, который вы предоставляете.</span><span class="sxs-lookup"><span data-stu-id="411fc-104">It can use a default template or a custom template that you provide.</span></span> <span data-ttu-id="411fc-105">Вы можете указать папку для экспорта самозаверяющих сертификатов в хранилище ключей или их последующего получения из него.</span><span class="sxs-lookup"><span data-stu-id="411fc-105">You have the option of specifying a folder to export the self-signed certificates to or fetching them later from the key vault.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="411fc-106">Максимальное</span><span class="sxs-lookup"><span data-stu-id="411fc-106">SYNTAX</span></span>

### <span data-ttu-id="411fc-107">ByDefaultArmTemplate (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="411fc-107">ByDefaultArmTemplate (Default)</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> [-CertificateOutputFolder <String>]
 [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 -Location <String> [-Name <String>] [-VmUserName <String>] [-ClusterSize <Int32>]
 [-CertificateSubjectName <String>] -VmPassword <SecureString> [-OS <OperatingSystem>] [-VmSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="411fc-108">ByExistingKeyVault</span><span class="sxs-lookup"><span data-stu-id="411fc-108">ByExistingKeyVault</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -SecretIdentifier <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="411fc-109">ByNewPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="411fc-109">ByNewPfxAndVaultName</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 [-CertificateOutputFolder <String>] [-CertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>]
 [-KeyVaultName <String>] [-CertificateSubjectName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="411fc-110">ByExistingPfxAndVaultName</span><span class="sxs-lookup"><span data-stu-id="411fc-110">ByExistingPfxAndVaultName</span></span>
```
New-AzureRmServiceFabricCluster [-ResourceGroupName] <String> -TemplateFile <String> -ParameterFile <String>
 -CertificateFile <String> [-CertificatePassword <SecureString>] [-SecondaryCertificateFile <String>]
 [-SecondaryCertificatePassword <SecureString>] [-KeyVaultResouceGroupName <String>] [-KeyVaultName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="411fc-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="411fc-111">DESCRIPTION</span></span>
<span data-ttu-id="411fc-112">В команде **New-AzureRmServiceFabricCluster** используются сертификаты, предоставленные и созданные системой самостоятельно подписанные сертификаты для настройки нового кластера фабрики служб.</span><span class="sxs-lookup"><span data-stu-id="411fc-112">The **New-AzureRmServiceFabricCluster** command uses certificates that you provide or system generated self-signed certificates to set up a new service fabric cluster.</span></span> <span data-ttu-id="411fc-113">Используемый шаблон может быть шаблоном по умолчанию или настраиваемым шаблоном, который вы предоставляете.</span><span class="sxs-lookup"><span data-stu-id="411fc-113">The template used can be a default template or a custom template that you provide.</span></span> <span data-ttu-id="411fc-114">Вы можете указать папку для экспорта самозаверяющих сертификатов или получить их позже из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="411fc-114">You have the option of specifying a folder to export the self-signed certificates or fetching them later from the key vault.</span></span>

<span data-ttu-id="411fc-115">Если вы указываете настраиваемый шаблон и файл параметров, вам не нужно предоставлять информацию о сертификате в файле параметров, система заполнит эти параметры.</span><span class="sxs-lookup"><span data-stu-id="411fc-115">If you are specifying a custom template and parameter file, you don't need to provide the certificate information in the parameter file, the system will populate these parameters.</span></span>

<span data-ttu-id="411fc-116">Четыре варианта описаны ниже.</span><span class="sxs-lookup"><span data-stu-id="411fc-116">The four options are detailed below.</span></span> <span data-ttu-id="411fc-117">Прокрутите вниз, чтобы получить объяснения каждого из параметров.</span><span class="sxs-lookup"><span data-stu-id="411fc-117">Scroll down for explanations of each of the parameters.</span></span>

## <span data-ttu-id="411fc-118">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="411fc-118">EXAMPLES</span></span>

### <span data-ttu-id="411fc-119">Пример 1: указание только размера кластера, имени субъекта сертификата и операционной системы для развертывания кластера.</span><span class="sxs-lookup"><span data-stu-id="411fc-119">Example 1: Specify only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>
```
$pass="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test01"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.cloudapp.azure.com" -f $RGname, $clusterloc
$pfxfolder="~\Documents"

Write-Output "create cluster in " $clusterloc "subject name for cert " $subname "and output the cert into " $pfxfolder

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -Location $clusterloc -ClusterSize 3 -VmPassword $pwd -CertificateSubjectName $subname -CertificateOutputFolder $pfxfolder -CertificatePassword $pwd -OS WindowsServer2016Datacenter
```

<span data-ttu-id="411fc-120">Эта команда задает только размер кластера, имя субъекта сертификата и операционную систему для развертывания кластера.</span><span class="sxs-lookup"><span data-stu-id="411fc-120">This command specifies only the cluster size, the cert subject name, and the OS to deploy a cluster.</span></span>

### <span data-ttu-id="411fc-121">Пример 2: Указание существующего ресурса сертификата в хранилище ключей и настраиваемого шаблона для развертывания кластера</span><span class="sxs-lookup"><span data-stu-id="411fc-121">Example 2: Specify an existing Certificate resource in a key vault and a custom template to deploy a cluster</span></span>
```
$RGname="test20"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secertId="https://test1.vault.azure.net:443/secrets/testcertificate4/56ec774dc61a462bbc645ffc9b4b225f"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -SecretIdentifier $secertId
```

<span data-ttu-id="411fc-122">Эта команда задает существующий ресурс сертификата в хранилище ключей и настраиваемый шаблон для развертывания кластера.</span><span class="sxs-lookup"><span data-stu-id="411fc-122">This command specifies an existing Certificate resource in a key vault and a custom template to deploy a cluster.</span></span>

### <span data-ttu-id="411fc-123">Пример 3: создание нового кластера с помощью настраиваемого шаблона.</span><span class="sxs-lookup"><span data-stu-id="411fc-123">Example 3: Create a new cluster using a custom template.</span></span> <span data-ttu-id="411fc-124">Укажите другое имя RG для хранилища ключей и погрузите систему в нее.</span><span class="sxs-lookup"><span data-stu-id="411fc-124">Specify the different RG name for the key vault and have the system upload the certificate to it</span></span>
```
$pwd="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$clusterloc="SouthCentralUS"
$subname="{0}.{1}.$clusterloc.cloudapp.azure.com" -f $RGName, $clusterloc
$pfxfolder="~\Documents"
$templateParmfile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="C:\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"
$secertId="https://test1.vault.azure.net:443/secrets/testcertificate4/55ec7c4dc61a462bbc645ffc9b4b225f"
$thumprint="C2D7E11DD35153A702A51D10A424A3014B9B6E8B"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateOutputFolder $pfxfolder -CertificatePassword $pwd -KeyVaultResouceGroupName $keyVaultRG  -KeyVaultName $keyVault -CertificateSubjectName $subname
```

<span data-ttu-id="411fc-125">Эта команда создает новый кластер с помощью настраиваемого шаблона.</span><span class="sxs-lookup"><span data-stu-id="411fc-125">This command creates a new cluster using a custom template.</span></span> <span data-ttu-id="411fc-126">Укажите другое имя RG для хранилища ключей и погрузите систему в нее.</span><span class="sxs-lookup"><span data-stu-id="411fc-126">Specify the different RG name for the key vault and have the system upload the certificate to it.</span></span>

### <span data-ttu-id="411fc-127">Пример 4: создание собственного сертификата и настраиваемого шаблона для создания нового кластера</span><span class="sxs-lookup"><span data-stu-id="411fc-127">Example 4: Bring your own Certificate and custom template and create a new cluster</span></span>
```
$certPwd="Password#1234" | ConvertTo-SecureString -AsPlainText -Force
$RGname="test20"
$keyVaultRG="test20kvrg"
$keyVault="test20kv"
$clusterloc="SouthCentralUS"
$pfxsourcefile="c:\Mycertificates\my2017Prodcert.pfx"
$templateParmfile="~\Documents\GitHub\azure-quickstart-templates-parms\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploytest.parameters.json"
$templateFile="~\GitHub\azure-quickstart-templates\service-fabric-secure-nsg-cluster-65-node-3-nodetype\azuredeploy.json"

New-AzureRmServiceFabricCluster -ResourceGroupName $RGname -TemplateFile $templateFile -ParameterFile $templateParmfile -CertificateSourceFile $pfxsourcefile -CertificatePassword $certpwd -KeyVaultResouceGroupName $keyVaultRG -KeyVaultName $keyVault
```

<span data-ttu-id="411fc-128">С помощью этой команды вы сможете настроить собственный сертификат и пользовательский шаблон и создать новый кластер.</span><span class="sxs-lookup"><span data-stu-id="411fc-128">This command will let you bring your own Certificate and custom template and create a new cluster.</span></span>

## <span data-ttu-id="411fc-129">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="411fc-129">PARAMETERS</span></span>

### <span data-ttu-id="411fc-130">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="411fc-130">-CertificateFile</span></span>
<span data-ttu-id="411fc-131">Существующий путь к файлу сертификата для основного сертификата кластера.</span><span class="sxs-lookup"><span data-stu-id="411fc-131">The existing certificate file path for the primary cluster certificate.</span></span>

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

### <span data-ttu-id="411fc-132">-CertificateOutputFolder</span><span class="sxs-lookup"><span data-stu-id="411fc-132">-CertificateOutputFolder</span></span>
<span data-ttu-id="411fc-133">Папка нового файла сертификата, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="411fc-133">The folder of the new certificate file to be created.</span></span>

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

### <span data-ttu-id="411fc-134">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="411fc-134">-CertificatePassword</span></span>
<span data-ttu-id="411fc-135">Пароль файла сертификата.</span><span class="sxs-lookup"><span data-stu-id="411fc-135">The password of the certificate file.</span></span>

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

### <span data-ttu-id="411fc-136">-CertificateSubjectName</span><span class="sxs-lookup"><span data-stu-id="411fc-136">-CertificateSubjectName</span></span>
<span data-ttu-id="411fc-137">Имя субъекта создаваемого сертификата.</span><span class="sxs-lookup"><span data-stu-id="411fc-137">The subject name of the certificate to be created.</span></span>

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

### <span data-ttu-id="411fc-138">-ClusterSize</span><span class="sxs-lookup"><span data-stu-id="411fc-138">-ClusterSize</span></span>
<span data-ttu-id="411fc-139">Количество узлов в кластере.</span><span class="sxs-lookup"><span data-stu-id="411fc-139">The number of nodes in the cluster.</span></span> <span data-ttu-id="411fc-140">По умолчанию — 5 узлов.</span><span class="sxs-lookup"><span data-stu-id="411fc-140">Default are 5 nodes.</span></span>

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

### <span data-ttu-id="411fc-141">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="411fc-141">-KeyVaultName</span></span>
<span data-ttu-id="411fc-142">Имя хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="411fc-142">Azure key vault name.</span></span> <span data-ttu-id="411fc-143">Если не задано, по умолчанию будет использоваться имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="411fc-143">If not given, it will be defaulted to the resource group name.</span></span>

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

### <span data-ttu-id="411fc-144">-KeyVaultResouceGroupName</span><span class="sxs-lookup"><span data-stu-id="411fc-144">-KeyVaultResouceGroupName</span></span>
<span data-ttu-id="411fc-145">Имя группы ресурсов для хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="411fc-145">Azure key vault resource group name.</span></span> <span data-ttu-id="411fc-146">Если не задано, по умолчанию будет использоваться имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="411fc-146">If not given, it will be defaulted to resource group name.</span></span>

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

### <span data-ttu-id="411fc-147">-Location</span><span class="sxs-lookup"><span data-stu-id="411fc-147">-Location</span></span>
<span data-ttu-id="411fc-148">Расположение группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="411fc-148">The resource group location.</span></span>

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

### <span data-ttu-id="411fc-149">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="411fc-149">-Name</span></span>
<span data-ttu-id="411fc-150">Укажите имя кластера.</span><span class="sxs-lookup"><span data-stu-id="411fc-150">Specify the name of the cluster.</span></span> <span data-ttu-id="411fc-151">Если не задано, оно будет совпадать с именем группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="411fc-151">If not given, it will be same as resource group name.</span></span>

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

### <span data-ttu-id="411fc-152">-OS</span><span class="sxs-lookup"><span data-stu-id="411fc-152">-OS</span></span>
<span data-ttu-id="411fc-153">Операционная система виртуальных машин, образующих кластер.</span><span class="sxs-lookup"><span data-stu-id="411fc-153">The Operating System of the VMs that make up the cluster.</span></span>

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

### <span data-ttu-id="411fc-154">-ParameterFile</span><span class="sxs-lookup"><span data-stu-id="411fc-154">-ParameterFile</span></span>
<span data-ttu-id="411fc-155">Путь к файлу параметров шаблона.</span><span class="sxs-lookup"><span data-stu-id="411fc-155">The path to the template parameter file.</span></span>

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

### <span data-ttu-id="411fc-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="411fc-156">-ResourceGroupName</span></span>
<span data-ttu-id="411fc-157">Укажите имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="411fc-157">Specify the name of the resource group.</span></span>

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

### <span data-ttu-id="411fc-158">-SecondaryCertificateFile</span><span class="sxs-lookup"><span data-stu-id="411fc-158">-SecondaryCertificateFile</span></span>
<span data-ttu-id="411fc-159">Существующий путь к файлу сертификата для вторичного сертификата кластера.</span><span class="sxs-lookup"><span data-stu-id="411fc-159">The existing certificate file path for the secondary cluster certificate.</span></span>

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

### <span data-ttu-id="411fc-160">-SecondaryCertificatePassword</span><span class="sxs-lookup"><span data-stu-id="411fc-160">-SecondaryCertificatePassword</span></span>
<span data-ttu-id="411fc-161">Пароль файла сертификата.</span><span class="sxs-lookup"><span data-stu-id="411fc-161">The password of the certificate file.</span></span>

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

### <span data-ttu-id="411fc-162">-SecretIdentifier</span><span class="sxs-lookup"><span data-stu-id="411fc-162">-SecretIdentifier</span></span>
<span data-ttu-id="411fc-163">Существующий секретный URL-адрес хранилища ключей Azure, например: " https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f ".</span><span class="sxs-lookup"><span data-stu-id="411fc-163">The existing Azure key vault secret URL, for example: 'https://mykv.vault.azure.net:443/secrets/mysecrets/55ec7c4dc61a462bbc645ffc9b4b225f'.</span></span>

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

### <span data-ttu-id="411fc-164">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="411fc-164">-TemplateFile</span></span>
<span data-ttu-id="411fc-165">Путь к файлу шаблона.</span><span class="sxs-lookup"><span data-stu-id="411fc-165">The path to the template file.</span></span>

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

### <span data-ttu-id="411fc-166">-VmPassword</span><span class="sxs-lookup"><span data-stu-id="411fc-166">-VmPassword</span></span>
<span data-ttu-id="411fc-167">Пароль виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="411fc-167">The password of the Vm.</span></span>

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

### <span data-ttu-id="411fc-168">-VmSku</span><span class="sxs-lookup"><span data-stu-id="411fc-168">-VmSku</span></span>
<span data-ttu-id="411fc-169">SKU виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="411fc-169">The Vm Sku.</span></span>

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

### <span data-ttu-id="411fc-170">-VmUserName</span><span class="sxs-lookup"><span data-stu-id="411fc-170">-VmUserName</span></span>
<span data-ttu-id="411fc-171">Имя пользователя для ведения журнала на ВМ.</span><span class="sxs-lookup"><span data-stu-id="411fc-171">The user name for logging to Vm.</span></span>

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

### <span data-ttu-id="411fc-172">-Confirm</span><span class="sxs-lookup"><span data-stu-id="411fc-172">-Confirm</span></span>
<span data-ttu-id="411fc-173">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="411fc-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="411fc-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="411fc-174">-WhatIf</span></span>
<span data-ttu-id="411fc-175">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="411fc-175">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="411fc-176">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="411fc-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="411fc-177">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="411fc-177">-DefaultProfile</span></span>
<span data-ttu-id="411fc-178">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="411fc-178">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="411fc-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="411fc-179">CommonParameters</span></span>
<span data-ttu-id="411fc-180">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="411fc-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="411fc-181">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="411fc-181">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="411fc-182">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="411fc-182">INPUTS</span></span>

### <span data-ttu-id="411fc-183">System. String</span><span class="sxs-lookup"><span data-stu-id="411fc-183">System.String</span></span>
<span data-ttu-id="411fc-184">System. Security. SecureString System. Int32 Microsoft. Azure. un, ServiceFabric. Models. для операционной системы</span><span class="sxs-lookup"><span data-stu-id="411fc-184">System.Security.SecureString System.Int32 Microsoft.Azure.Commands.ServiceFabric.Models.OperatingSystem</span></span>

## <span data-ttu-id="411fc-185">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="411fc-185">OUTPUTS</span></span>

### <span data-ttu-id="411fc-186">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span><span class="sxs-lookup"><span data-stu-id="411fc-186">Microsoft.Azure.Commands.ServiceFabric.Models.PSDeploymentResult</span></span>

## <span data-ttu-id="411fc-187">Пуск</span><span class="sxs-lookup"><span data-stu-id="411fc-187">NOTES</span></span>

## <span data-ttu-id="411fc-188">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="411fc-188">RELATED LINKS</span></span>

