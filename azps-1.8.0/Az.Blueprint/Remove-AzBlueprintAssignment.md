---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: ccf76449bf2f7e904cbfe6e2507e067df7661dae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731434"
---
# <span data-ttu-id="20e33-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="20e33-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="20e33-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="20e33-102">SYNOPSIS</span></span>
<span data-ttu-id="20e33-103">Удаление назначения из подписки.</span><span class="sxs-lookup"><span data-stu-id="20e33-103">Remove a blueprint assignment from a subscription.</span></span>

## <span data-ttu-id="20e33-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="20e33-104">SYNTAX</span></span>

### <span data-ttu-id="20e33-105">DeleteBlueprintAssignmentByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="20e33-105">DeleteBlueprintAssignmentByName (Default)</span></span>
```
Remove-AzBlueprintAssignment [[-SubscriptionId] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20e33-106">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="20e33-106">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment [[-SubscriptionId] <String>] [-InputObject] <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20e33-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="20e33-107">DESCRIPTION</span></span>
<span data-ttu-id="20e33-108">Удалить план, который был назначен для подписки.</span><span class="sxs-lookup"><span data-stu-id="20e33-108">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="20e33-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="20e33-109">EXAMPLES</span></span>

### <span data-ttu-id="20e33-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="20e33-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="20e33-111">Удаление задания из плана, указанного именем из указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="20e33-111">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="20e33-112">Командлет запросит подтверждение перед выполнением команды.</span><span class="sxs-lookup"><span data-stu-id="20e33-112">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="20e33-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="20e33-113">PARAMETERS</span></span>

### <span data-ttu-id="20e33-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20e33-114">-DefaultProfile</span></span>
<span data-ttu-id="20e33-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="20e33-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20e33-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20e33-116">-InputObject</span></span>
<span data-ttu-id="20e33-117">Объект назначения «чертеж».</span><span class="sxs-lookup"><span data-stu-id="20e33-117">Blueprint assignment object.</span></span>

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

### <span data-ttu-id="20e33-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="20e33-118">-Name</span></span>
<span data-ttu-id="20e33-119">Имя назначения для схемы.</span><span class="sxs-lookup"><span data-stu-id="20e33-119">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="20e33-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20e33-120">-PassThru</span></span>
<span data-ttu-id="20e33-121">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="20e33-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="20e33-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="20e33-122">-SubscriptionId</span></span>
<span data-ttu-id="20e33-123">Идентификатор подписки, на которую развертывается назначение.</span><span class="sxs-lookup"><span data-stu-id="20e33-123">Subscription Id the blueprint assignment is deployed to.</span></span>

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

### <span data-ttu-id="20e33-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20e33-124">-Confirm</span></span>
<span data-ttu-id="20e33-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="20e33-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20e33-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20e33-126">-WhatIf</span></span>
<span data-ttu-id="20e33-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="20e33-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20e33-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="20e33-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20e33-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20e33-129">CommonParameters</span></span>
<span data-ttu-id="20e33-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="20e33-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20e33-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20e33-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20e33-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="20e33-132">INPUTS</span></span>

### <span data-ttu-id="20e33-133">System. String</span><span class="sxs-lookup"><span data-stu-id="20e33-133">System.String</span></span>

### <span data-ttu-id="20e33-134">Microsoft. Azure. Commands. чертеж. Models. PSBlueprintAssignment []</span><span class="sxs-lookup"><span data-stu-id="20e33-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="20e33-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="20e33-135">OUTPUTS</span></span>

### <span data-ttu-id="20e33-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="20e33-136">System.Object</span></span>
## <span data-ttu-id="20e33-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="20e33-137">NOTES</span></span>

## <span data-ttu-id="20e33-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="20e33-138">RELATED LINKS</span></span>
