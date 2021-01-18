---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C2AF43D-18BF-4036-A355-FC27E406B18A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
ms.openlocfilehash: 6db3c5b5d899f9b7a32e6dbb20c280590bea93c6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504836"
---
# <span data-ttu-id="9d4e2-101">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="9d4e2-101">Add-AzHDInsightStorage</span></span>

## <span data-ttu-id="9d4e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d4e2-102">SYNOPSIS</span></span>
<span data-ttu-id="9d4e2-103">Добавляет ключ хранилища Azure к объекту конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="9d4e2-103">Adds an Azure Storage key to a cluster configuration object.</span></span>

## <span data-ttu-id="9d4e2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9d4e2-104">SYNTAX</span></span>

```
Add-AzHDInsightStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d4e2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d4e2-105">DESCRIPTION</span></span>
<span data-ttu-id="9d4e2-106">Cmdlet **Add-AzHDInsightStorage** добавляет запись учетной записи хранилища Azure к объекту конфигурации Azure HDInsight, созданному New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="9d4e2-106">The **Add-AzHDInsightStorage** cmdlet adds an Azure Storage account entry to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="9d4e2-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9d4e2-107">EXAMPLES</span></span>

### <span data-ttu-id="9d4e2-108">Пример 1. Добавление ключа хранилища Azure к объекту конфигурации кластера</span><span class="sxs-lookup"><span data-stu-id="9d4e2-108">Example 1: Add an Azure storage key to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Second storage account info
PS C:\> $secondStorageAccountResourceGroupName = "Group"
PS C:\> $secondStorageAccountName = "yourstorageacct002"
PS C:\> $secondStorageAccountKey = Get-AzStorageAccountKey `
PS C:\> -ResourceGroupName $secondStorageAccountResourceGroupName `
            -Name $secondStorageAccountName | %{ $_.Key1 }

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
                -StorageAccountResourceId $storageAccountResourceId `
                -StorageAccountKey $storageAccountKey `
                -StorageContainer $storageContainer
```

<span data-ttu-id="9d4e2-109">Эта команда добавляет запись учетной записи хранилища BLOB-lob в конфигурацию HDInsight с именем your-hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="9d4e2-109">This command adds an blob storage account entry to the HDInsight configuration named your-hadoop-001.</span></span>

## <span data-ttu-id="9d4e2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d4e2-110">PARAMETERS</span></span>

### <span data-ttu-id="9d4e2-111">-Config</span><span class="sxs-lookup"><span data-stu-id="9d4e2-111">-Config</span></span>
<span data-ttu-id="9d4e2-112">Определяет объект конфигурации кластера HDInsight, который изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d4e2-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="9d4e2-113">Этот объект создается с помощью **командылета New-AzHDInsightClusterConfig.**</span><span class="sxs-lookup"><span data-stu-id="9d4e2-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d4e2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d4e2-114">-DefaultProfile</span></span>
<span data-ttu-id="9d4e2-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9d4e2-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d4e2-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="9d4e2-116">-StorageAccountKey</span></span>
<span data-ttu-id="9d4e2-117">Указывает ключ учетной записи хранения для учетной записи хранения, которая будет добавлена в новый кластер.</span><span class="sxs-lookup"><span data-stu-id="9d4e2-117">Specifies the storage account key for the storage account to be added to the new cluster.</span></span>

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

### <span data-ttu-id="9d4e2-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9d4e2-118">-StorageAccountName</span></span>
<span data-ttu-id="9d4e2-119">Указывает имя учетной записи хранения, которая будет добавлена в кластер.</span><span class="sxs-lookup"><span data-stu-id="9d4e2-119">Specifies the storage account name for the storage account to be added to the cluster.</span></span>

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

### <span data-ttu-id="9d4e2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d4e2-120">CommonParameters</span></span>
<span data-ttu-id="9d4e2-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d4e2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d4e2-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d4e2-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d4e2-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9d4e2-123">INPUTS</span></span>

### <span data-ttu-id="9d4e2-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="9d4e2-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="9d4e2-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9d4e2-125">OUTPUTS</span></span>

### <span data-ttu-id="9d4e2-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="9d4e2-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="9d4e2-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9d4e2-127">NOTES</span></span>

## <span data-ttu-id="9d4e2-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9d4e2-128">RELATED LINKS</span></span>

[<span data-ttu-id="9d4e2-129">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="9d4e2-129">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)


