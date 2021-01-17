---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/restart-azhdinsighthost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Restart-AzHDInsightHost.md
ms.openlocfilehash: 4e0b5fda29696fb45515c3b478b9dc29ff67263e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322940"
---
# <span data-ttu-id="2bdc9-101">Restart-AzHDInsightHost</span><span class="sxs-lookup"><span data-stu-id="2bdc9-101">Restart-AzHDInsightHost</span></span>

## <span data-ttu-id="2bdc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bdc9-102">SYNOPSIS</span></span>
<span data-ttu-id="2bdc9-103">Перезапуск конкретных хостов кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2bdc9-103">Restarts the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="2bdc9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2bdc9-104">SYNTAX</span></span>

### <span data-ttu-id="2bdc9-105">SetByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2bdc9-105">SetByNameParameterSet (Default)</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String> [-Name] <String[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bdc9-106">SetByAzureHDInsightHostInfoParameterSet</span><span class="sxs-lookup"><span data-stu-id="2bdc9-106">SetByAzureHDInsightHostInfoParameterSet</span></span>
```
Restart-AzHDInsightHost [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AzureHDInsightHostInfo] <AzureHDInsightHostInfo[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bdc9-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2bdc9-107">DESCRIPTION</span></span>
<span data-ttu-id="2bdc9-108">Этот **проектлет Restart-AzHDInsightHost** перезапустит определенные hosts of HDInsight.</span><span class="sxs-lookup"><span data-stu-id="2bdc9-108">This **Restart-AzHDInsightHost** cmdlet restart the specific hosts of HDInsight cluster.</span></span>

## <span data-ttu-id="2bdc9-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2bdc9-109">EXAMPLES</span></span>

### <span data-ttu-id="2bdc9-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2bdc9-110">Example 1</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> Restart-AzHDInsightHost -ClusterName $clusterName -Name wn0, wn1
```

<span data-ttu-id="2bdc9-111">Эта команда перезапускет два хлама кластера: worknode1, worknode2.</span><span class="sxs-lookup"><span data-stu-id="2bdc9-111">This command restarts two hosts of the cluster: worknode1, worknode2.</span></span>

### <span data-ttu-id="2bdc9-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2bdc9-112">Example 2</span></span>
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $worknode1= Get-AzHDInsightHost -ClusterName $clusterName | Where-Object {$_.Name -like "wn1*"}
PS C:\> $worknode1 | Restart-AzHDInsightHost -ClusterName $clusterName
```

<span data-ttu-id="2bdc9-113">Эта команда показывает, как работать вместе с командлетом Get-AzHDInsightHost.</span><span class="sxs-lookup"><span data-stu-id="2bdc9-113">This command shows how to cooperate with the cmdlet 'Get-AzHDInsightHost'.</span></span>

## <span data-ttu-id="2bdc9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2bdc9-114">PARAMETERS</span></span>

### <span data-ttu-id="2bdc9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2bdc9-115">-AsJob</span></span>
<span data-ttu-id="2bdc9-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="2bdc9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2bdc9-117">-AzureHDInsightHostInfo</span><span class="sxs-lookup"><span data-stu-id="2bdc9-117">-AzureHDInsightHostInfo</span></span>
<span data-ttu-id="2bdc9-118">Возвращает или задает имя хоста.</span><span class="sxs-lookup"><span data-stu-id="2bdc9-118">Gets or sets the name of the host.</span></span>

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

### <span data-ttu-id="2bdc9-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2bdc9-119">-ClusterName</span></span>
<span data-ttu-id="2bdc9-120">Возвращает или задает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="2bdc9-120">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="2bdc9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bdc9-121">-DefaultProfile</span></span>
<span data-ttu-id="2bdc9-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2bdc9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bdc9-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2bdc9-123">-Name</span></span>
<span data-ttu-id="2bdc9-124">Возвращает или задает имя хоста.</span><span class="sxs-lookup"><span data-stu-id="2bdc9-124">Gets or sets the name of the host.</span></span>

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

### <span data-ttu-id="2bdc9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2bdc9-125">-PassThru</span></span>
<span data-ttu-id="2bdc9-126">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="2bdc9-126">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="2bdc9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bdc9-127">-ResourceGroupName</span></span>
<span data-ttu-id="2bdc9-128">Возвращает или задает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2bdc9-128">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="2bdc9-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2bdc9-129">-Confirm</span></span>
<span data-ttu-id="2bdc9-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bdc9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bdc9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bdc9-131">-WhatIf</span></span>
<span data-ttu-id="2bdc9-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bdc9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bdc9-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2bdc9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bdc9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bdc9-134">CommonParameters</span></span>
<span data-ttu-id="2bdc9-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bdc9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bdc9-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2bdc9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bdc9-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2bdc9-137">INPUTS</span></span>

### <span data-ttu-id="2bdc9-138">System.String[]</span><span class="sxs-lookup"><span data-stu-id="2bdc9-138">System.String[]</span></span>

### <span data-ttu-id="2bdc9-139">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo[]</span><span class="sxs-lookup"><span data-stu-id="2bdc9-139">Microsoft.Azure.Commands.HDInsight.Models.Management.AzureHDInsightHostInfo[]</span></span>

## <span data-ttu-id="2bdc9-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2bdc9-140">OUTPUTS</span></span>

### <span data-ttu-id="2bdc9-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2bdc9-141">System.Boolean</span></span>

## <span data-ttu-id="2bdc9-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2bdc9-142">NOTES</span></span>

## <span data-ttu-id="2bdc9-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2bdc9-143">RELATED LINKS</span></span>
