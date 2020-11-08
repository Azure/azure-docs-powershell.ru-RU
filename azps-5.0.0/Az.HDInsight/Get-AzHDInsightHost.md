---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
ms.openlocfilehash: 2e9e8858e79521c32cdf08b980584fd2b77dd955
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245373"
---
# <span data-ttu-id="43a59-101">Get-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="43a59-101">Get-AzHDInsightHost</span></span>

## <span data-ttu-id="43a59-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="43a59-102">SYNOPSIS</span></span>
<span data-ttu-id="43a59-103">Список узлов кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="43a59-103">Lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="43a59-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="43a59-104">SYNTAX</span></span>

### <span data-ttu-id="43a59-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="43a59-105">SetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43a59-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="43a59-106">SetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightHost [-ResourceId] <String> [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43a59-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43a59-107">SetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightHost [-InputObject] <AzureHDInsightCluster> [[-DefaultProfile] <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="43a59-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="43a59-108">DESCRIPTION</span></span>
<span data-ttu-id="43a59-109">Командлет **Get-AzHDInsightHost** содержит список узлов кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="43a59-109">The **Get-AzHDInsightHost** cmdlet lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="43a59-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="43a59-110">EXAMPLES</span></span>

### <span data-ttu-id="43a59-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="43a59-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Get-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="43a59-112">Эта команда перечисляет узлы кластера с именем кластера.</span><span class="sxs-lookup"><span data-stu-id="43a59-112">This command lists of cluster' hosts with cluster name.</span></span>

### <span data-ttu-id="43a59-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="43a59-113">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $cluster=Get-AzHDInsightCluster -ClusterName $clusterName
PS C:\> $cluster | Get-AzHDInsightHost
```

<span data-ttu-id="43a59-114">Эта команда перечисляет узлы кластера с конвейером.</span><span class="sxs-lookup"><span data-stu-id="43a59-114">This command lists of cluster' hosts with pipeline.</span></span>

## <span data-ttu-id="43a59-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="43a59-115">PARAMETERS</span></span>

### <span data-ttu-id="43a59-116">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="43a59-116">-ClusterName</span></span>
<span data-ttu-id="43a59-117">Возвращает или задает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="43a59-117">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="43a59-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43a59-118">-DefaultProfile</span></span>
<span data-ttu-id="43a59-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="43a59-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43a59-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43a59-120">-InputObject</span></span>
<span data-ttu-id="43a59-121">Возвращает или задает объект ввода.</span><span class="sxs-lookup"><span data-stu-id="43a59-121">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="43a59-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43a59-122">-ResourceGroupName</span></span>
<span data-ttu-id="43a59-123">Возвращает или задает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="43a59-123">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="43a59-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43a59-124">-ResourceId</span></span>
<span data-ttu-id="43a59-125">Возвращает или задает идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="43a59-125">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="43a59-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43a59-126">CommonParameters</span></span>
<span data-ttu-id="43a59-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="43a59-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43a59-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43a59-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43a59-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="43a59-129">INPUTS</span></span>

### <span data-ttu-id="43a59-130">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="43a59-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="43a59-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="43a59-131">OUTPUTS</span></span>

### <span data-ttu-id="43a59-132">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="43a59-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span></span>

## <span data-ttu-id="43a59-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="43a59-133">NOTES</span></span>

## <span data-ttu-id="43a59-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="43a59-134">RELATED LINKS</span></span>
