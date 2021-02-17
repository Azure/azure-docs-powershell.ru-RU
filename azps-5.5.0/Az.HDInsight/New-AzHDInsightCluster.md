---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: d4353e49c72f280ee89a1861682ab5d7c3061a9c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234345"
---
# <span data-ttu-id="1c7a5-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="1c7a5-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="1c7a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c7a5-102">SYNOPSIS</span></span>
<span data-ttu-id="1c7a5-103">Создает кластер Azure HDInsight в указанной группе ресурсов для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="1c7a5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1c7a5-104">SYNTAX</span></span>

### <span data-ttu-id="1c7a5-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1c7a5-105">Default (Default)</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
 [-AmbariDatabase <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-StorageContainer <String>] [-StorageRootPath <String>] [-StorageFileSystem <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>]
 [-KafkaManagementNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificatePassword <String>]
 [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>] [-DisksPerWorkerNode <Int32>]
 [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>] [-StorageAccountManagedIdentity <String>]
 [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>] [-EncryptionKeyVersion <String>]
 [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-EnableIDBroker] [-KafkaClientGroupId <String>]
 [-KafkaClientGroupName <String>] [-ResourceProviderConnection <String>] [-PrivateLink <String>]
 [-EnableComputeIsolation] [-ComputeIsolationHostSku <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1c7a5-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="1c7a5-106">CertificateFilePath</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
 [-AmbariDatabase <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-StorageContainer <String>] [-StorageRootPath <String>] [-StorageFileSystem <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>]
 [-KafkaManagementNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-StorageAccountManagedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>]
 [-EncryptionAtHost <Boolean>] [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-EnableIDBroker]
 [-KafkaClientGroupId <String>] [-KafkaClientGroupName <String>] [-ResourceProviderConnection <String>]
 [-PrivateLink <String>] [-EnableComputeIsolation] [-ComputeIsolationHostSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1c7a5-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="1c7a5-107">CertificateFileContents</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
 [-AmbariDatabase <AzureHDInsightMetastore>]
 [-AdditionalStorageAccounts <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-Configurations <System.Collections.Generic.Dictionary`2[System.String,System.Collections.Generic.Dictionary`2[System.String,System.String]]>]
 [-ScriptActions <System.Collections.Generic.Dictionary`2[Microsoft.Azure.Management.HDInsight.Models.ClusterNodeType,System.Collections.Generic.List`1[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightScriptAction]]>]
 [-StorageContainer <String>] [-StorageRootPath <String>] [-StorageFileSystem <String>] [-Version <String>]
 [-HeadNodeSize <String>] [-WorkerNodeSize <String>] [-EdgeNodeSize <String>]
 [-KafkaManagementNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>]
 [-ComponentVersion <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-VirtualNetworkId <String>] [-SubnetName <String>] [-OSType <OSType>] [-ClusterTier <Tier>]
 [-SshCredential <PSCredential>] [-SshPublicKey <String>] [-RdpCredential <PSCredential>]
 [-RdpAccessExpiry <DateTime>] [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-SecurityProfile <AzureHDInsightSecurityProfile>]
 [-DisksPerWorkerNode <Int32>] [-MinSupportedTlsVersion <String>] [-AssignedIdentity <String>]
 [-StorageAccountManagedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-EncryptionInTransit <Boolean>]
 [-EncryptionAtHost <Boolean>] [-AutoscaleConfiguration <AzureHDInsightAutoscale>] [-EnableIDBroker]
 [-KafkaClientGroupId <String>] [-KafkaClientGroupName <String>] [-ResourceProviderConnection <String>]
 [-PrivateLink <String>] [-EnableComputeIsolation] [-ComputeIsolationHostSku <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1c7a5-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c7a5-108">DESCRIPTION</span></span>
<span data-ttu-id="1c7a5-109">Служба New-AzHDInsightCluster создает кластер Azure HDInsight с использованием указанных параметров или объекта конфигурации, созданного с помощью New-AzHDInsightClusterConfig управления.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="1c7a5-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1c7a5-110">EXAMPLES</span></span>

### <span data-ttu-id="1c7a5-111">Пример 1. Создание кластера Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="1c7a5-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
```

<span data-ttu-id="1c7a5-112">Эта команда создает кластер в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-112">This command creates a cluster in the current subscription.</span></span>

### <span data-ttu-id="1c7a5-113">Пример 2. Создание кластера с шифрованием дисков под управлением клиента</span><span class="sxs-lookup"><span data-stu-id="1c7a5-113">Example 2: Create cluster with customer-managed key disk encryption</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AssignedIdentity $assignedIdentity `
            -EncryptionKeyName $encryptionKeyName `
            -EncryptionVaultUri $encryptionVaultUri `
            -EncryptionKeyVersion $encryptionKeyVersion
```

### <span data-ttu-id="1c7a5-114">Пример 3. Создание кластера Azure HDInsight, который обеспечивает шифрование при переходе</span><span class="sxs-lookup"><span data-stu-id="1c7a5-114">Example 3: Create an Azure HDInsight cluster which enables encryption in transit</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}}
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionInTransit $true `
```

### <span data-ttu-id="1c7a5-115">Пример 4. Создание кластера Azure HDInsight с функцией ретрансляции исходящие и частные ссылки</span><span class="sxs-lookup"><span data-stu-id="1c7a5-115">Example 4: Create an Azure HDInsight cluster with relay outbound and private link feature</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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
        $subnetName="yoursubnetname"

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -VirtualNetworkId $virtualNetworkId -SubnetName $subnetName `
            -ResourceProviderConnection Outbound -PrivateLink Enabled `
```

### <span data-ttu-id="1c7a5-116">Пример 5. Создание кластера Azure HDInsight, который обеспечивает шифрование на хосте</span><span class="sxs-lookup"><span data-stu-id="1c7a5-116">Example 5: Create an Azure HDInsight cluster which enables encryption at host</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionAtHost $true `
```

### <span data-ttu-id="1c7a5-117">Пример 6. Создание кластера Azure HDInsight, который обеспечивает автоматическую шкалу.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-117">Example 6: Create an Azure HDInsight cluster which enables autoscale.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AutoscaleConfiguration $autoscaleConfiguration
```

### <span data-ttu-id="1c7a5-118">Пример 7. Создание кластера Azure HDInsight с прокси-сервером rest Kafka.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-118">Example 7: Create an Azure HDInsight cluster with Kafka Rest Proxy.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Kafka Rest Proxy configuration info
        $kafkaClientGroupName = "yourclientgroupname"
        $kafkaClientGroupId = "yourclientgroupid"
        $kafkaManagementNodeSize = "Standard_D4_v2"
        $disksPerWorkerNode = 2

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Kafka `
            -ClusterSizeInNodes 4 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -KafkaClientGroupId  $kafkaClientGroupId -KafkaClientGroupName $kafkaClientGroupName `
            -KafkaManagementNodeSize $kafkaManagementNodeSize -DisksPerWorkerNode $disksPerWorkerNode
```

### <span data-ttu-id="1c7a5-119">Пример 8. Создание кластера Azure HDInsight с хранилищем Azure Data Lake Gen2.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-119">Example 8: Create an Azure HDInsight cluster with Azure Data Lake Gen2 storage.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageManagedIdentity = "yourstorageusermanagedidentity"
        $storageFileSystem = "filesystem01"
        $storageAccountType=AzureDataLakeStorageGen2

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
            -ClusterSizeInNodes 3 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountManagedIdentity $storageManagedIdentity `
            -StorageFileSystem $storageFileSystem `
            -StorageAccountType $storageAccountType `
            -SshCredential $clusterCreds
```

### <span data-ttu-id="1c7a5-120">Пример 9. Создание кластера Azure HDInsight с пакетом enterprise Security Package(ESP) и enable HDInsight ID Broker.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-120">Example 9: Create an Azure HDInsight cluster with Enterprise Security Package(ESP) and Enable HDInsight ID Broker.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountKey = "yourstorageaccountaccesskey"
        $storageContainer = "yourcontainer01"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # ESP configuration
        $domainResourceId = "your Azure AD Domin Service resource id"
        $domainUser = "yourdomainuser"
        $domainPassword = "yourdoaminpasswd"
        $domainPassword = ConvertTo-SecureString $domainPassword -AsPlainText -Force
        $domainCredential = New-Object System.Management.Automation.PSCredential($domainUser, $domainPassword)
        $clusterUserGroupDns = "dominusergroup"
        $ldapUrls = "ldaps://{your domain name}:636"

        $clusterTier = Premium
        $vnetId = "yourvnetid"
        $subnetName = "yoursubnetname"
        $assignedIdentity = "your user managed assigned identity resourcee id"

        #Create security profile
        $config= New-AzHDInsightClusterConfig|Add-AzHDInsightSecurityProfile -DomainResourceId $domainResourceId -DomainUserCredential $domainCredential -LdapsUrls $ldapUrls -ClusterUsersGroupDNs $clusterUserGroupDns

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusteTier $clusterTier `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 3 `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -VirtualNetworkId $vnetId -SubnetName $subnetName `
            -AssignedIdentity $assignedIdentity `
            -SecurityProfile $config.SecurityProfile -EnableIDBroker
```

### <span data-ttu-id="1c7a5-121">Пример 10. Создание кластера Azure HDInsight, который обеспечивает изоляцию компьютера.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-121">Example 10: Create an Azure HDInsight cluster which enables compute isolation.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
        $storageAccountName = "yourstorageacct001"
        $storageAccountKey = Get-AzStorageAccountKey `
            -ResourceGroupName $storageAccountResourceGroupName `
            -Name $storageAccountName | Where-Object {$_.KeyName -eq "key1"} | %{$_.Value}
        $storageContainer = "container002"

        # Cluster configuration info
        $location = "East US 2"
        $clusterResourceGroupName = "Group"
        $clusterName = "your-hadoop-002"
        $clusterCreds = Get-Credential
        $workerNodeSize="Standard_E16S_V3" # here is just an example
        $headNodeSize="Standard_E8S_V3"
        $zookeeperNodeSize="Standard_E2S_V3"

        # If the cluster's resource group doesn't exist yet, run:
        # New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

        # Create the cluster
        New-AzHDInsightCluster `
            -ClusterType Hadoop `
            -ClusterSizeInNodes 4 `
            -WorkerNodeSize $workerNodeSize `
            -HeadNodeSize $headNodeSize `
            -ZookeeperNodeSize $zookeeperNodeSize `
            -ResourceGroupName $clusterResourceGroupName `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds `
            -Location $location `
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EnableComputeIsolation `
```

## <span data-ttu-id="1c7a5-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c7a5-122">PARAMETERS</span></span>

### <span data-ttu-id="1c7a5-123">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="1c7a5-123">-AadTenantId</span></span>
<span data-ttu-id="1c7a5-124">Определяет ИД клиента Azure AD, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-124">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="1c7a5-125">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="1c7a5-125">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="1c7a5-126">Указывает дополнительные учетные записи хранилища Azure для кластера.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-126">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="1c7a5-127">Вы также можете использовать Add-AzHDInsightStorage управления.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-127">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="1c7a5-128">-AmbariDatabase</span><span class="sxs-lookup"><span data-stu-id="1c7a5-128">-AmbariDatabase</span></span>
<span data-ttu-id="1c7a5-129">Получает или задает базу данных для амгари.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-129">Gets or sets the database for ambari.</span></span>

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

### <span data-ttu-id="1c7a5-130">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="1c7a5-130">-ApplicationId</span></span>
<span data-ttu-id="1c7a5-131">Получает или задает ИД приложения-основной службы для доступа к Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-131">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="1c7a5-132">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="1c7a5-132">-AssignedIdentity</span></span>
<span data-ttu-id="1c7a5-133">Возвращает или устанавливает назначенное удостоверение.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-133">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="1c7a5-134">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c7a5-134">-AutoscaleConfiguration</span></span>
<span data-ttu-id="1c7a5-135">Получает или устанавливает конфигурацию автомасштаби</span><span class="sxs-lookup"><span data-stu-id="1c7a5-135">Gets or sets the autoscale configuration</span></span>

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

### <span data-ttu-id="1c7a5-136">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="1c7a5-136">-CertificateFileContents</span></span>
<span data-ttu-id="1c7a5-137">Определяет содержимое файла сертификата, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-137">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="1c7a5-138">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="1c7a5-138">-CertificateFilePath</span></span>
<span data-ttu-id="1c7a5-139">Путь к сертификату, который будет использоваться для проверки подлинности в качестве директора-службы.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-139">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="1c7a5-140">Кластер будет использовать его при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-140">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="1c7a5-141">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="1c7a5-141">-CertificatePassword</span></span>
<span data-ttu-id="1c7a5-142">Пароль сертификата, который будет использоваться для проверки подлинности в качестве директора-службы.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-142">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="1c7a5-143">Кластер будет использовать его при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-143">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="1c7a5-144">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1c7a5-144">-ClusterName</span></span>
<span data-ttu-id="1c7a5-145">Название кластера.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-145">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="1c7a5-146">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="1c7a5-146">-ClusterSizeInNodes</span></span>
<span data-ttu-id="1c7a5-147">Количество узлов рабочих групп.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-147">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="1c7a5-148">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="1c7a5-148">-ClusterTier</span></span>
<span data-ttu-id="1c7a5-149">Определяет уровень кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-149">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="1c7a5-150">По умолчанию этот стандарт.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-150">By default, this is Standard.</span></span>
<span data-ttu-id="1c7a5-151">Уровень Premium можно использовать только с кластерами Linux, и он позволяет использовать некоторые новые функции.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-151">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="1c7a5-152">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="1c7a5-152">-ClusterType</span></span>
<span data-ttu-id="1c7a5-153">Тип кластера, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-153">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="1c7a5-154">Доступны такие варианты: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka и RServer</span><span class="sxs-lookup"><span data-stu-id="1c7a5-154">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

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

### <span data-ttu-id="1c7a5-155">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="1c7a5-155">-ComponentVersion</span></span>
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

### <span data-ttu-id="1c7a5-156">-ComputeIsolationHostSku</span><span class="sxs-lookup"><span data-stu-id="1c7a5-156">-ComputeIsolationHostSku</span></span>
<span data-ttu-id="1c7a5-157">Получает или задает sku выделенных хостов для вычисления изоляции.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-157">Gets or sets the dedicated host sku for compute isolation.</span></span>

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

### <span data-ttu-id="1c7a5-158">-Config</span><span class="sxs-lookup"><span data-stu-id="1c7a5-158">-Config</span></span>
<span data-ttu-id="1c7a5-159">Определяет объект кластера, который будет использоваться для создания кластера.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-159">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="1c7a5-160">Этот объект можно создать с помощью New-AzHDInsightClusterConfig..</span><span class="sxs-lookup"><span data-stu-id="1c7a5-160">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="1c7a5-161">-Configurations</span><span class="sxs-lookup"><span data-stu-id="1c7a5-161">-Configurations</span></span>
<span data-ttu-id="1c7a5-162">Определяет конфигурацию этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-162">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="1c7a5-163">Вы также можете использовать Add-AzHDInsightConfigValues управления.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-163">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="1c7a5-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c7a5-164">-DefaultProfile</span></span>
<span data-ttu-id="1c7a5-165">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1c7a5-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1c7a5-166">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="1c7a5-166">-DisksPerWorkerNode</span></span>
<span data-ttu-id="1c7a5-167">Количество дисков для роли узла рабочего узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-167">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="1c7a5-168">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="1c7a5-168">-EdgeNodeSize</span></span>
<span data-ttu-id="1c7a5-169">Определяет размер виртуальной машины для узла границы.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-169">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="1c7a5-170">Используйте Get-AzVMSize для допустимых размеров VM и см. страницу цен HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-170">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="1c7a5-171">Этот параметр действителен только для кластеров RServer.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-171">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="1c7a5-172">-EnableComputeIsolation</span><span class="sxs-lookup"><span data-stu-id="1c7a5-172">-EnableComputeIsolation</span></span>
<span data-ttu-id="1c7a5-173">Позволяет вычислить изоляцию через HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-173">Enables HDInsight compute isolation feature.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c7a5-174">-EnableIDBroker</span><span class="sxs-lookup"><span data-stu-id="1c7a5-174">-EnableIDBroker</span></span>
<span data-ttu-id="1c7a5-175">Включает функцию брокеров удостоверений HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-175">Enables HDInsight Identity Broker feature.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c7a5-176">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="1c7a5-176">-EncryptionAlgorithm</span></span>
<span data-ttu-id="1c7a5-177">Получает или задает алгоритм шифрования.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-177">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="1c7a5-178">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="1c7a5-178">-EncryptionAtHost</span></span>
<span data-ttu-id="1c7a5-179">Получает или устанавливает флажок, который указывает на то, следует ли включить шифрование на хосте.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-179">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="1c7a5-180">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="1c7a5-180">-EncryptionInTransit</span></span>
<span data-ttu-id="1c7a5-181">Получает или устанавливает флажок, который указывает, следует ли включить шифрование при переходе.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-181">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="1c7a5-182">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="1c7a5-182">-EncryptionKeyName</span></span>
<span data-ttu-id="1c7a5-183">Возвращает или задает имя ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-183">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="1c7a5-184">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="1c7a5-184">-EncryptionKeyVersion</span></span>
<span data-ttu-id="1c7a5-185">Возвращает или задает версию ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-185">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="1c7a5-186">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="1c7a5-186">-EncryptionVaultUri</span></span>
<span data-ttu-id="1c7a5-187">Получает или задает uri хранилища шифрования.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-187">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="1c7a5-188">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="1c7a5-188">-HeadNodeSize</span></span>
<span data-ttu-id="1c7a5-189">Определяет размер виртуальной машины для узла head.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-189">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="1c7a5-190">Используйте Get-AzVMSize для допустимых размеров VM и см. страницу цен HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-190">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="1c7a5-191">-Вельмеха</span><span class="sxs-lookup"><span data-stu-id="1c7a5-191">-HiveMetastore</span></span>
<span data-ttu-id="1c7a5-192">Указывает, SQL базы данных, в которой хранятся метаданные "Вирус".</span><span class="sxs-lookup"><span data-stu-id="1c7a5-192">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="1c7a5-193">Вы также можете использовать Add-AzHDInsightMetastore управления.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-193">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="1c7a5-194">-httpCredential</span><span class="sxs-lookup"><span data-stu-id="1c7a5-194">-HttpCredential</span></span>
<span data-ttu-id="1c7a5-195">Определяет учетные данные для входа в кластер (HTTP).</span><span class="sxs-lookup"><span data-stu-id="1c7a5-195">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="1c7a5-196">-KafkaClientGroupId</span><span class="sxs-lookup"><span data-stu-id="1c7a5-196">-KafkaClientGroupId</span></span>
<span data-ttu-id="1c7a5-197">Получает или задает id группы клиентов для прокси-доступа к Rest Kafka.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-197">Gets or sets the client group id for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="1c7a5-198">-KafkaClientGroupName</span><span class="sxs-lookup"><span data-stu-id="1c7a5-198">-KafkaClientGroupName</span></span>
<span data-ttu-id="1c7a5-199">Получает или задает имя группы клиентов для прокси-сервера Kafka.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-199">Gets or sets the client group name for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="1c7a5-200">-KafkaManagementNodeSize</span><span class="sxs-lookup"><span data-stu-id="1c7a5-200">-KafkaManagementNodeSize</span></span>
<span data-ttu-id="1c7a5-201">Получает или задает размер узла управления Kafka.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-201">Gets or sets the size of the Kafka Management Node.</span></span>

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

### <span data-ttu-id="1c7a5-202">-Location</span><span class="sxs-lookup"><span data-stu-id="1c7a5-202">-Location</span></span>
<span data-ttu-id="1c7a5-203">Определяет расположение кластера.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-203">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="1c7a5-204">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="1c7a5-204">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="1c7a5-205">Получает или устанавливает минимальную поддерживаемую версию TLS.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-205">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="1c7a5-206">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="1c7a5-206">-ObjectId</span></span>
<span data-ttu-id="1c7a5-207">Определяет ИД объекта Azure AD (GUID) основной службы Azure AD, представляют кластер.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-207">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="1c7a5-208">Кластер будет использовать его при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-208">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="1c7a5-209">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="1c7a5-209">-OozieMetastore</span></span>
<span data-ttu-id="1c7a5-210">Указывает базу SQL, в которой хранятся метаданные Oozie.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-210">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="1c7a5-211">Вы также можете использовать Add-AzHDInsightMetastore управления.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-211">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="1c7a5-212">-OSType</span><span class="sxs-lookup"><span data-stu-id="1c7a5-212">-OSType</span></span>
<span data-ttu-id="1c7a5-213">Указывает операционную систему для кластера.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-213">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="1c7a5-214">Возможные варианты: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="1c7a5-214">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="1c7a5-215">-PrivateLink</span><span class="sxs-lookup"><span data-stu-id="1c7a5-215">-PrivateLink</span></span>
<span data-ttu-id="1c7a5-216">Возвращает или устанавливает частный тип ссылки.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-216">Gets or sets the private link type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c7a5-217">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="1c7a5-217">-RdpAccessExpiry</span></span>
<span data-ttu-id="1c7a5-218">Указывает срок действия в качестве объекта даты и времени для доступа к кластеру протокола удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-218">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="1c7a5-219">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="1c7a5-219">-RdpCredential</span></span>
<span data-ttu-id="1c7a5-220">Определяет учетные данные удаленного рабочего стола (RDP) для кластера.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-220">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="1c7a5-221">Это касается только кластеров Windows.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-221">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="1c7a5-222">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c7a5-222">-ResourceGroupName</span></span>
<span data-ttu-id="1c7a5-223">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-223">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="1c7a5-224">-ResourceProviderConnection</span><span class="sxs-lookup"><span data-stu-id="1c7a5-224">-ResourceProviderConnection</span></span>
<span data-ttu-id="1c7a5-225">Возвращает или устанавливает тип подключения к поставщику ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-225">Gets or sets the resource provider connection type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Inbound, Outbound

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c7a5-226">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="1c7a5-226">-ScriptActions</span></span>
<span data-ttu-id="1c7a5-227">Определяет действия сценария, которые будут запускаться на кластере в конце создания кластера.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-227">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="1c7a5-228">Вы также можете использовать Add-AzHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-228">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="1c7a5-229">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="1c7a5-229">-SecurityProfile</span></span>
<span data-ttu-id="1c7a5-230">Определяет свойства безопасности, связанные с созданием защищенного кластера.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-230">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="1c7a5-231">Вы также можете использовать Add-AzHDInsightSecurityProfile управления.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-231">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="1c7a5-232">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="1c7a5-232">-SshCredential</span></span>
<span data-ttu-id="1c7a5-233">Определяет учетные данные SSH, которые будут использоваться для подключений SSH.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-233">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="1c7a5-234">Это касается только кластеров Linux.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-234">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="1c7a5-235">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="1c7a5-235">-SshPublicKey</span></span>
<span data-ttu-id="1c7a5-236">Указывает открытый ключ, который будет использоваться для подключений SSH.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-236">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="1c7a5-237">Это касается только кластеров Linux.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-237">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="1c7a5-238">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="1c7a5-238">-StorageAccountKey</span></span>
<span data-ttu-id="1c7a5-239">Получает или задает ключ доступа к учетной записи хранения для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-239">Gets or sets the Storage Account Access Key for the Storage Account.</span></span>

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

### <span data-ttu-id="1c7a5-240">-StorageAccountManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="1c7a5-240">-StorageAccountManagedIdentity</span></span>
<span data-ttu-id="1c7a5-241">Возвращает или устанавливает управляемое удостоверение учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-241">Gets or sets the storage account managed identity.</span></span>

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

### <span data-ttu-id="1c7a5-242">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="1c7a5-242">-StorageAccountResourceId</span></span>
<span data-ttu-id="1c7a5-243">Получает или задает ИД ресурса хранилища для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-243">Gets or sets the Storage Resource Id for the Storage Account.</span></span>

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

### <span data-ttu-id="1c7a5-244">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="1c7a5-244">-StorageAccountType</span></span>
<span data-ttu-id="1c7a5-245">Возвращает или задает тип учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-245">Gets or sets the type of the storage account.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore, AzureDataLakeStorageGen2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c7a5-246">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="1c7a5-246">-StorageContainer</span></span>
<span data-ttu-id="1c7a5-247">Получает или задает имя storageContainer для учетной записи хранилища Azure по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-247">Gets or sets the StorageContainer name for the default Azure Storage Account</span></span>

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

### <span data-ttu-id="1c7a5-248">-StorageFileSystem</span><span class="sxs-lookup"><span data-stu-id="1c7a5-248">-StorageFileSystem</span></span>
<span data-ttu-id="1c7a5-249">Получает или задает файловую систему для учетной записи Azure Data Lake Storage Gen2 по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-249">Gets or sets the file system for the default Azure Data Lake Storage Gen2 account.</span></span>

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

### <span data-ttu-id="1c7a5-250">-StorageRootPath</span><span class="sxs-lookup"><span data-stu-id="1c7a5-250">-StorageRootPath</span></span>
<span data-ttu-id="1c7a5-251">Возвращает или задает путь к корню кластера в учетной записи для банка данных по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-251">Gets or sets the path to the root of the cluster in the default Data Lake Store Account.</span></span>

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

### <span data-ttu-id="1c7a5-252">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="1c7a5-252">-SubnetName</span></span>
<span data-ttu-id="1c7a5-253">Получает или задает имя подсети для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-253">Gets or sets the subnet name for this HDInsight cluster.</span></span>

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

### <span data-ttu-id="1c7a5-254">-Version</span><span class="sxs-lookup"><span data-stu-id="1c7a5-254">-Version</span></span>
<span data-ttu-id="1c7a5-255">Указывает версию HDI кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-255">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="1c7a5-256">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="1c7a5-256">-VirtualNetworkId</span></span>
<span data-ttu-id="1c7a5-257">Определяет ИД виртуальной сети, в которую нужно подавь кластер.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-257">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="1c7a5-258">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="1c7a5-258">-WorkerNodeSize</span></span>
<span data-ttu-id="1c7a5-259">Определяет размер виртуальной машины для узла "Работник".</span><span class="sxs-lookup"><span data-stu-id="1c7a5-259">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="1c7a5-260">Используйте Get-AzVMSize для допустимых размеров VM и см. страницу цен HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-260">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="1c7a5-261">-KeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="1c7a5-261">-ZookeeperNodeSize</span></span>
<span data-ttu-id="1c7a5-262">Определяет размер виртуальной машины для узлаKeeper.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-262">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="1c7a5-263">Используйте Get-AzVMSize для допустимых размеров VM и см. страницу цен HDInsight.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-263">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="1c7a5-264">Этот параметр действителен только для кластеров HBase или Storm.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-264">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="1c7a5-265">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c7a5-265">CommonParameters</span></span>
<span data-ttu-id="1c7a5-266">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c7a5-266">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c7a5-267">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c7a5-267">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c7a5-268">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1c7a5-268">INPUTS</span></span>

### <span data-ttu-id="1c7a5-269">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="1c7a5-269">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="1c7a5-270">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1c7a5-270">OUTPUTS</span></span>

### <span data-ttu-id="1c7a5-271">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="1c7a5-271">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="1c7a5-272">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1c7a5-272">NOTES</span></span>
<span data-ttu-id="1c7a5-273">Ключевые слова: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span><span class="sxs-lookup"><span data-stu-id="1c7a5-273">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="1c7a5-274">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1c7a5-274">RELATED LINKS</span></span>

[<span data-ttu-id="1c7a5-275">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="1c7a5-275">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

