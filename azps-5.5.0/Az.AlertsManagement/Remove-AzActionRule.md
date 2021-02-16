---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/remove-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
ms.openlocfilehash: 4462434bcda1045afcc8478bbd9c4b7a1718d478
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233852"
---
# <span data-ttu-id="325fd-101">Remove-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="325fd-101">Remove-AzActionRule</span></span>

## <span data-ttu-id="325fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="325fd-102">SYNOPSIS</span></span>
<span data-ttu-id="325fd-103">Удаление правила действия</span><span class="sxs-lookup"><span data-stu-id="325fd-103">Deletes a action rule</span></span>

## <span data-ttu-id="325fd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="325fd-104">SYNTAX</span></span>

### <span data-ttu-id="325fd-105">ByName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="325fd-105">ByName (Default)</span></span>
```
Remove-AzActionRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="325fd-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="325fd-106">ByResourceId</span></span>
```
Remove-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="325fd-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="325fd-107">ByInputObject</span></span>
```
Remove-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="325fd-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="325fd-108">DESCRIPTION</span></span>
<span data-ttu-id="325fd-109">Для удаления правила действия удаляется **cmdlet AzActionRule.**</span><span class="sxs-lookup"><span data-stu-id="325fd-109">**Remove-AzActionRule** cmdlet deletes a action rule.</span></span>

## <span data-ttu-id="325fd-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="325fd-110">EXAMPLES</span></span>

### <span data-ttu-id="325fd-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="325fd-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzActionRule -ResourceGroupName "test-rg" -Name "ActionRuleName"
```

<span data-ttu-id="325fd-112">Этот cmdlet удаляет правило действия с именем ActionRuleName в группе ресурсов test-rg</span><span class="sxs-lookup"><span data-stu-id="325fd-112">This cmdlet deletes the action rule with name ActionRuleName in resource group test-rg</span></span>

## <span data-ttu-id="325fd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="325fd-113">PARAMETERS</span></span>

### <span data-ttu-id="325fd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="325fd-114">-DefaultProfile</span></span>
<span data-ttu-id="325fd-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="325fd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="325fd-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="325fd-116">-InputObject</span></span>
<span data-ttu-id="325fd-117">Ресурс правил действий</span><span class="sxs-lookup"><span data-stu-id="325fd-117">The action rule resource</span></span>

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

### <span data-ttu-id="325fd-118">-Name</span><span class="sxs-lookup"><span data-stu-id="325fd-118">-Name</span></span>
<span data-ttu-id="325fd-119">Имя правила действия</span><span class="sxs-lookup"><span data-stu-id="325fd-119">Name of action rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="325fd-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="325fd-120">-PassThru</span></span>
<span data-ttu-id="325fd-121">PassThru возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="325fd-121">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="325fd-122">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="325fd-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="325fd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="325fd-123">-ResourceGroupName</span></span>
<span data-ttu-id="325fd-124">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="325fd-124">Resource Group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="325fd-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="325fd-125">-ResourceId</span></span>
<span data-ttu-id="325fd-126">Получите правило действий по ид ресурса.</span><span class="sxs-lookup"><span data-stu-id="325fd-126">Get Action rule by resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="325fd-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="325fd-127">-Confirm</span></span>
<span data-ttu-id="325fd-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="325fd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="325fd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="325fd-129">-WhatIf</span></span>
<span data-ttu-id="325fd-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="325fd-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="325fd-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="325fd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="325fd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="325fd-132">CommonParameters</span></span>
<span data-ttu-id="325fd-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="325fd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="325fd-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="325fd-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="325fd-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="325fd-135">INPUTS</span></span>

### <span data-ttu-id="325fd-136">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="325fd-136">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="325fd-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="325fd-137">OUTPUTS</span></span>

### <span data-ttu-id="325fd-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="325fd-138">System.Boolean</span></span>

## <span data-ttu-id="325fd-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="325fd-139">NOTES</span></span>

## <span data-ttu-id="325fd-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="325fd-140">RELATED LINKS</span></span>
