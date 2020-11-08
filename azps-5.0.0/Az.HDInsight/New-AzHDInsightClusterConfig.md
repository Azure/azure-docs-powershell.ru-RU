---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 1124136a580d0079690c60e31fe8de8649e3cafb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247841"
---
# <span data-ttu-id="225bd-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="225bd-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="225bd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="225bd-102">SYNOPSIS</span></span>
<span data-ttu-id="225bd-103">Создает несохраняемый объект конфигурации кластера, описывающий конфигурацию кластера Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="225bd-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="225bd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="225bd-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [-StorageAccountResourceId <String>] [-StorageAccountKey <String>]
 [-StorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-MinSupportedTlsVersion <String>]
 [-AssignedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>]
 [-EncryptionAtHost <Boolean>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="225bd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="225bd-105">DESCRIPTION</span></span>
<span data-ttu-id="225bd-106">Командлет **New-AzHDInsightClusterConfig** создает несохраняемый объект, который описывает конфигурацию кластера Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="225bd-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="225bd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="225bd-107">EXAMPLES</span></span>

### <span data-ttu-id="225bd-108">Пример 1: создание объекта конфигурации кластера</span><span class="sxs-lookup"><span data-stu-id="225bd-108">Example 1: Create a cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageaccountname"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer
```

<span data-ttu-id="225bd-109">Эта команда создает объект конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="225bd-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="225bd-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="225bd-110">PARAMETERS</span></span>

### <span data-ttu-id="225bd-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="225bd-111">-AadTenantId</span></span>
<span data-ttu-id="225bd-112">Указывает идентификатор клиента Azure AD, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="225bd-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225bd-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="225bd-113">-ApplicationId</span></span>
<span data-ttu-id="225bd-114">Возвращает или задает идентификатор приложения субъекта-службы для доступа к Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="225bd-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225bd-115">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="225bd-115">-AssignedIdentity</span></span>
<span data-ttu-id="225bd-116">Возвращает или задает назначенное удостоверение.</span><span class="sxs-lookup"><span data-stu-id="225bd-116">Gets or sets the assigned identity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225bd-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="225bd-117">-CertificateFileContents</span></span>
<span data-ttu-id="225bd-118">Указывает содержимое файла сертификата, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="225bd-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225bd-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="225bd-119">-CertificateFilePath</span></span>
<span data-ttu-id="225bd-120">Задает путь к файлу сертификата, который будет использоваться для проверки подлинности участника-службы.</span><span class="sxs-lookup"><span data-stu-id="225bd-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="225bd-121">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="225bd-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225bd-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="225bd-122">-CertificatePassword</span></span>
<span data-ttu-id="225bd-123">Указывает пароль сертификата, который будет использоваться для проверки подлинности в качестве субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="225bd-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="225bd-124">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="225bd-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225bd-125">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="225bd-125">-ClusterTier</span></span>
<span data-ttu-id="225bd-126">Указывает уровень кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="225bd-126">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="225bd-127">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="225bd-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="225bd-128">Стандартная</span><span class="sxs-lookup"><span data-stu-id="225bd-128">Standard</span></span>
- <span data-ttu-id="225bd-129">Premium по умолчанию используется значение Standard.</span><span class="sxs-lookup"><span data-stu-id="225bd-129">Premium The default value is Standard.</span></span>
<span data-ttu-id="225bd-130">Уровень Premium можно использовать только для кластеров Linux, а также для использования некоторых новых функций.</span><span class="sxs-lookup"><span data-stu-id="225bd-130">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.Tier
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225bd-131">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="225bd-131">-ClusterType</span></span>
<span data-ttu-id="225bd-132">Указывает тип создаваемого кластера.</span><span class="sxs-lookup"><span data-stu-id="225bd-132">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="225bd-133">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="225bd-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="225bd-134">Hadoop</span><span class="sxs-lookup"><span data-stu-id="225bd-134">Hadoop</span></span>
- <span data-ttu-id="225bd-135">HBase</span><span class="sxs-lookup"><span data-stu-id="225bd-135">HBase</span></span>
- <span data-ttu-id="225bd-136">Огонь</span><span class="sxs-lookup"><span data-stu-id="225bd-136">Storm</span></span>
- <span data-ttu-id="225bd-137">Spark</span><span class="sxs-lookup"><span data-stu-id="225bd-137">Spark</span></span>
- <span data-ttu-id="225bd-138">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="225bd-138">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="225bd-139">Kafka</span><span class="sxs-lookup"><span data-stu-id="225bd-139">Kafka</span></span>
- <span data-ttu-id="225bd-140">RServer</span><span class="sxs-lookup"><span data-stu-id="225bd-140">RServer</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225bd-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="225bd-141">-DefaultProfile</span></span>
<span data-ttu-id="225bd-142">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="225bd-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="225bd-143">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="225bd-143">-EdgeNodeSize</span></span>
<span data-ttu-id="225bd-144">Указывает размер виртуальной машины для граничного узла.</span><span class="sxs-lookup"><span data-stu-id="225bd-144">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="225bd-145">Используйте Get-AzVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="225bd-145">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="225bd-146">Этот параметр является допустимым только для кластеров RServer.</span><span class="sxs-lookup"><span data-stu-id="225bd-146">This parameter is valid only for RServer clusters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225bd-147">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="225bd-147">-EncryptionAlgorithm</span></span>
<span data-ttu-id="225bd-148">Возвращает или задает алгоритм шифрования.</span><span class="sxs-lookup"><span data-stu-id="225bd-148">Gets or sets the encryption algorithm.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA-OAEP-256, RSA1_5

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225bd-149">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="225bd-149">-EncryptionAtHost</span></span>
<span data-ttu-id="225bd-150">Возвращает или задает флаг, указывающий, следует ли включить шифрование на хосте или нет.</span><span class="sxs-lookup"><span data-stu-id="225bd-150">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225bd-151">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="225bd-151">-EncryptionInTransit</span></span>
<span data-ttu-id="225bd-152">Возвращает или задает флаг, указывающий, следует ли включить шифрование в пути или нет.</span><span class="sxs-lookup"><span data-stu-id="225bd-152">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225bd-153">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="225bd-153">-EncryptionKeyName</span></span>
<span data-ttu-id="225bd-154">Возвращает или задает имя ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="225bd-154">Gets or sets the encryption key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225bd-155">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="225bd-155">-EncryptionKeyVersion</span></span>
<span data-ttu-id="225bd-156">Возвращает или задает версию ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="225bd-156">Gets or sets the encryption key version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225bd-157">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="225bd-157">-EncryptionVaultUri</span></span>
<span data-ttu-id="225bd-158">Возвращает или задает универсальный код ресурса (URI) для хранилища шифрования.</span><span class="sxs-lookup"><span data-stu-id="225bd-158">Gets or sets the encryption vault uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225bd-159">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="225bd-159">-HeadNodeSize</span></span>
<span data-ttu-id="225bd-160">Задает размер виртуальной машины для головного узла.</span><span class="sxs-lookup"><span data-stu-id="225bd-160">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="225bd-161">Используйте Get-AzVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="225bd-161">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225bd-162">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="225bd-162">-HiveMetastore</span></span>
<span data-ttu-id="225bd-163">Указывает MetaStore для хранения метаданных куста.</span><span class="sxs-lookup"><span data-stu-id="225bd-163">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="225bd-164">Вы также можете использовать командлет Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="225bd-164">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225bd-165">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="225bd-165">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="225bd-166">Возвращает или задает минимальную поддерживаемую версию TLS.</span><span class="sxs-lookup"><span data-stu-id="225bd-166">Gets or sets the minimal supported TLS version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225bd-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="225bd-167">-ObjectId</span></span>
<span data-ttu-id="225bd-168">Указывает идентификатор объекта Azure AD (GUID) субъекта-службы Azure AD, который представляет этот кластер.</span><span class="sxs-lookup"><span data-stu-id="225bd-168">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="225bd-169">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="225bd-169">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225bd-170">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="225bd-170">-OozieMetastore</span></span>
<span data-ttu-id="225bd-171">Указывает MetaStore для хранения метаданных Oozie.</span><span class="sxs-lookup"><span data-stu-id="225bd-171">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="225bd-172">Вы также можете использовать командлет **Add-AzHDInsightMetastore** .</span><span class="sxs-lookup"><span data-stu-id="225bd-172">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225bd-173">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="225bd-173">-StorageAccountKey</span></span>
<span data-ttu-id="225bd-174">Возвращает или задает ключ доступа к учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="225bd-174">Gets or sets the storage account access key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225bd-175">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="225bd-175">-StorageAccountResourceId</span></span>
<span data-ttu-id="225bd-176">Возвращает или задает идентификатор ресурса учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="225bd-176">Gets or sets the storage account resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225bd-177">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="225bd-177">-StorageAccountType</span></span>
<span data-ttu-id="225bd-178">Возвращает или задает тип учетной записи хранения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="225bd-178">Gets or sets the type of the default storage account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore, AzureDataLakeStorageGen2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225bd-179">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="225bd-179">-WorkerNodeSize</span></span>
<span data-ttu-id="225bd-180">Указывает размер виртуальной машины для рабочего узла.</span><span class="sxs-lookup"><span data-stu-id="225bd-180">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="225bd-181">Используйте Get-AzVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="225bd-181">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225bd-182">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="225bd-182">-ZookeeperNodeSize</span></span>
<span data-ttu-id="225bd-183">Указывает размер виртуальной машины для узла Джесс.</span><span class="sxs-lookup"><span data-stu-id="225bd-183">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="225bd-184">Используйте Get-AzVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="225bd-184">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="225bd-185">Этот параметр является допустимым только для кластеров HBase и.</span><span class="sxs-lookup"><span data-stu-id="225bd-185">This parameter is valid only for HBase or Storm clusters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="225bd-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="225bd-186">CommonParameters</span></span>
<span data-ttu-id="225bd-187">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="225bd-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="225bd-188">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="225bd-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="225bd-189">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="225bd-189">INPUTS</span></span>

### <span data-ttu-id="225bd-190">Ничего</span><span class="sxs-lookup"><span data-stu-id="225bd-190">None</span></span>

## <span data-ttu-id="225bd-191">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="225bd-191">OUTPUTS</span></span>

### <span data-ttu-id="225bd-192">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="225bd-192">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="225bd-193">Пуск</span><span class="sxs-lookup"><span data-stu-id="225bd-193">NOTES</span></span>

## <span data-ttu-id="225bd-194">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="225bd-194">RELATED LINKS</span></span>

[<span data-ttu-id="225bd-195">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="225bd-195">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


