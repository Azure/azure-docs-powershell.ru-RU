---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 37E41DA2-B65B-4AA2-B6AB-F93CCA881C72
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightdefaultstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
ms.openlocfilehash: e4ecdb86d3c8b055f76303af5c3b86fc9813e167
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079630"
---
# <span data-ttu-id="d8b50-101">Set-AzHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="d8b50-101">Set-AzHDInsightDefaultStorage</span></span>

## <span data-ttu-id="d8b50-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d8b50-102">SYNOPSIS</span></span>
<span data-ttu-id="d8b50-103">Задает параметр учетной записи хранения по умолчанию в объекте конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="d8b50-103">Sets the default Storage account setting in a cluster configuration object.</span></span>

## <span data-ttu-id="d8b50-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d8b50-104">SYNTAX</span></span>

```
Set-AzHDInsightDefaultStorage [-Config] <AzureHDInsightConfig> [-StorageAccountName] <String>
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d8b50-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8b50-105">DESCRIPTION</span></span>
<span data-ttu-id="d8b50-106">Командлет **Set-AzHDInsightDefaultStorage** задает параметры учетной записи хранения по умолчанию в объекте конфигурации кластера Azure HDInsight, созданном с помощью командлета New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="d8b50-106">The **Set-AzHDInsightDefaultStorage** cmdlet sets the default Storage account setting in the Azure HDInsight cluster configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="d8b50-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d8b50-107">EXAMPLES</span></span>

### <span data-ttu-id="d8b50-108">Пример 1: Настройка учетной записи хранения по умолчанию для объекта конфигурации кластера</span><span class="sxs-lookup"><span data-stu-id="d8b50-108">Example 1: Set the default storage account for the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\>$storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Set-AzHDInsightDefaultStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
                -StorageContainer $storageContainer `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location
```

<span data-ttu-id="d8b50-109">Эта команда задает учетную запись хранения по умолчанию для объекта конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="d8b50-109">This command sets the default Storage account for a cluster configuration object.</span></span>

## <span data-ttu-id="d8b50-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d8b50-110">PARAMETERS</span></span>

### <span data-ttu-id="d8b50-111">-Config</span><span class="sxs-lookup"><span data-stu-id="d8b50-111">-Config</span></span>
<span data-ttu-id="d8b50-112">Указывает объект конфигурации кластера HDInsight, который изменяет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d8b50-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="d8b50-113">Этот объект создается командлетом **New-AzHDInsightClusterConfig** .</span><span class="sxs-lookup"><span data-stu-id="d8b50-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="d8b50-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8b50-114">-DefaultProfile</span></span>
<span data-ttu-id="d8b50-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d8b50-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8b50-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="d8b50-116">-StorageAccountKey</span></span>
<span data-ttu-id="d8b50-117">Указывает ключ учетной записи хранения Azure, используемой по умолчанию, которую будет использовать кластер HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d8b50-117">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8b50-118">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d8b50-118">-StorageAccountName</span></span>
<span data-ttu-id="d8b50-119">Указывает имя учетной записи хранения, используемой по умолчанию, которое будет использоваться кластером HDInsight.</span><span class="sxs-lookup"><span data-stu-id="d8b50-119">Specifies the name of the default storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="d8b50-120">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="d8b50-120">-StorageAccountType</span></span>
<span data-ttu-id="d8b50-121">Возвращает или задает тип учетной записи хранения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d8b50-121">Gets or sets the type of the default storage account.</span></span> <span data-ttu-id="d8b50-122">По умолчанию AzureStorage</span><span class="sxs-lookup"><span data-stu-id="d8b50-122">Defaults to AzureStorage</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType]
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8b50-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8b50-123">CommonParameters</span></span>
<span data-ttu-id="d8b50-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d8b50-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8b50-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8b50-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8b50-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d8b50-126">INPUTS</span></span>

### <span data-ttu-id="d8b50-127">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="d8b50-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="d8b50-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8b50-128">OUTPUTS</span></span>

### <span data-ttu-id="d8b50-129">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="d8b50-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="d8b50-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="d8b50-130">NOTES</span></span>

## <span data-ttu-id="d8b50-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8b50-131">RELATED LINKS</span></span>