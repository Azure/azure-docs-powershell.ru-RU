---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintAssignment.md
ms.openlocfilehash: 06398b9c5e880577606e0367722fc22c242d58f4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246112"
---
# <span data-ttu-id="c0def-101">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="c0def-101">Get-AzBlueprintAssignment</span></span>

## <span data-ttu-id="c0def-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c0def-102">SYNOPSIS</span></span>
<span data-ttu-id="c0def-103">Получение одного или нескольких назначений для чертежей.</span><span class="sxs-lookup"><span data-stu-id="c0def-103">Get one or more blueprint assignments.</span></span>

## <span data-ttu-id="c0def-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c0def-104">SYNTAX</span></span>

### <span data-ttu-id="c0def-105">SubscriptionScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c0def-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprintAssignment [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0def-106">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="c0def-106">BySubscriptionAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0def-107">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="c0def-107">ByManagementGroupAndName</span></span>
```
Get-AzBlueprintAssignment -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0def-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="c0def-108">ManagementGroupScope</span></span>
```
Get-AzBlueprintAssignment -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0def-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0def-109">DESCRIPTION</span></span>
<span data-ttu-id="c0def-110">Получение одного или нескольких назначений для чертежей.</span><span class="sxs-lookup"><span data-stu-id="c0def-110">Get one or more blueprint assignments.</span></span> <span data-ttu-id="c0def-111">В области подписок существуют назначения для планов.</span><span class="sxs-lookup"><span data-stu-id="c0def-111">Blueprint assignments exist at the subscription scope.</span></span>

## <span data-ttu-id="c0def-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c0def-112">EXAMPLES</span></span>

### <span data-ttu-id="c0def-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c0def-113">Example 1</span></span>
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

<span data-ttu-id="c0def-114">Получение назначений в заданной подписке.</span><span class="sxs-lookup"><span data-stu-id="c0def-114">Get the blueprint assignments within the specified subscription.</span></span>

### <span data-ttu-id="c0def-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c0def-115">Example 2</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myAssignmentName"
```

<span data-ttu-id="c0def-116">Получение задания из плана с заданным именем в указанной подписке.</span><span class="sxs-lookup"><span data-stu-id="c0def-116">Get the blueprint assignment with the given name within the specified subscription.</span></span>

### <span data-ttu-id="c0def-117">Пример 3</span><span class="sxs-lookup"><span data-stu-id="c0def-117">Example 3</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup"
```

<span data-ttu-id="c0def-118">Получение назначений в заданной группе управления.</span><span class="sxs-lookup"><span data-stu-id="c0def-118">Get the blueprint assignments within the specified management group.</span></span>

### <span data-ttu-id="c0def-119">Пример 4</span><span class="sxs-lookup"><span data-stu-id="c0def-119">Example 4</span></span>
```powershell
PS C:\> Get-AzBlueprintAssignment -ManagementGroupId "myManagementGroup" -Name "myAssignmentName"
```

<span data-ttu-id="c0def-120">Получение задания из схемы с заданным именем в указанной группе управления.</span><span class="sxs-lookup"><span data-stu-id="c0def-120">Get the blueprint assignment with the given name within the specified management group.</span></span>

## <span data-ttu-id="c0def-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c0def-121">PARAMETERS</span></span>

### <span data-ttu-id="c0def-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0def-122">-DefaultProfile</span></span>
<span data-ttu-id="c0def-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c0def-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0def-124">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="c0def-124">-ManagementGroupId</span></span>
<span data-ttu-id="c0def-125">Идентификатор группы управления, в которой сохранено назначение чертежей.</span><span class="sxs-lookup"><span data-stu-id="c0def-125">The ID of the management group where the Blueprint assignment is saved.</span></span>

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

### <span data-ttu-id="c0def-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c0def-126">-Name</span></span>
<span data-ttu-id="c0def-127">Имя назначения для схемы.</span><span class="sxs-lookup"><span data-stu-id="c0def-127">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="c0def-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c0def-128">-SubscriptionId</span></span>
<span data-ttu-id="c0def-129">Идентификатор подписки, на которую развертывается назначение.</span><span class="sxs-lookup"><span data-stu-id="c0def-129">Subscription Id the blueprint assignment is deployed to.</span></span>

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

### <span data-ttu-id="c0def-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0def-130">CommonParameters</span></span>
<span data-ttu-id="c0def-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c0def-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0def-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c0def-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0def-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c0def-133">INPUTS</span></span>

### <span data-ttu-id="c0def-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c0def-134">System.String</span></span>

## <span data-ttu-id="c0def-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c0def-135">OUTPUTS</span></span>

### <span data-ttu-id="c0def-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="c0def-136">System.Object</span></span>
## <span data-ttu-id="c0def-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="c0def-137">NOTES</span></span>

## <span data-ttu-id="c0def-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c0def-138">RELATED LINKS</span></span>
