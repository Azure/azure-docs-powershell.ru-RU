---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 27124aa859fc9c97a74a3ed401c67de328d93884
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073247"
---
# <span data-ttu-id="9351b-101">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9351b-101">New-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="9351b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9351b-102">SYNOPSIS</span></span>
<span data-ttu-id="9351b-103">Создает определение политики конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="9351b-103">Creates a service endpoint policy definition.</span></span>

## <span data-ttu-id="9351b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9351b-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicyDefinition -Name <String> [-Description <String>] [-ServiceResource <String[]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9351b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9351b-105">DESCRIPTION</span></span>
<span data-ttu-id="9351b-106">Командлет **New-AzServiceEndpointPolicyDefinition** создает определение политики конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="9351b-106">The **New-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="9351b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9351b-107">EXAMPLES</span></span>

### <span data-ttu-id="9351b-108">Пример 1: Создание политики конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="9351b-108">Example 1: Creates a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="9351b-109">Эта команда создает определение политики конечной точки службы с именем ServiceEndpointPolicyDefinition1, обслуживанием Microsoft. Storage, подписками на ресурсы служб/Sub1 и описанием "новое определение", которое принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $policydef.</span><span class="sxs-lookup"><span data-stu-id="9351b-109">This command creates the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="9351b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9351b-110">PARAMETERS</span></span>

### <span data-ttu-id="9351b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9351b-111">-DefaultProfile</span></span>
<span data-ttu-id="9351b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9351b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9351b-113">-Описание</span><span class="sxs-lookup"><span data-stu-id="9351b-113">-Description</span></span>
<span data-ttu-id="9351b-114">Описание определения</span><span class="sxs-lookup"><span data-stu-id="9351b-114">The description of the definition</span></span>

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

### <span data-ttu-id="9351b-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9351b-115">-Name</span></span>
<span data-ttu-id="9351b-116">Имя политики конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="9351b-116">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="9351b-117">-Служба</span><span class="sxs-lookup"><span data-stu-id="9351b-117">-Service</span></span>
<span data-ttu-id="9351b-118">Имя службы</span><span class="sxs-lookup"><span data-stu-id="9351b-118">Name of the service</span></span>

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

### <span data-ttu-id="9351b-119">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="9351b-119">-ServiceResource</span></span>
<span data-ttu-id="9351b-120">Список ресурсов служб</span><span class="sxs-lookup"><span data-stu-id="9351b-120">List of service resources</span></span>

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

### <span data-ttu-id="9351b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9351b-121">-Confirm</span></span>
<span data-ttu-id="9351b-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9351b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9351b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9351b-123">-WhatIf</span></span>
<span data-ttu-id="9351b-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9351b-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9351b-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9351b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9351b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9351b-126">CommonParameters</span></span>
<span data-ttu-id="9351b-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9351b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9351b-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9351b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9351b-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9351b-129">INPUTS</span></span>

### <span data-ttu-id="9351b-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="9351b-130">None</span></span>

## <span data-ttu-id="9351b-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9351b-131">OUTPUTS</span></span>

### <span data-ttu-id="9351b-132">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9351b-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="9351b-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="9351b-133">NOTES</span></span>

## <span data-ttu-id="9351b-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9351b-134">RELATED LINKS</span></span>

[<span data-ttu-id="9351b-135">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9351b-135">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="9351b-136">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9351b-136">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="9351b-137">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9351b-137">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="9351b-138">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="9351b-138">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
