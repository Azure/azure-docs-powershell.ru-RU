---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 5B1D72ED-7A1C-4360-B256-0066CC366E28
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/remove-azhdinsightclusterautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Remove-AzHDInsightClusterAutoscaleConfiguration.md
ms.openlocfilehash: 1dbfc382b935a9cc14dc42f85653a337f82ece38
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079058"
---
# <span data-ttu-id="354a1-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="354a1-101">Remove-AzHDInsightClusterAutoscaleConfiguration</span></span>

## <span data-ttu-id="354a1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="354a1-102">SYNOPSIS</span></span>
<span data-ttu-id="354a1-103">Удаляет конфигурацию автоматического масштабирования в кластере HDInsight.</span><span class="sxs-lookup"><span data-stu-id="354a1-103">Removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="354a1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="354a1-104">SYNTAX</span></span>

### <span data-ttu-id="354a1-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="354a1-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [[-ResourceGroupName] <String>] [-ClusterName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="354a1-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="354a1-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="354a1-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="354a1-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzHDInsightClusterAutoscaleConfiguration [-InputObject] <AzureHDInsightCluster> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="354a1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="354a1-108">DESCRIPTION</span></span>
<span data-ttu-id="354a1-109">Командлет **Remove-AzHDInsightClusterAutoscaleConfiguration** удаляет конфигурацию автомасштабирования в кластере HDInsight.</span><span class="sxs-lookup"><span data-stu-id="354a1-109">The **Remove-AzHDInsightClusterAutoscaleConfiguration** cmdlet removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="354a1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="354a1-110">EXAMPLES</span></span>

### <span data-ttu-id="354a1-111">Пример 1: Удаление конфигурации автомасштабирования в кластере HDInsight.</span><span class="sxs-lookup"><span data-stu-id="354a1-111">Example 1: Remove the autoscale configuration of the HDInsight cluster.</span></span>
```powershell
PS C:\> $clusterResourceGroup="group"
PS C:\> $clusterName="MyCluster"
PS C:\> Remove-AzHDInsightClusterAutoscaleConfiguration -ResourceGroupName $clusterResourceGroup -ClusterName $clusterName
```

<span data-ttu-id="354a1-112">Эта команда удаляет конфигурацию автоматического масштабирования в кластере HDInsight.</span><span class="sxs-lookup"><span data-stu-id="354a1-112">This command removes the autoscale configuration of the HDInsight cluster.</span></span>

## <span data-ttu-id="354a1-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="354a1-113">PARAMETERS</span></span>

### <span data-ttu-id="354a1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="354a1-114">-AsJob</span></span>
<span data-ttu-id="354a1-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="354a1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="354a1-116">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="354a1-116">-ClusterName</span></span>
<span data-ttu-id="354a1-117">Возвращает или задает имя кластера.</span><span class="sxs-lookup"><span data-stu-id="354a1-117">Gets or sets the name of the cluster.</span></span>

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

### <span data-ttu-id="354a1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="354a1-118">-DefaultProfile</span></span>
<span data-ttu-id="354a1-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="354a1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="354a1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="354a1-120">-InputObject</span></span>
<span data-ttu-id="354a1-121">Возвращает или задает объект ввода.</span><span class="sxs-lookup"><span data-stu-id="354a1-121">Gets or sets the input object.</span></span>

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

### <span data-ttu-id="354a1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="354a1-122">-ResourceGroupName</span></span>
<span data-ttu-id="354a1-123">Возвращает или задает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="354a1-123">Gets or sets the name of the resource group.</span></span>

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

### <span data-ttu-id="354a1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="354a1-124">-ResourceId</span></span>
<span data-ttu-id="354a1-125">Возвращает или задает идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="354a1-125">Gets or sets the resource id.</span></span>

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

### <span data-ttu-id="354a1-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="354a1-126">-Confirm</span></span>
<span data-ttu-id="354a1-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="354a1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="354a1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="354a1-128">-WhatIf</span></span>
<span data-ttu-id="354a1-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="354a1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="354a1-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="354a1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="354a1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="354a1-131">CommonParameters</span></span>
<span data-ttu-id="354a1-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="354a1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="354a1-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="354a1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="354a1-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="354a1-134">INPUTS</span></span>

### <span data-ttu-id="354a1-135">System. String</span><span class="sxs-lookup"><span data-stu-id="354a1-135">System.String</span></span>

### <span data-ttu-id="354a1-136">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="354a1-136">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster</span></span>

## <span data-ttu-id="354a1-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="354a1-137">OUTPUTS</span></span>

### <span data-ttu-id="354a1-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="354a1-138">System.Boolean</span></span>

## <span data-ttu-id="354a1-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="354a1-139">NOTES</span></span>

## <span data-ttu-id="354a1-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="354a1-140">RELATED LINKS</span></span>

<span data-ttu-id="354a1-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md) 
 [Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span><span class="sxs-lookup"><span data-stu-id="354a1-141">[New-AzHDInsightClusterAutoscaleConfiguration](./New-AzHDInsightClusterAutoscaleConfiguration.md)
[Set-AzHDInsightClusterAutoscaleConfiguration](./Set-AzHDInsightClusterAutoscaleConfiguration.md)
[Get-AzHDInsightClusterAutoscaleConfiguration](./Get-AzHDInsightClusterAutoscaleConfiguration.md)</span></span>
