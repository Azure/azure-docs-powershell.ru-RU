---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 37E41DA2-B65B-4AA2-B6AB-F93CCA881C72
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightdefaultstorage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightDefaultStorage.md
ms.openlocfilehash: 06a783d0faf32dc2a3a35b448b1316ef50ba3326
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322884"
---
# <span data-ttu-id="ed6c9-101">Set-AzHDInsightDefaultStorage</span><span class="sxs-lookup"><span data-stu-id="ed6c9-101">Set-AzHDInsightDefaultStorage</span></span>

## <span data-ttu-id="ed6c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed6c9-102">SYNOPSIS</span></span>
<span data-ttu-id="ed6c9-103">Задает учетную запись хранения по умолчанию в объекте конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="ed6c9-103">Sets the default Storage account setting in a cluster configuration object.</span></span>

## <span data-ttu-id="ed6c9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ed6c9-104">SYNTAX</span></span>

```
Set-AzHDInsightDefaultStorage [-Config] <AzureHDInsightConfig> [-StorageAccountResourceId] <String>
 [[-StorageAccountKey] <String>] [-StorageAccountType <StorageType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed6c9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ed6c9-105">DESCRIPTION</span></span>
<span data-ttu-id="ed6c9-106">Для **параметра Set-AzHDInsightDefaultStorage** заданы параметры учетной записи хранения по умолчанию в объекте конфигурации кластера Azure HDInsight, созданном с помощью New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="ed6c9-106">The **Set-AzHDInsightDefaultStorage** cmdlet sets the default Storage account setting in the Azure HDInsight cluster configuration object created by the New-AzHDInsightClusterConfig cmdlet.</span></span>

## <span data-ttu-id="ed6c9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ed6c9-107">EXAMPLES</span></span>

### <span data-ttu-id="ed6c9-108">Пример 1. Настройка учетной записи хранения по умолчанию для объекта конфигурации кластера</span><span class="sxs-lookup"><span data-stu-id="ed6c9-108">Example 1: Set the default storage account for the cluster configuration object</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountResourceId = "yourstorageaccountresourceid"
PS C:\> $storageAccountName = "yourstorageaccountname"
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
                -StorageAccountResourceId $storageAccountResourceId `
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

<span data-ttu-id="ed6c9-109">Эта команда задает учетную запись хранения по умолчанию для объекта конфигурации кластера.</span><span class="sxs-lookup"><span data-stu-id="ed6c9-109">This command sets the default Storage account for a cluster configuration object.</span></span>

## <span data-ttu-id="ed6c9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed6c9-110">PARAMETERS</span></span>

### <span data-ttu-id="ed6c9-111">-Config</span><span class="sxs-lookup"><span data-stu-id="ed6c9-111">-Config</span></span>
<span data-ttu-id="ed6c9-112">Определяет объект конфигурации кластера HDInsight, который изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed6c9-112">Specifies the HDInsight cluster configuration object that this cmdlet modifies.</span></span>
<span data-ttu-id="ed6c9-113">Этот объект создается с помощью **командылета New-AzHDInsightClusterConfig.**</span><span class="sxs-lookup"><span data-stu-id="ed6c9-113">This object is created by the **New-AzHDInsightClusterConfig** cmdlet.</span></span>

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

### <span data-ttu-id="ed6c9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed6c9-114">-DefaultProfile</span></span>
<span data-ttu-id="ed6c9-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="ed6c9-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed6c9-116">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ed6c9-116">-StorageAccountKey</span></span>
<span data-ttu-id="ed6c9-117">Указывает ключ учетной записи для используемой по умолчанию учетной записи хранилища Azure, которая будет использовать кластер HDInsight.</span><span class="sxs-lookup"><span data-stu-id="ed6c9-117">Specifies the account key for the default Azure Storage account that the HDInsight cluster will use.</span></span>

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

### <span data-ttu-id="ed6c9-118">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="ed6c9-118">-StorageAccountResourceId</span></span>
<span data-ttu-id="ed6c9-119">Имя учетной записи хранения, которая будет добавлена в новый кластер.</span><span class="sxs-lookup"><span data-stu-id="ed6c9-119">The storage account name for the storage account to be added to the new cluster.</span></span>

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

### <span data-ttu-id="ed6c9-120">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="ed6c9-120">-StorageAccountType</span></span>
<span data-ttu-id="ed6c9-121">Возвращает или задает тип учетной записи хранения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ed6c9-121">Gets or sets the type of the default storage account.</span></span> <span data-ttu-id="ed6c9-122">Значения по умолчанию для AzureStorage</span><span class="sxs-lookup"><span data-stu-id="ed6c9-122">Defaults to AzureStorage</span></span>

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

### <span data-ttu-id="ed6c9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed6c9-123">CommonParameters</span></span>
<span data-ttu-id="ed6c9-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed6c9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed6c9-125">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed6c9-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed6c9-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ed6c9-126">INPUTS</span></span>

### <span data-ttu-id="ed6c9-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="ed6c9-127">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="ed6c9-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ed6c9-128">OUTPUTS</span></span>

### <span data-ttu-id="ed6c9-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span><span class="sxs-lookup"><span data-stu-id="ed6c9-129">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightConfig</span></span>

## <span data-ttu-id="ed6c9-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ed6c9-130">NOTES</span></span>

## <span data-ttu-id="ed6c9-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ed6c9-131">RELATED LINKS</span></span>
