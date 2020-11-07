---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: c0d3d6518025aab22add0859bde69cb1ad279138
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93913001"
---
# <span data-ttu-id="3f27b-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="3f27b-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="3f27b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3f27b-102">SYNOPSIS</span></span>
<span data-ttu-id="3f27b-103">Создает кластер HDInsight Azure в указанной группе ресурсов для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="3f27b-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="3f27b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3f27b-104">SYNTAX</span></span>

### <span data-ttu-id="3f27b-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3f27b-105">Default (Default)</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [[-DefaultStorageAccountType] <StorageType>]
 [[-Config] <AzureHDInsightConfig>] [[-OozieMetastore] <AzureHDInsightMetastore>]
 [[-HiveMetastore] <AzureHDInsightMetastore>]
 [[-AdditionalStorageAccounts] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-Configurations] <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [[-ScriptActions] <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [[-DefaultStorageContainer] <String>] [[-DefaultStorageRootPath] <String>] [[-Version] <String>]
 [[-HeadNodeSize] <String>] [[-WorkerNodeSize] <String>] [[-EdgeNodeSize] <String>]
 [[-ZookeeperNodeSize] <String>] [[-ClusterType] <String>]
 [[-ComponentVersion] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-VirtualNetworkId] <String>] [[-SubnetName] <String>] [[-OSType] <OSType>] [[-ClusterTier] <Tier>]
 [[-SshCredential] <PSCredential>] [[-SshPublicKey] <String>] [[-RdpCredential] <PSCredential>]
 [[-RdpAccessExpiry] <DateTime>] [[-ObjectId] <Guid>] [[-ApplicationId] <Guid>]
 [[-CertificatePassword] <String>] [[-AadTenantId] <Guid>] [[-SecurityProfile] <AzureHDInsightSecurityProfile>]
 [[-DisksPerWorkerNode] <Int32>] [[-MinSupportedTlsVersion] <String>]
 [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f27b-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="3f27b-106">CertificateFilePath</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [[-DefaultStorageAccountType] <StorageType>]
 [[-Config] <AzureHDInsightConfig>] [[-OozieMetastore] <AzureHDInsightMetastore>]
 [[-HiveMetastore] <AzureHDInsightMetastore>]
 [[-AdditionalStorageAccounts] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-Configurations] <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [[-ScriptActions] <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [[-DefaultStorageContainer] <String>] [[-DefaultStorageRootPath] <String>] [[-Version] <String>]
 [[-HeadNodeSize] <String>] [[-WorkerNodeSize] <String>] [[-EdgeNodeSize] <String>]
 [[-ZookeeperNodeSize] <String>] [[-ClusterType] <String>]
 [[-ComponentVersion] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-VirtualNetworkId] <String>] [[-SubnetName] <String>] [[-OSType] <OSType>] [[-ClusterTier] <Tier>]
 [[-SshCredential] <PSCredential>] [[-SshPublicKey] <String>] [[-RdpCredential] <PSCredential>]
 [[-RdpAccessExpiry] <DateTime>] [[-ObjectId] <Guid>] [[-ApplicationId] <Guid>]
 [[-CertificateFilePath] <String>] [[-CertificatePassword] <String>] [[-AadTenantId] <Guid>]
 [[-SecurityProfile] <AzureHDInsightSecurityProfile>] [[-DisksPerWorkerNode] <Int32>]
 [[-MinSupportedTlsVersion] <String>] [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f27b-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="3f27b-107">CertificateFileContents</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [[-DefaultStorageAccountType] <StorageType>]
 [[-Config] <AzureHDInsightConfig>] [[-OozieMetastore] <AzureHDInsightMetastore>]
 [[-HiveMetastore] <AzureHDInsightMetastore>]
 [[-AdditionalStorageAccounts] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-Configurations] <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [[-ScriptActions] <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [[-DefaultStorageContainer] <String>] [[-DefaultStorageRootPath] <String>] [[-Version] <String>]
 [[-HeadNodeSize] <String>] [[-WorkerNodeSize] <String>] [[-EdgeNodeSize] <String>]
 [[-ZookeeperNodeSize] <String>] [[-ClusterType] <String>]
 [[-ComponentVersion] <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [[-VirtualNetworkId] <String>] [[-SubnetName] <String>] [[-OSType] <OSType>] [[-ClusterTier] <Tier>]
 [[-SshCredential] <PSCredential>] [[-SshPublicKey] <String>] [[-RdpCredential] <PSCredential>]
 [[-RdpAccessExpiry] <DateTime>] [[-ObjectId] <Guid>] [[-ApplicationId] <Guid>]
 [[-CertificateFileContents] <Byte[]>] [[-CertificatePassword] <String>] [[-AadTenantId] <Guid>]
 [[-SecurityProfile] <AzureHDInsightSecurityProfile>] [[-DisksPerWorkerNode] <Int32>]
 [[-MinSupportedTlsVersion] <String>] [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f27b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f27b-108">DESCRIPTION</span></span>
<span data-ttu-id="3f27b-109">New-AzHDInsightCluster создает кластер HDInsight Azure, используя указанные параметры или объект конфигурации, созданный с помощью командлета New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="3f27b-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="3f27b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3f27b-110">EXAMPLES</span></span>

### <span data-ttu-id="3f27b-111">Пример 1: Создание кластера HDInsight Azure</span><span class="sxs-lookup"><span data-stu-id="3f27b-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        #   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
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

<span data-ttu-id="3f27b-112">Эта команда создает кластер в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="3f27b-112">This command creates a cluster in the current subscription.</span></span>

## <span data-ttu-id="3f27b-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3f27b-113">PARAMETERS</span></span>

### <span data-ttu-id="3f27b-114">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="3f27b-114">-AadTenantId</span></span>
<span data-ttu-id="3f27b-115">Указывает идентификатор клиента Azure AD, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3f27b-115">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="3f27b-116">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="3f27b-116">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="3f27b-117">Указывает дополнительные учетные записи хранилища Azure для кластера.</span><span class="sxs-lookup"><span data-stu-id="3f27b-117">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="3f27b-118">Вы также можете использовать командлет Add-AzHDInsightStorage.</span><span class="sxs-lookup"><span data-stu-id="3f27b-118">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f27b-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3f27b-119">-ApplicationId</span></span>
<span data-ttu-id="3f27b-120">Возвращает или задает идентификатор приложения субъекта-службы для доступа к Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="3f27b-120">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="3f27b-121">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="3f27b-121">-CertificateFileContents</span></span>
<span data-ttu-id="3f27b-122">Указывает содержимое файла сертификата, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3f27b-122">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: CertificateFileContents
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f27b-123">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="3f27b-123">-CertificateFilePath</span></span>
<span data-ttu-id="3f27b-124">Задает путь к файлу сертификата, который будет использоваться для проверки подлинности участника-службы.</span><span class="sxs-lookup"><span data-stu-id="3f27b-124">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="3f27b-125">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3f27b-125">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: System.String
Parameter Sets: CertificateFilePath
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f27b-126">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="3f27b-126">-CertificatePassword</span></span>
<span data-ttu-id="3f27b-127">Указывает пароль сертификата, который будет использоваться для проверки подлинности в качестве субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="3f27b-127">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="3f27b-128">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3f27b-128">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="3f27b-129">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="3f27b-129">-ClusterName</span></span>
<span data-ttu-id="3f27b-130">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="3f27b-130">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f27b-131">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="3f27b-131">-ClusterSizeInNodes</span></span>
<span data-ttu-id="3f27b-132">Задает количество узлов рабочих процессов для кластера.</span><span class="sxs-lookup"><span data-stu-id="3f27b-132">Specifies the number of Worker nodes for the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f27b-133">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="3f27b-133">-ClusterTier</span></span>
<span data-ttu-id="3f27b-134">Указывает уровень кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3f27b-134">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="3f27b-135">По умолчанию это стандартный.</span><span class="sxs-lookup"><span data-stu-id="3f27b-135">By default, this is Standard.</span></span>
<span data-ttu-id="3f27b-136">Уровень Premium можно использовать только для кластеров Linux, а также для использования некоторых новых функций.</span><span class="sxs-lookup"><span data-stu-id="3f27b-136">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="3f27b-137">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="3f27b-137">-ClusterType</span></span>
<span data-ttu-id="3f27b-138">Указывает тип создаваемого кластера.</span><span class="sxs-lookup"><span data-stu-id="3f27b-138">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="3f27b-139">Доступны следующие варианты: Hadoop, HBase, INTERACTIVEHIVE, Kafka и RServer</span><span class="sxs-lookup"><span data-stu-id="3f27b-139">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

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

### <span data-ttu-id="3f27b-140">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="3f27b-140">-ComponentVersion</span></span>
```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f27b-141">-Config</span><span class="sxs-lookup"><span data-stu-id="3f27b-141">-Config</span></span>
<span data-ttu-id="3f27b-142">Указывает объект кластера, который будет использоваться для создания кластера.</span><span class="sxs-lookup"><span data-stu-id="3f27b-142">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="3f27b-143">Этот объект можно создать с помощью командлета New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="3f27b-143">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f27b-144">-Конфигурации</span><span class="sxs-lookup"><span data-stu-id="3f27b-144">-Configurations</span></span>
<span data-ttu-id="3f27b-145">Указывает конфигурации этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3f27b-145">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="3f27b-146">Вы также можете использовать командлет Add-AzHDInsightConfigValues.</span><span class="sxs-lookup"><span data-stu-id="3f27b-146">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f27b-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f27b-147">-DefaultProfile</span></span>
<span data-ttu-id="3f27b-148">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3f27b-148">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f27b-149">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="3f27b-149">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="3f27b-150">Указывает ключ учетной записи хранения Azure, используемой по умолчанию, которую будет использовать кластер HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3f27b-150">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="3f27b-151">Вы также можете использовать командлет Set-AzHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="3f27b-151">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f27b-152">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3f27b-152">-DefaultStorageAccountName</span></span>
<span data-ttu-id="3f27b-153">Указывает имя учетной записи хранения Azure, используемой по умолчанию, которое будет использоваться кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3f27b-153">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="3f27b-154">Вы также можете использовать командлет Set-AzHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="3f27b-154">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f27b-155">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="3f27b-155">-DefaultStorageAccountType</span></span>
<span data-ttu-id="3f27b-156">Указывает тип учетной записи хранения, используемой по умолчанию, которая будет использоваться кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3f27b-156">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="3f27b-157">Возможные значения: AzureStorage и AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="3f27b-157">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="3f27b-158">Если не указано, по умолчанию используется значение AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="3f27b-158">Defaults to AzureStorage if not specified.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: AzureStorage
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f27b-159">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3f27b-159">-DefaultStorageContainer</span></span>
<span data-ttu-id="3f27b-160">Указывает имя контейнера по умолчанию в учетной записи хранения Azure по умолчанию, который будет использоваться кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3f27b-160">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="3f27b-161">Вы также можете использовать командлет Set-AzHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="3f27b-161">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="3f27b-162">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="3f27b-162">-DefaultStorageRootPath</span></span>
<span data-ttu-id="3f27b-163">Указывает префикс пути в учетной записи Data Lake Store, который кластер HDInsight будет использовать в качестве файловой системы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3f27b-163">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

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

### <span data-ttu-id="3f27b-164">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="3f27b-164">-DisksPerWorkerNode</span></span>
<span data-ttu-id="3f27b-165">Задает количество дисков для роли узла рабочего процесса в кластере.</span><span class="sxs-lookup"><span data-stu-id="3f27b-165">Specifies the number of disks for worker node role in the cluster.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f27b-166">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="3f27b-166">-EdgeNodeSize</span></span>
<span data-ttu-id="3f27b-167">Указывает размер виртуальной машины для граничного узла.</span><span class="sxs-lookup"><span data-stu-id="3f27b-167">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="3f27b-168">Используйте Get-AzVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3f27b-168">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="3f27b-169">Этот параметр является допустимым только для кластеров RServer.</span><span class="sxs-lookup"><span data-stu-id="3f27b-169">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="3f27b-170">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="3f27b-170">-HeadNodeSize</span></span>
<span data-ttu-id="3f27b-171">Задает размер виртуальной машины для головного узла.</span><span class="sxs-lookup"><span data-stu-id="3f27b-171">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="3f27b-172">Используйте Get-AzVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3f27b-172">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="3f27b-173">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="3f27b-173">-HiveMetastore</span></span>
<span data-ttu-id="3f27b-174">Указывает базу данных SQL для хранения метаданных куста.</span><span class="sxs-lookup"><span data-stu-id="3f27b-174">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="3f27b-175">Вы также можете использовать командлет Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="3f27b-175">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="3f27b-176">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="3f27b-176">-HttpCredential</span></span>
<span data-ttu-id="3f27b-177">Задает учетные данные для входа в кластер (HTTP) для кластера.</span><span class="sxs-lookup"><span data-stu-id="3f27b-177">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f27b-178">-Location</span><span class="sxs-lookup"><span data-stu-id="3f27b-178">-Location</span></span>
<span data-ttu-id="3f27b-179">Задает расположение кластера.</span><span class="sxs-lookup"><span data-stu-id="3f27b-179">Specifies the location for the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f27b-180">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="3f27b-180">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="3f27b-181">Возвращает или задает минимальную поддерживаемую версию TLS.</span><span class="sxs-lookup"><span data-stu-id="3f27b-181">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="3f27b-182">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="3f27b-182">-ObjectId</span></span>
<span data-ttu-id="3f27b-183">Указывает идентификатор объекта Azure AD (GUID) субъекта-службы Azure AD, который представляет этот кластер.</span><span class="sxs-lookup"><span data-stu-id="3f27b-183">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="3f27b-184">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3f27b-184">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="3f27b-185">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="3f27b-185">-OozieMetastore</span></span>
<span data-ttu-id="3f27b-186">Определяет базу данных SQL для хранения метаданных Oozie.</span><span class="sxs-lookup"><span data-stu-id="3f27b-186">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="3f27b-187">Вы также можете использовать командлет Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="3f27b-187">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="3f27b-188">-OSType</span><span class="sxs-lookup"><span data-stu-id="3f27b-188">-OSType</span></span>
<span data-ttu-id="3f27b-189">Указывает операционную систему для кластера.</span><span class="sxs-lookup"><span data-stu-id="3f27b-189">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="3f27b-190">Возможные варианты: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="3f27b-190">Options are: Windows, Linux</span></span>

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.OSType
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f27b-191">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="3f27b-191">-RdpAccessExpiry</span></span>
<span data-ttu-id="3f27b-192">Задает срок действия в виде объекта DateTime для доступа к кластеру через протокол удаленного рабочего стола (RDP).</span><span class="sxs-lookup"><span data-stu-id="3f27b-192">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f27b-193">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="3f27b-193">-RdpCredential</span></span>
<span data-ttu-id="3f27b-194">Указывает учетные данные удаленного рабочего стола (RDP) для кластера.</span><span class="sxs-lookup"><span data-stu-id="3f27b-194">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="3f27b-195">Это относится только к кластерам Windows.</span><span class="sxs-lookup"><span data-stu-id="3f27b-195">This is only for Windows clusters.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f27b-196">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f27b-196">-ResourceGroupName</span></span>
<span data-ttu-id="3f27b-197">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3f27b-197">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f27b-198">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="3f27b-198">-ScriptActions</span></span>
<span data-ttu-id="3f27b-199">Задает действия сценария, которые должны выполняться в кластере по завершении создания кластера.</span><span class="sxs-lookup"><span data-stu-id="3f27b-199">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="3f27b-200">Вы также можете использовать Add-AzHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="3f27b-200">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]
Parameter Sets: (All)
Aliases:
Accepted values: HeadNode, WorkerNode, ZookeeperNode, EdgeNode

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f27b-201">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="3f27b-201">-SecurityProfile</span></span>
<span data-ttu-id="3f27b-202">Задает свойства, связанные с безопасностью, которые используются для создания надежного кластера.</span><span class="sxs-lookup"><span data-stu-id="3f27b-202">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="3f27b-203">Вы также можете использовать командлет Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="3f27b-203">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSecurityProfile
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f27b-204">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="3f27b-204">-SshCredential</span></span>
<span data-ttu-id="3f27b-205">Указывает учетные данные SSH, которые будут использоваться для подключений по протоколу SSH.</span><span class="sxs-lookup"><span data-stu-id="3f27b-205">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="3f27b-206">Это относится только к кластерам Linux.</span><span class="sxs-lookup"><span data-stu-id="3f27b-206">This is only for Linux clusters.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f27b-207">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="3f27b-207">-SshPublicKey</span></span>
<span data-ttu-id="3f27b-208">Указывает открытый ключ, который будет использоваться для подключений по протоколу SSH.</span><span class="sxs-lookup"><span data-stu-id="3f27b-208">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="3f27b-209">Это относится только к кластерам Linux.</span><span class="sxs-lookup"><span data-stu-id="3f27b-209">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="3f27b-210">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="3f27b-210">-SubnetName</span></span>
<span data-ttu-id="3f27b-211">Указывает имя подсети в выбранной виртуальной сети для кластера.</span><span class="sxs-lookup"><span data-stu-id="3f27b-211">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

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

### <span data-ttu-id="3f27b-212">-Version</span><span class="sxs-lookup"><span data-stu-id="3f27b-212">-Version</span></span>
<span data-ttu-id="3f27b-213">Указывает версию HDI кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3f27b-213">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="3f27b-214">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="3f27b-214">-VirtualNetworkId</span></span>
<span data-ttu-id="3f27b-215">Указывает ИД виртуальной сети, в которую подготавливается кластер.</span><span class="sxs-lookup"><span data-stu-id="3f27b-215">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="3f27b-216">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="3f27b-216">-WorkerNodeSize</span></span>
<span data-ttu-id="3f27b-217">Указывает размер виртуальной машины для рабочего узла.</span><span class="sxs-lookup"><span data-stu-id="3f27b-217">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="3f27b-218">Используйте Get-AzVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3f27b-218">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="3f27b-219">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="3f27b-219">-ZookeeperNodeSize</span></span>
<span data-ttu-id="3f27b-220">Указывает размер виртуальной машины для узла Джесс.</span><span class="sxs-lookup"><span data-stu-id="3f27b-220">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="3f27b-221">Используйте Get-AzVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="3f27b-221">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="3f27b-222">Этот параметр является допустимым только для кластеров HBase и.</span><span class="sxs-lookup"><span data-stu-id="3f27b-222">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="3f27b-223">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f27b-223">CommonParameters</span></span>
<span data-ttu-id="3f27b-224">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3f27b-224">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f27b-225">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f27b-225">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f27b-226">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3f27b-226">INPUTS</span></span>

### <span data-ttu-id="3f27b-227">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="3f27b-227">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="3f27b-228">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f27b-228">OUTPUTS</span></span>

### <span data-ttu-id="3f27b-229">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="3f27b-229">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="3f27b-230">Пуск</span><span class="sxs-lookup"><span data-stu-id="3f27b-230">NOTES</span></span>
<span data-ttu-id="3f27b-231">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, Hadoop, hdinsight, HD и Insights</span><span class="sxs-lookup"><span data-stu-id="3f27b-231">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="3f27b-232">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f27b-232">RELATED LINKS</span></span>

[<span data-ttu-id="3f27b-233">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="3f27b-233">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

