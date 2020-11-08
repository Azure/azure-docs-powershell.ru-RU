---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: 34f8b99ef4c8958415780fecb98c291d2845209d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065459"
---
# <span data-ttu-id="c6999-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="c6999-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="c6999-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c6999-102">SYNOPSIS</span></span>
<span data-ttu-id="c6999-103">Удаление назначения из подписки.</span><span class="sxs-lookup"><span data-stu-id="c6999-103">Remove a blueprint assignment from a subscription.</span></span>

## <span data-ttu-id="c6999-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c6999-104">SYNTAX</span></span>

### <span data-ttu-id="c6999-105">DeleteBlueprintAssignmentByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c6999-105">DeleteBlueprintAssignmentByName (Default)</span></span>
```
Remove-AzBlueprintAssignment [[-SubscriptionId] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6999-106">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="c6999-106">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment [[-SubscriptionId] <String>] [-InputObject] <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6999-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6999-107">DESCRIPTION</span></span>
<span data-ttu-id="c6999-108">Удалить план, который был назначен для подписки.</span><span class="sxs-lookup"><span data-stu-id="c6999-108">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="c6999-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c6999-109">EXAMPLES</span></span>

### <span data-ttu-id="c6999-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c6999-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="c6999-111">Удаление задания из плана, указанного именем из указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="c6999-111">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="c6999-112">Командлет запросит подтверждение перед выполнением команды.</span><span class="sxs-lookup"><span data-stu-id="c6999-112">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="c6999-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c6999-113">PARAMETERS</span></span>

### <span data-ttu-id="c6999-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6999-114">-DefaultProfile</span></span>
<span data-ttu-id="c6999-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c6999-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6999-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6999-116">-InputObject</span></span>
<span data-ttu-id="c6999-117">Объект назначения «чертеж».</span><span class="sxs-lookup"><span data-stu-id="c6999-117">Blueprint assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6999-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c6999-118">-Name</span></span>
<span data-ttu-id="c6999-119">Имя назначения для схемы.</span><span class="sxs-lookup"><span data-stu-id="c6999-119">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6999-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6999-120">-PassThru</span></span>
<span data-ttu-id="c6999-121">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="c6999-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c6999-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c6999-122">-SubscriptionId</span></span>
<span data-ttu-id="c6999-123">Идентификатор подписки, на которую развертывается назначение.</span><span class="sxs-lookup"><span data-stu-id="c6999-123">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6999-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6999-124">-Confirm</span></span>
<span data-ttu-id="c6999-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c6999-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6999-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6999-126">-WhatIf</span></span>
<span data-ttu-id="c6999-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c6999-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6999-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c6999-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6999-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6999-129">CommonParameters</span></span>
<span data-ttu-id="c6999-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c6999-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6999-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6999-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6999-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c6999-132">INPUTS</span></span>

### <span data-ttu-id="c6999-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c6999-133">System.String</span></span>

### <span data-ttu-id="c6999-134">Microsoft. Azure. Commands. чертеж. Models. PSBlueprintAssignment []</span><span class="sxs-lookup"><span data-stu-id="c6999-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="c6999-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6999-135">OUTPUTS</span></span>

### <span data-ttu-id="c6999-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="c6999-136">System.Object</span></span>
## <span data-ttu-id="c6999-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="c6999-137">NOTES</span></span>

## <span data-ttu-id="c6999-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c6999-138">RELATED LINKS</span></span>
