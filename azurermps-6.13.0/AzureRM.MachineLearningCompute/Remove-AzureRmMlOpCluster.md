---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/remove-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Remove-AzureRmMlOpCluster.md
ms.openlocfilehash: 5619b9ca4e7f5593a20baf04951d0d5594b31215
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560144"
---
# <span data-ttu-id="448cb-101">Remove-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="448cb-101">Remove-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="448cb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="448cb-102">SYNOPSIS</span></span>
<span data-ttu-id="448cb-103">Удаление кластера операций.</span><span class="sxs-lookup"><span data-stu-id="448cb-103">Removes an operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="448cb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="448cb-104">SYNTAX</span></span>

### <span data-ttu-id="448cb-105">RemoveByNameAndResourceGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="448cb-105">RemoveByNameAndResourceGroup (Default)</span></span>
```
Remove-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> [-IncludeAllResources]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="448cb-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="448cb-106">RemoveByInputObject</span></span>
```
Remove-AzureRmMlOpCluster -InputObject <PSOperationalizationCluster> [-IncludeAllResources]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="448cb-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="448cb-107">RemoveByResourceId</span></span>
```
Remove-AzureRmMlOpCluster -ResourceId <String> [-IncludeAllResources]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="448cb-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="448cb-108">DESCRIPTION</span></span>
<span data-ttu-id="448cb-109">Удаление кластера операций.</span><span class="sxs-lookup"><span data-stu-id="448cb-109">Removes an operationalization cluster.</span></span> <span data-ttu-id="448cb-110">Некоторые ресурсы, связанные с кластером, могут не быть удалены.</span><span class="sxs-lookup"><span data-stu-id="448cb-110">Some resources associated with the cluster might not all be removed.</span></span> <span data-ttu-id="448cb-111">Например, служба контейнера Azure будет удалена, но связанные виртуальные машины — нет.</span><span class="sxs-lookup"><span data-stu-id="448cb-111">For example, the Azure container service will get removed, but the associated VMs do not.</span></span> <span data-ttu-id="448cb-112">Учетная запись хранения, реестр контейнера и Application Insights не удаляются для диагностических данных.</span><span class="sxs-lookup"><span data-stu-id="448cb-112">The storage account, container registry, and application insights are not removed for diagnostic information.</span></span>

## <span data-ttu-id="448cb-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="448cb-113">EXAMPLES</span></span>

### <span data-ttu-id="448cb-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="448cb-114">Example 1</span></span>
```
PS C:\> Remove-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster
```

### <span data-ttu-id="448cb-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="448cb-115">Example 2</span></span>
```
PS C:\> Get-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster | Remove-AzureRmMlOpCluster
```

## <span data-ttu-id="448cb-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="448cb-116">PARAMETERS</span></span>

### <span data-ttu-id="448cb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="448cb-117">-DefaultProfile</span></span>
<span data-ttu-id="448cb-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="448cb-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="448cb-119">-IncludeAllResources</span><span class="sxs-lookup"><span data-stu-id="448cb-119">-IncludeAllResources</span></span>
<span data-ttu-id="448cb-120">Удаляет все ресурсы, созданные в кластере.</span><span class="sxs-lookup"><span data-stu-id="448cb-120">Removes all resources that were created with the cluster.</span></span>

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

### <span data-ttu-id="448cb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="448cb-121">-InputObject</span></span>
<span data-ttu-id="448cb-122">Объект кластера для операции.</span><span class="sxs-lookup"><span data-stu-id="448cb-122">The operationalization cluster object.</span></span>

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

### <span data-ttu-id="448cb-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="448cb-123">-Name</span></span>
<span data-ttu-id="448cb-124">Название кластера операций.</span><span class="sxs-lookup"><span data-stu-id="448cb-124">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="448cb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="448cb-125">-ResourceGroupName</span></span>
<span data-ttu-id="448cb-126">Имя группы ресурсов для кластера операций.</span><span class="sxs-lookup"><span data-stu-id="448cb-126">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="448cb-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="448cb-127">-ResourceId</span></span>
<span data-ttu-id="448cb-128">Идентификатор ресурса Azure для кластера "эксплуатация".</span><span class="sxs-lookup"><span data-stu-id="448cb-128">The Azure resource id for the operationalization cluster.</span></span>

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

### <span data-ttu-id="448cb-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="448cb-129">-Confirm</span></span>
<span data-ttu-id="448cb-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="448cb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="448cb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="448cb-131">-WhatIf</span></span>
<span data-ttu-id="448cb-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="448cb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="448cb-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="448cb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="448cb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="448cb-134">CommonParameters</span></span>
<span data-ttu-id="448cb-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="448cb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="448cb-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="448cb-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="448cb-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="448cb-137">INPUTS</span></span>

### <span data-ttu-id="448cb-138">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="448cb-138">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
<span data-ttu-id="448cb-139">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="448cb-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="448cb-140">System. String</span><span class="sxs-lookup"><span data-stu-id="448cb-140">System.String</span></span>

## <span data-ttu-id="448cb-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="448cb-141">OUTPUTS</span></span>

### <span data-ttu-id="448cb-142">System. void</span><span class="sxs-lookup"><span data-stu-id="448cb-142">System.Void</span></span>

## <span data-ttu-id="448cb-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="448cb-143">NOTES</span></span>

## <span data-ttu-id="448cb-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="448cb-144">RELATED LINKS</span></span>
