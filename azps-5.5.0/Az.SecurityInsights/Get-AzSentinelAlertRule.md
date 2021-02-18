---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRule.md
ms.openlocfilehash: 02dc3b58d9cd4b4be58b83f36cc6e42e11008812
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231956"
---
# <span data-ttu-id="433d0-101">Get-AzSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="433d0-101">Get-AzSentinelAlertRule</span></span>

## <span data-ttu-id="433d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="433d0-102">SYNOPSIS</span></span>
<span data-ttu-id="433d0-103">Возвращает аналитическое правило (правило оповещения).</span><span class="sxs-lookup"><span data-stu-id="433d0-103">Gets an Analytic (Alert Rule).</span></span>

## <span data-ttu-id="433d0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="433d0-104">SYNTAX</span></span>

### <span data-ttu-id="433d0-105">WorkspaceScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="433d0-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="433d0-106">AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="433d0-106">AlertRuleId</span></span>
```
Get-AzSentinelAlertRule -ResourceGroupName <String> -WorkspaceName <String> -AlertRuleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="433d0-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="433d0-107">ResourceId</span></span>
```
Get-AzSentinelAlertRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="433d0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="433d0-108">DESCRIPTION</span></span>
<span data-ttu-id="433d0-109">Для этой рабочей области **cmdlet Get-AzSentinelAlertRule** получает правило аналитики (правило оповещения).</span><span class="sxs-lookup"><span data-stu-id="433d0-109">The **Get-AzSentinelAlertRule** cmdlet gets an Analytic (Alert Rule) from the specified workspace.</span></span>
<span data-ttu-id="433d0-110">Если указать параметр *AlertRuleId,* возвращается один **объект AlertRule.**</span><span class="sxs-lookup"><span data-stu-id="433d0-110">If you specify the *AlertRuleId* parameter, a single **AlertRule** object is returned.</span></span>
<span data-ttu-id="433d0-111">Если не указать параметр *AlertRuleId,* возвращается массив, содержащий все правила оповещения в указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="433d0-111">If you do not specify the *AlertRuleId* parameter, an array containing all of the Alert Rules in the specified workspace are returned.</span></span>
<span data-ttu-id="433d0-112">Для обновления **alertRule** можно использовать объект AlertRule, например отключить **alertRule.**</span><span class="sxs-lookup"><span data-stu-id="433d0-112">You can use the **AlertRule** object to update the AlertRule, for example you can disable the **AlertRule**.</span></span>

## <span data-ttu-id="433d0-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="433d0-113">EXAMPLES</span></span>

### <span data-ttu-id="433d0-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="433d0-114">Example 1</span></span>
```powershell
PS C:\> $AlertRules = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="433d0-115">В этом примере все **alertRules** в указанной рабочей области сохраняется в переменной $AlertRules AlertRules.</span><span class="sxs-lookup"><span data-stu-id="433d0-115">This example gets all of the **AlertRules** in the specified workspace, and then stores it in the $AlertRules variable.</span></span>

### <span data-ttu-id="433d0-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="433d0-116">Example 2</span></span>
```powershell
PS C:\> $AlertRule = Get-AzSentinelAlertRule -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleId "MyAlertRuleId"
```

<span data-ttu-id="433d0-117">В этом примере в указанной рабочей области возвращается значение **AlertRule,** а затем $AlertRule переменной.</span><span class="sxs-lookup"><span data-stu-id="433d0-117">This example gets an **AlertRule** in the specified workspace, and then stores it in the $AlertRule variable.</span></span>

## <span data-ttu-id="433d0-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="433d0-118">PARAMETERS</span></span>

### <span data-ttu-id="433d0-119">-AlertRuleId</span><span class="sxs-lookup"><span data-stu-id="433d0-119">-AlertRuleId</span></span>
<span data-ttu-id="433d0-120">ИД правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="433d0-120">Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="433d0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="433d0-121">-DefaultProfile</span></span>
<span data-ttu-id="433d0-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="433d0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="433d0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="433d0-123">-ResourceGroupName</span></span>
<span data-ttu-id="433d0-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="433d0-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="433d0-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="433d0-125">-ResourceId</span></span>
<span data-ttu-id="433d0-126">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="433d0-126">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="433d0-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="433d0-127">-WorkspaceName</span></span>
<span data-ttu-id="433d0-128">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="433d0-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="433d0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="433d0-129">CommonParameters</span></span>
<span data-ttu-id="433d0-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="433d0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="433d0-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="433d0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="433d0-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="433d0-132">INPUTS</span></span>

### <span data-ttu-id="433d0-133">System.String</span><span class="sxs-lookup"><span data-stu-id="433d0-133">System.String</span></span>
## <span data-ttu-id="433d0-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="433d0-134">OUTPUTS</span></span>

### <span data-ttu-id="433d0-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span><span class="sxs-lookup"><span data-stu-id="433d0-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRules.PSSentinelAlertRule</span></span>
## <span data-ttu-id="433d0-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="433d0-136">NOTES</span></span>

## <span data-ttu-id="433d0-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="433d0-137">RELATED LINKS</span></span>
