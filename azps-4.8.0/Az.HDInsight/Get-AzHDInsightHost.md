---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightHost.md
ms.openlocfilehash: 2e9e8858e79521c32cdf08b980584fd2b77dd955
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078255"
---
# <span data-ttu-id="551ae-101">Get-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="551ae-101">Get-AzHDInsightHost</span></span>

## <span data-ttu-id="551ae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="551ae-102">SYNOPSIS</span></span>
<span data-ttu-id="551ae-103">Список узлов кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="551ae-103">Lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="551ae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="551ae-104">SYNTAX</span></span>

### <span data-ttu-id="551ae-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="551ae-105">SetByNameParameterSet (Default)</span></span>
```
Get-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="551ae-106">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="551ae-106">SetByResourceIdParameterSet</span></span>
```
Get-AzHDInsightHost [-ResourceId] <String> [[-DefaultProfile] <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="551ae-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="551ae-107">SetByInputObjectParameterSet</span></span>
```
Get-AzHDInsightHost [-InputObject] <AzureHDInsightCluster> [[-DefaultProfile] <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="551ae-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="551ae-108">DESCRIPTION</span></span>
<span data-ttu-id="551ae-109">Командлет **Get-AzHDInsightHost** содержит список узлов кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="551ae-109">The **Get-AzHDInsightHost** cmdlet lists the hosts of the HDInsight cluster.</span></span>

## <span data-ttu-id="551ae-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="551ae-110">EXAMPLES</span></span>

### <span data-ttu-id="551ae-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="551ae-111">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Get-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="551ae-112">Эта команда перечисляет узлы кластера с именем кластера.</span><span class="sxs-lookup"><span data-stu-id="551ae-112">This command lists of cluster' hosts with cluster name.</span></span>

### <span data-ttu-id="551ae-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="551ae-113">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $cluster=Get-AzHDInsightCluster -ClusterName $clusterName
PS C:\> $cluster | Get-AzHDInsightHost
```

<span data-ttu-id="551ae-114">Эта команда перечисляет узлы кластера с конвейером.</span><span class="sxs-lookup"><span data-stu-id="551ae-114">This command lists of cluster' hosts with pipeline.</span></span>

## <span data-ttu-id="551ae-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="551ae-115">PARAMETERS</span></span>

### <span data-ttu-id="551ae-116">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="551ae-116">-ClusterName</span></span>
<span data-ttu-id="551ae-117">Возвращает или задает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="551ae-117">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="551ae-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="551ae-118">-DefaultProfile</span></span>
<span data-ttu-id="551ae-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="551ae-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="551ae-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="551ae-120">-InputObject</span></span>
<span data-ttu-id="551ae-121">Возвращает или задает объект ввода.</span><span class="sxs-lookup"><span data-stu-id="551ae-121">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="551ae-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="551ae-122">-ResourceGroupName</span></span>
<span data-ttu-id="551ae-123">Возвращает или задает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="551ae-123">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="551ae-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="551ae-124">-ResourceId</span></span>
<span data-ttu-id="551ae-125">Возвращает или задает идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="551ae-125">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="551ae-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="551ae-126">CommonParameters</span></span>
<span data-ttu-id="551ae-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="551ae-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="551ae-128">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="551ae-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="551ae-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="551ae-129">INPUTS</span></span>

### <span data-ttu-id="551ae-130">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="551ae-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="551ae-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="551ae-131">OUTPUTS</span></span>

### <span data-ttu-id="551ae-132">Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="551ae-132">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo</span></span>

## <span data-ttu-id="551ae-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="551ae-133">NOTES</span></span>

## <span data-ttu-id="551ae-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="551ae-134">RELATED LINKS</span></span>
