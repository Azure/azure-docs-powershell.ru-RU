---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: 9008cb1dba2c39a2c552b2395f4115ca50a17fdf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079080"
---
# <span data-ttu-id="24bcc-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="24bcc-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="24bcc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="24bcc-102">SYNOPSIS</span></span>
<span data-ttu-id="24bcc-103">Создает кластер HDInsight Azure в указанной группе ресурсов для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="24bcc-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="24bcc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="24bcc-104">SYNTAX</span></span>

### <span data-ttu-id="24bcc-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="24bcc-105">Default (Default)</span></span>
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
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificatePassword <String>]
 [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DisksPerWorkerNode <Int32>]
 [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>] [-EncryptionAlgorithm <String>]
 [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>]
 [-PublicNetworkAccessType <String>] [-OutboundPublicNetworkAccessType <String>]
 [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="24bcc-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="24bcc-106">CertificateFilePath</span></span>
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
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>]
 [-EncryptionVaultUri <String>] [-PublicNetworkAccessType <String>] [-OutboundPublicNetworkAccessType <String>]
 [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="24bcc-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="24bcc-107">CertificateFileContents</span></span>
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
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>]
 [-EncryptionVaultUri <String>] [-PublicNetworkAccessType <String>] [-OutboundPublicNetworkAccessType <String>]
 [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="24bcc-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="24bcc-108">DESCRIPTION</span></span>
<span data-ttu-id="24bcc-109">New-AzHDInsightCluster создает кластер HDInsight Azure, используя указанные параметры или объект конфигурации, созданный с помощью командлета New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="24bcc-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="24bcc-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="24bcc-110">EXAMPLES</span></span>

### <span data-ttu-id="24bcc-111">Пример 1: Создание кластера HDInsight Azure</span><span class="sxs-lookup"><span data-stu-id="24bcc-111">Example 1: Create an Azure HDInsight cluster</span></span>
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
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
```

<span data-ttu-id="24bcc-112">Эта команда создает кластер в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="24bcc-112">This command creates a cluster in the current subscription.</span></span>

### <span data-ttu-id="24bcc-113">Пример 2: Создание кластера с помощью шифрования диска с управляемым пользователем ключом</span><span class="sxs-lookup"><span data-stu-id="24bcc-113">Example 2: Create cluster with customer-managed key disk encryption</span></span>
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
        $clusterName = "your-cmk-cluster"
        $clusterCreds = Get-Credential

        # Customer-managed Key info
        $assignedIdentity = "your-ami-resource-id"
        $encryptionKeyName = "new-key"
        $encryptionVaultUri = "https://MyKeyVault.vault.azure.net"
        $encryptionKeyVersion = "00000000000000000000000000000000"

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Spark `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AssignedIdentity $assignedIdentity `
            -EncryptionKeyName $encryptionKeyName `
            -EncryptionVaultUri $encryptionVaultUri `
            -EncryptionKeyVersion $encryptionKeyVersion
```

### <span data-ttu-id="24bcc-114">Пример 3: Создание кластера HDInsight Azure, который обеспечивает шифрование в пути</span><span class="sxs-lookup"><span data-stu-id="24bcc-114">Example 3: Create an Azure HDInsight cluster which enables encryption in transit</span></span>
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
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionInTransit $true `
```

### <span data-ttu-id="24bcc-115">Пример 4: Создание кластера HDInsight для Azure с помощью функции Private Link</span><span class="sxs-lookup"><span data-stu-id="24bcc-115">Example 4: Create an Azure HDInsight cluster with private link feature</span></span>
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
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Virtual network info
        $virtualNetworkId="yourvnetresourceid"
        $subnetName="yoursubnetresourceid"

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -VirtualNetworkId $virtualNetworkId -SubnetName $subnetName `
            -PublicNetworkAccessType OutboundOnly -OutboundPublicNetworkAccessType PublicLoadBalancer `
```

### <span data-ttu-id="24bcc-116">Пример 5: Создание кластера HDInsight Azure, который обеспечивает шифрование на узле</span><span class="sxs-lookup"><span data-stu-id="24bcc-116">Example 5: Create an Azure HDInsight cluster which enables encryption at host</span></span>
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
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionAtHost $true `
```

### <span data-ttu-id="24bcc-117">Пример 6: Создание кластера HDInsight Azure, который включает Автомасштабирование.</span><span class="sxs-lookup"><span data-stu-id="24bcc-117">Example 6: Create an Azure HDInsight cluster which enables autoscale.</span></span>
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
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create autoscale configuration
        $autoscaleConfiguration=New-AzHDInsightClusterAutoscaleConfiguration `
            -MinWorkerNodeCount 3 -MaxWorkerNodeCount 5

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
            -DefaultStorageAccountKey $storageAccountKey `
            -DefaultStorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AutoscaleConfiguration $autoscaleConfiguration
```

## <span data-ttu-id="24bcc-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="24bcc-118">PARAMETERS</span></span>

### <span data-ttu-id="24bcc-119">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="24bcc-119">-AadTenantId</span></span>
<span data-ttu-id="24bcc-120">Указывает идентификатор клиента Azure AD, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="24bcc-120">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="24bcc-121">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="24bcc-121">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="24bcc-122">Указывает дополнительные учетные записи хранилища Azure для кластера.</span><span class="sxs-lookup"><span data-stu-id="24bcc-122">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="24bcc-123">Вы также можете использовать командлет Add-AzHDInsightStorage.</span><span class="sxs-lookup"><span data-stu-id="24bcc-123">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="24bcc-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="24bcc-124">-ApplicationId</span></span>
<span data-ttu-id="24bcc-125">Возвращает или задает идентификатор приложения субъекта-службы для доступа к Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="24bcc-125">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="24bcc-126">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="24bcc-126">-AssignedIdentity</span></span>
<span data-ttu-id="24bcc-127">Возвращает или задает назначенное удостоверение.</span><span class="sxs-lookup"><span data-stu-id="24bcc-127">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="24bcc-128">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="24bcc-128">-AutoscaleConfiguration</span></span>
<span data-ttu-id="24bcc-129">Возвращает или задает конфигурацию автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="24bcc-129">Gets or sets the autoscale configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightAutoscale
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24bcc-130">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="24bcc-130">-CertificateFileContents</span></span>
<span data-ttu-id="24bcc-131">Указывает содержимое файла сертификата, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="24bcc-131">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="24bcc-132">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="24bcc-132">-CertificateFilePath</span></span>
<span data-ttu-id="24bcc-133">Задает путь к файлу сертификата, который будет использоваться для проверки подлинности участника-службы.</span><span class="sxs-lookup"><span data-stu-id="24bcc-133">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="24bcc-134">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="24bcc-134">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="24bcc-135">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="24bcc-135">-CertificatePassword</span></span>
<span data-ttu-id="24bcc-136">Указывает пароль сертификата, который будет использоваться для проверки подлинности в качестве субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="24bcc-136">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="24bcc-137">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="24bcc-137">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="24bcc-138">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="24bcc-138">-ClusterName</span></span>
<span data-ttu-id="24bcc-139">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="24bcc-139">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="24bcc-140">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="24bcc-140">-ClusterSizeInNodes</span></span>
<span data-ttu-id="24bcc-141">Задает количество узлов рабочих процессов для кластера.</span><span class="sxs-lookup"><span data-stu-id="24bcc-141">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="24bcc-142">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="24bcc-142">-ClusterTier</span></span>
<span data-ttu-id="24bcc-143">Указывает уровень кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="24bcc-143">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="24bcc-144">По умолчанию это стандартный.</span><span class="sxs-lookup"><span data-stu-id="24bcc-144">By default, this is Standard.</span></span>
<span data-ttu-id="24bcc-145">Уровень Premium можно использовать только для кластеров Linux, а также для использования некоторых новых функций.</span><span class="sxs-lookup"><span data-stu-id="24bcc-145">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="24bcc-146">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="24bcc-146">-ClusterType</span></span>
<span data-ttu-id="24bcc-147">Указывает тип создаваемого кластера.</span><span class="sxs-lookup"><span data-stu-id="24bcc-147">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="24bcc-148">Доступны следующие варианты: Hadoop, HBase, INTERACTIVEHIVE, Kafka и RServer</span><span class="sxs-lookup"><span data-stu-id="24bcc-148">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

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

### <span data-ttu-id="24bcc-149">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="24bcc-149">-ComponentVersion</span></span>
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

### <span data-ttu-id="24bcc-150">-Config</span><span class="sxs-lookup"><span data-stu-id="24bcc-150">-Config</span></span>
<span data-ttu-id="24bcc-151">Указывает объект кластера, который будет использоваться для создания кластера.</span><span class="sxs-lookup"><span data-stu-id="24bcc-151">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="24bcc-152">Этот объект можно создать с помощью командлета New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="24bcc-152">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="24bcc-153">-Конфигурации</span><span class="sxs-lookup"><span data-stu-id="24bcc-153">-Configurations</span></span>
<span data-ttu-id="24bcc-154">Указывает конфигурации этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="24bcc-154">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="24bcc-155">Вы также можете использовать командлет Add-AzHDInsightConfigValues.</span><span class="sxs-lookup"><span data-stu-id="24bcc-155">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="24bcc-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24bcc-156">-DefaultProfile</span></span>
<span data-ttu-id="24bcc-157">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="24bcc-157">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24bcc-158">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="24bcc-158">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="24bcc-159">Указывает ключ учетной записи хранения Azure, используемой по умолчанию, которую будет использовать кластер HDInsight.</span><span class="sxs-lookup"><span data-stu-id="24bcc-159">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="24bcc-160">Вы также можете использовать командлет Set-AzHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="24bcc-160">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="24bcc-161">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="24bcc-161">-DefaultStorageAccountName</span></span>
<span data-ttu-id="24bcc-162">Указывает имя учетной записи хранения Azure, используемой по умолчанию, которое будет использоваться кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="24bcc-162">Specifies the name of the default Azure Storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="24bcc-163">Вы также можете использовать командлет Set-AzHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="24bcc-163">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="24bcc-164">-DefaultStorageAccountType</span><span class="sxs-lookup"><span data-stu-id="24bcc-164">-DefaultStorageAccountType</span></span>
<span data-ttu-id="24bcc-165">Указывает тип учетной записи хранения, используемой по умолчанию, которая будет использоваться кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="24bcc-165">Specifies the type of the default storage account that the HDInsight cluster will use.</span></span> <span data-ttu-id="24bcc-166">Возможные значения: AzureStorage и AzureDataLakeStore.</span><span class="sxs-lookup"><span data-stu-id="24bcc-166">Possible values are AzureStorage and AzureDataLakeStore.</span></span> <span data-ttu-id="24bcc-167">Если не указано, по умолчанию используется значение AzureStorage.</span><span class="sxs-lookup"><span data-stu-id="24bcc-167">Defaults to AzureStorage if not specified.</span></span>

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

### <span data-ttu-id="24bcc-168">-DefaultStorageContainer</span><span class="sxs-lookup"><span data-stu-id="24bcc-168">-DefaultStorageContainer</span></span>
<span data-ttu-id="24bcc-169">Указывает имя контейнера по умолчанию в учетной записи хранения Azure по умолчанию, который будет использоваться кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="24bcc-169">Specifies the name of the default container in the default Azure storage account that the HDInsight cluster will use.</span></span>
<span data-ttu-id="24bcc-170">Вы также можете использовать командлет Set-AzHDInsightDefaultStorage.</span><span class="sxs-lookup"><span data-stu-id="24bcc-170">You can alternatively use the Set-AzHDInsightDefaultStorage cmdlet.</span></span>

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

### <span data-ttu-id="24bcc-171">-DefaultStorageRootPath</span><span class="sxs-lookup"><span data-stu-id="24bcc-171">-DefaultStorageRootPath</span></span>
<span data-ttu-id="24bcc-172">Указывает префикс пути в учетной записи Data Lake Store, который кластер HDInsight будет использовать в качестве файловой системы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="24bcc-172">Specifies the path-prefix in the Data Lake Store Account that the HDInsight cluster will use as the default filesystem.</span></span>

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

### <span data-ttu-id="24bcc-173">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="24bcc-173">-DisksPerWorkerNode</span></span>
<span data-ttu-id="24bcc-174">Задает количество дисков для роли узла рабочего процесса в кластере.</span><span class="sxs-lookup"><span data-stu-id="24bcc-174">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="24bcc-175">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="24bcc-175">-EdgeNodeSize</span></span>
<span data-ttu-id="24bcc-176">Указывает размер виртуальной машины для граничного узла.</span><span class="sxs-lookup"><span data-stu-id="24bcc-176">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="24bcc-177">Используйте Get-AzVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="24bcc-177">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="24bcc-178">Этот параметр является допустимым только для кластеров RServer.</span><span class="sxs-lookup"><span data-stu-id="24bcc-178">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="24bcc-179">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="24bcc-179">-EncryptionAlgorithm</span></span>
<span data-ttu-id="24bcc-180">Возвращает или задает алгоритм шифрования.</span><span class="sxs-lookup"><span data-stu-id="24bcc-180">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="24bcc-181">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="24bcc-181">-EncryptionAtHost</span></span>
<span data-ttu-id="24bcc-182">Возвращает или задает флаг, указывающий, следует ли включить шифрование на хосте или нет.</span><span class="sxs-lookup"><span data-stu-id="24bcc-182">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="24bcc-183">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="24bcc-183">-EncryptionInTransit</span></span>
<span data-ttu-id="24bcc-184">Возвращает или задает флаг, указывающий, следует ли включить шифрование в пути или нет.</span><span class="sxs-lookup"><span data-stu-id="24bcc-184">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="24bcc-185">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="24bcc-185">-EncryptionKeyName</span></span>
<span data-ttu-id="24bcc-186">Возвращает или задает имя ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="24bcc-186">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="24bcc-187">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="24bcc-187">-EncryptionKeyVersion</span></span>
<span data-ttu-id="24bcc-188">Возвращает или задает версию ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="24bcc-188">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="24bcc-189">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="24bcc-189">-EncryptionVaultUri</span></span>
<span data-ttu-id="24bcc-190">Возвращает или задает универсальный код ресурса (URI) для хранилища шифрования.</span><span class="sxs-lookup"><span data-stu-id="24bcc-190">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="24bcc-191">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="24bcc-191">-HeadNodeSize</span></span>
<span data-ttu-id="24bcc-192">Задает размер виртуальной машины для головного узла.</span><span class="sxs-lookup"><span data-stu-id="24bcc-192">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="24bcc-193">Используйте Get-AzVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="24bcc-193">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="24bcc-194">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="24bcc-194">-HiveMetastore</span></span>
<span data-ttu-id="24bcc-195">Указывает базу данных SQL для хранения метаданных куста.</span><span class="sxs-lookup"><span data-stu-id="24bcc-195">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="24bcc-196">Вы также можете использовать командлет Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="24bcc-196">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="24bcc-197">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="24bcc-197">-HttpCredential</span></span>
<span data-ttu-id="24bcc-198">Задает учетные данные для входа в кластер (HTTP) для кластера.</span><span class="sxs-lookup"><span data-stu-id="24bcc-198">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="24bcc-199">-Location</span><span class="sxs-lookup"><span data-stu-id="24bcc-199">-Location</span></span>
<span data-ttu-id="24bcc-200">Задает расположение кластера.</span><span class="sxs-lookup"><span data-stu-id="24bcc-200">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="24bcc-201">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="24bcc-201">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="24bcc-202">Возвращает или задает минимальную поддерживаемую версию TLS.</span><span class="sxs-lookup"><span data-stu-id="24bcc-202">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="24bcc-203">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="24bcc-203">-ObjectId</span></span>
<span data-ttu-id="24bcc-204">Указывает идентификатор объекта Azure AD (GUID) субъекта-службы Azure AD, который представляет этот кластер.</span><span class="sxs-lookup"><span data-stu-id="24bcc-204">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="24bcc-205">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="24bcc-205">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="24bcc-206">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="24bcc-206">-OozieMetastore</span></span>
<span data-ttu-id="24bcc-207">Определяет базу данных SQL для хранения метаданных Oozie.</span><span class="sxs-lookup"><span data-stu-id="24bcc-207">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="24bcc-208">Вы также можете использовать командлет Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="24bcc-208">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="24bcc-209">-OSType</span><span class="sxs-lookup"><span data-stu-id="24bcc-209">-OSType</span></span>
<span data-ttu-id="24bcc-210">Указывает операционную систему для кластера.</span><span class="sxs-lookup"><span data-stu-id="24bcc-210">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="24bcc-211">Возможные варианты: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="24bcc-211">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="24bcc-212">-OutboundPublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="24bcc-212">-OutboundPublicNetworkAccessType</span></span>
<span data-ttu-id="24bcc-213">Возвращает или задает тип исходящего доступа к общедоступной сети.</span><span class="sxs-lookup"><span data-stu-id="24bcc-213">Gets or sets the outbound access type to the public network.</span></span>

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

### <span data-ttu-id="24bcc-214">-PublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="24bcc-214">-PublicNetworkAccessType</span></span>
<span data-ttu-id="24bcc-215">Возвращает или задает тип доступа к общедоступной сети.</span><span class="sxs-lookup"><span data-stu-id="24bcc-215">Gets or sets the public network access type.</span></span>

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

### <span data-ttu-id="24bcc-216">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="24bcc-216">-RdpAccessExpiry</span></span>
<span data-ttu-id="24bcc-217">Задает срок действия в виде объекта DateTime для доступа к кластеру через протокол удаленного рабочего стола (RDP).</span><span class="sxs-lookup"><span data-stu-id="24bcc-217">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="24bcc-218">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="24bcc-218">-RdpCredential</span></span>
<span data-ttu-id="24bcc-219">Указывает учетные данные удаленного рабочего стола (RDP) для кластера.</span><span class="sxs-lookup"><span data-stu-id="24bcc-219">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="24bcc-220">Это относится только к кластерам Windows.</span><span class="sxs-lookup"><span data-stu-id="24bcc-220">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="24bcc-221">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24bcc-221">-ResourceGroupName</span></span>
<span data-ttu-id="24bcc-222">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="24bcc-222">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="24bcc-223">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="24bcc-223">-ScriptActions</span></span>
<span data-ttu-id="24bcc-224">Задает действия сценария, которые должны выполняться в кластере по завершении создания кластера.</span><span class="sxs-lookup"><span data-stu-id="24bcc-224">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="24bcc-225">Вы также можете использовать Add-AzHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="24bcc-225">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="24bcc-226">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="24bcc-226">-SecurityProfile</span></span>
<span data-ttu-id="24bcc-227">Задает свойства, связанные с безопасностью, которые используются для создания надежного кластера.</span><span class="sxs-lookup"><span data-stu-id="24bcc-227">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="24bcc-228">Вы также можете использовать командлет Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="24bcc-228">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="24bcc-229">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="24bcc-229">-SshCredential</span></span>
<span data-ttu-id="24bcc-230">Указывает учетные данные SSH, которые будут использоваться для подключений по протоколу SSH.</span><span class="sxs-lookup"><span data-stu-id="24bcc-230">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="24bcc-231">Это относится только к кластерам Linux.</span><span class="sxs-lookup"><span data-stu-id="24bcc-231">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="24bcc-232">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="24bcc-232">-SshPublicKey</span></span>
<span data-ttu-id="24bcc-233">Указывает открытый ключ, который будет использоваться для подключений по протоколу SSH.</span><span class="sxs-lookup"><span data-stu-id="24bcc-233">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="24bcc-234">Это относится только к кластерам Linux.</span><span class="sxs-lookup"><span data-stu-id="24bcc-234">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="24bcc-235">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="24bcc-235">-SubnetName</span></span>
<span data-ttu-id="24bcc-236">Указывает имя подсети в выбранной виртуальной сети для кластера.</span><span class="sxs-lookup"><span data-stu-id="24bcc-236">Specifies the name of a subnet within the chosen virtual network for the cluster.</span></span>

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

### <span data-ttu-id="24bcc-237">-Version</span><span class="sxs-lookup"><span data-stu-id="24bcc-237">-Version</span></span>
<span data-ttu-id="24bcc-238">Указывает версию HDI кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="24bcc-238">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="24bcc-239">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="24bcc-239">-VirtualNetworkId</span></span>
<span data-ttu-id="24bcc-240">Указывает ИД виртуальной сети, в которую подготавливается кластер.</span><span class="sxs-lookup"><span data-stu-id="24bcc-240">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="24bcc-241">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="24bcc-241">-WorkerNodeSize</span></span>
<span data-ttu-id="24bcc-242">Указывает размер виртуальной машины для рабочего узла.</span><span class="sxs-lookup"><span data-stu-id="24bcc-242">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="24bcc-243">Используйте Get-AzVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="24bcc-243">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="24bcc-244">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="24bcc-244">-ZookeeperNodeSize</span></span>
<span data-ttu-id="24bcc-245">Указывает размер виртуальной машины для узла Джесс.</span><span class="sxs-lookup"><span data-stu-id="24bcc-245">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="24bcc-246">Используйте Get-AzVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="24bcc-246">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="24bcc-247">Этот параметр является допустимым только для кластеров HBase и.</span><span class="sxs-lookup"><span data-stu-id="24bcc-247">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="24bcc-248">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24bcc-248">CommonParameters</span></span>
<span data-ttu-id="24bcc-249">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="24bcc-249">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24bcc-250">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="24bcc-250">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24bcc-251">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="24bcc-251">INPUTS</span></span>

### <span data-ttu-id="24bcc-252">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="24bcc-252">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="24bcc-253">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="24bcc-253">OUTPUTS</span></span>

### <span data-ttu-id="24bcc-254">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="24bcc-254">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="24bcc-255">Пуск</span><span class="sxs-lookup"><span data-stu-id="24bcc-255">NOTES</span></span>
<span data-ttu-id="24bcc-256">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, Hadoop, hdinsight, HD и Insights</span><span class="sxs-lookup"><span data-stu-id="24bcc-256">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="24bcc-257">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="24bcc-257">RELATED LINKS</span></span>

[<span data-ttu-id="24bcc-258">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="24bcc-258">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

