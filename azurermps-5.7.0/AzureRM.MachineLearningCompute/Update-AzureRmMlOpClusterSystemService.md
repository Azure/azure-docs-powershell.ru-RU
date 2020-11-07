---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/update-azurermmlopclustersystemservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/Update-AzureRmMlOpClusterSystemService.md
ms.openlocfilehash: 01f826746b92dd5aa82416e8207305b945ddb711
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733047"
---
# <span data-ttu-id="26752-101">Update-AzureRmMlOpClusterSystemService</span><span class="sxs-lookup"><span data-stu-id="26752-101">Update-AzureRmMlOpClusterSystemService</span></span>

## <span data-ttu-id="26752-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="26752-102">SYNOPSIS</span></span>
<span data-ttu-id="26752-103">Запускает обновление системных служб для кластера операций.</span><span class="sxs-lookup"><span data-stu-id="26752-103">Starts an update on the operationalization cluster's system services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26752-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="26752-104">SYNTAX</span></span>

### <span data-ttu-id="26752-105">StartUpdateWithNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="26752-105">StartUpdateWithNameAndResourceGroup</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26752-106">StartUpdateWithInputObject</span><span class="sxs-lookup"><span data-stu-id="26752-106">StartUpdateWithInputObject</span></span>
```
Update-AzureRmMlOpClusterSystemService -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26752-107">StartUpdateWithResourceId</span><span class="sxs-lookup"><span data-stu-id="26752-107">StartUpdateWithResourceId</span></span>
```
Update-AzureRmMlOpClusterSystemService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26752-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26752-108">DESCRIPTION</span></span>
<span data-ttu-id="26752-109">Системные службы могут обновляться независимо от кластера операций.</span><span class="sxs-lookup"><span data-stu-id="26752-109">The system services can be updated independently from the operationalization cluster.</span></span> <span data-ttu-id="26752-110">Чтобы запустить обновление на системных службах, используйте этот командлет.</span><span class="sxs-lookup"><span data-stu-id="26752-110">To start an update on the system services use this cmdlet.</span></span> <span data-ttu-id="26752-111">Если обновление недоступно, обновление будет запущено, и оно будет успешно возвращено.</span><span class="sxs-lookup"><span data-stu-id="26752-111">If no update is available an update will still be started and will return successfully.</span></span> <span data-ttu-id="26752-112">После того как обновление будет завершено, оно закончится, когда оно будет запущено, завершено и успешно.</span><span class="sxs-lookup"><span data-stu-id="26752-112">Once the update is finished it reports when it started, finished, and if it was successful.</span></span>

## <span data-ttu-id="26752-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="26752-113">EXAMPLES</span></span>

### <span data-ttu-id="26752-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="26752-114">Example 1</span></span>
```
PS C:\> Update-AzureRmMlOpClusterSystemService -ResourceGroupName my-group -Name my-cluster
```

<span data-ttu-id="26752-115">Запускает обновление системных служб в указанном кластере.</span><span class="sxs-lookup"><span data-stu-id="26752-115">Starts a system services update on the specified cluster.</span></span> 

## <span data-ttu-id="26752-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="26752-116">PARAMETERS</span></span>

### <span data-ttu-id="26752-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26752-117">-DefaultProfile</span></span>
<span data-ttu-id="26752-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="26752-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26752-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26752-119">-InputObject</span></span>
<span data-ttu-id="26752-120">Объект кластера для операции.</span><span class="sxs-lookup"><span data-stu-id="26752-120">The operationalization cluster object.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: StartUpdateWithInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26752-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="26752-121">-Name</span></span>
<span data-ttu-id="26752-122">Название кластера операций.</span><span class="sxs-lookup"><span data-stu-id="26752-122">The name of the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: StartUpdateWithNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26752-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26752-123">-ResourceGroupName</span></span>
<span data-ttu-id="26752-124">Имя группы ресурсов для кластера операций.</span><span class="sxs-lookup"><span data-stu-id="26752-124">The name of the resource group for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: StartUpdateWithNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26752-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="26752-125">-ResourceId</span></span>
<span data-ttu-id="26752-126">Идентификатор ресурса Azure для кластера "эксплуатация".</span><span class="sxs-lookup"><span data-stu-id="26752-126">The Azure resource id for the operationalization cluster.</span></span>

```yaml
Type: String
Parameter Sets: StartUpdateWithResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26752-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26752-127">-Confirm</span></span>
<span data-ttu-id="26752-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="26752-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26752-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26752-129">-WhatIf</span></span>
<span data-ttu-id="26752-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="26752-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26752-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="26752-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26752-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26752-132">CommonParameters</span></span>
<span data-ttu-id="26752-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="26752-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26752-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26752-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26752-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="26752-135">INPUTS</span></span>

### <span data-ttu-id="26752-136">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="26752-136">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

### <span data-ttu-id="26752-137">System. String</span><span class="sxs-lookup"><span data-stu-id="26752-137">System.String</span></span>

## <span data-ttu-id="26752-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="26752-138">OUTPUTS</span></span>

### <span data-ttu-id="26752-139">Microsoft. Azure. Commands. MachineLearningCompute. Models. PSUpdateSystemServicesResponse</span><span class="sxs-lookup"><span data-stu-id="26752-139">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSUpdateSystemServicesResponse</span></span>

## <span data-ttu-id="26752-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="26752-140">NOTES</span></span>

## <span data-ttu-id="26752-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26752-141">RELATED LINKS</span></span>

