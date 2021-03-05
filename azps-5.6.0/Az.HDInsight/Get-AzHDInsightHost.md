---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
ms.openlocfilehash: 5b58e535acae8d6d0845b6be8c838f8372af9c65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012115"
---
# <span data-ttu-id="8dd7b-101">Get-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="8dd7b-101">Get-AzHDInsightHost</span></span>

## <span data-ttu-id="8dd7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dd7b-102">SYNOPSIS</span></span>
<span data-ttu-id="8dd7b-103">Список хостов кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="8dd7b-103">Lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="8dd7b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8dd7b-104">SYNTAX</span></span>

### <span data-ttu-id="8dd7b-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8dd7b-105">SetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8dd7b-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dd7b-106">SetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightHost [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8dd7b-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dd7b-107">SetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightHost [-InputObject] <AzureHDInsightCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8dd7b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8dd7b-108">DESCRIPTION</span></span>
<span data-ttu-id="8dd7b-109">В этом списке перечислены hosts кластера HDInsight для **Get-AzHDInsightHost.**</span><span class="sxs-lookup"><span data-stu-id="8dd7b-109">The **Get-AzHDInsightHost** cmdlet lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="8dd7b-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8dd7b-110">EXAMPLES</span></span>

### <span data-ttu-id="8dd7b-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8dd7b-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Get-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="8dd7b-112">Этот список команд содержит названия групп кластеров.</span><span class="sxs-lookup"><span data-stu-id="8dd7b-112">This command lists of cluster' hosts with cluster name.</span></span>

### <span data-ttu-id="8dd7b-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8dd7b-113">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $cluster=Get-AzHDInsightCluster -ClusterName $clusterName
PS C:\> $cluster | Get-AzHDInsightHost
```

<span data-ttu-id="8dd7b-114">В этом списке команд перечислены hosts кластера с конвейером.</span><span class="sxs-lookup"><span data-stu-id="8dd7b-114">This command lists of cluster' hosts with pipeline.</span></span>

## <span data-ttu-id="8dd7b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8dd7b-115">PARAMETERS</span></span>

### <span data-ttu-id="8dd7b-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="8dd7b-116">-ClusterName</span></span>
<span data-ttu-id="8dd7b-117">Возвращает или задает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="8dd7b-117">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd7b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dd7b-118">-DefaultProfile</span></span>
<span data-ttu-id="8dd7b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8dd7b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8dd7b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8dd7b-120">-InputObject</span></span>
<span data-ttu-id="8dd7b-121">Возвращает или устанавливает объект ввода.</span><span class="sxs-lookup"><span data-stu-id="8dd7b-121">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8dd7b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dd7b-122">-ResourceGroupName</span></span>
<span data-ttu-id="8dd7b-123">Возвращает или задает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8dd7b-123">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8dd7b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8dd7b-124">-ResourceId</span></span>
<span data-ttu-id="8dd7b-125">Возвращает или задает ид ресурса.</span><span class="sxs-lookup"><span data-stu-id="8dd7b-125">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8dd7b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dd7b-126">CommonParameters</span></span>
<span data-ttu-id="8dd7b-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dd7b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dd7b-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8dd7b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dd7b-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8dd7b-129">INPUTS</span></span>

### <span data-ttu-id="8dd7b-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="8dd7b-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="8dd7b-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8dd7b-131">OUTPUTS</span></span>

### <span data-ttu-id="8dd7b-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="8dd7b-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span></span>

## <span data-ttu-id="8dd7b-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8dd7b-133">NOTES</span></span>

## <span data-ttu-id="8dd7b-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8dd7b-134">RELATED LINKS</span></span>
