---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/remove-azurermfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoor.md
ms.openlocfilehash: 8eae5034080bd1035cfe7e8331ca015820688e63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93731969"
---
# <span data-ttu-id="2275b-101">Remove-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="2275b-101">Remove-AzureRmFrontDoor</span></span>

## <span data-ttu-id="2275b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2275b-102">SYNOPSIS</span></span>
<span data-ttu-id="2275b-103">Удаление подсистемы балансировки нагрузки передней дверцы</span><span class="sxs-lookup"><span data-stu-id="2275b-103">Remove Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2275b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2275b-104">SYNTAX</span></span>

### <span data-ttu-id="2275b-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2275b-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2275b-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2275b-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2275b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2275b-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2275b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2275b-108">DESCRIPTION</span></span>
<span data-ttu-id="2275b-109">Командлет **Remove-AzureRmFrontDoor** удаляет подсистему балансировки нагрузки передней дверцы в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="2275b-109">The **Remove-AzureRmFrontDoor** cmdlet removes a Front Door load balancer under the current subscription</span></span>

## <span data-ttu-id="2275b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2275b-110">EXAMPLES</span></span>

### <span data-ttu-id="2275b-111">Пример 1: удалите "frontdoor1" в группе ресурсов "Rg1" в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="2275b-111">Example 1: Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

<span data-ttu-id="2275b-112">Удаление "frontdoor1" в группе ресурсов "Rg1" в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="2275b-112">Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="2275b-113">Пример 2: удаление всех FrontDoors в группе ресурсов "Rg1" в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="2275b-113">Example 2: Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor -ResourceGroupName "rg1" | Remove-AzureRmFrontDoor
```

<span data-ttu-id="2275b-114">Удаление всех FrontDoors в группе ресурсов "Rg1" в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="2275b-114">Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="2275b-115">Пример 3: удаление всех FrontDoors в рамках текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="2275b-115">Example 3: Remove all FrontDoors under the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor | Remove-AzureRmFrontDoor
```

<span data-ttu-id="2275b-116">Удаление всех FrontDoors в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="2275b-116">Remove all FrontDoors under the current subscription.</span></span>

### <span data-ttu-id="2275b-117">Пример 4: удаление всех FrontDoors с именем "frontdoor1" в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="2275b-117">Example 4: Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoor -Name "frontdoor1" | Remove-AzureRmFrontDoor
```

<span data-ttu-id="2275b-118">Удалите все FrontDoors с именем "frontdoor1" в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="2275b-118">Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>

## <span data-ttu-id="2275b-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2275b-119">PARAMETERS</span></span>

### <span data-ttu-id="2275b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2275b-120">-DefaultProfile</span></span>
<span data-ttu-id="2275b-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2275b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2275b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2275b-122">-InputObject</span></span>
<span data-ttu-id="2275b-123">Объект передней дверцы, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="2275b-123">The Front Door object to delete.</span></span>

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

### <span data-ttu-id="2275b-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2275b-124">-Name</span></span>
<span data-ttu-id="2275b-125">Имя передней дверцы, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="2275b-125">The name of the Front Door to delete.</span></span>

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

### <span data-ttu-id="2275b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2275b-126">-PassThru</span></span>
<span data-ttu-id="2275b-127">Возвращаемый объект (если указан).</span><span class="sxs-lookup"><span data-stu-id="2275b-127">Return object (if specified).</span></span>

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

### <span data-ttu-id="2275b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2275b-128">-ResourceGroupName</span></span>
<span data-ttu-id="2275b-129">Группа ресурсов, к которой принадлежит передняя дверь.</span><span class="sxs-lookup"><span data-stu-id="2275b-129">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="2275b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2275b-130">-ResourceId</span></span>
<span data-ttu-id="2275b-131">Идентификатор ресурса передней дверцы для удаления</span><span class="sxs-lookup"><span data-stu-id="2275b-131">Resource Id of the Front Door to delete</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2275b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2275b-132">-Confirm</span></span>
<span data-ttu-id="2275b-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2275b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2275b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2275b-134">-WhatIf</span></span>
<span data-ttu-id="2275b-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2275b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2275b-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2275b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2275b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2275b-137">CommonParameters</span></span>
<span data-ttu-id="2275b-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2275b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2275b-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2275b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2275b-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2275b-140">INPUTS</span></span>

### <span data-ttu-id="2275b-141">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="2275b-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="2275b-142">System. String</span><span class="sxs-lookup"><span data-stu-id="2275b-142">System.String</span></span>

### <span data-ttu-id="2275b-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2275b-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2275b-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2275b-144">OUTPUTS</span></span>

### <span data-ttu-id="2275b-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2275b-145">System.Boolean</span></span>

## <span data-ttu-id="2275b-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="2275b-146">NOTES</span></span>

## <span data-ttu-id="2275b-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2275b-147">RELATED LINKS</span></span>

<span data-ttu-id="2275b-148">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="2275b-148">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)</span></span>
