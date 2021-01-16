---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: eaab1bdf26fb1cb99bfa7e947a4b7140971fda53
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410612"
---
# <span data-ttu-id="f514a-101">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f514a-101">Add-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="f514a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f514a-102">SYNOPSIS</span></span>
<span data-ttu-id="f514a-103">Добавляет определение политики конечной точки службы в указанную политику.</span><span class="sxs-lookup"><span data-stu-id="f514a-103">Adds a service endpoint policy definition to a specified policy.</span></span>

## <span data-ttu-id="f514a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f514a-104">SYNTAX</span></span>

```
Add-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f514a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f514a-105">DESCRIPTION</span></span>
<span data-ttu-id="f514a-106">Для **этого к политике добавляется** определение конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="f514a-106">The **Add-AzServiceEndpointPolicyDefinition** cmdlet add a service endpoint policy definition to the policy.</span></span>

## <span data-ttu-id="f514a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f514a-107">EXAMPLES</span></span>

### <span data-ttu-id="f514a-108">Пример 1. Обновление определения политики конечной точки службы в политике конечных точек службы</span><span class="sxs-lookup"><span data-stu-id="f514a-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="f514a-109">Эта команда обновила определение политики конечной точки обслуживания с именами ServiceEndpointPolicyDefinition1, службой Microsoft.Storage, подписками на ресурсы службы/sub1 и описанием "Новое определение", которое принадлежит группе ресурсов ResourceGroup01 и хранит ее в переменной $policydef.</span><span class="sxs-lookup"><span data-stu-id="f514a-109">This command updated the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="f514a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f514a-110">PARAMETERS</span></span>

### <span data-ttu-id="f514a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f514a-111">-DefaultProfile</span></span>
<span data-ttu-id="f514a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f514a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f514a-113">-Description</span><span class="sxs-lookup"><span data-stu-id="f514a-113">-Description</span></span>
<span data-ttu-id="f514a-114">Описание определения</span><span class="sxs-lookup"><span data-stu-id="f514a-114">The description of the definition</span></span>

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

### <span data-ttu-id="f514a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f514a-115">-Name</span></span>
<span data-ttu-id="f514a-116">Имя определения политики конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="f514a-116">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="f514a-117">-Service</span><span class="sxs-lookup"><span data-stu-id="f514a-117">-Service</span></span>
<span data-ttu-id="f514a-118">Имя службы</span><span class="sxs-lookup"><span data-stu-id="f514a-118">Name of the service</span></span>

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

### <span data-ttu-id="f514a-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f514a-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="f514a-120">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f514a-120">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="f514a-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="f514a-121">-ServiceResource</span></span>
<span data-ttu-id="f514a-122">Список ресурсов службы</span><span class="sxs-lookup"><span data-stu-id="f514a-122">List of service resources</span></span>

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

### <span data-ttu-id="f514a-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f514a-123">-Confirm</span></span>
<span data-ttu-id="f514a-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f514a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f514a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f514a-125">-WhatIf</span></span>
<span data-ttu-id="f514a-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f514a-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f514a-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f514a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f514a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f514a-128">CommonParameters</span></span>
<span data-ttu-id="f514a-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f514a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f514a-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f514a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f514a-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f514a-131">INPUTS</span></span>

### <span data-ttu-id="f514a-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f514a-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="f514a-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f514a-133">OUTPUTS</span></span>

### <span data-ttu-id="f514a-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="f514a-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="f514a-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f514a-135">NOTES</span></span>

## <span data-ttu-id="f514a-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f514a-136">RELATED LINKS</span></span>

[<span data-ttu-id="f514a-137">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f514a-137">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="f514a-138">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f514a-138">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="f514a-139">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f514a-139">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="f514a-140">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="f514a-140">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
