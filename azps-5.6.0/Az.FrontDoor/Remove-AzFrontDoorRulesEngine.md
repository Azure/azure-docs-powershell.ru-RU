---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/remove-azfrontdoorrulesengine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorRulesEngine.md
ms.openlocfilehash: 84bcc64127636adc318935d1a7fd97f7ce79d760
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015235"
---
# <span data-ttu-id="36db2-101">Remove-AzFrontDoorRulesEngine</span><span class="sxs-lookup"><span data-stu-id="36db2-101">Remove-AzFrontDoorRulesEngine</span></span>

## <span data-ttu-id="36db2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36db2-102">SYNOPSIS</span></span>
<span data-ttu-id="36db2-103">Удаление обуха правил из передней двери</span><span class="sxs-lookup"><span data-stu-id="36db2-103">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="36db2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="36db2-104">SYNTAX</span></span>

### <span data-ttu-id="36db2-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="36db2-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceGroupName <String> -FrontDoorName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36db2-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="36db2-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -InputObject <PSRulesEngine> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36db2-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="36db2-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorRulesEngine -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36db2-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36db2-108">DESCRIPTION</span></span>
<span data-ttu-id="36db2-109">Удаление обуха правил из передней двери</span><span class="sxs-lookup"><span data-stu-id="36db2-109">Remove Rules Engine from Front Door</span></span>

## <span data-ttu-id="36db2-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="36db2-110">EXAMPLES</span></span>

### <span data-ttu-id="36db2-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="36db2-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name $rulesEngine.Name -PassThru
True
```

<span data-ttu-id="36db2-112">"Удалить конфигурацию яла правил".</span><span class="sxs-lookup"><span data-stu-id="36db2-112">Remove rules engine configuration.</span></span>

### <span data-ttu-id="36db2-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="36db2-113">Example 2</span></span>
```powershell
PS C:> Remove-AzFrontDoorRulesEngine -ResourceGroupName $resourceGroupName -FrontDoorName $frontDoorName -Name nonexistentRulesEngine
Remove-AzFrontDoorRulesEngine : Rules Engine with name 'nonexistentRulesEngine' in Front Door 'frontDoorName' in the resource group 'resourceGroupName' does not exist.
At line:1 char:1
+ Remove-AzFrontDoorRulesEngine -ResourceGroupName resourceGroupName -Fro ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
+ CategoryInfo          : CloseError: (:) [Remove-AzFrontDoorRulesEngine], PSArgumentException
+ FullyQualifiedErrorId : Microsoft.Azure.Commands.FrontDoor.Cmdlets.RemoveFrontDoorRulesEngine
```

<span data-ttu-id="36db2-114">Ожидаемый результат при удалении несущещающихся правил.</span><span class="sxs-lookup"><span data-stu-id="36db2-114">Expected outcome when removing a nonexistent rules engine configuration.</span></span>

## <span data-ttu-id="36db2-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36db2-115">PARAMETERS</span></span>

### <span data-ttu-id="36db2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36db2-116">-DefaultProfile</span></span>
<span data-ttu-id="36db2-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="36db2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36db2-118">-FrontDoorName</span><span class="sxs-lookup"><span data-stu-id="36db2-118">-FrontDoorName</span></span>
<span data-ttu-id="36db2-119">Имя передней двери.</span><span class="sxs-lookup"><span data-stu-id="36db2-119">Front Door name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36db2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36db2-120">-InputObject</span></span>
<span data-ttu-id="36db2-121">Объект обновимой обл. правил.</span><span class="sxs-lookup"><span data-stu-id="36db2-121">The Rules Engine object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36db2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="36db2-122">-Name</span></span>
<span data-ttu-id="36db2-123">Имя яла правила.</span><span class="sxs-lookup"><span data-stu-id="36db2-123">Rules engine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36db2-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36db2-124">-PassThru</span></span>
<span data-ttu-id="36db2-125">Возвращенный объект (если он указан).</span><span class="sxs-lookup"><span data-stu-id="36db2-125">Return object (if specified).</span></span>

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

### <span data-ttu-id="36db2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36db2-126">-ResourceGroupName</span></span>
<span data-ttu-id="36db2-127">Имя группы ресурсов, в которую будет создана front Door.</span><span class="sxs-lookup"><span data-stu-id="36db2-127">The resource group name that the Front Door will be created in.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36db2-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36db2-128">-ResourceId</span></span>
<span data-ttu-id="36db2-129">ИД ресурса для обновления правил (английского)</span><span class="sxs-lookup"><span data-stu-id="36db2-129">Resource Id of the RulesEngine to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36db2-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36db2-130">-Confirm</span></span>
<span data-ttu-id="36db2-131">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36db2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36db2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36db2-132">-WhatIf</span></span>
<span data-ttu-id="36db2-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36db2-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36db2-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="36db2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36db2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36db2-135">CommonParameters</span></span>
<span data-ttu-id="36db2-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36db2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36db2-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36db2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36db2-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36db2-138">INPUTS</span></span>

### <span data-ttu-id="36db2-139">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span><span class="sxs-lookup"><span data-stu-id="36db2-139">Microsoft.Azure.Commands.FrontDoor.Models.PSRulesEngine</span></span>

### <span data-ttu-id="36db2-140">System.String</span><span class="sxs-lookup"><span data-stu-id="36db2-140">System.String</span></span>

## <span data-ttu-id="36db2-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="36db2-141">OUTPUTS</span></span>

### <span data-ttu-id="36db2-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="36db2-142">System.Boolean</span></span>

## <span data-ttu-id="36db2-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="36db2-143">NOTES</span></span>

## <span data-ttu-id="36db2-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36db2-144">RELATED LINKS</span></span>
