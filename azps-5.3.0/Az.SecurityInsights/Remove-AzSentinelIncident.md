---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelIncident.md
ms.openlocfilehash: faf2c40bc43c1b42861bc93d2398d4d26731c112
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517537"
---
# <span data-ttu-id="8ba28-101">Remove-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="8ba28-101">Remove-AzSentinelIncident</span></span>

## <span data-ttu-id="8ba28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ba28-102">SYNOPSIS</span></span>
<span data-ttu-id="8ba28-103">Удаление инцидента.</span><span class="sxs-lookup"><span data-stu-id="8ba28-103">Delete an Incident.</span></span>

## <span data-ttu-id="8ba28-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8ba28-104">SYNTAX</span></span>

### <span data-ttu-id="8ba28-105">IncidentId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8ba28-105">IncidentId (Default)</span></span>
```
Remove-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ba28-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="8ba28-106">InputObject</span></span>
```
Remove-AzSentinelIncident -InputObject <PSSentinelIncident> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ba28-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8ba28-107">DESCRIPTION</span></span>
<span data-ttu-id="8ba28-108">**Cmdlet Remove-AzSentinelIncident** окончательно удаляет инцидент из указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="8ba28-108">The **Remove-AzSentinelIncident** cmdlet permanently deletes a Incident from a specified workspace.</span></span>
<span data-ttu-id="8ba28-109">Вы можете передать объект **инциденту** с помощью оператора конвейера или указать необходимые параметры.</span><span class="sxs-lookup"><span data-stu-id="8ba28-109">You can pass an **Incident** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="8ba28-110">Параметр Confirm и переменная $ConfirmPreference Windows PowerShell можно использовать для управления запросом на подтверждение с помощью cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ba28-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="8ba28-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8ba28-111">EXAMPLES</span></span>

### <span data-ttu-id="8ba28-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8ba28-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="8ba28-113">Эта команда удаляет инцидент из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="8ba28-113">This command removes the Incident from the workspace.</span></span>

## <span data-ttu-id="8ba28-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ba28-114">PARAMETERS</span></span>

### <span data-ttu-id="8ba28-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ba28-115">-DefaultProfile</span></span>
<span data-ttu-id="8ba28-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8ba28-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ba28-117">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="8ba28-117">-IncidentId</span></span>
<span data-ttu-id="8ba28-118">ИД инцидента.</span><span class="sxs-lookup"><span data-stu-id="8ba28-118">Incident Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba28-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ba28-119">-InputObject</span></span>
<span data-ttu-id="8ba28-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="8ba28-120">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba28-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ba28-121">-PassThru</span></span>
<span data-ttu-id="8ba28-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="8ba28-122">PassThru</span></span>

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

### <span data-ttu-id="8ba28-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ba28-123">-ResourceGroupName</span></span>
<span data-ttu-id="8ba28-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8ba28-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba28-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="8ba28-125">-WorkspaceName</span></span>
<span data-ttu-id="8ba28-126">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="8ba28-126">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ba28-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ba28-127">-Confirm</span></span>
<span data-ttu-id="8ba28-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ba28-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ba28-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ba28-129">-WhatIf</span></span>
<span data-ttu-id="8ba28-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ba28-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ba28-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8ba28-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ba28-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ba28-132">CommonParameters</span></span>
<span data-ttu-id="8ba28-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ba28-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ba28-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ba28-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ba28-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8ba28-135">INPUTS</span></span>

### <span data-ttu-id="8ba28-136">System.String</span><span class="sxs-lookup"><span data-stu-id="8ba28-136">System.String</span></span>
### <span data-ttu-id="8ba28-137">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="8ba28-137">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="8ba28-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8ba28-138">OUTPUTS</span></span>

### <span data-ttu-id="8ba28-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8ba28-139">System.Boolean</span></span>
## <span data-ttu-id="8ba28-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8ba28-140">NOTES</span></span>

## <span data-ttu-id="8ba28-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8ba28-141">RELATED LINKS</span></span>
