---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertruleaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleAction.md
ms.openlocfilehash: 6e60f4ed93dd3963fa748db250cacfcf0aeecce3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225284"
---
# <span data-ttu-id="0f0f7-101">Get-AzSentinelAlertRuleAction</span><span class="sxs-lookup"><span data-stu-id="0f0f7-101">Get-AzSentinelAlertRuleAction</span></span>

## <span data-ttu-id="0f0f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f0f7-102">SYNOPSIS</span></span>
<span data-ttu-id="0f0f7-103">Получите автоматический ответ (действие правила оповещения).</span><span class="sxs-lookup"><span data-stu-id="0f0f7-103">Get an Automated Response (Alert Rule Action).</span></span>

## <span data-ttu-id="0f0f7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0f0f7-104">SYNTAX</span></span>

### <span data-ttu-id="0f0f7-105">AlertRuleId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0f0f7-105">AlertRuleId (Default)</span></span>
```
Get-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f0f7-106">ActionId</span><span class="sxs-lookup"><span data-stu-id="0f0f7-106">ActionId</span></span>
```
Get-AzSentinelAlertRuleAction -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 -ActionId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f0f7-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f0f7-107">DESCRIPTION</span></span>
<span data-ttu-id="0f0f7-108">Cmdlet **Get-AzSentinelAlertRuleAction** получает действие "Автоматизированный ответ" (действие правила оповещения) из указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="0f0f7-108">The **Get-AzSentinelAlertRuleAction** cmdlet gets an Automated Response (Alert Rule Action) from the specified workspace.</span></span>
<span data-ttu-id="0f0f7-109">Если указать *параметры ActionId* и *AlertRuleId,* возвращается один **объект AlertRuleAction.**</span><span class="sxs-lookup"><span data-stu-id="0f0f7-109">If you specify the *ActionId* and *AlertRuleId* parameters, a single **AlertRuleAction** object is returned.</span></span>
<span data-ttu-id="0f0f7-110">Если не указать параметр *ActionId,* возвращается массив, содержащий все действия для определенного правила оповещения в указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="0f0f7-110">If you do not specify the *ActionId* parameter, an array containing all of the Actions for the specificed Alert Rule in the specified workspace are returned.</span></span>
<span data-ttu-id="0f0f7-111">Вы можете использовать объект **действия** для обновления действия, например  действие для правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="0f0f7-111">You can use the **Action** object to update the Action, for example you can change the the **Action** for an Alert Rule.</span></span>

## <span data-ttu-id="0f0f7-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0f0f7-112">EXAMPLES</span></span>

### <span data-ttu-id="0f0f7-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0f0f7-113">Example 1</span></span>
```powershell
PS C:\> $AlertRuleActions = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="0f0f7-114">В этом примере  все действия для заданного правила оповещения в указанной рабочей области, а затем $AlertRuleActions переменной.</span><span class="sxs-lookup"><span data-stu-id="0f0f7-114">This example gets all of the **Actions** for the specified Alert Rule in the specified workspace, and then stores it in the $AlertRuleActions variable.</span></span>

### <span data-ttu-id="0f0f7-115">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0f0f7-115">Example 2</span></span>
```powershell
PS C:\> $AlertRuleAction = Get-AzSentinelAlertRuleAction -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId" -ActionId "MyActionId"
```

<span data-ttu-id="0f0f7-116">В этом примере для указанного правила оповещения в указанной рабочей области возвращается правило **alertRuleAction,** а затем оно сохраняется в переменной $AlertRuleAction оповещения.</span><span class="sxs-lookup"><span data-stu-id="0f0f7-116">This example gets an **AlertRuleAction** for the specified Alert Rule in the specified workspace, and then stores it in the $AlertRuleAction variable.</span></span>

## <span data-ttu-id="0f0f7-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f0f7-117">PARAMETERS</span></span>

### <span data-ttu-id="0f0f7-118">-ActionId</span><span class="sxs-lookup"><span data-stu-id="0f0f7-118">-ActionId</span></span>
<span data-ttu-id="0f0f7-119">ИД действия.</span><span class="sxs-lookup"><span data-stu-id="0f0f7-119">Action Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ActionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f0f7-120">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="0f0f7-120">-AlertRuleId</span></span>
<span data-ttu-id="0f0f7-121">ИД правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="0f0f7-121">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f0f7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f0f7-122">-DefaultProfile</span></span>
<span data-ttu-id="0f0f7-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0f0f7-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f0f7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f0f7-124">-ResourceGroupName</span></span>
<span data-ttu-id="0f0f7-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0f0f7-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f0f7-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0f0f7-126">-WorkspaceName</span></span>
<span data-ttu-id="0f0f7-127">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="0f0f7-127">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f0f7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f0f7-128">CommonParameters</span></span>
<span data-ttu-id="0f0f7-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f0f7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f0f7-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f0f7-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f0f7-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0f0f7-131">INPUTS</span></span>

### <span data-ttu-id="0f0f7-132">Нет</span><span class="sxs-lookup"><span data-stu-id="0f0f7-132">None</span></span>
## <span data-ttu-id="0f0f7-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0f0f7-133">OUTPUTS</span></span>

### <span data-ttu-id="0f0f7-134">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span><span class="sxs-lookup"><span data-stu-id="0f0f7-134">Microsoft.Azure.Commands.SecurityInsights.Models.Actions.PSSentinelActionResponse</span></span>
## <span data-ttu-id="0f0f7-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0f0f7-135">NOTES</span></span>

## <span data-ttu-id="0f0f7-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0f0f7-136">RELATED LINKS</span></span>
