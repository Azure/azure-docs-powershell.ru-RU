---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: c907c60619f5a0a2fc5f0620f086ba0b99ca62ac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93903405"
---
# <span data-ttu-id="d2eb7-101">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d2eb7-101">Remove-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="d2eb7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d2eb7-102">SYNOPSIS</span></span>
<span data-ttu-id="d2eb7-103">Удаляет определение политики конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-103">Removes a service endpoint policy definition.</span></span>

## <span data-ttu-id="d2eb7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d2eb7-104">SYNTAX</span></span>

### <span data-ttu-id="d2eb7-105">RemoveByNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d2eb7-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2eb7-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2eb7-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -ResourceId <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2eb7-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2eb7-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -InputObject <PSServiceEndpointPolicyDefinition>
 -ServiceEndpointPolicy <PSServiceEndpointPolicy> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2eb7-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2eb7-108">DESCRIPTION</span></span>
<span data-ttu-id="d2eb7-109">Командлет **Remove-AzServiceEndpointPolicy** удаляет политику конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-109">The **Remove-AzServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="d2eb7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d2eb7-110">EXAMPLES</span></span>

### <span data-ttu-id="d2eb7-111">Пример 1: Удаление политики конечной точки службы с помощью имени</span><span class="sxs-lookup"><span data-stu-id="d2eb7-111">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="d2eb7-112">Эта команда удаляет политику конечной точки службы с именем PolicyDef1</span><span class="sxs-lookup"><span data-stu-id="d2eb7-112">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="d2eb7-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d2eb7-113">PARAMETERS</span></span>

### <span data-ttu-id="d2eb7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2eb7-114">-DefaultProfile</span></span>
<span data-ttu-id="d2eb7-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2eb7-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2eb7-116">-InputObject</span></span>
<span data-ttu-id="d2eb7-117">Объект определения политики конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-117">The service endpoint policy definition object.</span></span>

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

### <span data-ttu-id="d2eb7-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d2eb7-118">-Name</span></span>
<span data-ttu-id="d2eb7-119">Имя определения конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-119">The name of the service endpoint definition</span></span>

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

### <span data-ttu-id="d2eb7-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2eb7-120">-ResourceId</span></span>
<span data-ttu-id="d2eb7-121">Идентификатор определения конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-121">The ID of the service endpoint definition.</span></span>

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

### <span data-ttu-id="d2eb7-122">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d2eb7-122">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="d2eb7-123">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d2eb7-123">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="d2eb7-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2eb7-124">-Confirm</span></span>
<span data-ttu-id="d2eb7-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2eb7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2eb7-126">-WhatIf</span></span>
<span data-ttu-id="d2eb7-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2eb7-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2eb7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2eb7-129">CommonParameters</span></span>
<span data-ttu-id="d2eb7-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d2eb7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2eb7-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2eb7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2eb7-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d2eb7-132">INPUTS</span></span>

### <span data-ttu-id="d2eb7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="d2eb7-133">System.String</span></span>

### <span data-ttu-id="d2eb7-134">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d2eb7-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

### <span data-ttu-id="d2eb7-135">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d2eb7-135">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="d2eb7-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d2eb7-136">OUTPUTS</span></span>

### <span data-ttu-id="d2eb7-137">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="d2eb7-137">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="d2eb7-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="d2eb7-138">NOTES</span></span>

## <span data-ttu-id="d2eb7-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d2eb7-139">RELATED LINKS</span></span>

[<span data-ttu-id="d2eb7-140">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d2eb7-140">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="d2eb7-141">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d2eb7-141">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="d2eb7-142">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d2eb7-142">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="d2eb7-143">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d2eb7-143">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
