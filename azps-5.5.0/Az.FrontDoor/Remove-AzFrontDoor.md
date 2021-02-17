---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
ms.openlocfilehash: 133afe9b64fd9161bb7d39fadf6349803f9e2282
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100219996"
---
# <span data-ttu-id="51240-101">Remove-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="51240-101">Remove-AzFrontDoor</span></span>

## <span data-ttu-id="51240-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51240-102">SYNOPSIS</span></span>
<span data-ttu-id="51240-103">Удаление балансировки передней двери</span><span class="sxs-lookup"><span data-stu-id="51240-103">Remove Front Door load balancer</span></span>

## <span data-ttu-id="51240-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="51240-104">SYNTAX</span></span>

### <span data-ttu-id="51240-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="51240-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51240-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="51240-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51240-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="51240-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51240-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="51240-108">DESCRIPTION</span></span>
<span data-ttu-id="51240-109">Для **удаления балансиента** загрузки Front Door в рамках текущей подписки удаляется из-за ее накладных.</span><span class="sxs-lookup"><span data-stu-id="51240-109">The **Remove-AzFrontDoor** cmdlet removes a Front Door load balancer under the current subscription</span></span>

## <span data-ttu-id="51240-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="51240-110">EXAMPLES</span></span>

### <span data-ttu-id="51240-111">Пример 1. Удалите frontdoor1 в группе ресурсов "rg1" под текущей подпиской.</span><span class="sxs-lookup"><span data-stu-id="51240-111">Example 1: Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

<span data-ttu-id="51240-112">Удалите "frontdoor1" в группе ресурсов "rg1" под текущей подпиской.</span><span class="sxs-lookup"><span data-stu-id="51240-112">Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="51240-113">Пример 2. Удаление всех frontDoors в группе ресурсов "rg1" в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="51240-113">Example 2: Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" | Remove-AzFrontDoor
```

<span data-ttu-id="51240-114">Удалите все frontDoors в группе ресурсов "rg1" в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="51240-114">Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="51240-115">Пример 3. Удаление всех frontDoors в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="51240-115">Example 3: Remove all FrontDoors under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor | Remove-AzFrontDoor
```

<span data-ttu-id="51240-116">Удалите все frontDoors в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="51240-116">Remove all FrontDoors under the current subscription.</span></span>

### <span data-ttu-id="51240-117">Пример 4. Удалите все frontDoors с именем frontdoor1 в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="51240-117">Example 4: Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" | Remove-AzFrontDoor
```

<span data-ttu-id="51240-118">Удалите все frontDoors с именем frontdoor1 в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="51240-118">Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>

## <span data-ttu-id="51240-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51240-119">PARAMETERS</span></span>

### <span data-ttu-id="51240-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51240-120">-DefaultProfile</span></span>
<span data-ttu-id="51240-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="51240-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51240-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51240-122">-InputObject</span></span>
<span data-ttu-id="51240-123">Объект передней двери, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="51240-123">The Front Door object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51240-124">-Name</span><span class="sxs-lookup"><span data-stu-id="51240-124">-Name</span></span>
<span data-ttu-id="51240-125">Имя передней двери, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="51240-125">The name of the Front Door to delete.</span></span>

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

### <span data-ttu-id="51240-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51240-126">-PassThru</span></span>
<span data-ttu-id="51240-127">Возвращенный объект (если он указан).</span><span class="sxs-lookup"><span data-stu-id="51240-127">Return object (if specified).</span></span>

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

### <span data-ttu-id="51240-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51240-128">-ResourceGroupName</span></span>
<span data-ttu-id="51240-129">Группа ресурсов, к которой относится front Door.</span><span class="sxs-lookup"><span data-stu-id="51240-129">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="51240-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="51240-130">-ResourceId</span></span>
<span data-ttu-id="51240-131">ИД ресурса передней двери, который нужно удалить</span><span class="sxs-lookup"><span data-stu-id="51240-131">Resource Id of the Front Door to delete</span></span>

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

### <span data-ttu-id="51240-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51240-132">-Confirm</span></span>
<span data-ttu-id="51240-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="51240-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51240-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51240-134">-WhatIf</span></span>
<span data-ttu-id="51240-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51240-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51240-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="51240-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51240-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51240-137">CommonParameters</span></span>
<span data-ttu-id="51240-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51240-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51240-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="51240-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51240-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="51240-140">INPUTS</span></span>

### <span data-ttu-id="51240-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="51240-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="51240-142">System.String</span><span class="sxs-lookup"><span data-stu-id="51240-142">System.String</span></span>

## <span data-ttu-id="51240-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="51240-143">OUTPUTS</span></span>

### <span data-ttu-id="51240-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="51240-144">System.Boolean</span></span>

## <span data-ttu-id="51240-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="51240-145">NOTES</span></span>

## <span data-ttu-id="51240-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="51240-146">RELATED LINKS</span></span>

<span data-ttu-id="51240-147">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="51240-147">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)</span></span>