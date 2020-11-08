---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
ms.openlocfilehash: ec68316ecac3921f37641b83f45b9bd922e90b46
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077748"
---
# <span data-ttu-id="44b6d-101">Remove-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="44b6d-101">Remove-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="44b6d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="44b6d-102">SYNOPSIS</span></span>
<span data-ttu-id="44b6d-103">Удаление политики WAF</span><span class="sxs-lookup"><span data-stu-id="44b6d-103">Remove WAF policy</span></span>

## <span data-ttu-id="44b6d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="44b6d-104">SYNTAX</span></span>

### <span data-ttu-id="44b6d-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="44b6d-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44b6d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44b6d-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44b6d-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="44b6d-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44b6d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="44b6d-108">DESCRIPTION</span></span>
<span data-ttu-id="44b6d-109">Командлет **Remove-AzFrontDoorWafPolicy** УДАЛЯЕТ политику WAF в рамках текущей подписки.</span><span class="sxs-lookup"><span data-stu-id="44b6d-109">The **Remove-AzFrontDoorWafPolicy** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="44b6d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="44b6d-110">EXAMPLES</span></span>

### <span data-ttu-id="44b6d-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="44b6d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName
```

<span data-ttu-id="44b6d-112">Удалите политику WAF с именем $policyName в $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="44b6d-112">Remove the WAF policy called $policyName in $resourceGroupName.</span></span>

### <span data-ttu-id="44b6d-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="44b6d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Remove-AzFrontDoorWafPolicy
```

<span data-ttu-id="44b6d-114">Удалите все WAF политики в $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="44b6d-114">Remove all WAF policy in $resourceGroupName.</span></span>

## <span data-ttu-id="44b6d-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="44b6d-115">PARAMETERS</span></span>

### <span data-ttu-id="44b6d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44b6d-116">-DefaultProfile</span></span>
<span data-ttu-id="44b6d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="44b6d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44b6d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44b6d-118">-InputObject</span></span>
<span data-ttu-id="44b6d-119">Объект политики WAF, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="44b6d-119">The WAF policy object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44b6d-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="44b6d-120">-Name</span></span>
<span data-ttu-id="44b6d-121">Имя удаляемой политики WAF.</span><span class="sxs-lookup"><span data-stu-id="44b6d-121">The name of the WAF policy to delete.</span></span>

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

### <span data-ttu-id="44b6d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44b6d-122">-PassThru</span></span>
<span data-ttu-id="44b6d-123">Возвращаемый объект (если указан).</span><span class="sxs-lookup"><span data-stu-id="44b6d-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="44b6d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44b6d-124">-ResourceGroupName</span></span>
<span data-ttu-id="44b6d-125">Группа ресурсов, к которой относится политика WAF.</span><span class="sxs-lookup"><span data-stu-id="44b6d-125">The resource group to which the WAF policy belongs.</span></span>

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

### <span data-ttu-id="44b6d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44b6d-126">-ResourceId</span></span>
<span data-ttu-id="44b6d-127">Идентификатор ресурса политики WAF, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="44b6d-127">Resource Id of the WAF policy to delete</span></span>

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

### <span data-ttu-id="44b6d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44b6d-128">-Confirm</span></span>
<span data-ttu-id="44b6d-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="44b6d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44b6d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44b6d-130">-WhatIf</span></span>
<span data-ttu-id="44b6d-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="44b6d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44b6d-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="44b6d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44b6d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44b6d-133">CommonParameters</span></span>
<span data-ttu-id="44b6d-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="44b6d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44b6d-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44b6d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44b6d-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="44b6d-136">INPUTS</span></span>

### <span data-ttu-id="44b6d-137">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="44b6d-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="44b6d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="44b6d-138">System.String</span></span>

## <span data-ttu-id="44b6d-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="44b6d-139">OUTPUTS</span></span>

### <span data-ttu-id="44b6d-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="44b6d-140">System.Boolean</span></span>

## <span data-ttu-id="44b6d-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="44b6d-141">NOTES</span></span>

## <span data-ttu-id="44b6d-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="44b6d-142">RELATED LINKS</span></span>

<span data-ttu-id="44b6d-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="44b6d-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span></span>
