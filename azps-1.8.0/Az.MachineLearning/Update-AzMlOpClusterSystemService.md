---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearningCompute.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlopclustersystemservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlOpClusterSystemService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlOpClusterSystemService.md
ms.openlocfilehash: 0e673cd74d87cee990130c1fd58b9049eec9ff15
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93899722"
---
# <span data-ttu-id="fc3c8-101">Update-AzMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="fc3c8-101">Update-AzMlOpClusterSystemService</span></span>

## <span data-ttu-id="fc3c8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fc3c8-102">SYNOPSIS</span></span>
<span data-ttu-id="fc3c8-103">Запускает обновление системных служб для кластера операций.</span><span class="sxs-lookup"><span data-stu-id="fc3c8-103">Starts an update on the operationalization cluster's system services.</span></span>

## <span data-ttu-id="fc3c8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fc3c8-104">SYNTAX</span></span>

### <span data-ttu-id="fc3c8-105">StartUpdateWithNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="fc3c8-105">StartUpdateWithNameAndResourceGroup</span></span>
```
Update-AzMlOpClusterSystemService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc3c8-106">StartUpdateWithInputObject</span><span class="sxs-lookup"><span data-stu-id="fc3c8-106">StartUpdateWithInputObject</span></span>
```
Update-AzMlOpClusterSystemService -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc3c8-107">StartUpdateWithResourceId</span><span class="sxs-lookup"><span data-stu-id="fc3c8-107">StartUpdateWithResourceId</span></span>
```
Update-AzMlOpClusterSystemService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc3c8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc3c8-108">DESCRIPTION</span></span>
<span data-ttu-id="fc3c8-109">Системные службы могут обновляться независимо от кластера операций.</span><span class="sxs-lookup"><span data-stu-id="fc3c8-109">The system services can be updated independently from the operationalization cluster.</span></span> <span data-ttu-id="fc3c8-110">Чтобы запустить обновление на системных службах, используйте этот командлет.</span><span class="sxs-lookup"><span data-stu-id="fc3c8-110">To start an update on the system services use this cmdlet.</span></span> <span data-ttu-id="fc3c8-111">Если обновление недоступно, обновление будет запущено, и оно будет успешно возвращено.</span><span class="sxs-lookup"><span data-stu-id="fc3c8-111">If no update is available an update will still be started and will return successfully.</span></span> <span data-ttu-id="fc3c8-112">После того как обновление будет завершено, оно закончится, когда оно будет запущено, завершено и успешно.</span><span class="sxs-lookup"><span data-stu-id="fc3c8-112">Once the update is finished it reports when it started, finished, and if it was successful.</span></span>

## <span data-ttu-id="fc3c8-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fc3c8-113">EXAMPLES</span></span>

### <span data-ttu-id="fc3c8-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fc3c8-114">Example 1</span></span>
```
PS C:\> Update-AzMlOpClusterSystemService -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="fc3c8-115">Запускает обновление системных служб в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="fc3c8-115">Starts a system services update on the specified cluster.</span></span> 

## <span data-ttu-id="fc3c8-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fc3c8-116">PARAMETERS</span></span>

### <span data-ttu-id="fc3c8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc3c8-117">-DefaultProfile</span></span>
<span data-ttu-id="fc3c8-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fc3c8-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc3c8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc3c8-119">-InputObject</span></span>
<span data-ttu-id="fc3c8-120">Объект кластера для операции.</span><span class="sxs-lookup"><span data-stu-id="fc3c8-120">The operationalization cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: StartUpdateWithInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc3c8-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fc3c8-121">-Name</span></span>
<span data-ttu-id="fc3c8-122">Название кластера операций.</span><span class="sxs-lookup"><span data-stu-id="fc3c8-122">The name of the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: StartUpdateWithNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc3c8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc3c8-123">-ResourceGroupName</span></span>
<span data-ttu-id="fc3c8-124">Имя группы ресурсов для кластера операций.</span><span class="sxs-lookup"><span data-stu-id="fc3c8-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: StartUpdateWithNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc3c8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc3c8-125">-ResourceId</span></span>
<span data-ttu-id="fc3c8-126">Идентификатор ресурса Azure для кластера "эксплуатация".</span><span class="sxs-lookup"><span data-stu-id="fc3c8-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: StartUpdateWithResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc3c8-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc3c8-127">-Confirm</span></span>
<span data-ttu-id="fc3c8-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fc3c8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc3c8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc3c8-129">-WhatIf</span></span>
<span data-ttu-id="fc3c8-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fc3c8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc3c8-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fc3c8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc3c8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc3c8-132">CommonParameters</span></span>
<span data-ttu-id="fc3c8-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fc3c8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc3c8-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc3c8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc3c8-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fc3c8-135">INPUTS</span></span>

### <span data-ttu-id="fc3c8-136">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="fc3c8-136">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="fc3c8-137">System. String</span><span class="sxs-lookup"><span data-stu-id="fc3c8-137">System.String</span></span>

## <span data-ttu-id="fc3c8-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc3c8-138">OUTPUTS</span></span>

### <span data-ttu-id="fc3c8-139">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSUpdateSystemServicesResponse</span><span class="sxs-lookup"><span data-stu-id="fc3c8-139">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSUpdateSystemServicesResponse</span></span>

## <span data-ttu-id="fc3c8-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="fc3c8-140">NOTES</span></span>

## <span data-ttu-id="fc3c8-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fc3c8-141">RELATED LINKS</span></span>
