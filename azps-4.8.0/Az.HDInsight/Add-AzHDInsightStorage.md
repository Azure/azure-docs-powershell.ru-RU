---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C2AF43D-18BF-4036-A355-FC27E406B18A
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/add-azhdinsightstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Add-AzHDInsightStorage.md
ms.openlocfilehash: 43850e035a59674b06502db1486de0d90fe6e4ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242766"
---
# <span data-ttu-id="a8e43-101">Add-AzHDInsightStorage</span><span class="sxs-lookup"><span data-stu-id="a8e43-101">Add-AzHDInsightStorage</span></span>

## <span data-ttu-id="a8e43-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a8e43-102">SYNOPSIS</span></span>
<span data-ttu-id="a8e43-103">Добавляет ключ хранилища Azure к объекту конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="a8e43-103">Adds an Azure Storage key to a cluster configuration object.</span></span>

## <span data-ttu-id="a8e43-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a8e43-104">SYNTAX</span></span>

```
Add-AzHDInsightStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8e43-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8e43-105">DESCRIPTION</span></span>
<span data-ttu-id="a8e43-106">Командлет **Add-AzHDInsightStorage** добавляет запись учетной записи хранения Azure в объект конфигурации HDInsight Azure, созданный командлетом New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="a8e43-106">The **Add-AzHDInsightStorage** cmdlet adds an Azure Storage account entry to the Azure HDInsight configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="a8e43-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a8e43-107">EXAMPLES</span></span>

### <span data-ttu-id="a8e43-108">Пример 1: Добавление ключа хранилища Azure в объект конфигурации кластера</span><span class="sxs-lookup"><span data-stu-id="a8e43-108">Example 1: Add an Azure storage key to the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
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
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

<span data-ttu-id="a8e43-109">Эта команда добавляет запись учетной записи хранения BLOB в конфигурацию HDInsight с именем-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="a8e43-109">This command adds an blob storage account entry to the HDInsight configuration named your-hadoop-001.</span></span>

## <span data-ttu-id="a8e43-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a8e43-110">PARAMETERS</span></span>

### <span data-ttu-id="a8e43-111">-Config</span><span class="sxs-lookup"><span data-stu-id="a8e43-111">-Config</span></span>
<span data-ttu-id="a8e43-112">Указывает объект конфигурации кластера HDInsight, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a8e43-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="a8e43-113">Этот объект создается командлетом **New-AzHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="a8e43-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="a8e43-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8e43-114">-DefaultProfile</span></span>
<span data-ttu-id="a8e43-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a8e43-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a8e43-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a8e43-116">-StorageAccountKey</span></span>
<span data-ttu-id="a8e43-117">Задает ключ учетной записи хранения для учетной записи хранения, которую нужно добавить в новый кластер.</span><span class="sxs-lookup"><span data-stu-id="a8e43-117">Specifies the storage account key for the storage account to be added to the new cluster.</span></span>

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

### <span data-ttu-id="a8e43-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="a8e43-118">-StorageAccountName</span></span>
<span data-ttu-id="a8e43-119">Указывает имя учетной записи хранения для учетной записи хранения, которую нужно добавить в кластер.</span><span class="sxs-lookup"><span data-stu-id="a8e43-119">Specifies the storage account name for the storage account to be added to the cluster.</span></span>

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

### <span data-ttu-id="a8e43-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8e43-120">CommonParameters</span></span>
<span data-ttu-id="a8e43-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a8e43-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8e43-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8e43-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8e43-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a8e43-123">INPUTS</span></span>

### <span data-ttu-id="a8e43-124">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="a8e43-124">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="a8e43-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a8e43-125">OUTPUTS</span></span>

### <span data-ttu-id="a8e43-126">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="a8e43-126">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="a8e43-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="a8e43-127">NOTES</span></span>

## <span data-ttu-id="a8e43-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a8e43-128">RELATED LINKS</span></span>

[<span data-ttu-id="a8e43-129">New-AzHDInsightClusterConfig</span><span class="sxs-lookup"><span data-stu-id="a8e43-129">New-AzHDInsightClusterConfig</span></span>](./New-AzHDInsightClusterConfig.md)

