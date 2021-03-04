---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/get-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
ms.openlocfilehash: 375eca319a1db467e97addac50faa3f91fe0ecc5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954867"
---
# <span data-ttu-id="0ede3-101">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="0ede3-101">Get-AzBlueprintAssignment</span></span>

## <span data-ttu-id="0ede3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ede3-102">SYNOPSIS</span></span>
<span data-ttu-id="0ede3-103">Получите одно или несколько заданий по работе с чертежами.</span><span class="sxs-lookup"><span data-stu-id="0ede3-103">Get one or more blueprint assignments.</span></span>

## <span data-ttu-id="0ede3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0ede3-104">SYNTAX</span></span>

### <span data-ttu-id="0ede3-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0ede3-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprintAssignment [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ede3-106">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="0ede3-106">BySubscriptionAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ede3-107">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="0ede3-107">ByManagementGroupAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ede3-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="0ede3-108">ManagementGroupScope</span></span>
```
Get-AzBlueprintAssignment -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ede3-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0ede3-109">DESCRIPTION</span></span>
<span data-ttu-id="0ede3-110">Получите одно или несколько заданий по работе с чертежами.</span><span class="sxs-lookup"><span data-stu-id="0ede3-110">Get one or more blueprint assignments.</span></span> <span data-ttu-id="0ede3-111">В области подписки есть задания Blueprint.</span><span class="sxs-lookup"><span data-stu-id="0ede3-111">Blueprint assignments exist at the subscription scope.</span></span>

## <span data-ttu-id="0ede3-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0ede3-112">EXAMPLES</span></span>

### <span data-ttu-id="0ede3-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0ede3-113">Example 1</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000"

Name              : Assignment-PS-BlueprintDefinition
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/Assignment-PS-BlueprintDefinition
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : AllResourcesReadOnly
ProvisioningState : Succeeded
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="0ede3-114">Получите задания чертежа в рамках указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="0ede3-114">Get the blueprint assignments within the specified subscription.</span></span>

### <span data-ttu-id="0ede3-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0ede3-115">Example 2</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myAssignmentName"
```

<span data-ttu-id="0ede3-116">Получите название чертежа с указанным именем в пределах указанной подписки.</span><span class="sxs-lookup"><span data-stu-id="0ede3-116">Get the blueprint assignment with the given name within the specified subscription.</span></span>

### <span data-ttu-id="0ede3-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="0ede3-117">Example 3</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup"
```

<span data-ttu-id="0ede3-118">Получите задания по работе с чертежами в пределах указанной группы управления.</span><span class="sxs-lookup"><span data-stu-id="0ede3-118">Get the blueprint assignments within the specified management group.</span></span>

### <span data-ttu-id="0ede3-119">Пример 4</span><span class="sxs-lookup"><span data-stu-id="0ede3-119">Example 4</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup" -Name "myAssignmentName"
```

<span data-ttu-id="0ede3-120">Получите название проекта с указанным именем в указанной группе управления.</span><span class="sxs-lookup"><span data-stu-id="0ede3-120">Get the blueprint assignment with the given name within the specified management group.</span></span>

## <span data-ttu-id="0ede3-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0ede3-121">PARAMETERS</span></span>

### <span data-ttu-id="0ede3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ede3-122">-DefaultProfile</span></span>
<span data-ttu-id="0ede3-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0ede3-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ede3-124">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="0ede3-124">-ManagementGroupId</span></span>
<span data-ttu-id="0ede3-125">ИД группы управления, в которой сохранено назначение "Чертеж".</span><span class="sxs-lookup"><span data-stu-id="0ede3-125">The ID of the management group where the Blueprint assignment is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupAndName, ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ede3-126">-Name</span><span class="sxs-lookup"><span data-stu-id="0ede3-126">-Name</span></span>
<span data-ttu-id="0ede3-127">Название задания «Чертеж».</span><span class="sxs-lookup"><span data-stu-id="0ede3-127">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName, ByManagementGroupAndName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ede3-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0ede3-128">-SubscriptionId</span></span>
<span data-ttu-id="0ede3-129">Для этого развернется подписка с ИД чертежа.</span><span class="sxs-lookup"><span data-stu-id="0ede3-129">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, BySubscriptionAndName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ede3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ede3-130">CommonParameters</span></span>
<span data-ttu-id="0ede3-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ede3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ede3-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ede3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ede3-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0ede3-133">INPUTS</span></span>

### <span data-ttu-id="0ede3-134">System.String</span><span class="sxs-lookup"><span data-stu-id="0ede3-134">System.String</span></span>

## <span data-ttu-id="0ede3-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0ede3-135">OUTPUTS</span></span>

### <span data-ttu-id="0ede3-136">System.Object</span><span class="sxs-lookup"><span data-stu-id="0ede3-136">System.Object</span></span>
## <span data-ttu-id="0ede3-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0ede3-137">NOTES</span></span>

## <span data-ttu-id="0ede3-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0ede3-138">RELATED LINKS</span></span>
