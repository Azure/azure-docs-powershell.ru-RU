---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 38dc23c2bebe3c608833e55bcb4ffb2d687f9041
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912999"
---
# <span data-ttu-id="a05a6-101">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="a05a6-101">New-AzHDInsightClusterConfig</span></span>

## <span data-ttu-id="a05a6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a05a6-102">SYNOPSIS</span></span>
<span data-ttu-id="a05a6-103">Создает несохраняемый объект конфигурации кластера, описывающий конфигурацию кластера Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="a05a6-103">Creates a non-persisted cluster configuration object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="a05a6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a05a6-104">SYNTAX</span></span>

```
New-AzHDInsightClusterConfig [[-DefaultStorageAccountName] <String>] [[-DefaultStorageAccountKey] <String>]
 [[-DefaultStorageAccountType] <StorageType>] [[-OozieMetastore] <AzureHDInsightMetastore>]
 [[-HiveMetastore] <AzureHDInsightMetastore>] [[-HeadNodeSize] <String>] [[-WorkerNodeSize] <String>]
 [[-EdgeNodeSize] <String>] [[-ZookeeperNodeSize] <String>] [[-ClusterType] <String>] [[-ClusterTier] <Tier>]
 [[-ObjectId] <Guid>] [[-ApplicationId] <Guid>] [[-CertificateFileContents] <Byte[]>]
 [[-CertificateFilePath] <String>] [[-CertificatePassword] <String>] [[-AadTenantId] <Guid>]
 [[-MinSupportedTlsVersion] <String>] [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a05a6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a05a6-105">DESCRIPTION</span></span>
<span data-ttu-id="a05a6-106">Командлет **New-AzHDInsightClusterConfig** создает несохраняемый объект, который описывает конфигурацию кластера Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="a05a6-106">The **New-AzHDInsightClusterConfig** cmdlet creates a non-persisted object that describes an Azure HDInsight cluster configuration.</span></span>

## <span data-ttu-id="a05a6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a05a6-107">EXAMPLES</span></span>

### <span data-ttu-id="a05a6-108">Пример 1: создание объекта конфигурации кластера</span><span class="sxs-lookup"><span data-stu-id="a05a6-108">Example 1: Create a cluster configuration object</span></span>
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

<span data-ttu-id="a05a6-109">Эта команда создает объект конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="a05a6-109">This command creates a cluster configuration object.</span></span>

## <span data-ttu-id="a05a6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a05a6-110">PARAMETERS</span></span>

### <span data-ttu-id="a05a6-111">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="a05a6-111">-AadTenantId</span></span>
<span data-ttu-id="a05a6-112">Указывает идентификатор клиента Azure AD, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a05a6-112">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="a05a6-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a05a6-113">-ApplicationId</span></span>
<span data-ttu-id="a05a6-114">Возвращает или задает идентификатор приложения субъекта-службы для доступа к Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="a05a6-114">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="a05a6-115">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="a05a6-115">-CertificateFileContents</span></span>
<span data-ttu-id="a05a6-116">Указывает содержимое файла сертификата, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a05a6-116">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="a05a6-117">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="a05a6-117">-CertificateFilePath</span></span>
<span data-ttu-id="a05a6-118">Задает путь к файлу сертификата, который будет использоваться для проверки подлинности участника-службы.</span><span class="sxs-lookup"><span data-stu-id="a05a6-118">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="a05a6-119">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a05a6-119">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="a05a6-120">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="a05a6-120">-CertificatePassword</span></span>
<span data-ttu-id="a05a6-121">Указывает пароль сертификата, который будет использоваться для проверки подлинности в качестве субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="a05a6-121">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="a05a6-122">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a05a6-122">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="a05a6-123">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="a05a6-123">-ClusterTier</span></span>
<span data-ttu-id="a05a6-124">Указывает уровень кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="a05a6-124">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="a05a6-125">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a05a6-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a05a6-126">Стандартная</span><span class="sxs-lookup"><span data-stu-id="a05a6-126">Standard</span></span>
- <span data-ttu-id="a05a6-127">Premium по умолчанию используется значение Standard.</span><span class="sxs-lookup"><span data-stu-id="a05a6-127">Premium The default value is Standard.</span></span>
<span data-ttu-id="a05a6-128">Уровень Premium можно использовать только для кластеров Linux, а также для использования некоторых новых функций.</span><span class="sxs-lookup"><span data-stu-id="a05a6-128">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="a05a6-129">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="a05a6-129">-ClusterType</span></span>
<span data-ttu-id="a05a6-130">Указывает тип создаваемого кластера.</span><span class="sxs-lookup"><span data-stu-id="a05a6-130">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="a05a6-131">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a05a6-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a05a6-132">Hadoop</span><span class="sxs-lookup"><span data-stu-id="a05a6-132">Hadoop</span></span>
- <span data-ttu-id="a05a6-133">HBase</span><span class="sxs-lookup"><span data-stu-id="a05a6-133">HBase</span></span>
- <span data-ttu-id="a05a6-134">Огонь</span><span class="sxs-lookup"><span data-stu-id="a05a6-134">Storm</span></span>
- <span data-ttu-id="a05a6-135">Spark</span><span class="sxs-lookup"><span data-stu-id="a05a6-135">Spark</span></span>
- <span data-ttu-id="a05a6-136">INTERACTIVEHIVE</span><span class="sxs-lookup"><span data-stu-id="a05a6-136">INTERACTIVEHIVE</span></span>
- <span data-ttu-id="a05a6-137">Kafka</span><span class="sxs-lookup"><span data-stu-id="a05a6-137">Kafka</span></span>
- <span data-ttu-id="a05a6-138">RServer</span><span class="sxs-lookup"><span data-stu-id="a05a6-138">RServer</span></span>

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

### <span data-ttu-id="a05a6-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a05a6-139">-DefaultProfile</span></span>
<span data-ttu-id="a05a6-140">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a05a6-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a05a6-141">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a05a6-141">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="a05a6-142">Указывает ключ учетной записи хранения Azure, используемой по умолчанию, которую будет использовать кластер HDInsight.</span><span class="sxs-lookup"><span data-stu-id="a05a6-142">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="a05a6-143">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a05a6-143">-DefaultStorageAccountName</span></span>
<span data-ttu-id="a05a6-144">Указывает имя учетной записи хранения, используемой по умолчанию, которое будет использоваться кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="a05a6-144">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="a05a6-145">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="a05a6-145">-DefaultStorageAccountType</span></span>
<span data-ttu-id="a05a6-146">Указывает тип учетной записи хранения, используемой по умолчанию, которая будет использоваться кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="a05a6-146">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="a05a6-147">Возможные значения: AzureStorage и AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="a05a6-147">Possible values are AzureStorage and AzureDataLakeStore.</span></span>

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

### <span data-ttu-id="a05a6-148">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="a05a6-148">-EdgeNodeSize</span></span>
<span data-ttu-id="a05a6-149">Указывает размер виртуальной машины для граничного узла.</span><span class="sxs-lookup"><span data-stu-id="a05a6-149">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="a05a6-150">Используйте Get-AzVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="a05a6-150">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="a05a6-151">Этот параметр является допустимым только для кластеров RServer.</span><span class="sxs-lookup"><span data-stu-id="a05a6-151">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="a05a6-152">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="a05a6-152">-HeadNodeSize</span></span>
<span data-ttu-id="a05a6-153">Задает размер виртуальной машины для головного узла.</span><span class="sxs-lookup"><span data-stu-id="a05a6-153">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="a05a6-154">Используйте Get-AzVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="a05a6-154">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="a05a6-155">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="a05a6-155">-HiveMetastore</span></span>
<span data-ttu-id="a05a6-156">Указывает MetaStore для хранения метаданных куста.</span><span class="sxs-lookup"><span data-stu-id="a05a6-156">Specifies the metastore to store Hive metadata.</span></span>
<span data-ttu-id="a05a6-157">Вы также можете использовать командлет Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="a05a6-157">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="a05a6-158">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="a05a6-158">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="a05a6-159">Возвращает или задает минимальную поддерживаемую версию TLS.</span><span class="sxs-lookup"><span data-stu-id="a05a6-159">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="a05a6-160">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a05a6-160">-ObjectId</span></span>
<span data-ttu-id="a05a6-161">Указывает идентификатор объекта Azure AD (GUID) субъекта-службы Azure AD, который представляет этот кластер.</span><span class="sxs-lookup"><span data-stu-id="a05a6-161">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="a05a6-162">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a05a6-162">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="a05a6-163">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="a05a6-163">-OozieMetastore</span></span>
<span data-ttu-id="a05a6-164">Указывает MetaStore для хранения метаданных Oozie.</span><span class="sxs-lookup"><span data-stu-id="a05a6-164">Specifies the metastore to store Oozie metadata.</span></span>
<span data-ttu-id="a05a6-165">Вы также можете использовать командлет **Add-AzHDInsightMetastore** .</span><span class="sxs-lookup"><span data-stu-id="a05a6-165">You can alternatively use the **Add-AzHDInsightMetastore** cmdlet.</span></span>

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

### <span data-ttu-id="a05a6-166">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="a05a6-166">-WorkerNodeSize</span></span>
<span data-ttu-id="a05a6-167">Указывает размер виртуальной машины для рабочего узла.</span><span class="sxs-lookup"><span data-stu-id="a05a6-167">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="a05a6-168">Используйте Get-AzVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="a05a6-168">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="a05a6-169">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="a05a6-169">-ZookeeperNodeSize</span></span>
<span data-ttu-id="a05a6-170">Указывает размер виртуальной машины для узла Джесс.</span><span class="sxs-lookup"><span data-stu-id="a05a6-170">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="a05a6-171">Используйте Get-AzVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="a05a6-171">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="a05a6-172">Этот параметр является допустимым только для кластеров HBase и.</span><span class="sxs-lookup"><span data-stu-id="a05a6-172">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="a05a6-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a05a6-173">CommonParameters</span></span>
<span data-ttu-id="a05a6-174">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a05a6-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a05a6-175">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a05a6-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a05a6-176">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a05a6-176">INPUTS</span></span>

### <span data-ttu-id="a05a6-177">Ничего</span><span class="sxs-lookup"><span data-stu-id="a05a6-177">None</span></span>

## <span data-ttu-id="a05a6-178">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a05a6-178">OUTPUTS</span></span>

### <span data-ttu-id="a05a6-179">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="a05a6-179">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="a05a6-180">Пуск</span><span class="sxs-lookup"><span data-stu-id="a05a6-180">NOTES</span></span>

## <span data-ttu-id="a05a6-181">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a05a6-181">RELATED LINKS</span></span>

[<span data-ttu-id="a05a6-182">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="a05a6-182">Add-AzHDInsightStorage</span></span>](./Add-AzHDInsightStorage.md)


