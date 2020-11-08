---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: eaab1bdf26fb1cb99bfa7e947a4b7140971fda53
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249891"
---
# <span data-ttu-id="226c7-101">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="226c7-101">Add-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="226c7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="226c7-102">SYNOPSIS</span></span>
<span data-ttu-id="226c7-103">Добавляет определение политики конечной точки службы к указанной политике.</span><span class="sxs-lookup"><span data-stu-id="226c7-103">Adds a service endpoint policy definition to a specified policy.</span></span>

## <span data-ttu-id="226c7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="226c7-104">SYNTAX</span></span>

```
Add-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="226c7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="226c7-105">DESCRIPTION</span></span>
<span data-ttu-id="226c7-106">Командлет **Add-AzServiceEndpointPolicyDefinition** добавляет определение политики конечной точки службы в политику.</span><span class="sxs-lookup"><span data-stu-id="226c7-106">The **Add-AzServiceEndpointPolicyDefinition** cmdlet add a service endpoint policy definition to the policy.</span></span>

## <span data-ttu-id="226c7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="226c7-107">EXAMPLES</span></span>

### <span data-ttu-id="226c7-108">Пример 1: обновление определения политики конечной точки службы в политике конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="226c7-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="226c7-109">Эта команда обновила определение политики конечной точки службы с именем ServiceEndpointPolicyDefinition1, обслуживанием Microsoft. Storage, подписками на ресурсы служб/Sub1 и описанием "новое определение", которое принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $policydef.</span><span class="sxs-lookup"><span data-stu-id="226c7-109">This command updated the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="226c7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="226c7-110">PARAMETERS</span></span>

### <span data-ttu-id="226c7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="226c7-111">-DefaultProfile</span></span>
<span data-ttu-id="226c7-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="226c7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="226c7-113">-Описание</span><span class="sxs-lookup"><span data-stu-id="226c7-113">-Description</span></span>
<span data-ttu-id="226c7-114">Описание определения</span><span class="sxs-lookup"><span data-stu-id="226c7-114">The description of the definition</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="226c7-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="226c7-115">-Name</span></span>
<span data-ttu-id="226c7-116">Имя определения политики конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="226c7-116">The name of the service endpoint policy definition</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="226c7-117">-Служба</span><span class="sxs-lookup"><span data-stu-id="226c7-117">-Service</span></span>
<span data-ttu-id="226c7-118">Имя службы</span><span class="sxs-lookup"><span data-stu-id="226c7-118">Name of the service</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="226c7-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="226c7-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="226c7-120">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="226c7-120">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="226c7-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="226c7-121">-ServiceResource</span></span>
<span data-ttu-id="226c7-122">Список ресурсов служб</span><span class="sxs-lookup"><span data-stu-id="226c7-122">List of service resources</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="226c7-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="226c7-123">-Confirm</span></span>
<span data-ttu-id="226c7-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="226c7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="226c7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="226c7-125">-WhatIf</span></span>
<span data-ttu-id="226c7-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="226c7-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="226c7-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="226c7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="226c7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="226c7-128">CommonParameters</span></span>
<span data-ttu-id="226c7-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="226c7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="226c7-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="226c7-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="226c7-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="226c7-131">INPUTS</span></span>

### <span data-ttu-id="226c7-132">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="226c7-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="226c7-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="226c7-133">OUTPUTS</span></span>

### <span data-ttu-id="226c7-134">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="226c7-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="226c7-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="226c7-135">NOTES</span></span>

## <span data-ttu-id="226c7-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="226c7-136">RELATED LINKS</span></span>

[<span data-ttu-id="226c7-137">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="226c7-137">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="226c7-138">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="226c7-138">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="226c7-139">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="226c7-139">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="226c7-140">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="226c7-140">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
