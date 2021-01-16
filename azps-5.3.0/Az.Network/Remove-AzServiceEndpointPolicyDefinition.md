---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 146e43ce5f1816994a1d408e215e4b3e27c2bbca
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507777"
---
# <span data-ttu-id="1faae-101">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1faae-101">Remove-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="1faae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1faae-102">SYNOPSIS</span></span>
<span data-ttu-id="1faae-103">Удаляет определение политики конечных точек службы.</span><span class="sxs-lookup"><span data-stu-id="1faae-103">Removes a service endpoint policy definition.</span></span>

## <span data-ttu-id="1faae-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1faae-104">SYNTAX</span></span>

### <span data-ttu-id="1faae-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1faae-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1faae-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1faae-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -ResourceId <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1faae-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1faae-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -InputObject <PSServiceEndpointPolicyDefinition>
 -ServiceEndpointPolicy <PSServiceEndpointPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1faae-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1faae-108">DESCRIPTION</span></span>
<span data-ttu-id="1faae-109">Для удаления политики конечных точек службы будет назначена cmdlet **Remove-AzServiceEndpointPolicy.**</span><span class="sxs-lookup"><span data-stu-id="1faae-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="1faae-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1faae-110">EXAMPLES</span></span>

### <span data-ttu-id="1faae-111">Пример 1. Удаление политики конечной точки службы с использованием имени</span><span class="sxs-lookup"><span data-stu-id="1faae-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="1faae-112">Эта команда удаляет политику конечной точки службы с именем PolicyDef1.</span><span class="sxs-lookup"><span data-stu-id="1faae-112">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="1faae-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1faae-113">PARAMETERS</span></span>

### <span data-ttu-id="1faae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1faae-114">-DefaultProfile</span></span>
<span data-ttu-id="1faae-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1faae-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1faae-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1faae-116">-InputObject</span></span>
<span data-ttu-id="1faae-117">Объект определения конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="1faae-117">The service endpoint policy definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1faae-118">-Name</span><span class="sxs-lookup"><span data-stu-id="1faae-118">-Name</span></span>
<span data-ttu-id="1faae-119">Имя определения конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="1faae-119">The name of the service endpoint definition</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1faae-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1faae-120">-ResourceId</span></span>
<span data-ttu-id="1faae-121">ИД определения конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="1faae-121">The ID of the service endpoint definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1faae-122">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="1faae-122">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="1faae-123">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="1faae-123">The ServiceEndpointPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1faae-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1faae-124">-Confirm</span></span>
<span data-ttu-id="1faae-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1faae-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1faae-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1faae-126">-WhatIf</span></span>
<span data-ttu-id="1faae-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1faae-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1faae-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1faae-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1faae-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1faae-129">CommonParameters</span></span>
<span data-ttu-id="1faae-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1faae-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1faae-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1faae-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1faae-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1faae-132">INPUTS</span></span>

### <span data-ttu-id="1faae-133">System.String</span><span class="sxs-lookup"><span data-stu-id="1faae-133">System.String</span></span>

### <span data-ttu-id="1faae-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1faae-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

### <span data-ttu-id="1faae-135">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="1faae-135">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="1faae-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1faae-136">OUTPUTS</span></span>

### <span data-ttu-id="1faae-137">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="1faae-137">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="1faae-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1faae-138">NOTES</span></span>

## <span data-ttu-id="1faae-139">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1faae-139">RELATED LINKS</span></span>

[<span data-ttu-id="1faae-140">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1faae-140">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="1faae-141">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1faae-141">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="1faae-142">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1faae-142">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="1faae-143">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1faae-143">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
