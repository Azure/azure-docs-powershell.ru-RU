---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: f4592a371e528c7779e07251bf79677dac47e6df
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323361"
---
# <span data-ttu-id="2d7f0-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="2d7f0-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="2d7f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d7f0-102">SYNOPSIS</span></span>
<span data-ttu-id="2d7f0-103">Создает кластер Azure HDInsight в указанной группе ресурсов для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="2d7f0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2d7f0-104">SYNTAX</span></span>

### <span data-ttu-id="2d7f0-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2d7f0-105">Default (Default)</span></span>
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
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d7f0-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="2d7f0-106">CertificateFilePath</span></span>
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
 [-PrivateLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d7f0-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="2d7f0-107">CertificateFileContents</span></span>
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
 [-PrivateLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d7f0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d7f0-108">DESCRIPTION</span></span>
<span data-ttu-id="2d7f0-109">Служба New-AzHDInsightCluster создает кластер Azure HDInsight с использованием указанных параметров или объекта конфигурации, созданного с помощью New-AzHDInsightClusterConfig управления.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="2d7f0-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2d7f0-110">EXAMPLES</span></span>

### <span data-ttu-id="2d7f0-111">Пример 1. Создание кластера Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="2d7f0-111">Example 1: Create an Azure HDInsight cluster</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
```

<span data-ttu-id="2d7f0-112">Эта команда создает кластер в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-112">This command creates a cluster in the current subscription.</span></span>

### <span data-ttu-id="2d7f0-113">Пример 2. Создание кластера с шифрованием дисков под управлением клиента</span><span class="sxs-lookup"><span data-stu-id="2d7f0-113">Example 2: Create cluster with customer-managed key disk encryption</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AssignedIdentity $assignedIdentity `
            -EncryptionKeyName $encryptionKeyName `
            -EncryptionVaultUri $encryptionVaultUri `
            -EncryptionKeyVersion $encryptionKeyVersion
```

### <span data-ttu-id="2d7f0-114">Пример 3. Создание кластера Azure HDInsight, который обеспечивает шифрование при переходе</span><span class="sxs-lookup"><span data-stu-id="2d7f0-114">Example 3: Create an Azure HDInsight cluster which enables encryption in transit</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionInTransit $true `
```

### <span data-ttu-id="2d7f0-115">Пример 4. Создание кластера Azure HDInsight с функцией ретрансляции исходящие и частные ссылки</span><span class="sxs-lookup"><span data-stu-id="2d7f0-115">Example 4: Create an Azure HDInsight cluster with relay outbound and private link feature</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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

### <span data-ttu-id="2d7f0-116">Пример 5. Создание кластера Azure HDInsight, который обеспечивает шифрование на хосте</span><span class="sxs-lookup"><span data-stu-id="2d7f0-116">Example 5: Create an Azure HDInsight cluster which enables encryption at host</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -EncryptionAtHost $true `
```

### <span data-ttu-id="2d7f0-117">Пример 6. Создание кластера Azure HDInsight, который обеспечивает автоматическую шкалу.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-117">Example 6: Create an Azure HDInsight cluster which enables autoscale.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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
            -StorageAccountResourceId $storageAccountResourceId `
            -StorageAccountKey $storageAccountKey `
            -StorageContainer $storageContainer `
            -SshCredential $clusterCreds `
            -AutoscaleConfiguration $autoscaleConfiguration
```

### <span data-ttu-id="2d7f0-118">Пример 7. Создание кластера Azure HDInsight с прокси-сервером rest Kafka.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-118">Example 7: Create an Azure HDInsight cluster with Kafka Rest Proxy.</span></span>
```
PS C:\&gt; # Primary storage account info
        $storageAccountResourceGroupName = "Group"
        $storageAccountResourceId = "yourstorageaccountresourceid"
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

### <span data-ttu-id="2d7f0-119">Пример 8. Создание кластера Azure HDInsight с хранилищем Azure Data Lake Gen2.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-119">Example 8: Create an Azure HDInsight cluster with Azure Data Lake Gen2 storage.</span></span>
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

### <span data-ttu-id="2d7f0-120">Пример 9. Создание кластера Azure HDInsight с пакетом enterprise Security Package(ESP) и enable HDInsight ID Broker.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-120">Example 9: Create an Azure HDInsight cluster with Enterprise Security Package(ESP) and Enable HDInsight ID Broker.</span></span>
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

## <span data-ttu-id="2d7f0-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d7f0-121">PARAMETERS</span></span>

### <span data-ttu-id="2d7f0-122">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="2d7f0-122">-AadTenantId</span></span>
<span data-ttu-id="2d7f0-123">Определяет ИД клиента Azure AD, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-123">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="2d7f0-124">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="2d7f0-124">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="2d7f0-125">Указывает дополнительные учетные записи хранилища Azure для кластера.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-125">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="2d7f0-126">Вы также можете использовать Add-AzHDInsightStorage управления.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-126">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="2d7f0-127">-AmbariDatabase</span><span class="sxs-lookup"><span data-stu-id="2d7f0-127">-AmbariDatabase</span></span>
<span data-ttu-id="2d7f0-128">Возвращает или задает базу данных для амгари.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-128">Gets or sets the database for ambari.</span></span>

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

### <span data-ttu-id="2d7f0-129">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="2d7f0-129">-ApplicationId</span></span>
<span data-ttu-id="2d7f0-130">Получает или задает ИД приложения -службы для доступа к Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-130">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="2d7f0-131">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="2d7f0-131">-AssignedIdentity</span></span>
<span data-ttu-id="2d7f0-132">Возвращает или устанавливает назначенное удостоверение.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-132">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="2d7f0-133">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="2d7f0-133">-AutoscaleConfiguration</span></span>
<span data-ttu-id="2d7f0-134">Получает или устанавливает конфигурацию автомасштаби</span><span class="sxs-lookup"><span data-stu-id="2d7f0-134">Gets or sets the autoscale configuration</span></span>

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

### <span data-ttu-id="2d7f0-135">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="2d7f0-135">-CertificateFileContents</span></span>
<span data-ttu-id="2d7f0-136">Определяет содержимое файла сертификата, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-136">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="2d7f0-137">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="2d7f0-137">-CertificateFilePath</span></span>
<span data-ttu-id="2d7f0-138">Путь к сертификату, который будет использоваться для проверки подлинности в качестве директора-службы.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-138">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="2d7f0-139">Кластер будет использовать его при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-139">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="2d7f0-140">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="2d7f0-140">-CertificatePassword</span></span>
<span data-ttu-id="2d7f0-141">Пароль сертификата, который будет использоваться для проверки подлинности в качестве директора-службы.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-141">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="2d7f0-142">Кластер будет использовать его при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-142">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="2d7f0-143">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2d7f0-143">-ClusterName</span></span>
<span data-ttu-id="2d7f0-144">Название кластера.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-144">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="2d7f0-145">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="2d7f0-145">-ClusterSizeInNodes</span></span>
<span data-ttu-id="2d7f0-146">Количество узлов рабочих групп.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-146">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="2d7f0-147">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="2d7f0-147">-ClusterTier</span></span>
<span data-ttu-id="2d7f0-148">Определяет уровень кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-148">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="2d7f0-149">По умолчанию этот стандарт.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-149">By default, this is Standard.</span></span>
<span data-ttu-id="2d7f0-150">Уровень Premium можно использовать только с кластерами Linux, и он позволяет использовать некоторые новые функции.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-150">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="2d7f0-151">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="2d7f0-151">-ClusterType</span></span>
<span data-ttu-id="2d7f0-152">Тип кластера, который нужно создать.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-152">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="2d7f0-153">Доступны такие варианты: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka и RServer</span><span class="sxs-lookup"><span data-stu-id="2d7f0-153">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

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

### <span data-ttu-id="2d7f0-154">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="2d7f0-154">-ComponentVersion</span></span>
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

### <span data-ttu-id="2d7f0-155">-Config</span><span class="sxs-lookup"><span data-stu-id="2d7f0-155">-Config</span></span>
<span data-ttu-id="2d7f0-156">Определяет объект кластера, который будет использоваться для создания кластера.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-156">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="2d7f0-157">Этот объект можно создать с помощью New-AzHDInsightClusterConfig..</span><span class="sxs-lookup"><span data-stu-id="2d7f0-157">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="2d7f0-158">-Configurations</span><span class="sxs-lookup"><span data-stu-id="2d7f0-158">-Configurations</span></span>
<span data-ttu-id="2d7f0-159">Определяет конфигурацию этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-159">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="2d7f0-160">Вы также можете использовать Add-AzHDInsightConfigValues управления.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-160">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="2d7f0-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d7f0-161">-DefaultProfile</span></span>
<span data-ttu-id="2d7f0-162">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2d7f0-162">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d7f0-163">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="2d7f0-163">-DisksPerWorkerNode</span></span>
<span data-ttu-id="2d7f0-164">Количество дисков для роли узла рабочего узла в кластере.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-164">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="2d7f0-165">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="2d7f0-165">-EdgeNodeSize</span></span>
<span data-ttu-id="2d7f0-166">Определяет размер виртуальной машины для узла границы.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-166">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="2d7f0-167">Используйте Get-AzVMSize для допустимых размеров VM и см. страницу цен HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-167">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="2d7f0-168">Этот параметр действителен только для кластеров RServer.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-168">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="2d7f0-169">-EnableIDBroker</span><span class="sxs-lookup"><span data-stu-id="2d7f0-169">-EnableIDBroker</span></span>
<span data-ttu-id="2d7f0-170">Включает функцию брокеров удостоверений HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-170">Enables HDInsight Identity Broker feature.</span></span>

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

### <span data-ttu-id="2d7f0-171">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="2d7f0-171">-EncryptionAlgorithm</span></span>
<span data-ttu-id="2d7f0-172">Получает или задает алгоритм шифрования.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-172">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="2d7f0-173">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="2d7f0-173">-EncryptionAtHost</span></span>
<span data-ttu-id="2d7f0-174">Получает или устанавливает флажок, который указывает на то, следует ли включить шифрование на хосте.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-174">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="2d7f0-175">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="2d7f0-175">-EncryptionInTransit</span></span>
<span data-ttu-id="2d7f0-176">Получает или устанавливает флажок, который указывает, следует ли включить шифрование при переходе.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-176">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="2d7f0-177">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="2d7f0-177">-EncryptionKeyName</span></span>
<span data-ttu-id="2d7f0-178">Получает или задает имя ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-178">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="2d7f0-179">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="2d7f0-179">-EncryptionKeyVersion</span></span>
<span data-ttu-id="2d7f0-180">Возвращает или задает версию ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-180">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="2d7f0-181">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="2d7f0-181">-EncryptionVaultUri</span></span>
<span data-ttu-id="2d7f0-182">Получает или задает uri хранилища шифрования.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-182">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="2d7f0-183">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="2d7f0-183">-HeadNodeSize</span></span>
<span data-ttu-id="2d7f0-184">Определяет размер виртуальной машины для узла head.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-184">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="2d7f0-185">Используйте Get-AzVMSize для допустимых размеров VM и см. страницу цен HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-185">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="2d7f0-186">-Вельмеха</span><span class="sxs-lookup"><span data-stu-id="2d7f0-186">-HiveMetastore</span></span>
<span data-ttu-id="2d7f0-187">Указывает, SQL базы данных, в которой хранятся метаданные "Вирус".</span><span class="sxs-lookup"><span data-stu-id="2d7f0-187">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="2d7f0-188">Вы также можете использовать Add-AzHDInsightMetastore управления.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-188">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="2d7f0-189">-httpCredential</span><span class="sxs-lookup"><span data-stu-id="2d7f0-189">-HttpCredential</span></span>
<span data-ttu-id="2d7f0-190">Определяет учетные данные для входа в кластер (HTTP).</span><span class="sxs-lookup"><span data-stu-id="2d7f0-190">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="2d7f0-191">-KafkaClientGroupId</span><span class="sxs-lookup"><span data-stu-id="2d7f0-191">-KafkaClientGroupId</span></span>
<span data-ttu-id="2d7f0-192">Получает или задает id группы клиентов для прокси-доступа к Rest Kafka.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-192">Gets or sets the client group id for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="2d7f0-193">-KafkaClientGroupName</span><span class="sxs-lookup"><span data-stu-id="2d7f0-193">-KafkaClientGroupName</span></span>
<span data-ttu-id="2d7f0-194">Получает или задает имя группы клиентов для прокси-сервера Kafka.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-194">Gets or sets the client group name for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="2d7f0-195">-KafkaManagementNodeSize</span><span class="sxs-lookup"><span data-stu-id="2d7f0-195">-KafkaManagementNodeSize</span></span>
<span data-ttu-id="2d7f0-196">Получает или задает размер узла управления Kafka.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-196">Gets or sets the size of the Kafka Management Node.</span></span>

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

### <span data-ttu-id="2d7f0-197">-Location</span><span class="sxs-lookup"><span data-stu-id="2d7f0-197">-Location</span></span>
<span data-ttu-id="2d7f0-198">Определяет расположение кластера.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-198">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="2d7f0-199">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="2d7f0-199">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="2d7f0-200">Получает или устанавливает минимальную поддерживаемую версию TLS.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-200">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="2d7f0-201">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="2d7f0-201">-ObjectId</span></span>
<span data-ttu-id="2d7f0-202">Определяет ИД объекта Azure AD (GUID) основной службы Azure AD, представляют кластер.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-202">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="2d7f0-203">Кластер будет использовать его при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-203">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="2d7f0-204">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="2d7f0-204">-OozieMetastore</span></span>
<span data-ttu-id="2d7f0-205">Указывает базу SQL, в которой хранятся метаданные Oozie.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-205">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="2d7f0-206">Вы также можете использовать Add-AzHDInsightMetastore управления.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-206">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="2d7f0-207">-OSType</span><span class="sxs-lookup"><span data-stu-id="2d7f0-207">-OSType</span></span>
<span data-ttu-id="2d7f0-208">Указывает операционную систему для кластера.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-208">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="2d7f0-209">Возможные варианты: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="2d7f0-209">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="2d7f0-210">-PrivateLink</span><span class="sxs-lookup"><span data-stu-id="2d7f0-210">-PrivateLink</span></span>
<span data-ttu-id="2d7f0-211">Возвращает или устанавливает частный тип ссылки.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-211">Gets or sets the private link type.</span></span>

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

### <span data-ttu-id="2d7f0-212">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="2d7f0-212">-RdpAccessExpiry</span></span>
<span data-ttu-id="2d7f0-213">Указывает срок действия в качестве объекта даты и времени для доступа к кластеру протокола удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-213">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="2d7f0-214">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="2d7f0-214">-RdpCredential</span></span>
<span data-ttu-id="2d7f0-215">Определяет учетные данные удаленного рабочего стола (RDP) для кластера.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-215">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="2d7f0-216">Это касается только кластеров Windows.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-216">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="2d7f0-217">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d7f0-217">-ResourceGroupName</span></span>
<span data-ttu-id="2d7f0-218">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-218">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="2d7f0-219">-ResourceProviderConnection</span><span class="sxs-lookup"><span data-stu-id="2d7f0-219">-ResourceProviderConnection</span></span>
<span data-ttu-id="2d7f0-220">Возвращает или устанавливает тип подключения к поставщику ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-220">Gets or sets the resource provider connection type.</span></span>

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

### <span data-ttu-id="2d7f0-221">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="2d7f0-221">-ScriptActions</span></span>
<span data-ttu-id="2d7f0-222">Определяет действия сценария, которые будут запускаться на кластере в конце создания кластера.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-222">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="2d7f0-223">Вы также можете использовать Add-AzHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-223">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="2d7f0-224">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="2d7f0-224">-SecurityProfile</span></span>
<span data-ttu-id="2d7f0-225">Определяет свойства безопасности, связанные с созданием защищенного кластера.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-225">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="2d7f0-226">Вы также можете использовать Add-AzHDInsightSecurityProfile управления.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-226">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="2d7f0-227">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="2d7f0-227">-SshCredential</span></span>
<span data-ttu-id="2d7f0-228">Определяет учетные данные SSH, которые будут использоваться для подключений SSH.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-228">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="2d7f0-229">Это касается только кластеров Linux.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-229">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="2d7f0-230">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="2d7f0-230">-SshPublicKey</span></span>
<span data-ttu-id="2d7f0-231">Указывает открытый ключ, который будет использоваться для подключений SSH.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-231">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="2d7f0-232">Это касается только кластеров Linux.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-232">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="2d7f0-233">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="2d7f0-233">-StorageAccountKey</span></span>
<span data-ttu-id="2d7f0-234">Получает или задает ключ доступа к учетной записи хранения для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-234">Gets or sets the Storage Account Access Key for the Storage Account.</span></span>

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

### <span data-ttu-id="2d7f0-235">-StorageAccountManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="2d7f0-235">-StorageAccountManagedIdentity</span></span>
<span data-ttu-id="2d7f0-236">Возвращает или устанавливает управляемое удостоверение учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-236">Gets or sets the storage account managed identity.</span></span>

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

### <span data-ttu-id="2d7f0-237">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="2d7f0-237">-StorageAccountResourceId</span></span>
<span data-ttu-id="2d7f0-238">Возвращает или задает ИД ресурса хранилища для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-238">Gets or sets the Storage Resource Id for the Storage Account.</span></span>

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

### <span data-ttu-id="2d7f0-239">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="2d7f0-239">-StorageAccountType</span></span>
<span data-ttu-id="2d7f0-240">Возвращает или задает тип учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-240">Gets or sets the type of the storage account.</span></span>

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

### <span data-ttu-id="2d7f0-241">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="2d7f0-241">-StorageContainer</span></span>
<span data-ttu-id="2d7f0-242">Получает или задает имя storageContainer для учетной записи хранилища Azure по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-242">Gets or sets the StorageContainer name for the default Azure Storage Account</span></span>

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

### <span data-ttu-id="2d7f0-243">-StorageFileSystem</span><span class="sxs-lookup"><span data-stu-id="2d7f0-243">-StorageFileSystem</span></span>
<span data-ttu-id="2d7f0-244">Получает или задает файловую систему для учетной записи Azure Data Lake Storage Gen2 по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-244">Gets or sets the file system for the default Azure Data Lake Storage Gen2 account.</span></span>

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

### <span data-ttu-id="2d7f0-245">-StorageRootPath</span><span class="sxs-lookup"><span data-stu-id="2d7f0-245">-StorageRootPath</span></span>
<span data-ttu-id="2d7f0-246">Возвращает или задает путь к корню кластера в учетной записи для банка данных по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-246">Gets or sets the path to the root of the cluster in the default Data Lake Store Account.</span></span>

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

### <span data-ttu-id="2d7f0-247">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="2d7f0-247">-SubnetName</span></span>
<span data-ttu-id="2d7f0-248">Получает или задает имя подсети для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-248">Gets or sets the subnet name for this HDInsight cluster.</span></span>

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

### <span data-ttu-id="2d7f0-249">-Версия</span><span class="sxs-lookup"><span data-stu-id="2d7f0-249">-Version</span></span>
<span data-ttu-id="2d7f0-250">Указывает версию HDI кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-250">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="2d7f0-251">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="2d7f0-251">-VirtualNetworkId</span></span>
<span data-ttu-id="2d7f0-252">Определяет ИД виртуальной сети, в которую нужно подавь кластер.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-252">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="2d7f0-253">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="2d7f0-253">-WorkerNodeSize</span></span>
<span data-ttu-id="2d7f0-254">Определяет размер виртуальной машины для узла "Работник".</span><span class="sxs-lookup"><span data-stu-id="2d7f0-254">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="2d7f0-255">Используйте Get-AzVMSize для допустимых размеров VM и см. страницу цен HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-255">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="2d7f0-256">-KeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="2d7f0-256">-ZookeeperNodeSize</span></span>
<span data-ttu-id="2d7f0-257">Определяет размер виртуальной машины для узлаKeeper.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-257">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="2d7f0-258">Используйте Get-AzVMSize для допустимых размеров VM и см. страницу цен HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-258">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="2d7f0-259">Этот параметр действителен только для кластеров HBase или Storm.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-259">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="2d7f0-260">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d7f0-260">CommonParameters</span></span>
<span data-ttu-id="2d7f0-261">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d7f0-261">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d7f0-262">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d7f0-262">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d7f0-263">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2d7f0-263">INPUTS</span></span>

### <span data-ttu-id="2d7f0-264">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="2d7f0-264">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="2d7f0-265">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2d7f0-265">OUTPUTS</span></span>

### <span data-ttu-id="2d7f0-266">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="2d7f0-266">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="2d7f0-267">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2d7f0-267">NOTES</span></span>
<span data-ttu-id="2d7f0-268">Ключевые слова: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span><span class="sxs-lookup"><span data-stu-id="2d7f0-268">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="2d7f0-269">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d7f0-269">RELATED LINKS</span></span>

[<span data-ttu-id="2d7f0-270">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="2d7f0-270">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

