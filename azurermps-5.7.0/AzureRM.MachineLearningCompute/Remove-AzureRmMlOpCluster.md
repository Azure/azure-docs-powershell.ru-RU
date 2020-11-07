---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/remove-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
ms.openlocfilehash: 9836856ffd663939de8ca0e28635d81785c9c898
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "93735208"
---
# <span data-ttu-id="e8f87-101">Remove-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="e8f87-101">Remove-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="e8f87-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e8f87-102">SYNOPSIS</span></span>
<span data-ttu-id="e8f87-103">Удаление кластера операций.</span><span class="sxs-lookup"><span data-stu-id="e8f87-103">Removes an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8f87-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e8f87-104">SYNTAX</span></span>

### <span data-ttu-id="e8f87-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e8f87-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeAllResources] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8f87-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="e8f87-106">RemoveByInputObject</span></span>
```
Remove-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeAllResources] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8f87-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="e8f87-107">RemoveByResourceId</span></span>
```
Remove-AzureRmMlOpCluster -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeAllResources] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e8f87-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8f87-108">DESCRIPTION</span></span>
<span data-ttu-id="e8f87-109">Удаление кластера операций.</span><span class="sxs-lookup"><span data-stu-id="e8f87-109">Removes an operationalization cluster.</span></span> <span data-ttu-id="e8f87-110">Некоторые ресурсы, связанные с кластером, могут не быть удалены.</span><span class="sxs-lookup"><span data-stu-id="e8f87-110">Some resources associated with the cluster might not all be removed.</span></span> <span data-ttu-id="e8f87-111">Например, служба контейнера Azure будет удалена, но связанные виртуальные машины — нет.</span><span class="sxs-lookup"><span data-stu-id="e8f87-111">For example, the Azure container service will get removed, but the associated VMs do not.</span></span> <span data-ttu-id="e8f87-112">Учетная запись хранения, реестр контейнера и Application Insights не удаляются для диагностических данных.</span><span class="sxs-lookup"><span data-stu-id="e8f87-112">The storage account, container registry, and application insights are not removed for diagnostic information.</span></span>

## <span data-ttu-id="e8f87-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e8f87-113">EXAMPLES</span></span>

### <span data-ttu-id="e8f87-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e8f87-114">Example 1</span></span>
```
PS C:\> Remove-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="e8f87-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e8f87-115">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzureRmMlOpCluster
```

## <span data-ttu-id="e8f87-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e8f87-116">PARAMETERS</span></span>

### <span data-ttu-id="e8f87-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8f87-117">-DefaultProfile</span></span>
<span data-ttu-id="e8f87-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e8f87-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8f87-119">-IncludeAllResources</span><span class="sxs-lookup"><span data-stu-id="e8f87-119">-IncludeAllResources</span></span>
<span data-ttu-id="e8f87-120">Удаляет все ресурсы, созданные в кластере.</span><span class="sxs-lookup"><span data-stu-id="e8f87-120">Removes all resources that were created with the cluster.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8f87-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8f87-121">-InputObject</span></span>
<span data-ttu-id="e8f87-122">Объект кластера для операции.</span><span class="sxs-lookup"><span data-stu-id="e8f87-122">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: RemoveByInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e8f87-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e8f87-123">-Name</span></span>
<span data-ttu-id="e8f87-124">Название кластера операций.</span><span class="sxs-lookup"><span data-stu-id="e8f87-124">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8f87-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8f87-125">-ResourceGroupName</span></span>
<span data-ttu-id="e8f87-126">Имя группы ресурсов для кластера операций.</span><span class="sxs-lookup"><span data-stu-id="e8f87-126">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8f87-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8f87-127">-ResourceId</span></span>
<span data-ttu-id="e8f87-128">Идентификатор ресурса Azure для кластера "эксплуатация".</span><span class="sxs-lookup"><span data-stu-id="e8f87-128">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8f87-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8f87-129">-Confirm</span></span>
<span data-ttu-id="e8f87-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e8f87-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8f87-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8f87-131">-WhatIf</span></span>
<span data-ttu-id="e8f87-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e8f87-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8f87-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e8f87-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8f87-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8f87-134">CommonParameters</span></span>
<span data-ttu-id="e8f87-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e8f87-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8f87-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8f87-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8f87-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e8f87-137">INPUTS</span></span>

### <span data-ttu-id="e8f87-138">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="e8f87-138">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="e8f87-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e8f87-139">System.String</span></span>

## <span data-ttu-id="e8f87-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e8f87-140">OUTPUTS</span></span>

### <span data-ttu-id="e8f87-141">System. void</span><span class="sxs-lookup"><span data-stu-id="e8f87-141">System.Void</span></span>

## <span data-ttu-id="e8f87-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="e8f87-142">NOTES</span></span>

## <span data-ttu-id="e8f87-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e8f87-143">RELATED LINKS</span></span>

