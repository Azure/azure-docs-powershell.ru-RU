---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelalertruletemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelAlertRuleTemplate.md
ms.openlocfilehash: aa5dabced1439d8a754e220d56f7309c7b2df3e0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217612"
---
# <span data-ttu-id="fa51f-101">Get-AzSentinelAlertRuleTemplate</span><span class="sxs-lookup"><span data-stu-id="fa51f-101">Get-AzSentinelAlertRuleTemplate</span></span>

## <span data-ttu-id="fa51f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa51f-102">SYNOPSIS</span></span>
<span data-ttu-id="fa51f-103">Получить шаблон аналитического правила.</span><span class="sxs-lookup"><span data-stu-id="fa51f-103">Get Analytic Rule Template.</span></span>

## <span data-ttu-id="fa51f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fa51f-104">SYNTAX</span></span>

### <span data-ttu-id="fa51f-105">WorkspaceScope (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fa51f-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa51f-106">AlertRuleTemplateId</span><span class="sxs-lookup"><span data-stu-id="fa51f-106">AlertRuleTemplateId</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceGroupName <String> -WorkspaceName <String>
 -AlertRuleTemplateId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa51f-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa51f-107">ResourceId</span></span>
```
Get-AzSentinelAlertRuleTemplate -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fa51f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fa51f-108">DESCRIPTION</span></span>
<span data-ttu-id="fa51f-109">Для получения шаблона правила оповещения из указанной рабочей области возвращается **cmdlet Get-AzSentinelAlertRuleTemplate.**</span><span class="sxs-lookup"><span data-stu-id="fa51f-109">The **Get-AzSentinelAlertRuleTemplate** cmdlet gets an Alert Rule Template from the specified workspace.</span></span>
<span data-ttu-id="fa51f-110">Если указать параметр *AlertRuleTemplateId,* возвращается один **объект AlertRuleTemplate.**</span><span class="sxs-lookup"><span data-stu-id="fa51f-110">If you specify the *AlertRuleTemplateId* parameter, a single **AlertRuleTemplate** object is returned.</span></span>
<span data-ttu-id="fa51f-111">Если параметр *AlertRuleTemplateId* не задан, возвращается массив, содержащий все шаблоны правил оповещения в указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="fa51f-111">If you do not specify the *AlertRuleTemplateId* parameter, an array containing all of the Alert Rule Templates in the specified workspace are returned.</span></span>
<span data-ttu-id="fa51f-112">Объект **AlertRuleTemplate можно** использовать для создания нового правила оповещения.</span><span class="sxs-lookup"><span data-stu-id="fa51f-112">You can use the **AlertRuleTemplate** object to create a new Alert Rule.</span></span>

## <span data-ttu-id="fa51f-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fa51f-113">EXAMPLES</span></span>

### <span data-ttu-id="fa51f-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fa51f-114">Example 1</span></span>
```powershell
PS C:\> $AlertRuleTemplates = Get-AzSentinelAlertRuleTemplate -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="fa51f-115">В этом примере все **alertRuleTemplates** в указанной рабочей области сохраняется в переменной $AlertRuleTemplates Оповещения.</span><span class="sxs-lookup"><span data-stu-id="fa51f-115">This example gets all of the **AlertRuleTemplates** in the specified workspace, and then stores it in the $AlertRuleTemplates variable.</span></span>

### <span data-ttu-id="fa51f-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fa51f-116">Example 2</span></span>
```powershell
PS C:\> $AlertRuleTemplate = Get-AzSentinelAlertRuleTemplate -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AlertRuleTemplateId "MyAlertRuleTemplateId"
```

<span data-ttu-id="fa51f-117">В этом примере **alertRuleTemplate в** указанной рабочей области сохраняется в переменной $AlertRuleTemplate AlertRuleTemplate.</span><span class="sxs-lookup"><span data-stu-id="fa51f-117">This example gets an **AlertRuleTemplate** in the specified workspace, and then stores it in the $AlertRuleTemplate variable.</span></span>

## <span data-ttu-id="fa51f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa51f-118">PARAMETERS</span></span>

### <span data-ttu-id="fa51f-119">-AlertRuleTemplateId</span><span class="sxs-lookup"><span data-stu-id="fa51f-119">-AlertRuleTemplateId</span></span>
<span data-ttu-id="fa51f-120">Шаблон ид правила оповещения шаблона.</span><span class="sxs-lookup"><span data-stu-id="fa51f-120">Template Alert Rule Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AlertRuleTemplateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fa51f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa51f-121">-DefaultProfile</span></span>
<span data-ttu-id="fa51f-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fa51f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa51f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa51f-123">-ResourceGroupName</span></span>
<span data-ttu-id="fa51f-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fa51f-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleTemplateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa51f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa51f-125">-ResourceId</span></span>
<span data-ttu-id="fa51f-126">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="fa51f-126">Resource Id.</span></span>

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

### <span data-ttu-id="fa51f-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="fa51f-127">-WorkspaceName</span></span>
<span data-ttu-id="fa51f-128">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="fa51f-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, AlertRuleTemplateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa51f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa51f-129">CommonParameters</span></span>
<span data-ttu-id="fa51f-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa51f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa51f-131">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa51f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa51f-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fa51f-132">INPUTS</span></span>

### <span data-ttu-id="fa51f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="fa51f-133">System.String</span></span>
## <span data-ttu-id="fa51f-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fa51f-134">OUTPUTS</span></span>

### <span data-ttu-id="fa51f-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRuleTemplates.PSSentinelAlertRuleTemplate</span><span class="sxs-lookup"><span data-stu-id="fa51f-135">Microsoft.Azure.Commands.SecurityInsights.Models.AlertRuleTemplates.PSSentinelAlertRuleTemplate</span></span>
## <span data-ttu-id="fa51f-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fa51f-136">NOTES</span></span>

## <span data-ttu-id="fa51f-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fa51f-137">RELATED LINKS</span></span>
