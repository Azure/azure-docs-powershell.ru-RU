---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
ms.openlocfilehash: 430c2aa7f38e6246c13ef6045f52346b580d20fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228417"
---
# <span data-ttu-id="42420-101">Get-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="42420-101">Get-AzHDInsightHost</span></span>

## <span data-ttu-id="42420-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42420-102">SYNOPSIS</span></span>
<span data-ttu-id="42420-103">Список хостов кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="42420-103">Lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="42420-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="42420-104">SYNTAX</span></span>

### <span data-ttu-id="42420-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="42420-105">SetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42420-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="42420-106">SetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightHost [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42420-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="42420-107">SetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightHost [-InputObject] <AzureHDInsightCluster> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="42420-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="42420-108">DESCRIPTION</span></span>
<span data-ttu-id="42420-109">В этом списке перечислены hosts кластера HDInsight для **Get-AzHDInsightHost.**</span><span class="sxs-lookup"><span data-stu-id="42420-109">The **Get-AzHDInsightHost** cmdlet lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="42420-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="42420-110">EXAMPLES</span></span>

### <span data-ttu-id="42420-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="42420-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Get-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="42420-112">Этот список команд содержит названия групп кластеров.</span><span class="sxs-lookup"><span data-stu-id="42420-112">This command lists of cluster' hosts with cluster name.</span></span>

### <span data-ttu-id="42420-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="42420-113">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $cluster=Get-AzHDInsightCluster -ClusterName $clusterName
PS C:\> $cluster | Get-AzHDInsightHost
```

<span data-ttu-id="42420-114">В этом списке команд перечислены hosts кластера с конвейером.</span><span class="sxs-lookup"><span data-stu-id="42420-114">This command lists of cluster' hosts with pipeline.</span></span>

## <span data-ttu-id="42420-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42420-115">PARAMETERS</span></span>

### <span data-ttu-id="42420-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="42420-116">-ClusterName</span></span>
<span data-ttu-id="42420-117">Возвращает или задает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="42420-117">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="42420-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42420-118">-DefaultProfile</span></span>
<span data-ttu-id="42420-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="42420-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42420-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42420-120">-InputObject</span></span>
<span data-ttu-id="42420-121">Возвращает или задает объект ввода.</span><span class="sxs-lookup"><span data-stu-id="42420-121">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="42420-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42420-122">-ResourceGroupName</span></span>
<span data-ttu-id="42420-123">Возвращает или задает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="42420-123">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="42420-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42420-124">-ResourceId</span></span>
<span data-ttu-id="42420-125">Возвращает или задает ид ресурса.</span><span class="sxs-lookup"><span data-stu-id="42420-125">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="42420-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42420-126">CommonParameters</span></span>
<span data-ttu-id="42420-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42420-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42420-128">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="42420-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42420-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="42420-129">INPUTS</span></span>

### <span data-ttu-id="42420-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="42420-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="42420-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="42420-131">OUTPUTS</span></span>

### <span data-ttu-id="42420-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="42420-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span></span>

## <span data-ttu-id="42420-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="42420-133">NOTES</span></span>

## <span data-ttu-id="42420-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="42420-134">RELATED LINKS</span></span>
