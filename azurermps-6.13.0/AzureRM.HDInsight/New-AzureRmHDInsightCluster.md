---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
ms.openlocfilehash: b10fe80fb0a58267212912f554d044b2715fd1d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93564472"
---
# <span data-ttu-id="ea6c0-101">New-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ea6c0-101">New-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="ea6c0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ea6c0-102">SYNOPSIS</span></span>
<span data-ttu-id="ea6c0-103">Создает кластер HDInsight Azure в указанной группе ресурсов для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea6c0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ea6c0-104">SYNTAX</span></span>

### <span data-ttu-id="ea6c0-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ea6c0-105">Default (Default)</span></span>
```
New-AzureRmHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificatePassword <String>] [-AadTenantId <Guid>]
 [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DisksPerWorkerNode <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea6c0-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="ea6c0-106">CertificateFilePath</span></span>
```
New-AzureRmHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ea6c0-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="ea6c0-107">CertificateFileContents</span></span>
```
New-AzureRmHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-DefaultStorageAccountName] <String>]
 [[-DefaultStorageAccountKey] <String>] [-DefaultStorageAccountType <StorageType>]
 [-Config <AzureHDInsightConfig>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-DefaultStorageContainer <String>] [-DefaultStorageRootPath <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>]
 [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-CertificateFileContents <Byte[]>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea6c0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea6c0-108">DESCRIPTION</span></span>
<span data-ttu-id="ea6c0-109">New-AzureHDInsightCluster создает кластер HDInsight Azure, используя указанные параметры или объект конфигурации, созданный с помощью командлета New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-109">The New-AzureHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="ea6c0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ea6c0-110">EXAMPLES</span></span>

### <span data-ttu-id="ea6c0-111">Пример 1: Создание кластера HDInsight Azure</span><span class="sxs-lookup"><span data-stu-id="ea6c0-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzureStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | %{ $_.Key1 }
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        #   New-AzureRMResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzureRmHDInsightCluster `
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

<span data-ttu-id="ea6c0-112">Эта команда создает кластер в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-112">This command creates a cluster in the current subscription.</span></span>

## <span data-ttu-id="ea6c0-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ea6c0-113">PARAMETERS</span></span>

### <span data-ttu-id="ea6c0-114">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="ea6c0-114">-AadTenantId</span></span>
<span data-ttu-id="ea6c0-115">Указывает идентификатор клиента Azure AD, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-115">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="ea6c0-116">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="ea6c0-116">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="ea6c0-117">Указывает дополнительные учетные записи хранилища Azure для кластера.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-117">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="ea6c0-118">Вы также можете использовать командлет Add-AzureRmHDInsightStorage.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-118">You can alternatively use the Add-AzureRmHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="ea6c0-119">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="ea6c0-119">-CertificateFileContents</span></span>
<span data-ttu-id="ea6c0-120">Указывает содержимое файла сертификата, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-120">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="ea6c0-121">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="ea6c0-121">-CertificateFilePath</span></span>
<span data-ttu-id="ea6c0-122">Задает путь к файлу сертификата, который будет использоваться для проверки подлинности участника-службы.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-122">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="ea6c0-123">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-123">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="ea6c0-124">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="ea6c0-124">-CertificatePassword</span></span>
<span data-ttu-id="ea6c0-125">Указывает пароль сертификата, который будет использоваться для проверки подлинности в качестве субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-125">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="ea6c0-126">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-126">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="ea6c0-127">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="ea6c0-127">-ClusterName</span></span>
<span data-ttu-id="ea6c0-128">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-128">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="ea6c0-129">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="ea6c0-129">-ClusterSizeInNodes</span></span>
<span data-ttu-id="ea6c0-130">Задает количество узлов рабочих процессов для кластера.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-130">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="ea6c0-131">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="ea6c0-131">-ClusterTier</span></span>
<span data-ttu-id="ea6c0-132">Указывает уровень кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-132">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="ea6c0-133">По умолчанию это стандартный.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-133">By default, this is Standard.</span></span>
<span data-ttu-id="ea6c0-134">Уровень Premium можно использовать только для кластеров Linux, а также для использования некоторых новых функций.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-134">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="ea6c0-135">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="ea6c0-135">-ClusterType</span></span>
<span data-ttu-id="ea6c0-136">Указывает тип создаваемого кластера.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-136">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="ea6c0-137">Возможные варианты: Hadoop, HBase, г., Spark</span><span class="sxs-lookup"><span data-stu-id="ea6c0-137">Options are: Hadoop, HBase, Storm, Spark</span></span>

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

### <span data-ttu-id="ea6c0-138">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="ea6c0-138">-ComponentVersion</span></span>
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

### <span data-ttu-id="ea6c0-139">-Config</span><span class="sxs-lookup"><span data-stu-id="ea6c0-139">-Config</span></span>
<span data-ttu-id="ea6c0-140">Указывает объект кластера, который будет использоваться для создания кластера.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-140">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="ea6c0-141">Этот объект можно создать с помощью командлета New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-141">This object can be created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="ea6c0-142">-Конфигурации</span><span class="sxs-lookup"><span data-stu-id="ea6c0-142">-Configurations</span></span>
<span data-ttu-id="ea6c0-143">Указывает конфигурации этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-143">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="ea6c0-144">Вы также можете использовать командлет Add-AzureRmHDInsightConfigValues.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-144">You can alternatively use the Add-AzureRmHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="ea6c0-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea6c0-145">-DefaultProfile</span></span>
<span data-ttu-id="ea6c0-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ea6c0-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea6c0-147">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ea6c0-147">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="ea6c0-148">Указывает ключ учетной записи хранения Azure, используемой по умолчанию, которую будет использовать кластер HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-148">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="ea6c0-149">Вы также можете использовать командлет Set-AzureRmHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-149">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="ea6c0-150">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ea6c0-150">-DefaultStorageAccountName</span></span>
<span data-ttu-id="ea6c0-151">Указывает имя учетной записи хранения Azure, используемой по умолчанию, которое будет использоваться кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-151">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="ea6c0-152">Вы также можете использовать командлет Set-AzureRmHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-152">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="ea6c0-153">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="ea6c0-153">-DefaultStorageAccountType</span></span>
<span data-ttu-id="ea6c0-154">Указывает тип учетной записи хранения, используемой по умолчанию, которая будет использоваться кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-154">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="ea6c0-155">Возможные значения: AzureStorage и AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-155">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="ea6c0-156">Если не указано, по умолчанию используется значение AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-156">Defaults to AzureStorage if not specified.</span></span>

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

### <span data-ttu-id="ea6c0-157">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="ea6c0-157">-DefaultStorageContainer</span></span>
<span data-ttu-id="ea6c0-158">Указывает имя контейнера по умолчанию в учетной записи хранения Azure по умолчанию, который будет использоваться кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-158">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="ea6c0-159">Вы также можете использовать командлет Set-AzureRmHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-159">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="ea6c0-160">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="ea6c0-160">-DefaultStorageRootPath</span></span>
<span data-ttu-id="ea6c0-161">Указывает префикс пути в учетной записи Data Lake Store, который кластер HDInsight будет использовать в качестве файловой системы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-161">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

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

### <span data-ttu-id="ea6c0-162">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="ea6c0-162">-DisksPerWorkerNode</span></span>
<span data-ttu-id="ea6c0-163">Задает количество дисков для роли узла рабочего процесса в кластере.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-163">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="ea6c0-164">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="ea6c0-164">-EdgeNodeSize</span></span>
<span data-ttu-id="ea6c0-165">Указывает размер виртуальной машины для граничного узла.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-165">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="ea6c0-166">Используйте Get-AzureRmVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-166">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="ea6c0-167">Этот параметр является допустимым только для кластеров RServer.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-167">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="ea6c0-168">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="ea6c0-168">-HeadNodeSize</span></span>
<span data-ttu-id="ea6c0-169">Задает размер виртуальной машины для головного узла.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-169">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="ea6c0-170">Используйте Get-AzureRmVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-170">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="ea6c0-171">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="ea6c0-171">-HiveMetastore</span></span>
<span data-ttu-id="ea6c0-172">Указывает базу данных SQL для хранения метаданных куста.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-172">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="ea6c0-173">Вы также можете использовать командлет Add-AzureRmHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-173">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="ea6c0-174">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="ea6c0-174">-HttpCredential</span></span>
<span data-ttu-id="ea6c0-175">Задает учетные данные для входа в кластер (HTTP) для кластера.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-175">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="ea6c0-176">-Location</span><span class="sxs-lookup"><span data-stu-id="ea6c0-176">-Location</span></span>
<span data-ttu-id="ea6c0-177">Задает расположение кластера.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-177">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="ea6c0-178">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ea6c0-178">-ObjectId</span></span>
<span data-ttu-id="ea6c0-179">Указывает идентификатор объекта Azure AD (GUID) субъекта-службы Azure AD, который представляет этот кластер.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-179">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="ea6c0-180">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-180">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="ea6c0-181">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="ea6c0-181">-OozieMetastore</span></span>
<span data-ttu-id="ea6c0-182">Определяет базу данных SQL для хранения метаданных Oozie.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-182">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="ea6c0-183">Вы также можете использовать командлет Add-AzureRmHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-183">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="ea6c0-184">-OSType</span><span class="sxs-lookup"><span data-stu-id="ea6c0-184">-OSType</span></span>
<span data-ttu-id="ea6c0-185">Указывает операционную систему для кластера.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-185">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="ea6c0-186">Возможные варианты: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="ea6c0-186">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="ea6c0-187">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="ea6c0-187">-RdpAccessExpiry</span></span>
<span data-ttu-id="ea6c0-188">Задает срок действия в виде объекта DateTime для доступа к кластеру через протокол удаленного рабочего стола (RDP).</span><span class="sxs-lookup"><span data-stu-id="ea6c0-188">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="ea6c0-189">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="ea6c0-189">-RdpCredential</span></span>
<span data-ttu-id="ea6c0-190">Указывает учетные данные удаленного рабочего стола (RDP) для кластера.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-190">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="ea6c0-191">Это относится только к кластерам Windows.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-191">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="ea6c0-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea6c0-192">-ResourceGroupName</span></span>
<span data-ttu-id="ea6c0-193">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-193">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="ea6c0-194">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="ea6c0-194">-ScriptActions</span></span>
<span data-ttu-id="ea6c0-195">Задает действия сценария, которые должны выполняться в кластере по завершении создания кластера.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-195">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="ea6c0-196">Вы также можете использовать Add-AzureRmHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-196">You can alternatively use Add-AzureRmHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="ea6c0-197">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="ea6c0-197">-SecurityProfile</span></span>
<span data-ttu-id="ea6c0-198">Задает свойства, связанные с безопасностью, которые используются для создания надежного кластера.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-198">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="ea6c0-199">Вы также можете использовать командлет Add-AzureRmHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-199">You can alternatively use the Add-AzureRmHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="ea6c0-200">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="ea6c0-200">-SshCredential</span></span>
<span data-ttu-id="ea6c0-201">Указывает учетные данные SSH, которые будут использоваться для подключений по протоколу SSH.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-201">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="ea6c0-202">Это относится только к кластерам Linux.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-202">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="ea6c0-203">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="ea6c0-203">-SshPublicKey</span></span>
<span data-ttu-id="ea6c0-204">Указывает открытый ключ, который будет использоваться для подключений по протоколу SSH.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-204">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="ea6c0-205">Это относится только к кластерам Linux.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-205">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="ea6c0-206">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="ea6c0-206">-SubnetName</span></span>
<span data-ttu-id="ea6c0-207">Указывает имя подсети в выбранной виртуальной сети для кластера.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-207">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

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

### <span data-ttu-id="ea6c0-208">-Version</span><span class="sxs-lookup"><span data-stu-id="ea6c0-208">-Version</span></span>
<span data-ttu-id="ea6c0-209">Указывает версию HDI кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-209">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="ea6c0-210">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="ea6c0-210">-VirtualNetworkId</span></span>
<span data-ttu-id="ea6c0-211">Указывает ИД виртуальной сети, в которую подготавливается кластер.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-211">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="ea6c0-212">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="ea6c0-212">-WorkerNodeSize</span></span>
<span data-ttu-id="ea6c0-213">Указывает размер виртуальной машины для рабочего узла.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-213">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="ea6c0-214">Используйте Get-AzureRmVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-214">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="ea6c0-215">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="ea6c0-215">-ZookeeperNodeSize</span></span>
<span data-ttu-id="ea6c0-216">Указывает размер виртуальной машины для узла Джесс.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-216">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="ea6c0-217">Используйте Get-AzureRmVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-217">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="ea6c0-218">Этот параметр является допустимым только для кластеров HBase и.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-218">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="ea6c0-219">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea6c0-219">CommonParameters</span></span>
<span data-ttu-id="ea6c0-220">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ea6c0-220">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea6c0-221">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea6c0-221">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea6c0-222">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ea6c0-222">INPUTS</span></span>

### <span data-ttu-id="ea6c0-223">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="ea6c0-223">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>
<span data-ttu-id="ea6c0-224">Параметры: config (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ea6c0-224">Parameters: Config (ByValue)</span></span>

## <span data-ttu-id="ea6c0-225">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea6c0-225">OUTPUTS</span></span>

### <span data-ttu-id="ea6c0-226">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="ea6c0-226">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="ea6c0-227">Пуск</span><span class="sxs-lookup"><span data-stu-id="ea6c0-227">NOTES</span></span>
<span data-ttu-id="ea6c0-228">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, Hadoop, hdinsight, HD и Insights</span><span class="sxs-lookup"><span data-stu-id="ea6c0-228">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="ea6c0-229">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea6c0-229">RELATED LINKS</span></span>

[<span data-ttu-id="ea6c0-230">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="ea6c0-230">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)

