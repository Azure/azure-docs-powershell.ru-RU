---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5B1D72ED-7A1C-4360-B256-0066CC366E28
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 1dbfc382b935a9cc14dc42f85653a337f82ece38
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234273"
---
# <span data-ttu-id="76dca-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="76dca-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="76dca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76dca-102">SYNOPSIS</span></span>
<span data-ttu-id="76dca-103">Удаляет настройку автоматических шкал кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="76dca-103">Removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="76dca-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="76dca-104">SYNTAX</span></span>

### <span data-ttu-id="76dca-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="76dca-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76dca-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="76dca-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76dca-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76dca-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76dca-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76dca-108">DESCRIPTION</span></span>
<span data-ttu-id="76dca-109">Для удаления из кластера **HDInsightClusterAutoscaleConfiguration** удаляется настройка автомасштабирования кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="76dca-109">The **Remove-AzHDInsightClusterAutoscaleConfiguration** cmdlet removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="76dca-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="76dca-110">EXAMPLES</span></span>

### <span data-ttu-id="76dca-111">Пример 1. Удаление настройки автомасштабы кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="76dca-111">Example 1: Remove the autoscale configuration of the HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Remove-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="76dca-112">Эта команда удаляет конфигурацию автомасштабы кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="76dca-112">This command removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="76dca-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76dca-113">PARAMETERS</span></span>

### <span data-ttu-id="76dca-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76dca-114">-AsJob</span></span>
<span data-ttu-id="76dca-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="76dca-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="76dca-116">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="76dca-116">-ClusterName</span></span>
<span data-ttu-id="76dca-117">Возвращает или задает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="76dca-117">Gets or sets the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76dca-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76dca-118">-DefaultProfile</span></span>
<span data-ttu-id="76dca-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="76dca-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76dca-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="76dca-120">-InputObject</span></span>
<span data-ttu-id="76dca-121">Возвращает или устанавливает объект ввода.</span><span class="sxs-lookup"><span data-stu-id="76dca-121">Gets or sets the input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76dca-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76dca-122">-ResourceGroupName</span></span>
<span data-ttu-id="76dca-123">Возвращает или задает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="76dca-123">Gets or sets the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76dca-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76dca-124">-ResourceId</span></span>
<span data-ttu-id="76dca-125">Возвращает или задает ид ресурса.</span><span class="sxs-lookup"><span data-stu-id="76dca-125">Gets or sets the resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76dca-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76dca-126">-Confirm</span></span>
<span data-ttu-id="76dca-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76dca-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76dca-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76dca-128">-WhatIf</span></span>
<span data-ttu-id="76dca-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76dca-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76dca-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="76dca-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76dca-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76dca-131">CommonParameters</span></span>
<span data-ttu-id="76dca-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76dca-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76dca-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76dca-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76dca-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="76dca-134">INPUTS</span></span>

### <span data-ttu-id="76dca-135">System.String</span><span class="sxs-lookup"><span data-stu-id="76dca-135">System.String</span></span>

### <span data-ttu-id="76dca-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="76dca-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="76dca-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="76dca-137">OUTPUTS</span></span>

### <span data-ttu-id="76dca-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="76dca-138">System.Boolean</span></span>

## <span data-ttu-id="76dca-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="76dca-139">NOTES</span></span>

## <span data-ttu-id="76dca-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76dca-140">RELATED LINKS</span></span>

<span data-ttu-id="76dca-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="76dca-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
