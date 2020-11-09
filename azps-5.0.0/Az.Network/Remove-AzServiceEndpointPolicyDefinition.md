---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 146e43ce5f1816994a1d408e215e4b3e27c2bbca
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246392"
---
# <span data-ttu-id="e3bba-101">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e3bba-101">Remove-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="e3bba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e3bba-102">SYNOPSIS</span></span>
<span data-ttu-id="e3bba-103">Удаляет определение политики конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="e3bba-103">Removes a service endpoint policy definition.</span></span>

## <span data-ttu-id="e3bba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e3bba-104">SYNTAX</span></span>

### <span data-ttu-id="e3bba-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e3bba-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3bba-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3bba-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -ResourceId <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3bba-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3bba-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -InputObject <PSServiceEndpointPolicyDefinition>
 -ServiceEndpointPolicy <PSServiceEndpointPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3bba-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3bba-108">DESCRIPTION</span></span>
<span data-ttu-id="e3bba-109">Командлет **Remove-AzServiceEndpointPolicy** удаляет политику конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="e3bba-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="e3bba-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e3bba-110">EXAMPLES</span></span>

### <span data-ttu-id="e3bba-111">Пример 1: Удаление политики конечной точки службы с помощью имени</span><span class="sxs-lookup"><span data-stu-id="e3bba-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="e3bba-112">Эта команда удаляет политику конечной точки службы с именем PolicyDef1</span><span class="sxs-lookup"><span data-stu-id="e3bba-112">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="e3bba-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e3bba-113">PARAMETERS</span></span>

### <span data-ttu-id="e3bba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3bba-114">-DefaultProfile</span></span>
<span data-ttu-id="e3bba-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e3bba-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3bba-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e3bba-116">-InputObject</span></span>
<span data-ttu-id="e3bba-117">Объект определения политики конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="e3bba-117">The service endpoint policy definition object.</span></span>

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

### <span data-ttu-id="e3bba-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e3bba-118">-Name</span></span>
<span data-ttu-id="e3bba-119">Имя определения конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="e3bba-119">The name of the service endpoint definition</span></span>

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

### <span data-ttu-id="e3bba-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3bba-120">-ResourceId</span></span>
<span data-ttu-id="e3bba-121">Идентификатор определения конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="e3bba-121">The ID of the service endpoint definition.</span></span>

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

### <span data-ttu-id="e3bba-122">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e3bba-122">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="e3bba-123">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e3bba-123">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="e3bba-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3bba-124">-Confirm</span></span>
<span data-ttu-id="e3bba-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e3bba-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3bba-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3bba-126">-WhatIf</span></span>
<span data-ttu-id="e3bba-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e3bba-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e3bba-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e3bba-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3bba-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3bba-129">CommonParameters</span></span>
<span data-ttu-id="e3bba-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e3bba-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3bba-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3bba-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3bba-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e3bba-132">INPUTS</span></span>

### <span data-ttu-id="e3bba-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e3bba-133">System.String</span></span>

### <span data-ttu-id="e3bba-134">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e3bba-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

### <span data-ttu-id="e3bba-135">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e3bba-135">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="e3bba-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3bba-136">OUTPUTS</span></span>

### <span data-ttu-id="e3bba-137">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e3bba-137">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="e3bba-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="e3bba-138">NOTES</span></span>

## <span data-ttu-id="e3bba-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e3bba-139">RELATED LINKS</span></span>

[<span data-ttu-id="e3bba-140">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e3bba-140">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="e3bba-141">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e3bba-141">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="e3bba-142">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e3bba-142">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="e3bba-143">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e3bba-143">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)