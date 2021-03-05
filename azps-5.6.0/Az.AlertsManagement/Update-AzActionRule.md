---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/update-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
ms.openlocfilehash: 7dcbf947975719a30282037d592469a986990d50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993096"
---
# <span data-ttu-id="f0723-101">Update-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="f0723-101">Update-AzActionRule</span></span>

## <span data-ttu-id="f0723-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0723-102">SYNOPSIS</span></span>
<span data-ttu-id="f0723-103">Обновляет свойства правил действий.</span><span class="sxs-lookup"><span data-stu-id="f0723-103">Updates action rule properties.</span></span>

## <span data-ttu-id="f0723-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f0723-104">SYNTAX</span></span>

### <span data-ttu-id="f0723-105">ByNameSimplifiedPatch (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f0723-105">ByNameSimplifiedPatch (Default)</span></span>
```
Update-AzActionRule -Name <String> -ResourceGroupName <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0723-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f0723-106">ByResourceId</span></span>
```
Update-AzActionRule -ResourceId <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0723-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f0723-107">ByInputObject</span></span>
```
Update-AzActionRule -InputObject <PSActionRule> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0723-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0723-108">DESCRIPTION</span></span>
<span data-ttu-id="f0723-109">**Командлет Update-AzActionRule** обновляет свойства правила действия — состояние и теги.</span><span class="sxs-lookup"><span data-stu-id="f0723-109">**Update-AzActionRule** cmdlet updates action rule properties - status and tags.</span></span>

## <span data-ttu-id="f0723-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f0723-110">EXAMPLES</span></span>

### <span data-ttu-id="f0723-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f0723-111">Example 1</span></span>
```powershell
PS C:\> Update-AzActionRule -ResourceGroupName "test-rg" -Name "Test-ActionRule" -Status "Disabled"
```

<span data-ttu-id="f0723-112">Этот cmdlet отключает правило действия.</span><span class="sxs-lookup"><span data-stu-id="f0723-112">This cmdlet disables the action rule.</span></span> 

## <span data-ttu-id="f0723-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0723-113">PARAMETERS</span></span>

### <span data-ttu-id="f0723-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0723-114">-DefaultProfile</span></span>
<span data-ttu-id="f0723-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f0723-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0723-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0723-116">-InputObject</span></span>
<span data-ttu-id="f0723-117">Ресурс правил действий</span><span class="sxs-lookup"><span data-stu-id="f0723-117">The action rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0723-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f0723-118">-Name</span></span>
<span data-ttu-id="f0723-119">Имя правила действия</span><span class="sxs-lookup"><span data-stu-id="f0723-119">Action rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0723-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0723-120">-ResourceGroupName</span></span>
<span data-ttu-id="f0723-121">Имя правила действия</span><span class="sxs-lookup"><span data-stu-id="f0723-121">Action rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0723-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0723-122">-ResourceId</span></span>
<span data-ttu-id="f0723-123">ИД ресурса правила действия</span><span class="sxs-lookup"><span data-stu-id="f0723-123">The resource id of action rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0723-124">-Status</span><span class="sxs-lookup"><span data-stu-id="f0723-124">-Status</span></span>
<span data-ttu-id="f0723-125">Состояние правила действия</span><span class="sxs-lookup"><span data-stu-id="f0723-125">Action rule status</span></span>

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

### <span data-ttu-id="f0723-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="f0723-126">-Tag</span></span>
<span data-ttu-id="f0723-127">Теги правил действий</span><span class="sxs-lookup"><span data-stu-id="f0723-127">Action rule tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0723-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0723-128">-Confirm</span></span>
<span data-ttu-id="f0723-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0723-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0723-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0723-130">-WhatIf</span></span>
<span data-ttu-id="f0723-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0723-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0723-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f0723-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0723-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0723-133">CommonParameters</span></span>
<span data-ttu-id="f0723-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0723-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0723-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0723-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0723-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f0723-136">INPUTS</span></span>

### <span data-ttu-id="f0723-137">System.String</span><span class="sxs-lookup"><span data-stu-id="f0723-137">System.String</span></span>

### <span data-ttu-id="f0723-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="f0723-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="f0723-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f0723-139">OUTPUTS</span></span>

### <span data-ttu-id="f0723-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="f0723-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="f0723-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f0723-141">NOTES</span></span>

## <span data-ttu-id="f0723-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0723-142">RELATED LINKS</span></span>
