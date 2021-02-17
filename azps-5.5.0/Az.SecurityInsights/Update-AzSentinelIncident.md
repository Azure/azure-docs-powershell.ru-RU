---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelIncident.md
ms.openlocfilehash: c98270b4e69d80e18ba721de0a6379d40d21fc75
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100223193"
---
# <span data-ttu-id="f8bb3-101">Update-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="f8bb3-101">Update-AzSentinelIncident</span></span>

## <span data-ttu-id="f8bb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8bb3-102">SYNOPSIS</span></span>
<span data-ttu-id="f8bb3-103">Обновив инцидент.</span><span class="sxs-lookup"><span data-stu-id="f8bb3-103">Update an Incident.</span></span>

## <span data-ttu-id="f8bb3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f8bb3-104">SYNTAX</span></span>

### <span data-ttu-id="f8bb3-105">IncidentId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f8bb3-105">IncidentId (Default)</span></span>
```
Update-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> -IncidentID <String>
 [-Classification <String>] [-ClassificationComment <String>] [-ClassificationReason <String>]
 [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8bb3-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f8bb3-106">InputObject</span></span>
```
Update-AzSentinelIncident -InputObject <PSSentinelIncident> [-Classification <String>]
 [-ClassificationComment <String>] [-ClassificationReason <String>] [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8bb3-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8bb3-107">ResourceId</span></span>
```
Update-AzSentinelIncident -ResourceId <String> [-Classification <String>] [-ClassificationComment <String>]
 [-ClassificationReason <String>] [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8bb3-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8bb3-108">DESCRIPTION</span></span>
<span data-ttu-id="f8bb3-109">Для инцидентов в указанной рабочей области **обновляется cmdlet Update-AzSentinelIncident.**</span><span class="sxs-lookup"><span data-stu-id="f8bb3-109">The **Update-AzSentinelIncident** cmdlet updates the Incident in the specified workspace.</span></span>
<span data-ttu-id="f8bb3-110">Объект incident **можно** передать в качестве параметра или с помощью оператора конвейера либо указать необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="f8bb3-110">You can pass an **Incident** object as a parameter or by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="f8bb3-111">С помощью переменных *Confirm* и $ConfirmPreference Windows PowerShell можно управлять запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8bb3-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="f8bb3-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f8bb3-112">EXAMPLES</span></span>

### <span data-ttu-id="f8bb3-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f8bb3-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId" -Severity High
```

<span data-ttu-id="f8bb3-114">Команда получает инцидент *incidentid* и задает для свойства *Severity* (Высокая) *уровень важности.*</span><span class="sxs-lookup"><span data-stu-id="f8bb3-114">The command gets the Incident by *IncidentId* and sets the *Severity* property to *High*.</span></span>  <span data-ttu-id="f8bb3-115">Все остальные свойства остаются одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="f8bb3-115">All other properties remain the same.</span></span>

## <span data-ttu-id="f8bb3-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8bb3-116">PARAMETERS</span></span>

### <span data-ttu-id="f8bb3-117">-Классификация</span><span class="sxs-lookup"><span data-stu-id="f8bb3-117">-Classification</span></span>
<span data-ttu-id="f8bb3-118">Incident Classificaiton.</span><span class="sxs-lookup"><span data-stu-id="f8bb3-118">Incident Classificaiton.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: BenignPositive, FalsePositive, TruePositive, Undetermined

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8bb3-119">-ClassificationComment</span><span class="sxs-lookup"><span data-stu-id="f8bb3-119">-ClassificationComment</span></span>
<span data-ttu-id="f8bb3-120">Комментарий к классу инцидентов.</span><span class="sxs-lookup"><span data-stu-id="f8bb3-120">Incident Classificaiton Comment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8bb3-121">-ClassificationReason</span><span class="sxs-lookup"><span data-stu-id="f8bb3-121">-ClassificationReason</span></span>
<span data-ttu-id="f8bb3-122">Incident Classificaiton Reason.</span><span class="sxs-lookup"><span data-stu-id="f8bb3-122">Incident Classificaiton Reason.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: InaccurateData, IncorrectAlertLogic, SuspiciousActivity, SuspiciousButExpected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8bb3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8bb3-123">-DefaultProfile</span></span>
<span data-ttu-id="f8bb3-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f8bb3-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8bb3-125">-Description</span><span class="sxs-lookup"><span data-stu-id="f8bb3-125">-Description</span></span>
<span data-ttu-id="f8bb3-126">Описание.</span><span class="sxs-lookup"><span data-stu-id="f8bb3-126">Description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8bb3-127">-IncidentID</span><span class="sxs-lookup"><span data-stu-id="f8bb3-127">-IncidentID</span></span>
<span data-ttu-id="f8bb3-128">ИД инцидента.</span><span class="sxs-lookup"><span data-stu-id="f8bb3-128">Incident Id.</span></span>

```yaml
Type: String
Parameter Sets: IncidentId, ParentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8bb3-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8bb3-129">-InputObject</span></span>
<span data-ttu-id="f8bb3-130">InputObject.</span><span class="sxs-lookup"><span data-stu-id="f8bb3-130">InputObject.</span></span>

```yaml
Type: PSSentinelIncident
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8bb3-131">-Label</span><span class="sxs-lookup"><span data-stu-id="f8bb3-131">-Label</span></span>
<span data-ttu-id="f8bb3-132">Метки инцидентов.</span><span class="sxs-lookup"><span data-stu-id="f8bb3-132">Incident Labels.</span></span>

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

### <span data-ttu-id="f8bb3-133">-Владелец</span><span class="sxs-lookup"><span data-stu-id="f8bb3-133">-Owner</span></span>
<span data-ttu-id="f8bb3-134">Владелец инцидента.</span><span class="sxs-lookup"><span data-stu-id="f8bb3-134">Incident Owner.</span></span>

```yaml
Type: PSSentinelIncidentOwner
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8bb3-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8bb3-135">-ResourceGroupName</span></span>
<span data-ttu-id="f8bb3-136">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f8bb3-136">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8bb3-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8bb3-137">-ResourceId</span></span>
<span data-ttu-id="f8bb3-138">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="f8bb3-138">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8bb3-139">-Severity</span><span class="sxs-lookup"><span data-stu-id="f8bb3-139">-Severity</span></span>
<span data-ttu-id="f8bb3-140">Серьезность инцидента.</span><span class="sxs-lookup"><span data-stu-id="f8bb3-140">Incident Severity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: High, Informational, Low, Medium

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8bb3-141">-Status</span><span class="sxs-lookup"><span data-stu-id="f8bb3-141">-Status</span></span>
<span data-ttu-id="f8bb3-142">"Состояние инцидента".</span><span class="sxs-lookup"><span data-stu-id="f8bb3-142">Incident Status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Active, Closed, New

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8bb3-143">-Title</span><span class="sxs-lookup"><span data-stu-id="f8bb3-143">-Title</span></span>
<span data-ttu-id="f8bb3-144">Название инцидента.</span><span class="sxs-lookup"><span data-stu-id="f8bb3-144">Incident Title.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8bb3-145">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f8bb3-145">-WorkspaceName</span></span>
<span data-ttu-id="f8bb3-146">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="f8bb3-146">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8bb3-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8bb3-147">-Confirm</span></span>
<span data-ttu-id="f8bb3-148">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f8bb3-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8bb3-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8bb3-149">-WhatIf</span></span>
<span data-ttu-id="f8bb3-150">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8bb3-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8bb3-151">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f8bb3-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8bb3-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8bb3-152">CommonParameters</span></span>
<span data-ttu-id="f8bb3-153">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8bb3-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8bb3-154">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8bb3-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8bb3-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f8bb3-155">INPUTS</span></span>

### <span data-ttu-id="f8bb3-156">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="f8bb3-156">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>

### <span data-ttu-id="f8bb3-157">System.String</span><span class="sxs-lookup"><span data-stu-id="f8bb3-157">System.String</span></span>

### <span data-ttu-id="f8bb3-158">System.Collections.Generic.IList'1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="f8bb3-158">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="f8bb3-159">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="f8bb3-159">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span></span>

## <span data-ttu-id="f8bb3-160">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f8bb3-160">OUTPUTS</span></span>

### <span data-ttu-id="f8bb3-161">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="f8bb3-161">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>

## <span data-ttu-id="f8bb3-162">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f8bb3-162">NOTES</span></span>

## <span data-ttu-id="f8bb3-163">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8bb3-163">RELATED LINKS</span></span>
