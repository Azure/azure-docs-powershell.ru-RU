---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 634beeaf33515ac5e89011ab47eaea34eccaa581
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730275"
---
# <span data-ttu-id="7c1e3-101">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7c1e3-101">New-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="7c1e3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7c1e3-102">SYNOPSIS</span></span>
<span data-ttu-id="7c1e3-103">Создает определение политики конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="7c1e3-103">Creates a service endpoint policy definition.</span></span>

## <span data-ttu-id="7c1e3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7c1e3-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicyDefinition -Name <String> [-Description <String>] [-ServiceResource <String[]>]
 [-Service <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c1e3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c1e3-105">DESCRIPTION</span></span>
<span data-ttu-id="7c1e3-106">Командлет **New-AzServiceEndpointPolicyDefinition** создает определение политики конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="7c1e3-106">The **New-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="7c1e3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7c1e3-107">EXAMPLES</span></span>

### <span data-ttu-id="7c1e3-108">Пример 1: Создание политики конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="7c1e3-108">Example 1: Creates a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="7c1e3-109">Эта команда создает определение политики конечной точки службы с именем ServiceEndpointPolicyDefinition1, обслуживанием Microsoft. Storage, подписками на ресурсы служб/Sub1 и описанием "новое определение", которое принадлежит группе ресурсов с именем ResourceGroup01, и сохраняет его в переменной $policydef.</span><span class="sxs-lookup"><span data-stu-id="7c1e3-109">This command creates the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="7c1e3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7c1e3-110">PARAMETERS</span></span>

### <span data-ttu-id="7c1e3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c1e3-111">-DefaultProfile</span></span>
<span data-ttu-id="7c1e3-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7c1e3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c1e3-113">-Описание</span><span class="sxs-lookup"><span data-stu-id="7c1e3-113">-Description</span></span>
<span data-ttu-id="7c1e3-114">Описание определения</span><span class="sxs-lookup"><span data-stu-id="7c1e3-114">The description of the definition</span></span>

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

### <span data-ttu-id="7c1e3-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7c1e3-115">-Name</span></span>
<span data-ttu-id="7c1e3-116">Имя политики конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="7c1e3-116">The name of the service endpoint policy</span></span>

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

### <span data-ttu-id="7c1e3-117">-Служба</span><span class="sxs-lookup"><span data-stu-id="7c1e3-117">-Service</span></span>
<span data-ttu-id="7c1e3-118">Имя службы</span><span class="sxs-lookup"><span data-stu-id="7c1e3-118">Name of the service</span></span>

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

### <span data-ttu-id="7c1e3-119">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="7c1e3-119">-ServiceResource</span></span>
<span data-ttu-id="7c1e3-120">Список ресурсов служб</span><span class="sxs-lookup"><span data-stu-id="7c1e3-120">List of service resources</span></span>

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

### <span data-ttu-id="7c1e3-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c1e3-121">-Confirm</span></span>
<span data-ttu-id="7c1e3-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7c1e3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c1e3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c1e3-123">-WhatIf</span></span>
<span data-ttu-id="7c1e3-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7c1e3-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c1e3-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7c1e3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c1e3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c1e3-126">CommonParameters</span></span>
<span data-ttu-id="7c1e3-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7c1e3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c1e3-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c1e3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c1e3-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7c1e3-129">INPUTS</span></span>

### <span data-ttu-id="7c1e3-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="7c1e3-130">None</span></span>

## <span data-ttu-id="7c1e3-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7c1e3-131">OUTPUTS</span></span>

### <span data-ttu-id="7c1e3-132">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7c1e3-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="7c1e3-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="7c1e3-133">NOTES</span></span>

## <span data-ttu-id="7c1e3-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7c1e3-134">RELATED LINKS</span></span>

[<span data-ttu-id="7c1e3-135">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7c1e3-135">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="7c1e3-136">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7c1e3-136">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="7c1e3-137">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7c1e3-137">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="7c1e3-138">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7c1e3-138">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
