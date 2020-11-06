---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
ms.openlocfilehash: fc89ff40c36fc444eec23089288849aa5ffe592c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569352"
---
# <span data-ttu-id="f3640-101">Update-AzureRmMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="f3640-101">Update-AzureRmMlOpClusterSystemService</span></span>

## <span data-ttu-id="f3640-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f3640-102">SYNOPSIS</span></span>
<span data-ttu-id="f3640-103">Запускает обновление системных служб для кластера операций.</span><span class="sxs-lookup"><span data-stu-id="f3640-103">Starts an update on the operationalization cluster's system services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3640-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f3640-104">SYNTAX</span></span>

### <span data-ttu-id="f3640-105">Запустите обновление системных служб с помощью входных параметров командлета.</span><span class="sxs-lookup"><span data-stu-id="f3640-105">Start a system services update from cmdlet input parameters.</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceGroupName <String> -Name <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f3640-106">Запустите обновление системных служб из определения экземпляра PSOperationalizationCluster.</span><span class="sxs-lookup"><span data-stu-id="f3640-106">Start a system services update from an PSOperationalizationCluster instance definition.</span></span>
```
Update-AzureRmMlOpClusterSystemService -InputObject <PSOperationalizationCluster> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="f3640-107">Запустите обновление системных служб из идентификатора Azure ресурс.</span><span class="sxs-lookup"><span data-stu-id="f3640-107">Start a system services update from an Azure resouce id.</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceId <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="f3640-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3640-108">DESCRIPTION</span></span>
<span data-ttu-id="f3640-109">Системные службы могут обновляться независимо от кластера операций.</span><span class="sxs-lookup"><span data-stu-id="f3640-109">The system services can be updated independently from the operationalization cluster.</span></span> <span data-ttu-id="f3640-110">Чтобы запустить обновление на системных службах, используйте этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f3640-110">To start an update on the system services use this cmdlet.</span></span> <span data-ttu-id="f3640-111">Если обновление недоступно, обновление будет запущено, и оно будет успешно возвращено.</span><span class="sxs-lookup"><span data-stu-id="f3640-111">If no update is available an update will still be started and will return successfully.</span></span> <span data-ttu-id="f3640-112">После того как обновление будет завершено, оно закончится, когда оно будет запущено, завершено и успешно.</span><span class="sxs-lookup"><span data-stu-id="f3640-112">Once the update is finished it reports when it started, finished, and if it was successful.</span></span>

## <span data-ttu-id="f3640-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f3640-113">EXAMPLES</span></span>

### <span data-ttu-id="f3640-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f3640-114">Example 1</span></span>
```
PS C:\> Update-AzureRmMlOpClusterSystemService -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="f3640-115">Запускает обновление системных служб в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="f3640-115">Starts a system services update on the specified cluster.</span></span> 

## <span data-ttu-id="f3640-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f3640-116">PARAMETERS</span></span>

### <span data-ttu-id="f3640-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3640-117">-InputObject</span></span>
<span data-ttu-id="f3640-118">Объект кластера для операции.</span><span class="sxs-lookup"><span data-stu-id="f3640-118">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Start a system services update from an PSOperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3640-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3640-119">-Confirm</span></span>
<span data-ttu-id="f3640-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f3640-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3640-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f3640-121">-Name</span></span>
<span data-ttu-id="f3640-122">Название кластера операций.</span><span class="sxs-lookup"><span data-stu-id="f3640-122">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Start a system services update from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3640-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3640-123">-ResourceGroupName</span></span>
<span data-ttu-id="f3640-124">Имя группы ресурсов для кластера операций.</span><span class="sxs-lookup"><span data-stu-id="f3640-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Start a system services update from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3640-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f3640-125">-ResourceId</span></span>
<span data-ttu-id="f3640-126">Идентификатор ресурса Azure для кластера "эксплуатация".</span><span class="sxs-lookup"><span data-stu-id="f3640-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: Start a system services update from an Azure resouce id.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3640-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3640-127">-WhatIf</span></span>
<span data-ttu-id="f3640-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f3640-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3640-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f3640-129">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="f3640-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f3640-130">INPUTS</span></span>

### <span data-ttu-id="f3640-131">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="f3640-131">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>
### <span data-ttu-id="f3640-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f3640-132">System.String</span></span>


## <span data-ttu-id="f3640-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3640-133">OUTPUTS</span></span>

### <span data-ttu-id="f3640-134">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSUpdateSystemServicesResponse</span><span class="sxs-lookup"><span data-stu-id="f3640-134">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSUpdateSystemServicesResponse</span></span>


## <span data-ttu-id="f3640-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="f3640-135">NOTES</span></span>

## <span data-ttu-id="f3640-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3640-136">RELATED LINKS</span></span>

