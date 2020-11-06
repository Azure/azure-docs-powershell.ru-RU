---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightCluster.md
ms.openlocfilehash: 2e778f84eabf7e5dc4dd325d2a17361064c5d99f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569979"
---
# <span data-ttu-id="d5448-101">New-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d5448-101">New-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="d5448-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d5448-102">SYNOPSIS</span></span>
<span data-ttu-id="d5448-103">Создает кластер HDInsight Azure в указанной группе ресурсов для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="d5448-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5448-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d5448-104">SYNTAX</span></span>

### <span data-ttu-id="d5448-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d5448-105">Default (Default)</span></span>
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

### <span data-ttu-id="d5448-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="d5448-106">CertificateFilePath</span></span>
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

### <span data-ttu-id="d5448-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="d5448-107">CertificateFileContents</span></span>
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

## <span data-ttu-id="d5448-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5448-108">DESCRIPTION</span></span>
<span data-ttu-id="d5448-109">New-AzureHDInsightCluster создает кластер HDInsight Azure, используя указанные параметры или объект конфигурации, созданный с помощью командлета New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="d5448-109">The New-AzureHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="d5448-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d5448-110">EXAMPLES</span></span>

### <span data-ttu-id="d5448-111">--------------------------Пример 1: Создание кластера Azure HDInsight--------------------------</span><span class="sxs-lookup"><span data-stu-id="d5448-111">--------------------------  Example 1: Create an Azure HDInsight cluster  --------------------------</span></span>
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

<span data-ttu-id="d5448-112">Эта команда создает кластер в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="d5448-112">This command creates a cluster in the current subscription.</span></span>

## <span data-ttu-id="d5448-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d5448-113">PARAMETERS</span></span>

### <span data-ttu-id="d5448-114">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="d5448-114">-AadTenantId</span></span>
<span data-ttu-id="d5448-115">Указывает идентификатор клиента Azure AD, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d5448-115">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-116">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="d5448-116">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="d5448-117">Указывает дополнительные учетные записи хранилища Azure для кластера.</span><span class="sxs-lookup"><span data-stu-id="d5448-117">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="d5448-118">Вы также можете использовать командлет Add-AzureRmHDInsightStorage.</span><span class="sxs-lookup"><span data-stu-id="d5448-118">You can alternatively use the Add-AzureRmHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="d5448-119">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="d5448-119">-CertificateFileContents</span></span>
<span data-ttu-id="d5448-120">Указывает содержимое файла сертификата, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d5448-120">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Byte[]
Parameter Sets: CertificateFileContents
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-121">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="d5448-121">-CertificateFilePath</span></span>
<span data-ttu-id="d5448-122">Задает путь к файлу сертификата, который будет использоваться для проверки подлинности участника-службы.</span><span class="sxs-lookup"><span data-stu-id="d5448-122">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="d5448-123">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d5448-123">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: String
Parameter Sets: CertificateFilePath
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-124">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="d5448-124">-CertificatePassword</span></span>
<span data-ttu-id="d5448-125">Указывает пароль сертификата, который будет использоваться для проверки подлинности в качестве субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="d5448-125">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="d5448-126">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d5448-126">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-127">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="d5448-127">-ClusterName</span></span>
<span data-ttu-id="d5448-128">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="d5448-128">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-129">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="d5448-129">-ClusterSizeInNodes</span></span>
<span data-ttu-id="d5448-130">Задает количество узлов рабочих процессов для кластера.</span><span class="sxs-lookup"><span data-stu-id="d5448-130">Specifies the number of Worker nodes for the cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-131">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="d5448-131">-ClusterTier</span></span>
<span data-ttu-id="d5448-132">Указывает уровень кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d5448-132">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="d5448-133">По умолчанию это стандартный.</span><span class="sxs-lookup"><span data-stu-id="d5448-133">By default, this is Standard.</span></span>
<span data-ttu-id="d5448-134">Уровень Premium можно использовать только для кластеров Linux, а также для использования некоторых новых функций.</span><span class="sxs-lookup"><span data-stu-id="d5448-134">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

```yaml
Type: Tier
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-135">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="d5448-135">-ClusterType</span></span>
<span data-ttu-id="d5448-136">Указывает тип создаваемого кластера.</span><span class="sxs-lookup"><span data-stu-id="d5448-136">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="d5448-137">Возможные варианты: Hadoop, HBase, г., Spark</span><span class="sxs-lookup"><span data-stu-id="d5448-137">Options are: Hadoop, HBase, Storm, Spark</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-138">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="d5448-138">-ComponentVersion</span></span>
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

### <span data-ttu-id="d5448-139">-Config</span><span class="sxs-lookup"><span data-stu-id="d5448-139">-Config</span></span>
<span data-ttu-id="d5448-140">Указывает объект кластера, который будет использоваться для создания кластера.</span><span class="sxs-lookup"><span data-stu-id="d5448-140">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="d5448-141">Этот объект можно создать с помощью командлета New-AzureRmHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="d5448-141">This object can be created by using the New-AzureRmHDInsightClusterConfig cmdlet.</span></span>

```yaml
Type: AzureHDInsightConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-142">-Конфигурации</span><span class="sxs-lookup"><span data-stu-id="d5448-142">-Configurations</span></span>
<span data-ttu-id="d5448-143">Указывает конфигурации этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d5448-143">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="d5448-144">Вы также можете использовать командлет Add-AzureRmHDInsightConfigValues.</span><span class="sxs-lookup"><span data-stu-id="d5448-144">You can alternatively use the Add-AzureRmHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="d5448-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5448-145">-DefaultProfile</span></span>
<span data-ttu-id="d5448-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d5448-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5448-147">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d5448-147">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="d5448-148">Указывает ключ учетной записи хранения Azure, используемой по умолчанию, которую будет использовать кластер HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d5448-148">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="d5448-149">Вы также можете использовать командлет Set-AzureRmHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="d5448-149">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-150">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d5448-150">-DefaultStorageAccountName</span></span>
<span data-ttu-id="d5448-151">Указывает имя учетной записи хранения Azure, используемой по умолчанию, которое будет использоваться кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d5448-151">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="d5448-152">Вы также можете использовать командлет Set-AzureRmHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="d5448-152">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-153">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="d5448-153">-DefaultStorageAccountType</span></span>
<span data-ttu-id="d5448-154">Указывает тип учетной записи хранения, используемой по умолчанию, которая будет использоваться кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d5448-154">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="d5448-155">Возможные значения: AzureStorage и AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="d5448-155">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="d5448-156">Если не указано, по умолчанию используется значение AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="d5448-156">Defaults to AzureStorage if not specified.</span></span>

```yaml
Type: StorageType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: AzureStorage
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-157">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="d5448-157">-DefaultStorageContainer</span></span>
<span data-ttu-id="d5448-158">Указывает имя контейнера по умолчанию в учетной записи хранения Azure по умолчанию, который будет использоваться кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d5448-158">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="d5448-159">Вы также можете использовать командлет Set-AzureRmHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="d5448-159">You can alternatively use the Set-AzureRmHDInsightDefaultStorage cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-160">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="d5448-160">-DefaultStorageRootPath</span></span>
<span data-ttu-id="d5448-161">Указывает префикс пути в учетной записи Data Lake Store, который кластер HDInsight будет использовать в качестве файловой системы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d5448-161">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-162">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="d5448-162">-DisksPerWorkerNode</span></span>
<span data-ttu-id="d5448-163">Задает количество дисков для роли узла рабочего процесса в кластере.</span><span class="sxs-lookup"><span data-stu-id="d5448-163">Specifies the number of disks for worker node role in the cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-164">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="d5448-164">-EdgeNodeSize</span></span>
<span data-ttu-id="d5448-165">Указывает размер виртуальной машины для граничного узла.</span><span class="sxs-lookup"><span data-stu-id="d5448-165">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="d5448-166">Используйте Get-AzureRmVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d5448-166">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="d5448-167">Этот параметр является допустимым только для кластеров RServer.</span><span class="sxs-lookup"><span data-stu-id="d5448-167">This parameter is valid only for RServer clusters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-168">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="d5448-168">-HeadNodeSize</span></span>
<span data-ttu-id="d5448-169">Задает размер виртуальной машины для головного узла.</span><span class="sxs-lookup"><span data-stu-id="d5448-169">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="d5448-170">Используйте Get-AzureRmVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d5448-170">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-171">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="d5448-171">-HiveMetastore</span></span>
<span data-ttu-id="d5448-172">Указывает базу данных SQL для хранения метаданных куста.</span><span class="sxs-lookup"><span data-stu-id="d5448-172">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="d5448-173">Вы также можете использовать командлет Add-AzureRmHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="d5448-173">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

```yaml
Type: AzureHDInsightMetastore
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-174">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="d5448-174">-HttpCredential</span></span>
<span data-ttu-id="d5448-175">Задает учетные данные для входа в кластер (HTTP) для кластера.</span><span class="sxs-lookup"><span data-stu-id="d5448-175">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-176">-Location</span><span class="sxs-lookup"><span data-stu-id="d5448-176">-Location</span></span>
<span data-ttu-id="d5448-177">Задает расположение кластера.</span><span class="sxs-lookup"><span data-stu-id="d5448-177">Specifies the location for the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-178">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d5448-178">-ObjectId</span></span>
<span data-ttu-id="d5448-179">Указывает идентификатор объекта Azure AD (GUID) субъекта-службы Azure AD, который представляет этот кластер.</span><span class="sxs-lookup"><span data-stu-id="d5448-179">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="d5448-180">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d5448-180">The cluster will use this when accessing Azure Data Lake Store.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-181">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="d5448-181">-OozieMetastore</span></span>
<span data-ttu-id="d5448-182">Определяет базу данных SQL для хранения метаданных Oozie.</span><span class="sxs-lookup"><span data-stu-id="d5448-182">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="d5448-183">Вы также можете использовать командлет Add-AzureRmHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="d5448-183">You can alternatively use the Add-AzureRmHDInsightMetastore cmdlet.</span></span>

```yaml
Type: AzureHDInsightMetastore
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-184">-OSType</span><span class="sxs-lookup"><span data-stu-id="d5448-184">-OSType</span></span>
<span data-ttu-id="d5448-185">Указывает операционную систему для кластера.</span><span class="sxs-lookup"><span data-stu-id="d5448-185">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="d5448-186">Возможные варианты: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="d5448-186">Options are: Windows, Linux</span></span>

```yaml
Type: OSType
Parameter Sets: (All)
Aliases: 
Accepted values: Windows, Linux

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-187">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="d5448-187">-RdpAccessExpiry</span></span>
<span data-ttu-id="d5448-188">Задает срок действия в виде объекта DateTime для доступа к кластеру через протокол удаленного рабочего стола (RDP).</span><span class="sxs-lookup"><span data-stu-id="d5448-188">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-189">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="d5448-189">-RdpCredential</span></span>
<span data-ttu-id="d5448-190">Указывает учетные данные удаленного рабочего стола (RDP) для кластера.</span><span class="sxs-lookup"><span data-stu-id="d5448-190">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="d5448-191">Это относится только к кластерам Windows.</span><span class="sxs-lookup"><span data-stu-id="d5448-191">This is only for Windows clusters.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5448-192">-ResourceGroupName</span></span>
<span data-ttu-id="d5448-193">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d5448-193">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-194">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="d5448-194">-ScriptActions</span></span>
<span data-ttu-id="d5448-195">Задает действия сценария, которые должны выполняться в кластере по завершении создания кластера.</span><span class="sxs-lookup"><span data-stu-id="d5448-195">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="d5448-196">Вы также можете использовать Add-AzureRmHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="d5448-196">You can alternatively use Add-AzureRmHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="d5448-197">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="d5448-197">-SecurityProfile</span></span>
<span data-ttu-id="d5448-198">Задает свойства, связанные с безопасностью, которые используются для создания надежного кластера.</span><span class="sxs-lookup"><span data-stu-id="d5448-198">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="d5448-199">Вы также можете использовать командлет Add-AzureRmHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="d5448-199">You can alternatively use the Add-AzureRmHDInsightSecurityProfile cmdlet.</span></span>

```yaml
Type: AzureHDInsightSecurityProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-200">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="d5448-200">-SshCredential</span></span>
<span data-ttu-id="d5448-201">Указывает учетные данные SSH, которые будут использоваться для подключений по протоколу SSH.</span><span class="sxs-lookup"><span data-stu-id="d5448-201">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="d5448-202">Это относится только к кластерам Linux.</span><span class="sxs-lookup"><span data-stu-id="d5448-202">This is only for Linux clusters.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-203">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="d5448-203">-SshPublicKey</span></span>
<span data-ttu-id="d5448-204">Указывает открытый ключ, который будет использоваться для подключений по протоколу SSH.</span><span class="sxs-lookup"><span data-stu-id="d5448-204">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="d5448-205">Это относится только к кластерам Linux.</span><span class="sxs-lookup"><span data-stu-id="d5448-205">This is only for Linux clusters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-206">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="d5448-206">-SubnetName</span></span>
<span data-ttu-id="d5448-207">Указывает имя подсети в выбранной виртуальной сети для кластера.</span><span class="sxs-lookup"><span data-stu-id="d5448-207">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-208">-Version</span><span class="sxs-lookup"><span data-stu-id="d5448-208">-Version</span></span>
<span data-ttu-id="d5448-209">Указывает версию HDI кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d5448-209">Specifies the HDI version of the HDInsight cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-210">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="d5448-210">-VirtualNetworkId</span></span>
<span data-ttu-id="d5448-211">Указывает ИД виртуальной сети, в которую подготавливается кластер.</span><span class="sxs-lookup"><span data-stu-id="d5448-211">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-212">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="d5448-212">-WorkerNodeSize</span></span>
<span data-ttu-id="d5448-213">Указывает размер виртуальной машины для рабочего узла.</span><span class="sxs-lookup"><span data-stu-id="d5448-213">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="d5448-214">Используйте Get-AzureRmVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d5448-214">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-215">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="d5448-215">-ZookeeperNodeSize</span></span>
<span data-ttu-id="d5448-216">Указывает размер виртуальной машины для узла Джесс.</span><span class="sxs-lookup"><span data-stu-id="d5448-216">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="d5448-217">Используйте Get-AzureRmVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d5448-217">Use Get-AzureRmVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="d5448-218">Этот параметр является допустимым только для кластеров HBase и.</span><span class="sxs-lookup"><span data-stu-id="d5448-218">This parameter is valid only for HBase or Storm clusters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5448-219">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5448-219">CommonParameters</span></span>
<span data-ttu-id="d5448-220">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d5448-220">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5448-221">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5448-221">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5448-222">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d5448-222">INPUTS</span></span>

### <span data-ttu-id="d5448-223">AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="d5448-223">AzureHDInsightConfig</span></span>
<span data-ttu-id="d5448-224">Параметр config принимает значение типа "AzureHDInsightConfig" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="d5448-224">Parameter 'Config' accepts value of type 'AzureHDInsightConfig' from the pipeline</span></span>

## <span data-ttu-id="d5448-225">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5448-225">OUTPUTS</span></span>

### <span data-ttu-id="d5448-226">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="d5448-226">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="d5448-227">Пуск</span><span class="sxs-lookup"><span data-stu-id="d5448-227">NOTES</span></span>
<span data-ttu-id="d5448-228">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, Hadoop, hdinsight, HD и Insights</span><span class="sxs-lookup"><span data-stu-id="d5448-228">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="d5448-229">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5448-229">RELATED LINKS</span></span>

[<span data-ttu-id="d5448-230">New-AzureRmHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="d5448-230">New-AzureRmHDInsightClusterConfig</span></span>](./New-AzureRmHDInsightClusterConfig.md)

