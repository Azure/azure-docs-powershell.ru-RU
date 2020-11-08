---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/restart-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
ms.openlocfilehash: d4b184dfbf834822110369e40fbbfb4eb168e424
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247833"
---
# <span data-ttu-id="8f97b-101">Restart-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="8f97b-101">Restart-AzHDInsightHost</span></span>

## <span data-ttu-id="8f97b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8f97b-102">SYNOPSIS</span></span>
<span data-ttu-id="8f97b-103">Перезапускает определенные узлы кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="8f97b-103">Restarts the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="8f97b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8f97b-104">SYNTAX</span></span>

### <span data-ttu-id="8f97b-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8f97b-105">SetByNameParameterSet (Default)</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String> [-Name] <String[]> [-AsJob]
 [[-DefaultProfile] <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f97b-106">SetByAzureHDInsightHostInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f97b-106">SetByAzureHDInsightHostInfoParameterSet</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AzureHDInsightHostInfo] <AzureHDInsightHostInfo[]> [-AsJob] [[-DefaultProfile] <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f97b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f97b-107">DESCRIPTION</span></span>
<span data-ttu-id="8f97b-108">Перезапустите командлет **AzHDInsightHost** , перезапустите конкретные узлы кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="8f97b-108">This **Restart-AzHDInsightHost** cmdlet restart the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="8f97b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8f97b-109">EXAMPLES</span></span>

### <span data-ttu-id="8f97b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8f97b-110">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Restart-AzHDInsightHost -ClusterName $clusterName -Name wn0, wn1
```

<span data-ttu-id="8f97b-111">Эта команда перезапускает два узла кластера: worknode1, worknode2.</span><span class="sxs-lookup"><span data-stu-id="8f97b-111">This command restarts two hosts of the cluster: worknode1, worknode2.</span></span>

### <span data-ttu-id="8f97b-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8f97b-112">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $worknode1= Get-AzHDInsightHost -ClusterName $clusterName | Where-Object {$_.Name -like "wn1*"}
PS C:\> $worknode1 | Restart-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="8f97b-113">Эта команда показывает, как взаимодействовать с командлетом Get-AzHDInsightHost.</span><span class="sxs-lookup"><span data-stu-id="8f97b-113">This command shows how to cooperate with the cmdlet 'Get-AzHDInsightHost'.</span></span>

## <span data-ttu-id="8f97b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8f97b-114">PARAMETERS</span></span>

### <span data-ttu-id="8f97b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f97b-115">-AsJob</span></span>
<span data-ttu-id="8f97b-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8f97b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8f97b-117">-AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="8f97b-117">-AzureHDInsightHostInfo</span></span>
<span data-ttu-id="8f97b-118">Возвращает или задает имя узла.</span><span class="sxs-lookup"><span data-stu-id="8f97b-118">Gets or sets the name of the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo[]
Parameter Sets: SetByAzureHDInsightHostInfoParameterSet
Aliases: Host

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f97b-119">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="8f97b-119">-ClusterName</span></span>
<span data-ttu-id="8f97b-120">Возвращает или задает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="8f97b-120">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="8f97b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f97b-121">-DefaultProfile</span></span>
<span data-ttu-id="8f97b-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8f97b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f97b-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8f97b-123">-Name</span></span>
<span data-ttu-id="8f97b-124">Возвращает или задает имя узла.</span><span class="sxs-lookup"><span data-stu-id="8f97b-124">Gets or sets the name of the host.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByNameParameterSet
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f97b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8f97b-125">-PassThru</span></span>
<span data-ttu-id="8f97b-126">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="8f97b-126">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="8f97b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f97b-127">-ResourceGroupName</span></span>
<span data-ttu-id="8f97b-128">Возвращает или задает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8f97b-128">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f97b-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8f97b-129">-Confirm</span></span>
<span data-ttu-id="8f97b-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8f97b-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f97b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f97b-131">-WhatIf</span></span>
<span data-ttu-id="8f97b-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8f97b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f97b-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8f97b-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f97b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f97b-134">CommonParameters</span></span>
<span data-ttu-id="8f97b-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8f97b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f97b-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f97b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f97b-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8f97b-137">INPUTS</span></span>

### <span data-ttu-id="8f97b-138">System. Collections. Generic. IList ' 1 [[Microsoft. Azure. Commands. HDInsight. командлеты. HDInsight, версия = 3.2.0.0, культура = нейтральная, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="8f97b-138">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo, Microsoft.Azure.PowerShell.Cmdlets.HDInsight, Version=3.2.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="8f97b-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f97b-139">OUTPUTS</span></span>

### <span data-ttu-id="8f97b-140">Microsoft. Azure. Management. HDInsight. Models. Cluster</span><span class="sxs-lookup"><span data-stu-id="8f97b-140">Microsoft.Azure.Management.HDInsight.Models.Cluster</span></span>

## <span data-ttu-id="8f97b-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="8f97b-141">NOTES</span></span>

## <span data-ttu-id="8f97b-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f97b-142">RELATED LINKS</span></span>
