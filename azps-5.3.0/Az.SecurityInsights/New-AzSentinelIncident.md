---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncident.md
ms.openlocfilehash: b3618f178ea5dee54991c037da78ac51f2ed4502
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517561"
---
# <span data-ttu-id="23ef3-101">New-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="23ef3-101">New-AzSentinelIncident</span></span>

## <span data-ttu-id="23ef3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23ef3-102">SYNOPSIS</span></span>
<span data-ttu-id="23ef3-103">Создать инцидент.</span><span class="sxs-lookup"><span data-stu-id="23ef3-103">Create an Incident.</span></span>

## <span data-ttu-id="23ef3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="23ef3-104">SYNTAX</span></span>

```
New-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> [-IncidentId <String>]
 [-Classificaton <String>] [-ClassificationComment <String>] [-ClassificationReason <String>]
 [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23ef3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23ef3-105">DESCRIPTION</span></span>
<span data-ttu-id="23ef3-106">**Новый-AzSentinelIncident** создает инцидент из указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="23ef3-106">The **New-AzSentinelIncident** cmdlet creates a Incident from the specified workspace.</span></span>
<span data-ttu-id="23ef3-107">Параметр Confirm  и переменная $ConfirmPreference Windows PowerShell можно использовать для управления запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23ef3-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="23ef3-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="23ef3-108">EXAMPLES</span></span>

### <span data-ttu-id="23ef3-109">Пример 1</span><span class="sxs-lookup"><span data-stu-id="23ef3-109">Example 1</span></span>
```powershell
PS C:\> $Incident = New-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Title "NewIncident" -Severity Low -Status New
```

<span data-ttu-id="23ef3-110">В этом примере создается **инцидент** в указанной рабочей области, а затем он сохраняется в переменной $Incident безопасности.</span><span class="sxs-lookup"><span data-stu-id="23ef3-110">This example creates an **Incident** in the specified workspace, and then stores it in the $Incident variable.</span></span>

## <span data-ttu-id="23ef3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23ef3-111">PARAMETERS</span></span>

### <span data-ttu-id="23ef3-112">-ClassificationComment</span><span class="sxs-lookup"><span data-stu-id="23ef3-112">-ClassificationComment</span></span>
<span data-ttu-id="23ef3-113">Комментарий к классу инцидентов.</span><span class="sxs-lookup"><span data-stu-id="23ef3-113">Incident Classificaiton Comment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23ef3-114">-ClassificationReason</span><span class="sxs-lookup"><span data-stu-id="23ef3-114">-ClassificationReason</span></span>
<span data-ttu-id="23ef3-115">Incident Classificaiton Reason.</span><span class="sxs-lookup"><span data-stu-id="23ef3-115">Incident Classificaiton Reason.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: InaccurateData, IncorrectAlertLogic, SuspiciousActivity, SuspiciousButExpected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23ef3-116">-Classificaton</span><span class="sxs-lookup"><span data-stu-id="23ef3-116">-Classificaton</span></span>
<span data-ttu-id="23ef3-117">Incident Classificaiton.</span><span class="sxs-lookup"><span data-stu-id="23ef3-117">Incident Classificaiton.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: BenignPositive, FalsePositive, TruePositive, Undetermined

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23ef3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23ef3-118">-DefaultProfile</span></span>
<span data-ttu-id="23ef3-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="23ef3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23ef3-120">-Description</span><span class="sxs-lookup"><span data-stu-id="23ef3-120">-Description</span></span>
<span data-ttu-id="23ef3-121">Описание.</span><span class="sxs-lookup"><span data-stu-id="23ef3-121">Description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23ef3-122">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="23ef3-122">-IncidentId</span></span>
<span data-ttu-id="23ef3-123">ИД инцидента.</span><span class="sxs-lookup"><span data-stu-id="23ef3-123">Incident Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23ef3-124">-Label</span><span class="sxs-lookup"><span data-stu-id="23ef3-124">-Label</span></span>
<span data-ttu-id="23ef3-125">Метки инцидентов.</span><span class="sxs-lookup"><span data-stu-id="23ef3-125">Incident Labels.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23ef3-126">-Владелец</span><span class="sxs-lookup"><span data-stu-id="23ef3-126">-Owner</span></span>
<span data-ttu-id="23ef3-127">Владелец инцидента.</span><span class="sxs-lookup"><span data-stu-id="23ef3-127">Incident Owner.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23ef3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23ef3-128">-ResourceGroupName</span></span>
<span data-ttu-id="23ef3-129">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="23ef3-129">Resource group name.</span></span>

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

### <span data-ttu-id="23ef3-130">-Severity</span><span class="sxs-lookup"><span data-stu-id="23ef3-130">-Severity</span></span>
<span data-ttu-id="23ef3-131">Серьезность инцидента.</span><span class="sxs-lookup"><span data-stu-id="23ef3-131">Incident Severity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: High, Informational, Low, Medium

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23ef3-132">-Status</span><span class="sxs-lookup"><span data-stu-id="23ef3-132">-Status</span></span>
<span data-ttu-id="23ef3-133">"Состояние инцидента".</span><span class="sxs-lookup"><span data-stu-id="23ef3-133">Incident Status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Active, Closed, New

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23ef3-134">-Title</span><span class="sxs-lookup"><span data-stu-id="23ef3-134">-Title</span></span>
<span data-ttu-id="23ef3-135">Название инцидента.</span><span class="sxs-lookup"><span data-stu-id="23ef3-135">Incident Title.</span></span>

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

### <span data-ttu-id="23ef3-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="23ef3-136">-WorkspaceName</span></span>
<span data-ttu-id="23ef3-137">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="23ef3-137">Workspace Name.</span></span>

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

### <span data-ttu-id="23ef3-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23ef3-138">-Confirm</span></span>
<span data-ttu-id="23ef3-139">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23ef3-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23ef3-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23ef3-140">-WhatIf</span></span>
<span data-ttu-id="23ef3-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23ef3-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="23ef3-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="23ef3-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23ef3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23ef3-143">CommonParameters</span></span>
<span data-ttu-id="23ef3-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23ef3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23ef3-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="23ef3-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23ef3-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="23ef3-146">INPUTS</span></span>

### <span data-ttu-id="23ef3-147">System.Collections.Generic.IList'1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="23ef3-147">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
### <span data-ttu-id="23ef3-148">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="23ef3-148">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span></span>
## <span data-ttu-id="23ef3-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="23ef3-149">OUTPUTS</span></span>

### <span data-ttu-id="23ef3-150">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="23ef3-150">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="23ef3-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="23ef3-151">NOTES</span></span>

## <span data-ttu-id="23ef3-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23ef3-152">RELATED LINKS</span></span>
