---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: a372654faa9c3f157c44e5f60ff2f4244cd16d7e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720820"
---
# <span data-ttu-id="4489f-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="4489f-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="4489f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4489f-102">SYNOPSIS</span></span>
<span data-ttu-id="4489f-103">Создает кластер HDInsight Azure в указанной группе ресурсов для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="4489f-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="4489f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4489f-104">SYNTAX</span></span>

### <span data-ttu-id="4489f-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4489f-105">Default (Default)</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
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

### <span data-ttu-id="4489f-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="4489f-106">CertificateFilePath</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
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

### <span data-ttu-id="4489f-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="4489f-107">CertificateFileContents</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
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

## <span data-ttu-id="4489f-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4489f-108">DESCRIPTION</span></span>
<span data-ttu-id="4489f-109">New-AzHDInsightCluster создает кластер HDInsight Azure, используя указанные параметры или объект конфигурации, созданный с помощью командлета New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="4489f-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="4489f-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4489f-110">EXAMPLES</span></span>

### <span data-ttu-id="4489f-111">Пример 1: Создание кластера HDInsight Azure</span><span class="sxs-lookup"><span data-stu-id="4489f-111">Example 1: Create an Azure HDInsight cluster</span></span>
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

<span data-ttu-id="4489f-112">Эта команда создает кластер в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="4489f-112">This command creates a cluster in the current subscription.</span></span>

## <span data-ttu-id="4489f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4489f-113">PARAMETERS</span></span>

### <span data-ttu-id="4489f-114">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="4489f-114">-AadTenantId</span></span>
<span data-ttu-id="4489f-115">Указывает идентификатор клиента Azure AD, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4489f-115">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="4489f-116">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="4489f-116">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="4489f-117">Указывает дополнительные учетные записи хранилища Azure для кластера.</span><span class="sxs-lookup"><span data-stu-id="4489f-117">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="4489f-118">Вы также можете использовать командлет Add-AzHDInsightStorage.</span><span class="sxs-lookup"><span data-stu-id="4489f-118">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="4489f-119">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="4489f-119">-CertificateFileContents</span></span>
<span data-ttu-id="4489f-120">Указывает содержимое файла сертификата, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4489f-120">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="4489f-121">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="4489f-121">-CertificateFilePath</span></span>
<span data-ttu-id="4489f-122">Задает путь к файлу сертификата, который будет использоваться для проверки подлинности участника-службы.</span><span class="sxs-lookup"><span data-stu-id="4489f-122">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="4489f-123">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4489f-123">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="4489f-124">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="4489f-124">-CertificatePassword</span></span>
<span data-ttu-id="4489f-125">Указывает пароль сертификата, который будет использоваться для проверки подлинности в качестве субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="4489f-125">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="4489f-126">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4489f-126">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="4489f-127">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="4489f-127">-ClusterName</span></span>
<span data-ttu-id="4489f-128">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="4489f-128">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="4489f-129">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="4489f-129">-ClusterSizeInNodes</span></span>
<span data-ttu-id="4489f-130">Задает количество узлов рабочих процессов для кластера.</span><span class="sxs-lookup"><span data-stu-id="4489f-130">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="4489f-131">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="4489f-131">-ClusterTier</span></span>
<span data-ttu-id="4489f-132">Указывает уровень кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4489f-132">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="4489f-133">По умолчанию это стандартный.</span><span class="sxs-lookup"><span data-stu-id="4489f-133">By default, this is Standard.</span></span>
<span data-ttu-id="4489f-134">Уровень Premium можно использовать только для кластеров Linux, а также для использования некоторых новых функций.</span><span class="sxs-lookup"><span data-stu-id="4489f-134">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="4489f-135">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="4489f-135">-ClusterType</span></span>
<span data-ttu-id="4489f-136">Указывает тип создаваемого кластера.</span><span class="sxs-lookup"><span data-stu-id="4489f-136">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="4489f-137">Возможные варианты: Hadoop, HBase, г., Spark</span><span class="sxs-lookup"><span data-stu-id="4489f-137">Options are: Hadoop, HBase, Storm, Spark</span></span>

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

### <span data-ttu-id="4489f-138">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="4489f-138">-ComponentVersion</span></span>
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

### <span data-ttu-id="4489f-139">-Config</span><span class="sxs-lookup"><span data-stu-id="4489f-139">-Config</span></span>
<span data-ttu-id="4489f-140">Указывает объект кластера, который будет использоваться для создания кластера.</span><span class="sxs-lookup"><span data-stu-id="4489f-140">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="4489f-141">Этот объект можно создать с помощью командлета New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="4489f-141">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="4489f-142">-Конфигурации</span><span class="sxs-lookup"><span data-stu-id="4489f-142">-Configurations</span></span>
<span data-ttu-id="4489f-143">Указывает конфигурации этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4489f-143">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="4489f-144">Вы также можете использовать командлет Add-AzHDInsightConfigValues.</span><span class="sxs-lookup"><span data-stu-id="4489f-144">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="4489f-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4489f-145">-DefaultProfile</span></span>
<span data-ttu-id="4489f-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4489f-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4489f-147">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="4489f-147">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="4489f-148">Указывает ключ учетной записи хранения Azure, используемой по умолчанию, которую будет использовать кластер HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4489f-148">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="4489f-149">Вы также можете использовать командлет Set-AzHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="4489f-149">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="4489f-150">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="4489f-150">-DefaultStorageAccountName</span></span>
<span data-ttu-id="4489f-151">Указывает имя учетной записи хранения Azure, используемой по умолчанию, которое будет использоваться кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4489f-151">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="4489f-152">Вы также можете использовать командлет Set-AzHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="4489f-152">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="4489f-153">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="4489f-153">-DefaultStorageAccountType</span></span>
<span data-ttu-id="4489f-154">Указывает тип учетной записи хранения, используемой по умолчанию, которая будет использоваться кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4489f-154">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="4489f-155">Возможные значения: AzureStorage и AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="4489f-155">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="4489f-156">Если не указано, по умолчанию используется значение AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="4489f-156">Defaults to AzureStorage if not specified.</span></span>

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

### <span data-ttu-id="4489f-157">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="4489f-157">-DefaultStorageContainer</span></span>
<span data-ttu-id="4489f-158">Указывает имя контейнера по умолчанию в учетной записи хранения Azure по умолчанию, который будет использоваться кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4489f-158">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="4489f-159">Вы также можете использовать командлет Set-AzHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="4489f-159">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="4489f-160">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="4489f-160">-DefaultStorageRootPath</span></span>
<span data-ttu-id="4489f-161">Указывает префикс пути в учетной записи Data Lake Store, который кластер HDInsight будет использовать в качестве файловой системы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4489f-161">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

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

### <span data-ttu-id="4489f-162">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="4489f-162">-DisksPerWorkerNode</span></span>
<span data-ttu-id="4489f-163">Задает количество дисков для роли узла рабочего процесса в кластере.</span><span class="sxs-lookup"><span data-stu-id="4489f-163">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="4489f-164">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="4489f-164">-EdgeNodeSize</span></span>
<span data-ttu-id="4489f-165">Указывает размер виртуальной машины для граничного узла.</span><span class="sxs-lookup"><span data-stu-id="4489f-165">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="4489f-166">Используйте Get-AzVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4489f-166">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="4489f-167">Этот параметр является допустимым только для кластеров RServer.</span><span class="sxs-lookup"><span data-stu-id="4489f-167">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="4489f-168">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="4489f-168">-HeadNodeSize</span></span>
<span data-ttu-id="4489f-169">Задает размер виртуальной машины для головного узла.</span><span class="sxs-lookup"><span data-stu-id="4489f-169">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="4489f-170">Используйте Get-AzVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4489f-170">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="4489f-171">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="4489f-171">-HiveMetastore</span></span>
<span data-ttu-id="4489f-172">Указывает базу данных SQL для хранения метаданных куста.</span><span class="sxs-lookup"><span data-stu-id="4489f-172">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="4489f-173">Вы также можете использовать командлет Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="4489f-173">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="4489f-174">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="4489f-174">-HttpCredential</span></span>
<span data-ttu-id="4489f-175">Задает учетные данные для входа в кластер (HTTP) для кластера.</span><span class="sxs-lookup"><span data-stu-id="4489f-175">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="4489f-176">-Location</span><span class="sxs-lookup"><span data-stu-id="4489f-176">-Location</span></span>
<span data-ttu-id="4489f-177">Задает расположение кластера.</span><span class="sxs-lookup"><span data-stu-id="4489f-177">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="4489f-178">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4489f-178">-ObjectId</span></span>
<span data-ttu-id="4489f-179">Указывает идентификатор объекта Azure AD (GUID) субъекта-службы Azure AD, который представляет этот кластер.</span><span class="sxs-lookup"><span data-stu-id="4489f-179">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="4489f-180">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4489f-180">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="4489f-181">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="4489f-181">-OozieMetastore</span></span>
<span data-ttu-id="4489f-182">Определяет базу данных SQL для хранения метаданных Oozie.</span><span class="sxs-lookup"><span data-stu-id="4489f-182">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="4489f-183">Вы также можете использовать командлет Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="4489f-183">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="4489f-184">-OSType</span><span class="sxs-lookup"><span data-stu-id="4489f-184">-OSType</span></span>
<span data-ttu-id="4489f-185">Указывает операционную систему для кластера.</span><span class="sxs-lookup"><span data-stu-id="4489f-185">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="4489f-186">Возможные варианты: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="4489f-186">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="4489f-187">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="4489f-187">-RdpAccessExpiry</span></span>
<span data-ttu-id="4489f-188">Задает срок действия в виде объекта DateTime для доступа к кластеру через протокол удаленного рабочего стола (RDP).</span><span class="sxs-lookup"><span data-stu-id="4489f-188">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="4489f-189">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="4489f-189">-RdpCredential</span></span>
<span data-ttu-id="4489f-190">Указывает учетные данные удаленного рабочего стола (RDP) для кластера.</span><span class="sxs-lookup"><span data-stu-id="4489f-190">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="4489f-191">Это относится только к кластерам Windows.</span><span class="sxs-lookup"><span data-stu-id="4489f-191">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="4489f-192">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4489f-192">-ResourceGroupName</span></span>
<span data-ttu-id="4489f-193">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4489f-193">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="4489f-194">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="4489f-194">-ScriptActions</span></span>
<span data-ttu-id="4489f-195">Задает действия сценария, которые должны выполняться в кластере по завершении создания кластера.</span><span class="sxs-lookup"><span data-stu-id="4489f-195">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="4489f-196">Вы также можете использовать Add-AzHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="4489f-196">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="4489f-197">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="4489f-197">-SecurityProfile</span></span>
<span data-ttu-id="4489f-198">Задает свойства, связанные с безопасностью, которые используются для создания надежного кластера.</span><span class="sxs-lookup"><span data-stu-id="4489f-198">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="4489f-199">Вы также можете использовать командлет Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="4489f-199">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="4489f-200">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="4489f-200">-SshCredential</span></span>
<span data-ttu-id="4489f-201">Указывает учетные данные SSH, которые будут использоваться для подключений по протоколу SSH.</span><span class="sxs-lookup"><span data-stu-id="4489f-201">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="4489f-202">Это относится только к кластерам Linux.</span><span class="sxs-lookup"><span data-stu-id="4489f-202">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="4489f-203">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="4489f-203">-SshPublicKey</span></span>
<span data-ttu-id="4489f-204">Указывает открытый ключ, который будет использоваться для подключений по протоколу SSH.</span><span class="sxs-lookup"><span data-stu-id="4489f-204">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="4489f-205">Это относится только к кластерам Linux.</span><span class="sxs-lookup"><span data-stu-id="4489f-205">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="4489f-206">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="4489f-206">-SubnetName</span></span>
<span data-ttu-id="4489f-207">Указывает имя подсети в выбранной виртуальной сети для кластера.</span><span class="sxs-lookup"><span data-stu-id="4489f-207">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

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

### <span data-ttu-id="4489f-208">-Version</span><span class="sxs-lookup"><span data-stu-id="4489f-208">-Version</span></span>
<span data-ttu-id="4489f-209">Указывает версию HDI кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4489f-209">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="4489f-210">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="4489f-210">-VirtualNetworkId</span></span>
<span data-ttu-id="4489f-211">Указывает ИД виртуальной сети, в которую подготавливается кластер.</span><span class="sxs-lookup"><span data-stu-id="4489f-211">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="4489f-212">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="4489f-212">-WorkerNodeSize</span></span>
<span data-ttu-id="4489f-213">Указывает размер виртуальной машины для рабочего узла.</span><span class="sxs-lookup"><span data-stu-id="4489f-213">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="4489f-214">Используйте Get-AzVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4489f-214">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="4489f-215">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="4489f-215">-ZookeeperNodeSize</span></span>
<span data-ttu-id="4489f-216">Указывает размер виртуальной машины для узла Джесс.</span><span class="sxs-lookup"><span data-stu-id="4489f-216">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="4489f-217">Используйте Get-AzVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="4489f-217">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="4489f-218">Этот параметр является допустимым только для кластеров HBase и.</span><span class="sxs-lookup"><span data-stu-id="4489f-218">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="4489f-219">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4489f-219">CommonParameters</span></span>
<span data-ttu-id="4489f-220">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4489f-220">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4489f-221">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4489f-221">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4489f-222">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4489f-222">INPUTS</span></span>

### <span data-ttu-id="4489f-223">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="4489f-223">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="4489f-224">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4489f-224">OUTPUTS</span></span>

### <span data-ttu-id="4489f-225">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="4489f-225">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="4489f-226">Пуск</span><span class="sxs-lookup"><span data-stu-id="4489f-226">NOTES</span></span>
<span data-ttu-id="4489f-227">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, Hadoop, hdinsight, HD и Insights</span><span class="sxs-lookup"><span data-stu-id="4489f-227">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="4489f-228">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4489f-228">RELATED LINKS</span></span>

[<span data-ttu-id="4489f-229">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="4489f-229">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

