---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 66857c9d12bb23ffdccb893b8fae8bfc7c6e0f4f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079075"
---
# <span data-ttu-id="ed9fb-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="ed9fb-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="ed9fb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ed9fb-102">SYNOPSIS</span></span>
<span data-ttu-id="ed9fb-103">Создает несохраняемый объект конфигурации кластера, описывающий конфигурацию кластера Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="ed9fb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ed9fb-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-MinSupportedTlsVersion <String>]
 [-AssignedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-PublicNetworkAccessType <String>]
 [-OutboundPublicNetworkAccessType <String>] [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed9fb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed9fb-105">DESCRIPTION</span></span>
<span data-ttu-id="ed9fb-106">Командлет **New-AzHDInsightClusterConfig** создает несохраняемый объект, который описывает конфигурацию кластера Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="ed9fb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ed9fb-107">EXAMPLES</span></span>

### <span data-ttu-id="ed9fb-108">Пример 1: создание объекта конфигурации кластера</span><span class="sxs-lookup"><span data-stu-id="ed9fb-108">Example 1: Create a cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
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
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="ed9fb-109">Эта команда создает объект конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="ed9fb-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ed9fb-110">PARAMETERS</span></span>

### <span data-ttu-id="ed9fb-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="ed9fb-111">-AadTenantId</span></span>
<span data-ttu-id="ed9fb-112">Указывает идентификатор клиента Azure AD, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="ed9fb-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ed9fb-113">-ApplicationId</span></span>
<span data-ttu-id="ed9fb-114">Возвращает или задает идентификатор приложения субъекта-службы для доступа к Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="ed9fb-115">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ed9fb-115">-AssignedIdentity</span></span>
<span data-ttu-id="ed9fb-116">Возвращает или задает назначенное удостоверение.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-116">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="ed9fb-117">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="ed9fb-117">-CertificateFileContents</span></span>
<span data-ttu-id="ed9fb-118">Указывает содержимое файла сертификата, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-118">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="ed9fb-119">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="ed9fb-119">-CertificateFilePath</span></span>
<span data-ttu-id="ed9fb-120">Задает путь к файлу сертификата, который будет использоваться для проверки подлинности участника-службы.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-120">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="ed9fb-121">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-121">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="ed9fb-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="ed9fb-122">-CertificatePassword</span></span>
<span data-ttu-id="ed9fb-123">Указывает пароль сертификата, который будет использоваться для проверки подлинности в качестве субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-123">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="ed9fb-124">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-124">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="ed9fb-125">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="ed9fb-125">-ClusterTier</span></span>
<span data-ttu-id="ed9fb-126">Указывает уровень кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-126">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="ed9fb-127">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ed9fb-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ed9fb-128">Стандартная</span><span class="sxs-lookup"><span data-stu-id="ed9fb-128">Standard</span></span>
- <span data-ttu-id="ed9fb-129">Premium по умолчанию используется значение Standard.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-129">Premium The default value is Standard.</span></span>
<span data-ttu-id="ed9fb-130">Уровень Premium можно использовать только для кластеров Linux, а также для использования некоторых новых функций.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-130">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="ed9fb-131">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="ed9fb-131">-ClusterType</span></span>
<span data-ttu-id="ed9fb-132">Указывает тип создаваемого кластера.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-132">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="ed9fb-133">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="ed9fb-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ed9fb-134">Hadoop</span><span class="sxs-lookup"><span data-stu-id="ed9fb-134">Hadoop</span></span>
- <span data-ttu-id="ed9fb-135">HBase</span><span class="sxs-lookup"><span data-stu-id="ed9fb-135">HBase</span></span>
- <span data-ttu-id="ed9fb-136">Огонь</span><span class="sxs-lookup"><span data-stu-id="ed9fb-136">Storm</span></span>
- <span data-ttu-id="ed9fb-137">Spark</span><span class="sxs-lookup"><span data-stu-id="ed9fb-137">Spark</span></span>
- <span data-ttu-id="ed9fb-138">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="ed9fb-138">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="ed9fb-139">Kafka</span><span class="sxs-lookup"><span data-stu-id="ed9fb-139">Kafka</span></span>
- <span data-ttu-id="ed9fb-140">RServer</span><span class="sxs-lookup"><span data-stu-id="ed9fb-140">RServer</span></span>

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

### <span data-ttu-id="ed9fb-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed9fb-141">-DefaultProfile</span></span>
<span data-ttu-id="ed9fb-142">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ed9fb-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed9fb-143">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ed9fb-143">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="ed9fb-144">Указывает ключ учетной записи хранения Azure, используемой по умолчанию, которую будет использовать кластер HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-144">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="ed9fb-145">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ed9fb-145">-DefaultStorageAccountName</span></span>
<span data-ttu-id="ed9fb-146">Указывает имя учетной записи хранения, используемой по умолчанию, которое будет использоваться кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-146">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="ed9fb-147">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="ed9fb-147">-DefaultStorageAccountType</span></span>
<span data-ttu-id="ed9fb-148">Указывает тип учетной записи хранения, используемой по умолчанию, которая будет использоваться кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-148">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="ed9fb-149">Возможные значения: AzureStorage и AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-149">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: AzureStorage
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9fb-150">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="ed9fb-150">-EdgeNodeSize</span></span>
<span data-ttu-id="ed9fb-151">Указывает размер виртуальной машины для граничного узла.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-151">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="ed9fb-152">Используйте Get-AzVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-152">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="ed9fb-153">Этот параметр является допустимым только для кластеров RServer.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-153">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="ed9fb-154">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="ed9fb-154">-EncryptionAlgorithm</span></span>
<span data-ttu-id="ed9fb-155">Возвращает или задает алгоритм шифрования.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-155">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="ed9fb-156">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="ed9fb-156">-EncryptionAtHost</span></span>
<span data-ttu-id="ed9fb-157">Возвращает или задает флаг, указывающий, следует ли включить шифрование на хосте или нет.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-157">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="ed9fb-158">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="ed9fb-158">-EncryptionInTransit</span></span>
<span data-ttu-id="ed9fb-159">Возвращает или задает флаг, указывающий, следует ли включить шифрование в пути или нет.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-159">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="ed9fb-160">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="ed9fb-160">-EncryptionKeyName</span></span>
<span data-ttu-id="ed9fb-161">Возвращает или задает имя ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-161">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="ed9fb-162">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="ed9fb-162">-EncryptionKeyVersion</span></span>
<span data-ttu-id="ed9fb-163">Возвращает или задает версию ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-163">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="ed9fb-164">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="ed9fb-164">-EncryptionVaultUri</span></span>
<span data-ttu-id="ed9fb-165">Возвращает или задает универсальный код ресурса (URI) для хранилища шифрования.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-165">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="ed9fb-166">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="ed9fb-166">-HeadNodeSize</span></span>
<span data-ttu-id="ed9fb-167">Задает размер виртуальной машины для головного узла.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-167">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="ed9fb-168">Используйте Get-AzVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-168">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="ed9fb-169">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="ed9fb-169">-HiveMetastore</span></span>
<span data-ttu-id="ed9fb-170">Указывает MetaStore для хранения метаданных куста.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-170">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="ed9fb-171">Вы также можете использовать командлет Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-171">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="ed9fb-172">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="ed9fb-172">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="ed9fb-173">Возвращает или задает минимальную поддерживаемую версию TLS.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-173">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="ed9fb-174">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ed9fb-174">-ObjectId</span></span>
<span data-ttu-id="ed9fb-175">Указывает идентификатор объекта Azure AD (GUID) субъекта-службы Azure AD, который представляет этот кластер.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-175">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="ed9fb-176">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-176">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="ed9fb-177">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="ed9fb-177">-OozieMetastore</span></span>
<span data-ttu-id="ed9fb-178">Указывает MetaStore для хранения метаданных Oozie.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-178">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="ed9fb-179">Вы также можете использовать командлет **Add-AzHDInsightMetastore** .</span><span class="sxs-lookup"><span data-stu-id="ed9fb-179">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="ed9fb-180">-OutboundPublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="ed9fb-180">-OutboundPublicNetworkAccessType</span></span>
<span data-ttu-id="ed9fb-181">Возвращает или задает тип исходящего доступа к общедоступной сети.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-181">Gets or sets the outbound access type to the public network.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PublicLoadBalancer, UDR

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9fb-182">-PublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="ed9fb-182">-PublicNetworkAccessType</span></span>
<span data-ttu-id="ed9fb-183">Возвращает или задает тип доступа к общедоступной сети.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-183">Gets or sets the public network access type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: InboundAndOutbound, OutboundOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed9fb-184">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="ed9fb-184">-WorkerNodeSize</span></span>
<span data-ttu-id="ed9fb-185">Указывает размер виртуальной машины для рабочего узла.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-185">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="ed9fb-186">Используйте Get-AzVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-186">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="ed9fb-187">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="ed9fb-187">-ZookeeperNodeSize</span></span>
<span data-ttu-id="ed9fb-188">Указывает размер виртуальной машины для узла Джесс.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-188">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="ed9fb-189">Используйте Get-AzVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-189">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="ed9fb-190">Этот параметр является допустимым только для кластеров HBase и.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-190">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="ed9fb-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed9fb-191">CommonParameters</span></span>
<span data-ttu-id="ed9fb-192">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ed9fb-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed9fb-193">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed9fb-193">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed9fb-194">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ed9fb-194">INPUTS</span></span>

### <span data-ttu-id="ed9fb-195">Ничего</span><span class="sxs-lookup"><span data-stu-id="ed9fb-195">None</span></span>

## <span data-ttu-id="ed9fb-196">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed9fb-196">OUTPUTS</span></span>

### <span data-ttu-id="ed9fb-197">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="ed9fb-197">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="ed9fb-198">Пуск</span><span class="sxs-lookup"><span data-stu-id="ed9fb-198">NOTES</span></span>

## <span data-ttu-id="ed9fb-199">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed9fb-199">RELATED LINKS</span></span>

[<span data-ttu-id="ed9fb-200">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="ed9fb-200">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


