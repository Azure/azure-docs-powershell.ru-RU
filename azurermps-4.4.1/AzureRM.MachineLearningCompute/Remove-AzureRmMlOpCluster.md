---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
ms.openlocfilehash: 63e401c09a2d224b53d260855990198a409d4846
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733107"
---
# <span data-ttu-id="3f0ef-101">Remove-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="3f0ef-101">Remove-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="3f0ef-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3f0ef-102">SYNOPSIS</span></span>
<span data-ttu-id="3f0ef-103">Удаление кластера операций.</span><span class="sxs-lookup"><span data-stu-id="3f0ef-103">Removes an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f0ef-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3f0ef-104">SYNTAX</span></span>

### <span data-ttu-id="3f0ef-105">Удаление кластера выопераций из входных параметров командлета.</span><span class="sxs-lookup"><span data-stu-id="3f0ef-105">Remove an operationalization cluster from cmdlet input parameters.</span></span>
```
Remove-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="3f0ef-106">Удаление кластера выопераций из определения экземпляра OperationalizationCluster.</span><span class="sxs-lookup"><span data-stu-id="3f0ef-106">Remove an operationalization cluster from an OperationalizationCluster instance definition.</span></span>
```
Remove-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="3f0ef-107">Удаление кластера выопераций из идентификатора ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="3f0ef-107">Remove an operationalization cluster from an Azure resouce id.</span></span>
```
Remove-AzureRmMlOpCluster -ResourceId <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="3f0ef-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f0ef-108">DESCRIPTION</span></span>
<span data-ttu-id="3f0ef-109">Удаление кластера операций.</span><span class="sxs-lookup"><span data-stu-id="3f0ef-109">Removes an operationalization cluster.</span></span> <span data-ttu-id="3f0ef-110">Некоторые ресурсы, связанные с кластером, могут не быть удалены.</span><span class="sxs-lookup"><span data-stu-id="3f0ef-110">Some resources associated with the cluster might not all be removed.</span></span> <span data-ttu-id="3f0ef-111">Например, служба контейнера Azure будет удалена, но связанные виртуальные машины — нет.</span><span class="sxs-lookup"><span data-stu-id="3f0ef-111">For example, the Azure container service will get removed, but the associated VMs do not.</span></span> <span data-ttu-id="3f0ef-112">Учетная запись хранения, реестр контейнера и Application Insights не удаляются для диагностических данных.</span><span class="sxs-lookup"><span data-stu-id="3f0ef-112">The storage account, container registry, and application insights are not removed for diagnostic information.</span></span>

## <span data-ttu-id="3f0ef-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3f0ef-113">EXAMPLES</span></span>

### <span data-ttu-id="3f0ef-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3f0ef-114">Example 1</span></span>
```
PS C:\> Remove-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="3f0ef-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="3f0ef-115">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzureRmMlOpCluster 
```

## <span data-ttu-id="3f0ef-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3f0ef-116">PARAMETERS</span></span>

### <span data-ttu-id="3f0ef-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f0ef-117">-InputObject</span></span>
<span data-ttu-id="3f0ef-118">Объект кластера для операции.</span><span class="sxs-lookup"><span data-stu-id="3f0ef-118">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Remove an operationalization cluster from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f0ef-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3f0ef-119">-Confirm</span></span>
<span data-ttu-id="3f0ef-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3f0ef-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f0ef-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3f0ef-121">-Name</span></span>
<span data-ttu-id="3f0ef-122">Название кластера операций.</span><span class="sxs-lookup"><span data-stu-id="3f0ef-122">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f0ef-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f0ef-123">-ResourceGroupName</span></span>
<span data-ttu-id="3f0ef-124">Имя группы ресурсов для кластера операций.</span><span class="sxs-lookup"><span data-stu-id="3f0ef-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f0ef-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f0ef-125">-ResourceId</span></span>
<span data-ttu-id="3f0ef-126">Идентификатор ресурса Azure для кластера "эксплуатация".</span><span class="sxs-lookup"><span data-stu-id="3f0ef-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Remove an operationalization cluster from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f0ef-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f0ef-127">-WhatIf</span></span>
<span data-ttu-id="3f0ef-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3f0ef-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f0ef-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3f0ef-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="3f0ef-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3f0ef-130">INPUTS</span></span>

### <span data-ttu-id="3f0ef-131">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="3f0ef-131">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="3f0ef-132">System. String</span><span class="sxs-lookup"><span data-stu-id="3f0ef-132">System.String</span></span>


## <span data-ttu-id="3f0ef-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3f0ef-133">OUTPUTS</span></span>

### <span data-ttu-id="3f0ef-134">System. void</span><span class="sxs-lookup"><span data-stu-id="3f0ef-134">System.Void</span></span>


## <span data-ttu-id="3f0ef-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="3f0ef-135">NOTES</span></span>

## <span data-ttu-id="3f0ef-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3f0ef-136">RELATED LINKS</span></span>

