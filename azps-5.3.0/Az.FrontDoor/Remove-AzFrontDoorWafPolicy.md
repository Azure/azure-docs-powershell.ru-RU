---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
ms.openlocfilehash: ec68316ecac3921f37641b83f45b9bd922e90b46
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507406"
---
# <span data-ttu-id="965b9-101">Remove-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="965b9-101">Remove-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="965b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="965b9-102">SYNOPSIS</span></span>
<span data-ttu-id="965b9-103">Удаление политики WAF</span><span class="sxs-lookup"><span data-stu-id="965b9-103">Remove WAF policy</span></span>

## <span data-ttu-id="965b9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="965b9-104">SYNTAX</span></span>

### <span data-ttu-id="965b9-105">ByFieldsParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="965b9-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="965b9-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="965b9-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="965b9-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="965b9-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="965b9-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="965b9-108">DESCRIPTION</span></span>
<span data-ttu-id="965b9-109">Для текущей подписки удаляется политика WAF, удаляемая из-за нее с ее начертателем **Remove-AzFrontDoorWafPolicy.**</span><span class="sxs-lookup"><span data-stu-id="965b9-109">The **Remove-AzFrontDoorWafPolicy** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="965b9-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="965b9-110">EXAMPLES</span></span>

### <span data-ttu-id="965b9-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="965b9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName
```

<span data-ttu-id="965b9-112">Удалите политику WAF, которая $policyName в $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="965b9-112">Remove the WAF policy called $policyName in $resourceGroupName.</span></span>

### <span data-ttu-id="965b9-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="965b9-113">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Remove-AzFrontDoorWafPolicy
```

<span data-ttu-id="965b9-114">Удалите все политики WAF в $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="965b9-114">Remove all WAF policy in $resourceGroupName.</span></span>

## <span data-ttu-id="965b9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="965b9-115">PARAMETERS</span></span>

### <span data-ttu-id="965b9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="965b9-116">-DefaultProfile</span></span>
<span data-ttu-id="965b9-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="965b9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="965b9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="965b9-118">-InputObject</span></span>
<span data-ttu-id="965b9-119">Объект политики WAF, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="965b9-119">The WAF policy object to delete.</span></span>

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

### <span data-ttu-id="965b9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="965b9-120">-Name</span></span>
<span data-ttu-id="965b9-121">Имя удаляемой политики WAF.</span><span class="sxs-lookup"><span data-stu-id="965b9-121">The name of the WAF policy to delete.</span></span>

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

### <span data-ttu-id="965b9-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="965b9-122">-PassThru</span></span>
<span data-ttu-id="965b9-123">Возвращенный объект (если он указан).</span><span class="sxs-lookup"><span data-stu-id="965b9-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="965b9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="965b9-124">-ResourceGroupName</span></span>
<span data-ttu-id="965b9-125">Группа ресурсов, к которой относится политика WAF.</span><span class="sxs-lookup"><span data-stu-id="965b9-125">The resource group to which the WAF policy belongs.</span></span>

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

### <span data-ttu-id="965b9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="965b9-126">-ResourceId</span></span>
<span data-ttu-id="965b9-127">ИД ресурса политики WAF, удаляемой</span><span class="sxs-lookup"><span data-stu-id="965b9-127">Resource Id of the WAF policy to delete</span></span>

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

### <span data-ttu-id="965b9-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="965b9-128">-Confirm</span></span>
<span data-ttu-id="965b9-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="965b9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="965b9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="965b9-130">-WhatIf</span></span>
<span data-ttu-id="965b9-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="965b9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="965b9-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="965b9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="965b9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="965b9-133">CommonParameters</span></span>
<span data-ttu-id="965b9-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="965b9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="965b9-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="965b9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="965b9-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="965b9-136">INPUTS</span></span>

### <span data-ttu-id="965b9-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="965b9-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="965b9-138">System.String</span><span class="sxs-lookup"><span data-stu-id="965b9-138">System.String</span></span>

## <span data-ttu-id="965b9-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="965b9-139">OUTPUTS</span></span>

### <span data-ttu-id="965b9-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="965b9-140">System.Boolean</span></span>

## <span data-ttu-id="965b9-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="965b9-141">NOTES</span></span>

## <span data-ttu-id="965b9-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="965b9-142">RELATED LINKS</span></span>

<span data-ttu-id="965b9-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="965b9-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span></span>
