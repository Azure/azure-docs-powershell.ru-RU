---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 691AC991-3249-487C-A0DF-C579ED7D00E7
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightCluster.md
ms.openlocfilehash: b42b93bbecef5ec56495be632788bd1373ae9db1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245357"
---
# <span data-ttu-id="20fd7-101">New-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="20fd7-101">New-AzHDInsightCluster</span></span>

## <span data-ttu-id="20fd7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="20fd7-102">SYNOPSIS</span></span>
<span data-ttu-id="20fd7-103">Создает кластер HDInsight Azure в указанной группе ресурсов для текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="20fd7-103">Creates an Azure HDInsight cluster in the specified resource group for the current subscription.</span></span>

## <span data-ttu-id="20fd7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="20fd7-104">SYNTAX</span></span>

### <span data-ttu-id="20fd7-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="20fd7-105">Default (Default)</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
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
 [-KafkaClientGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20fd7-106">CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="20fd7-106">CertificateFilePath</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
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
 [-KafkaClientGroupId <String>] [-KafkaClientGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="20fd7-107">CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="20fd7-107">CertificateFileContents</span></span>
```
New-AzHDInsightCluster [-Location] <String> [-ResourceGroupName] <String> [-ClusterName] <String>
 [-ClusterSizeInNodes] <Int32> [-HttpCredential] <PSCredential> [[-StorageAccountResourceId] <String>]
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-Config <AzureHDInsightConfig>]
 [-OozieMetastore <AzureHDInsightMetastore>] [-HiveMetastore <AzureHDInsightMetastore>]
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
 [-KafkaClientGroupId <String>] [-KafkaClientGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="20fd7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="20fd7-108">DESCRIPTION</span></span>
<span data-ttu-id="20fd7-109">New-AzHDInsightCluster создает кластер HDInsight Azure, используя указанные параметры или объект конфигурации, созданный с помощью командлета New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="20fd7-109">The New-AzHDInsightCluster creates an Azure HDInsight cluster by using the specified parameters or by using a configuration object that is created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="20fd7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="20fd7-110">EXAMPLES</span></span>

### <span data-ttu-id="20fd7-111">Пример 1: Создание кластера HDInsight Azure</span><span class="sxs-lookup"><span data-stu-id="20fd7-111">Example 1: Create an Azure HDInsight cluster</span></span>
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

<span data-ttu-id="20fd7-112">Эта команда создает кластер в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="20fd7-112">This command creates a cluster in the current subscription.</span></span>

### <span data-ttu-id="20fd7-113">Пример 2: Создание кластера с помощью шифрования диска с управляемым пользователем ключом</span><span class="sxs-lookup"><span data-stu-id="20fd7-113">Example 2: Create cluster with customer-managed key disk encryption</span></span>
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

### <span data-ttu-id="20fd7-114">Пример 3: Создание кластера HDInsight Azure, который обеспечивает шифрование в пути</span><span class="sxs-lookup"><span data-stu-id="20fd7-114">Example 3: Create an Azure HDInsight cluster which enables encryption in transit</span></span>
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

### <span data-ttu-id="20fd7-115">Пример 4: Создание кластера HDInsight для Azure с помощью функции Private Link</span><span class="sxs-lookup"><span data-stu-id="20fd7-115">Example 4: Create an Azure HDInsight cluster with private link feature</span></span>
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
            -PublicNetworkAccessType OutboundOnly -OutboundPublicNetworkAccessType PublicLoadBalancer `
```

### <span data-ttu-id="20fd7-116">Пример 5: Создание кластера HDInsight Azure, который обеспечивает шифрование на узле</span><span class="sxs-lookup"><span data-stu-id="20fd7-116">Example 5: Create an Azure HDInsight cluster which enables encryption at host</span></span>
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

### <span data-ttu-id="20fd7-117">Пример 6: Создание кластера HDInsight Azure, который включает Автомасштабирование.</span><span class="sxs-lookup"><span data-stu-id="20fd7-117">Example 6: Create an Azure HDInsight cluster which enables autoscale.</span></span>
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

### <span data-ttu-id="20fd7-118">Пример 7: Создание кластера HDInsight Azure с помощью прокси-сервера Kafka RESTful.</span><span class="sxs-lookup"><span data-stu-id="20fd7-118">Example 7: Create an Azure HDInsight cluster with Kafka Rest Proxy.</span></span>
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

### <span data-ttu-id="20fd7-119">Пример 8: Создание кластера HDInsight Azure с хранилищем Azure Data Lake Gen2.</span><span class="sxs-lookup"><span data-stu-id="20fd7-119">Example 8: Create an Azure HDInsight cluster with Azure Data Lake Gen2 storage.</span></span>
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

### <span data-ttu-id="20fd7-120">Пример 9: Создание кластера HDInsight Azure с пакетом безопасности Enterprise (ESP) и включение брокера ИДЕНТИФИКАТОРов HDInsight.</span><span class="sxs-lookup"><span data-stu-id="20fd7-120">Example 9: Create an Azure HDInsight cluster with Enterprise Security Package(ESP) and Enable HDInsight ID Broker.</span></span>
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

## <span data-ttu-id="20fd7-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="20fd7-121">PARAMETERS</span></span>

### <span data-ttu-id="20fd7-122">-AadTenantId</span><span class="sxs-lookup"><span data-stu-id="20fd7-122">-AadTenantId</span></span>
<span data-ttu-id="20fd7-123">Указывает идентификатор клиента Azure AD, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="20fd7-123">Specifies the Azure AD Tenant ID that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="20fd7-124">-AdditionalStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="20fd7-124">-AdditionalStorageAccounts</span></span>
<span data-ttu-id="20fd7-125">Указывает дополнительные учетные записи хранилища Azure для кластера.</span><span class="sxs-lookup"><span data-stu-id="20fd7-125">Specifies the additional Azure Storage accounts for the cluster.</span></span>
<span data-ttu-id="20fd7-126">Вы также можете использовать командлет Add-AzHDInsightStorage.</span><span class="sxs-lookup"><span data-stu-id="20fd7-126">You can alternatively use the Add-AzHDInsightStorage cmdlet.</span></span>

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

### <span data-ttu-id="20fd7-127">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="20fd7-127">-ApplicationId</span></span>
<span data-ttu-id="20fd7-128">Возвращает или задает идентификатор приложения субъекта-службы для доступа к Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="20fd7-128">Gets or sets the Service Principal Application Id for accessing Azure Data Lake.</span></span>

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

### <span data-ttu-id="20fd7-129">-AssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="20fd7-129">-AssignedIdentity</span></span>
<span data-ttu-id="20fd7-130">Возвращает или задает назначенное удостоверение.</span><span class="sxs-lookup"><span data-stu-id="20fd7-130">Gets or sets the assigned identity.</span></span>

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

### <span data-ttu-id="20fd7-131">-AutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="20fd7-131">-AutoscaleConfiguration</span></span>
<span data-ttu-id="20fd7-132">Возвращает или задает конфигурацию автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="20fd7-132">Gets or sets the autoscale configuration</span></span>

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

### <span data-ttu-id="20fd7-133">-CertificateFileContents</span><span class="sxs-lookup"><span data-stu-id="20fd7-133">-CertificateFileContents</span></span>
<span data-ttu-id="20fd7-134">Указывает содержимое файла сертификата, который будет использоваться при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="20fd7-134">Specifies file contents of the certificate that will be used when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="20fd7-135">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="20fd7-135">-CertificateFilePath</span></span>
<span data-ttu-id="20fd7-136">Задает путь к файлу сертификата, который будет использоваться для проверки подлинности участника-службы.</span><span class="sxs-lookup"><span data-stu-id="20fd7-136">Specifies the file path to the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="20fd7-137">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="20fd7-137">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="20fd7-138">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="20fd7-138">-CertificatePassword</span></span>
<span data-ttu-id="20fd7-139">Указывает пароль сертификата, который будет использоваться для проверки подлинности в качестве субъекта-службы.</span><span class="sxs-lookup"><span data-stu-id="20fd7-139">Specifies the password for the certificate that will be used to authenticate as the Service Principal.</span></span>
<span data-ttu-id="20fd7-140">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="20fd7-140">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="20fd7-141">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="20fd7-141">-ClusterName</span></span>
<span data-ttu-id="20fd7-142">Указывает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="20fd7-142">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="20fd7-143">-ClusterSizeInNodes</span><span class="sxs-lookup"><span data-stu-id="20fd7-143">-ClusterSizeInNodes</span></span>
<span data-ttu-id="20fd7-144">Задает количество узлов рабочих процессов для кластера.</span><span class="sxs-lookup"><span data-stu-id="20fd7-144">Specifies the number of Worker nodes for the cluster.</span></span>

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

### <span data-ttu-id="20fd7-145">-ClusterTier</span><span class="sxs-lookup"><span data-stu-id="20fd7-145">-ClusterTier</span></span>
<span data-ttu-id="20fd7-146">Указывает уровень кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="20fd7-146">Specifies the HDInsight cluster tier.</span></span>
<span data-ttu-id="20fd7-147">По умолчанию это стандартный.</span><span class="sxs-lookup"><span data-stu-id="20fd7-147">By default, this is Standard.</span></span>
<span data-ttu-id="20fd7-148">Уровень Premium можно использовать только для кластеров Linux, а также для использования некоторых новых функций.</span><span class="sxs-lookup"><span data-stu-id="20fd7-148">The Premium tier can only be used with Linux clusters, and it enables the use of some new features.</span></span>

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

### <span data-ttu-id="20fd7-149">-ClusterType</span><span class="sxs-lookup"><span data-stu-id="20fd7-149">-ClusterType</span></span>
<span data-ttu-id="20fd7-150">Указывает тип создаваемого кластера.</span><span class="sxs-lookup"><span data-stu-id="20fd7-150">Specifies the type of cluster to create.</span></span>
<span data-ttu-id="20fd7-151">Доступны следующие варианты: Hadoop, HBase, INTERACTIVEHIVE, Kafka и RServer</span><span class="sxs-lookup"><span data-stu-id="20fd7-151">Options are: Hadoop, HBase, Storm, Spark, INTERACTIVEHIVE, Kafka, and RServer</span></span>

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

### <span data-ttu-id="20fd7-152">-ComponentVersion</span><span class="sxs-lookup"><span data-stu-id="20fd7-152">-ComponentVersion</span></span>
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

### <span data-ttu-id="20fd7-153">-Config</span><span class="sxs-lookup"><span data-stu-id="20fd7-153">-Config</span></span>
<span data-ttu-id="20fd7-154">Указывает объект кластера, который будет использоваться для создания кластера.</span><span class="sxs-lookup"><span data-stu-id="20fd7-154">Specifies the cluster object to be used to create the cluster.</span></span>
<span data-ttu-id="20fd7-155">Этот объект можно создать с помощью командлета New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="20fd7-155">This object can be created by using the New-AzHDInsightClusterConfig cmdlet.</span></span>

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

### <span data-ttu-id="20fd7-156">-Конфигурации</span><span class="sxs-lookup"><span data-stu-id="20fd7-156">-Configurations</span></span>
<span data-ttu-id="20fd7-157">Указывает конфигурации этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="20fd7-157">Specifies the configurations of this HDInsight cluster.</span></span>
<span data-ttu-id="20fd7-158">Вы также можете использовать командлет Add-AzHDInsightConfigValues.</span><span class="sxs-lookup"><span data-stu-id="20fd7-158">You can alternatively use the Add-AzHDInsightConfigValues cmdlet.</span></span>

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

### <span data-ttu-id="20fd7-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20fd7-159">-DefaultProfile</span></span>
<span data-ttu-id="20fd7-160">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="20fd7-160">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20fd7-161">-DisksPerWorkerNode</span><span class="sxs-lookup"><span data-stu-id="20fd7-161">-DisksPerWorkerNode</span></span>
<span data-ttu-id="20fd7-162">Задает количество дисков для роли узла рабочего процесса в кластере.</span><span class="sxs-lookup"><span data-stu-id="20fd7-162">Specifies the number of disks for worker node role in the cluster.</span></span>

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

### <span data-ttu-id="20fd7-163">-EdgeNodeSize</span><span class="sxs-lookup"><span data-stu-id="20fd7-163">-EdgeNodeSize</span></span>
<span data-ttu-id="20fd7-164">Указывает размер виртуальной машины для граничного узла.</span><span class="sxs-lookup"><span data-stu-id="20fd7-164">Specifies the size of the virtual machine for the edge node.</span></span> <span data-ttu-id="20fd7-165">Используйте Get-AzVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="20fd7-165">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span> <span data-ttu-id="20fd7-166">Этот параметр является допустимым только для кластеров RServer.</span><span class="sxs-lookup"><span data-stu-id="20fd7-166">This parameter is valid only for RServer clusters.</span></span>

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

### <span data-ttu-id="20fd7-167">-EnableIDBroker</span><span class="sxs-lookup"><span data-stu-id="20fd7-167">-EnableIDBroker</span></span>
<span data-ttu-id="20fd7-168">Включает компонент Брокер удостоверений HDInsight.</span><span class="sxs-lookup"><span data-stu-id="20fd7-168">Enables HDInsight Identity Broker feature.</span></span>

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

### <span data-ttu-id="20fd7-169">-EncryptionAlgorithm</span><span class="sxs-lookup"><span data-stu-id="20fd7-169">-EncryptionAlgorithm</span></span>
<span data-ttu-id="20fd7-170">Возвращает или задает алгоритм шифрования.</span><span class="sxs-lookup"><span data-stu-id="20fd7-170">Gets or sets the encryption algorithm.</span></span>

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

### <span data-ttu-id="20fd7-171">-EncryptionAtHost</span><span class="sxs-lookup"><span data-stu-id="20fd7-171">-EncryptionAtHost</span></span>
<span data-ttu-id="20fd7-172">Возвращает или задает флаг, указывающий, следует ли включить шифрование на хосте или нет.</span><span class="sxs-lookup"><span data-stu-id="20fd7-172">Gets or sets the flag which indicates whether enable encryption at host or not.</span></span>

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

### <span data-ttu-id="20fd7-173">-EncryptionInTransit</span><span class="sxs-lookup"><span data-stu-id="20fd7-173">-EncryptionInTransit</span></span>
<span data-ttu-id="20fd7-174">Возвращает или задает флаг, указывающий, следует ли включить шифрование в пути или нет.</span><span class="sxs-lookup"><span data-stu-id="20fd7-174">Gets or sets the flag which indicates whether enable encryption in transit or not.</span></span>

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

### <span data-ttu-id="20fd7-175">-EncryptionKeyName</span><span class="sxs-lookup"><span data-stu-id="20fd7-175">-EncryptionKeyName</span></span>
<span data-ttu-id="20fd7-176">Возвращает или задает имя ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="20fd7-176">Gets or sets the encryption key name.</span></span>

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

### <span data-ttu-id="20fd7-177">-EncryptionKeyVersion</span><span class="sxs-lookup"><span data-stu-id="20fd7-177">-EncryptionKeyVersion</span></span>
<span data-ttu-id="20fd7-178">Возвращает или задает версию ключа шифрования.</span><span class="sxs-lookup"><span data-stu-id="20fd7-178">Gets or sets the encryption key version.</span></span>

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

### <span data-ttu-id="20fd7-179">-EncryptionVaultUri</span><span class="sxs-lookup"><span data-stu-id="20fd7-179">-EncryptionVaultUri</span></span>
<span data-ttu-id="20fd7-180">Возвращает или задает универсальный код ресурса (URI) для хранилища шифрования.</span><span class="sxs-lookup"><span data-stu-id="20fd7-180">Gets or sets the encryption vault uri.</span></span>

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

### <span data-ttu-id="20fd7-181">-HeadNodeSize</span><span class="sxs-lookup"><span data-stu-id="20fd7-181">-HeadNodeSize</span></span>
<span data-ttu-id="20fd7-182">Задает размер виртуальной машины для головного узла.</span><span class="sxs-lookup"><span data-stu-id="20fd7-182">Specifies the size of the virtual machine for the Head node.</span></span>
<span data-ttu-id="20fd7-183">Используйте Get-AzVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="20fd7-183">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="20fd7-184">-HiveMetastore</span><span class="sxs-lookup"><span data-stu-id="20fd7-184">-HiveMetastore</span></span>
<span data-ttu-id="20fd7-185">Указывает базу данных SQL для хранения метаданных куста.</span><span class="sxs-lookup"><span data-stu-id="20fd7-185">Specifies the SQL Database to store Hive metadata.</span></span>
<span data-ttu-id="20fd7-186">Вы также можете использовать командлет Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="20fd7-186">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="20fd7-187">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="20fd7-187">-HttpCredential</span></span>
<span data-ttu-id="20fd7-188">Задает учетные данные для входа в кластер (HTTP) для кластера.</span><span class="sxs-lookup"><span data-stu-id="20fd7-188">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="20fd7-189">-KafkaClientGroupId</span><span class="sxs-lookup"><span data-stu-id="20fd7-189">-KafkaClientGroupId</span></span>
<span data-ttu-id="20fd7-190">Возвращает или задает идентификатор клиентской группы для доступа к прокси-серверу Kafka RESTful.</span><span class="sxs-lookup"><span data-stu-id="20fd7-190">Gets or sets the client group id for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="20fd7-191">-KafkaClientGroupName</span><span class="sxs-lookup"><span data-stu-id="20fd7-191">-KafkaClientGroupName</span></span>
<span data-ttu-id="20fd7-192">Возвращает или задает имя клиентской группы для доступа к прокси-серверу Kafka RESTful.</span><span class="sxs-lookup"><span data-stu-id="20fd7-192">Gets or sets the client group name for Kafka Rest Proxy access.</span></span>

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

### <span data-ttu-id="20fd7-193">-KafkaManagementNodeSize</span><span class="sxs-lookup"><span data-stu-id="20fd7-193">-KafkaManagementNodeSize</span></span>
<span data-ttu-id="20fd7-194">Возвращает или задает размер узла управления Kafka.</span><span class="sxs-lookup"><span data-stu-id="20fd7-194">Gets or sets the size of the Kafka Management Node.</span></span>

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

### <span data-ttu-id="20fd7-195">-Location</span><span class="sxs-lookup"><span data-stu-id="20fd7-195">-Location</span></span>
<span data-ttu-id="20fd7-196">Задает расположение кластера.</span><span class="sxs-lookup"><span data-stu-id="20fd7-196">Specifies the location for the cluster.</span></span>

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

### <span data-ttu-id="20fd7-197">-MinSupportedTlsVersion</span><span class="sxs-lookup"><span data-stu-id="20fd7-197">-MinSupportedTlsVersion</span></span>
<span data-ttu-id="20fd7-198">Возвращает или задает минимальную поддерживаемую версию TLS.</span><span class="sxs-lookup"><span data-stu-id="20fd7-198">Gets or sets the minimal supported TLS version.</span></span>

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

### <span data-ttu-id="20fd7-199">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="20fd7-199">-ObjectId</span></span>
<span data-ttu-id="20fd7-200">Указывает идентификатор объекта Azure AD (GUID) субъекта-службы Azure AD, который представляет этот кластер.</span><span class="sxs-lookup"><span data-stu-id="20fd7-200">Specifies the Azure AD object ID (a GUID) of the Azure AD Service Principal that represents the cluster.</span></span>
<span data-ttu-id="20fd7-201">Кластер будет использовать этот параметр при доступе к Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="20fd7-201">The cluster will use this when accessing Azure Data Lake Store.</span></span>

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

### <span data-ttu-id="20fd7-202">-OozieMetastore</span><span class="sxs-lookup"><span data-stu-id="20fd7-202">-OozieMetastore</span></span>
<span data-ttu-id="20fd7-203">Определяет базу данных SQL для хранения метаданных Oozie.</span><span class="sxs-lookup"><span data-stu-id="20fd7-203">Specifies the SQL Database to store Oozie metadata.</span></span>
<span data-ttu-id="20fd7-204">Вы также можете использовать командлет Add-AzHDInsightMetastore.</span><span class="sxs-lookup"><span data-stu-id="20fd7-204">You can alternatively use the Add-AzHDInsightMetastore cmdlet.</span></span>

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

### <span data-ttu-id="20fd7-205">-OSType</span><span class="sxs-lookup"><span data-stu-id="20fd7-205">-OSType</span></span>
<span data-ttu-id="20fd7-206">Указывает операционную систему для кластера.</span><span class="sxs-lookup"><span data-stu-id="20fd7-206">Specifies the operating system for the cluster.</span></span>
<span data-ttu-id="20fd7-207">Возможные варианты: Windows, Linux</span><span class="sxs-lookup"><span data-stu-id="20fd7-207">Options are: Windows, Linux</span></span>

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

### <span data-ttu-id="20fd7-208">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="20fd7-208">-RdpAccessExpiry</span></span>
<span data-ttu-id="20fd7-209">Задает срок действия в виде объекта DateTime для доступа к кластеру через протокол удаленного рабочего стола (RDP).</span><span class="sxs-lookup"><span data-stu-id="20fd7-209">Specifies the expiration, as a DateTime object, for Remote Desktop Protocol (RDP) access to a cluster.</span></span>

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

### <span data-ttu-id="20fd7-210">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="20fd7-210">-RdpCredential</span></span>
<span data-ttu-id="20fd7-211">Указывает учетные данные удаленного рабочего стола (RDP) для кластера.</span><span class="sxs-lookup"><span data-stu-id="20fd7-211">Specifies the Remote Desktop (RDP) credentials for the cluster.</span></span>
<span data-ttu-id="20fd7-212">Это относится только к кластерам Windows.</span><span class="sxs-lookup"><span data-stu-id="20fd7-212">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="20fd7-213">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20fd7-213">-ResourceGroupName</span></span>
<span data-ttu-id="20fd7-214">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="20fd7-214">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="20fd7-215">-ScriptActions</span><span class="sxs-lookup"><span data-stu-id="20fd7-215">-ScriptActions</span></span>
<span data-ttu-id="20fd7-216">Задает действия сценария, которые должны выполняться в кластере по завершении создания кластера.</span><span class="sxs-lookup"><span data-stu-id="20fd7-216">Specifies the script actions to run on the cluster at the end of cluster creation.</span></span>
<span data-ttu-id="20fd7-217">Вы также можете использовать Add-AzHDInsightScriptAction.</span><span class="sxs-lookup"><span data-stu-id="20fd7-217">You can alternatively use Add-AzHDInsightScriptAction.</span></span>

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

### <span data-ttu-id="20fd7-218">-SecurityProfile</span><span class="sxs-lookup"><span data-stu-id="20fd7-218">-SecurityProfile</span></span>
<span data-ttu-id="20fd7-219">Задает свойства, связанные с безопасностью, которые используются для создания надежного кластера.</span><span class="sxs-lookup"><span data-stu-id="20fd7-219">Specifies the security related properties used to create a secure cluster.</span></span>
<span data-ttu-id="20fd7-220">Вы также можете использовать командлет Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="20fd7-220">You can alternatively use the Add-AzHDInsightSecurityProfile cmdlet.</span></span>

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

### <span data-ttu-id="20fd7-221">-SshCredential</span><span class="sxs-lookup"><span data-stu-id="20fd7-221">-SshCredential</span></span>
<span data-ttu-id="20fd7-222">Указывает учетные данные SSH, которые будут использоваться для подключений по протоколу SSH.</span><span class="sxs-lookup"><span data-stu-id="20fd7-222">Specifies the SSH credential to be used for SSH connections.</span></span>
<span data-ttu-id="20fd7-223">Это относится только к кластерам Linux.</span><span class="sxs-lookup"><span data-stu-id="20fd7-223">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="20fd7-224">-SshPublicKey</span><span class="sxs-lookup"><span data-stu-id="20fd7-224">-SshPublicKey</span></span>
<span data-ttu-id="20fd7-225">Указывает открытый ключ, который будет использоваться для подключений по протоколу SSH.</span><span class="sxs-lookup"><span data-stu-id="20fd7-225">Specifies the public key to be used for SSH connections.</span></span>
<span data-ttu-id="20fd7-226">Это относится только к кластерам Linux.</span><span class="sxs-lookup"><span data-stu-id="20fd7-226">This is only for Linux clusters.</span></span>

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

### <span data-ttu-id="20fd7-227">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="20fd7-227">-StorageAccountKey</span></span>
<span data-ttu-id="20fd7-228">Возвращает или задает ключ доступа учетной записи хранения для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="20fd7-228">Gets or sets the Storage Account Access Key for the Storage Account.</span></span>

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

### <span data-ttu-id="20fd7-229">-StorageAccountManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="20fd7-229">-StorageAccountManagedIdentity</span></span>
<span data-ttu-id="20fd7-230">Возвращает или задает управляемое удостоверение учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="20fd7-230">Gets or sets the storage account managed identity.</span></span>

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

### <span data-ttu-id="20fd7-231">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="20fd7-231">-StorageAccountResourceId</span></span>
<span data-ttu-id="20fd7-232">Возвращает или задает идентификатор ресурса хранилища для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="20fd7-232">Gets or sets the Storage Resource Id for the Storage Account.</span></span>

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

### <span data-ttu-id="20fd7-233">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="20fd7-233">-StorageAccountType</span></span>
<span data-ttu-id="20fd7-234">Возвращает или задает тип учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="20fd7-234">Gets or sets the type of the storage account.</span></span>

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

### <span data-ttu-id="20fd7-235">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="20fd7-235">-StorageContainer</span></span>
<span data-ttu-id="20fd7-236">Возвращает или задает имя StorageContainer для учетной записи хранения Azure по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="20fd7-236">Gets or sets the StorageContainer name for the default Azure Storage Account</span></span>

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

### <span data-ttu-id="20fd7-237">-StorageFileSystem</span><span class="sxs-lookup"><span data-stu-id="20fd7-237">-StorageFileSystem</span></span>
<span data-ttu-id="20fd7-238">Возвращает или задает файловую систему для учетной записи Gen2 Azure Data Lake Storage.</span><span class="sxs-lookup"><span data-stu-id="20fd7-238">Gets or sets the file system for the default Azure Data Lake Storage Gen2 account.</span></span>

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

### <span data-ttu-id="20fd7-239">-StorageRootPath</span><span class="sxs-lookup"><span data-stu-id="20fd7-239">-StorageRootPath</span></span>
<span data-ttu-id="20fd7-240">Возвращает или задает путь к корню кластера в учетной записи Data Lake Store по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="20fd7-240">Gets or sets the path to the root of the cluster in the default Data Lake Store Account.</span></span>

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

### <span data-ttu-id="20fd7-241">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="20fd7-241">-SubnetName</span></span>
<span data-ttu-id="20fd7-242">Возвращает или задает имя подсети для этого кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="20fd7-242">Gets or sets the subnet name for this HDInsight cluster.</span></span>

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

### <span data-ttu-id="20fd7-243">-Version</span><span class="sxs-lookup"><span data-stu-id="20fd7-243">-Version</span></span>
<span data-ttu-id="20fd7-244">Указывает версию HDI кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="20fd7-244">Specifies the HDI version of the HDInsight cluster.</span></span>

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

### <span data-ttu-id="20fd7-245">-VirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="20fd7-245">-VirtualNetworkId</span></span>
<span data-ttu-id="20fd7-246">Указывает ИД виртуальной сети, в которую подготавливается кластер.</span><span class="sxs-lookup"><span data-stu-id="20fd7-246">Specifies the ID of the virtual network into which to provision the cluster.</span></span>

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

### <span data-ttu-id="20fd7-247">-WorkerNodeSize</span><span class="sxs-lookup"><span data-stu-id="20fd7-247">-WorkerNodeSize</span></span>
<span data-ttu-id="20fd7-248">Указывает размер виртуальной машины для рабочего узла.</span><span class="sxs-lookup"><span data-stu-id="20fd7-248">Specifies the size of the virtual machine for the Worker node.</span></span>
<span data-ttu-id="20fd7-249">Используйте Get-AzVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="20fd7-249">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>

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

### <span data-ttu-id="20fd7-250">-ZookeeperNodeSize</span><span class="sxs-lookup"><span data-stu-id="20fd7-250">-ZookeeperNodeSize</span></span>
<span data-ttu-id="20fd7-251">Указывает размер виртуальной машины для узла Джесс.</span><span class="sxs-lookup"><span data-stu-id="20fd7-251">Specifies the size of the virtual machine for the Zookeeper node.</span></span>
<span data-ttu-id="20fd7-252">Используйте Get-AzVMSize для приемлемых размеров ВМ и ознакомьтесь со страницей цены HDInsight.</span><span class="sxs-lookup"><span data-stu-id="20fd7-252">Use Get-AzVMSize for acceptable VM sizes, and see HDInsight's pricing page.</span></span>
<span data-ttu-id="20fd7-253">Этот параметр является допустимым только для кластеров HBase и.</span><span class="sxs-lookup"><span data-stu-id="20fd7-253">This parameter is valid only for HBase or Storm clusters.</span></span>

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

### <span data-ttu-id="20fd7-254">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20fd7-254">CommonParameters</span></span>
<span data-ttu-id="20fd7-255">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="20fd7-255">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20fd7-256">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20fd7-256">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20fd7-257">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="20fd7-257">INPUTS</span></span>

### <span data-ttu-id="20fd7-258">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="20fd7-258">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="20fd7-259">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="20fd7-259">OUTPUTS</span></span>

### <span data-ttu-id="20fd7-260">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="20fd7-260">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="20fd7-261">Пуск</span><span class="sxs-lookup"><span data-stu-id="20fd7-261">NOTES</span></span>
<span data-ttu-id="20fd7-262">Ключевые слова: Azure, azurerm, ARM, Resource, менеджмент, руководитель, Hadoop, hdinsight, HD и Insights</span><span class="sxs-lookup"><span data-stu-id="20fd7-262">Keywords: azure, azurerm, arm, resource, management, manager, hadoop, hdinsight, hd, insight</span></span>

## <span data-ttu-id="20fd7-263">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="20fd7-263">RELATED LINKS</span></span>

[<span data-ttu-id="20fd7-264">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="20fd7-264">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)
