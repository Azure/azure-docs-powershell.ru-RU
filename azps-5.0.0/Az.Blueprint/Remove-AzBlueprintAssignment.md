---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: 40452c250b58edf4d1e45f54c953dee8c433c436
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246097"
---
# <span data-ttu-id="55f7c-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="55f7c-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="55f7c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="55f7c-102">SYNOPSIS</span></span>
<span data-ttu-id="55f7c-103">Удаление назначения из подписки или группы управления.</span><span class="sxs-lookup"><span data-stu-id="55f7c-103">Remove a blueprint assignment from a subscription or a management group.</span></span>

## <span data-ttu-id="55f7c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="55f7c-104">SYNTAX</span></span>

### <span data-ttu-id="55f7c-105">BySubscriptionAndName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="55f7c-105">BySubscriptionAndName (Default)</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [[-SubscriptionId] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55f7c-106">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="55f7c-106">ByManagementGroupAndName</span></span>
```
Remove-AzBlueprintAssignment [-Name] <String> [-ManagementGroupId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="55f7c-107">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="55f7c-107">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment -InputObject <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55f7c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="55f7c-108">DESCRIPTION</span></span>
<span data-ttu-id="55f7c-109">Удалить план, который был назначен для подписки.</span><span class="sxs-lookup"><span data-stu-id="55f7c-109">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="55f7c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="55f7c-110">EXAMPLES</span></span>

### <span data-ttu-id="55f7c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="55f7c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="55f7c-112">Удаление задания из плана, указанного именем из указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="55f7c-112">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="55f7c-113">Командлет запросит подтверждение перед выполнением команды.</span><span class="sxs-lookup"><span data-stu-id="55f7c-113">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="55f7c-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="55f7c-114">PARAMETERS</span></span>

### <span data-ttu-id="55f7c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55f7c-115">-DefaultProfile</span></span>
<span data-ttu-id="55f7c-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="55f7c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55f7c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="55f7c-117">-InputObject</span></span>
<span data-ttu-id="55f7c-118">Объект назначения «чертеж».</span><span class="sxs-lookup"><span data-stu-id="55f7c-118">Blueprint assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55f7c-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="55f7c-119">-ManagementGroupId</span></span>
<span data-ttu-id="55f7c-120">Идентификатор группы управления, в которой сохранено назначение чертежей.</span><span class="sxs-lookup"><span data-stu-id="55f7c-120">The ID of the management group where the Blueprint assignment is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55f7c-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="55f7c-121">-Name</span></span>
<span data-ttu-id="55f7c-122">Имя назначения для схемы.</span><span class="sxs-lookup"><span data-stu-id="55f7c-122">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, ByManagementGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55f7c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="55f7c-123">-PassThru</span></span>
<span data-ttu-id="55f7c-124">После установки командлет возвращает объект, который представляет собой удаленное назначение.</span><span class="sxs-lookup"><span data-stu-id="55f7c-124">When set, the cmdlet will return an object representing the removed Blueprint assignment.</span></span> <span data-ttu-id="55f7c-125">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="55f7c-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="55f7c-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="55f7c-126">-SubscriptionId</span></span>
<span data-ttu-id="55f7c-127">Идентификатор подписки, на которую развертывается назначение.</span><span class="sxs-lookup"><span data-stu-id="55f7c-127">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55f7c-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="55f7c-128">-Confirm</span></span>
<span data-ttu-id="55f7c-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="55f7c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55f7c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55f7c-130">-WhatIf</span></span>
<span data-ttu-id="55f7c-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="55f7c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55f7c-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="55f7c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55f7c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55f7c-133">CommonParameters</span></span>
<span data-ttu-id="55f7c-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="55f7c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55f7c-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="55f7c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55f7c-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="55f7c-136">INPUTS</span></span>

### <span data-ttu-id="55f7c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="55f7c-137">System.String</span></span>

### <span data-ttu-id="55f7c-138">Microsoft. Azure. Commands. чертеж. Models. PSBlueprintAssignment []</span><span class="sxs-lookup"><span data-stu-id="55f7c-138">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="55f7c-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="55f7c-139">OUTPUTS</span></span>

### <span data-ttu-id="55f7c-140">System. Object</span><span class="sxs-lookup"><span data-stu-id="55f7c-140">System.Object</span></span>
## <span data-ttu-id="55f7c-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="55f7c-141">NOTES</span></span>

## <span data-ttu-id="55f7c-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="55f7c-142">RELATED LINKS</span></span>
