---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlOpCluster.md
ms.openlocfilehash: de297c94be69773d07efedfae42ccc029fc13414
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93899741"
---
# <span data-ttu-id="8707a-101">Remove-AzMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="8707a-101">Remove-AzMlOpCluster</span></span>

## <span data-ttu-id="8707a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8707a-102">SYNOPSIS</span></span>
<span data-ttu-id="8707a-103">Удаление кластера операций.</span><span class="sxs-lookup"><span data-stu-id="8707a-103">Removes an operationalization cluster.</span></span>

## <span data-ttu-id="8707a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8707a-104">SYNTAX</span></span>

### <span data-ttu-id="8707a-105">RemoveByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8707a-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzMlOpCluster -ResourceGroupName <String> -Name <String> [-IncludeAllResources]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8707a-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="8707a-106">RemoveByInputObject</span></span>
```
Remove-AzMlOpCluster -InputObject <PSOperationalizationCluster> [-IncludeAllResources]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8707a-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="8707a-107">RemoveByResourceId</span></span>
```
Remove-AzMlOpCluster -ResourceId <String> [-IncludeAllResources] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8707a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8707a-108">DESCRIPTION</span></span>
<span data-ttu-id="8707a-109">Удаление кластера операций.</span><span class="sxs-lookup"><span data-stu-id="8707a-109">Removes an operationalization cluster.</span></span> <span data-ttu-id="8707a-110">Некоторые ресурсы, связанные с кластером, могут не быть удалены.</span><span class="sxs-lookup"><span data-stu-id="8707a-110">Some resources associated with the cluster might not all be removed.</span></span> <span data-ttu-id="8707a-111">Например, служба контейнера Azure будет удалена, но связанные виртуальные машины — нет.</span><span class="sxs-lookup"><span data-stu-id="8707a-111">For example, the Azure container service will get removed, but the associated VMs do not.</span></span> <span data-ttu-id="8707a-112">Учетная запись хранения, реестр контейнера и Application Insights не удаляются для диагностических данных.</span><span class="sxs-lookup"><span data-stu-id="8707a-112">The storage account, container registry, and application insights are not removed for diagnostic information.</span></span>

## <span data-ttu-id="8707a-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8707a-113">EXAMPLES</span></span>

### <span data-ttu-id="8707a-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8707a-114">Example 1</span></span>
```
PS C:\> Remove-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="8707a-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8707a-115">Example 2</span></span>
```
PS C:\> Get-AzMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzMlOpCluster
```

## <span data-ttu-id="8707a-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8707a-116">PARAMETERS</span></span>

### <span data-ttu-id="8707a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8707a-117">-DefaultProfile</span></span>
<span data-ttu-id="8707a-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8707a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8707a-119">-IncludeAllResources</span><span class="sxs-lookup"><span data-stu-id="8707a-119">-IncludeAllResources</span></span>
<span data-ttu-id="8707a-120">Удаляет все ресурсы, созданные в кластере.</span><span class="sxs-lookup"><span data-stu-id="8707a-120">Removes all resources that were created with the cluster.</span></span>

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

### <span data-ttu-id="8707a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8707a-121">-InputObject</span></span>
<span data-ttu-id="8707a-122">Объект кластера для операции.</span><span class="sxs-lookup"><span data-stu-id="8707a-122">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: RemoveByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8707a-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8707a-123">-Name</span></span>
<span data-ttu-id="8707a-124">Название кластера операций.</span><span class="sxs-lookup"><span data-stu-id="8707a-124">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8707a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8707a-125">-ResourceGroupName</span></span>
<span data-ttu-id="8707a-126">Имя группы ресурсов для кластера операций.</span><span class="sxs-lookup"><span data-stu-id="8707a-126">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8707a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8707a-127">-ResourceId</span></span>
<span data-ttu-id="8707a-128">Идентификатор ресурса Azure для кластера "эксплуатация".</span><span class="sxs-lookup"><span data-stu-id="8707a-128">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8707a-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8707a-129">-Confirm</span></span>
<span data-ttu-id="8707a-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8707a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8707a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8707a-131">-WhatIf</span></span>
<span data-ttu-id="8707a-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8707a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8707a-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8707a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8707a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8707a-134">CommonParameters</span></span>
<span data-ttu-id="8707a-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8707a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8707a-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8707a-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8707a-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8707a-137">INPUTS</span></span>

### <span data-ttu-id="8707a-138">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="8707a-138">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="8707a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8707a-139">System.String</span></span>

## <span data-ttu-id="8707a-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8707a-140">OUTPUTS</span></span>

### <span data-ttu-id="8707a-141">System. void</span><span class="sxs-lookup"><span data-stu-id="8707a-141">System.Void</span></span>

## <span data-ttu-id="8707a-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="8707a-142">NOTES</span></span>

## <span data-ttu-id="8707a-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8707a-143">RELATED LINKS</span></span>
