---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
ms.openlocfilehash: 133afe9b64fd9161bb7d39fadf6349803f9e2282
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236701"
---
# <span data-ttu-id="02a7c-101">Remove-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="02a7c-101">Remove-AzFrontDoor</span></span>

## <span data-ttu-id="02a7c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="02a7c-102">SYNOPSIS</span></span>
<span data-ttu-id="02a7c-103">Удаление подсистемы балансировки нагрузки передней дверцы</span><span class="sxs-lookup"><span data-stu-id="02a7c-103">Remove Front Door load balancer</span></span>

## <span data-ttu-id="02a7c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="02a7c-104">SYNTAX</span></span>

### <span data-ttu-id="02a7c-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="02a7c-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02a7c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02a7c-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02a7c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="02a7c-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02a7c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="02a7c-108">DESCRIPTION</span></span>
<span data-ttu-id="02a7c-109">Командлет **Remove-AzFrontDoor** удаляет подсистему балансировки нагрузки передней дверцы в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="02a7c-109">The **Remove-AzFrontDoor** cmdlet removes a Front Door load balancer under the current subscription</span></span>

## <span data-ttu-id="02a7c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="02a7c-110">EXAMPLES</span></span>

### <span data-ttu-id="02a7c-111">Пример 1: удалите "frontdoor1" в группе ресурсов "Rg1" в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="02a7c-111">Example 1: Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

<span data-ttu-id="02a7c-112">Удаление "frontdoor1" в группе ресурсов "Rg1" в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="02a7c-112">Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="02a7c-113">Пример 2: удаление всех FrontDoors в группе ресурсов "Rg1" в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="02a7c-113">Example 2: Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" | Remove-AzFrontDoor
```

<span data-ttu-id="02a7c-114">Удаление всех FrontDoors в группе ресурсов "Rg1" в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="02a7c-114">Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="02a7c-115">Пример 3: удаление всех FrontDoors в рамках текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="02a7c-115">Example 3: Remove all FrontDoors under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor | Remove-AzFrontDoor
```

<span data-ttu-id="02a7c-116">Удаление всех FrontDoors в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="02a7c-116">Remove all FrontDoors under the current subscription.</span></span>

### <span data-ttu-id="02a7c-117">Пример 4: удаление всех FrontDoors с именем "frontdoor1" в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="02a7c-117">Example 4: Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" | Remove-AzFrontDoor
```

<span data-ttu-id="02a7c-118">Удалите все FrontDoors с именем "frontdoor1" в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="02a7c-118">Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>

## <span data-ttu-id="02a7c-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="02a7c-119">PARAMETERS</span></span>

### <span data-ttu-id="02a7c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02a7c-120">-DefaultProfile</span></span>
<span data-ttu-id="02a7c-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="02a7c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02a7c-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02a7c-122">-InputObject</span></span>
<span data-ttu-id="02a7c-123">Объект передней дверцы, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="02a7c-123">The Front Door object to delete.</span></span>

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

### <span data-ttu-id="02a7c-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="02a7c-124">-Name</span></span>
<span data-ttu-id="02a7c-125">Имя передней дверцы, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="02a7c-125">The name of the Front Door to delete.</span></span>

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

### <span data-ttu-id="02a7c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02a7c-126">-PassThru</span></span>
<span data-ttu-id="02a7c-127">Возвращаемый объект (если указан).</span><span class="sxs-lookup"><span data-stu-id="02a7c-127">Return object (if specified).</span></span>

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

### <span data-ttu-id="02a7c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02a7c-128">-ResourceGroupName</span></span>
<span data-ttu-id="02a7c-129">Группа ресурсов, к которой принадлежит передняя дверь.</span><span class="sxs-lookup"><span data-stu-id="02a7c-129">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="02a7c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02a7c-130">-ResourceId</span></span>
<span data-ttu-id="02a7c-131">Идентификатор ресурса передней дверцы для удаления</span><span class="sxs-lookup"><span data-stu-id="02a7c-131">Resource Id of the Front Door to delete</span></span>

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

### <span data-ttu-id="02a7c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02a7c-132">-Confirm</span></span>
<span data-ttu-id="02a7c-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="02a7c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02a7c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02a7c-134">-WhatIf</span></span>
<span data-ttu-id="02a7c-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="02a7c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02a7c-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="02a7c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02a7c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02a7c-137">CommonParameters</span></span>
<span data-ttu-id="02a7c-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="02a7c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02a7c-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02a7c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02a7c-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="02a7c-140">INPUTS</span></span>

### <span data-ttu-id="02a7c-141">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="02a7c-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="02a7c-142">System. String</span><span class="sxs-lookup"><span data-stu-id="02a7c-142">System.String</span></span>

## <span data-ttu-id="02a7c-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="02a7c-143">OUTPUTS</span></span>

### <span data-ttu-id="02a7c-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="02a7c-144">System.Boolean</span></span>

## <span data-ttu-id="02a7c-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="02a7c-145">NOTES</span></span>

## <span data-ttu-id="02a7c-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="02a7c-146">RELATED LINKS</span></span>

<span data-ttu-id="02a7c-147">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="02a7c-147">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)</span></span>