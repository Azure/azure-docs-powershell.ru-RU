---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/remove-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 707f3157cead45d501cdfdaf357222cdaceac826
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015224"
---
# <span data-ttu-id="f0532-101">Remove-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="f0532-101">Remove-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="f0532-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0532-102">SYNOPSIS</span></span>
<span data-ttu-id="f0532-103">Удаление политики WAF</span><span class="sxs-lookup"><span data-stu-id="f0532-103">Remove WAF policy</span></span>

## <span data-ttu-id="f0532-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f0532-104">SYNTAX</span></span>

### <span data-ttu-id="f0532-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f0532-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0532-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0532-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0532-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0532-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0532-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f0532-108">DESCRIPTION</span></span>
<span data-ttu-id="f0532-109">Для текущей подписки удаляется политика WAF, удаляемая из-за нее с ее начертателем **Remove-AzFrontDoorWafPolicy.**</span><span class="sxs-lookup"><span data-stu-id="f0532-109">The **Remove-AzFrontDoorWafPolicy** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="f0532-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f0532-110">EXAMPLES</span></span>

### <span data-ttu-id="f0532-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f0532-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName
```

<span data-ttu-id="f0532-112">Удалите политику WAF, которая $policyName в $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="f0532-112">Remove the WAF policy called $policyName in $resourceGroupName.</span></span>

### <span data-ttu-id="f0532-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f0532-113">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Remove-AzFrontDoorWafPolicy
```

<span data-ttu-id="f0532-114">Удалите все политики WAF в $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="f0532-114">Remove all WAF policy in $resourceGroupName.</span></span>

## <span data-ttu-id="f0532-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0532-115">PARAMETERS</span></span>

### <span data-ttu-id="f0532-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0532-116">-DefaultProfile</span></span>
<span data-ttu-id="f0532-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f0532-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0532-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0532-118">-InputObject</span></span>
<span data-ttu-id="f0532-119">Объект политики WAF, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="f0532-119">The WAF policy object to delete.</span></span>

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

### <span data-ttu-id="f0532-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f0532-120">-Name</span></span>
<span data-ttu-id="f0532-121">Имя удаляемой политики WAF.</span><span class="sxs-lookup"><span data-stu-id="f0532-121">The name of the WAF policy to delete.</span></span>

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

### <span data-ttu-id="f0532-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0532-122">-PassThru</span></span>
<span data-ttu-id="f0532-123">Возвращенный объект (если он указан).</span><span class="sxs-lookup"><span data-stu-id="f0532-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="f0532-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0532-124">-ResourceGroupName</span></span>
<span data-ttu-id="f0532-125">Группа ресурсов, к которой относится политика WAF.</span><span class="sxs-lookup"><span data-stu-id="f0532-125">The resource group to which the WAF policy belongs.</span></span>

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

### <span data-ttu-id="f0532-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0532-126">-ResourceId</span></span>
<span data-ttu-id="f0532-127">ИД ресурса политики WAF, удаляемой</span><span class="sxs-lookup"><span data-stu-id="f0532-127">Resource Id of the WAF policy to delete</span></span>

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

### <span data-ttu-id="f0532-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f0532-128">-Confirm</span></span>
<span data-ttu-id="f0532-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0532-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0532-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0532-130">-WhatIf</span></span>
<span data-ttu-id="f0532-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0532-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0532-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f0532-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0532-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0532-133">CommonParameters</span></span>
<span data-ttu-id="f0532-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0532-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0532-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0532-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0532-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f0532-136">INPUTS</span></span>

### <span data-ttu-id="f0532-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="f0532-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="f0532-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f0532-138">System.String</span></span>

## <span data-ttu-id="f0532-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f0532-139">OUTPUTS</span></span>

### <span data-ttu-id="f0532-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f0532-140">System.Boolean</span></span>

## <span data-ttu-id="f0532-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f0532-141">NOTES</span></span>

## <span data-ttu-id="f0532-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f0532-142">RELATED LINKS</span></span>

<span data-ttu-id="f0532-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="f0532-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span></span>
