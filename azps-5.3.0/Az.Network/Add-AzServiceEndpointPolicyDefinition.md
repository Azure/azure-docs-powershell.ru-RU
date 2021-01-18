---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: eaab1bdf26fb1cb99bfa7e947a4b7140971fda53
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506142"
---
# <span data-ttu-id="57151-101">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="57151-101">Add-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="57151-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57151-102">SYNOPSIS</span></span>
<span data-ttu-id="57151-103">Добавляет определение политики конечной точки службы в указанную политику.</span><span class="sxs-lookup"><span data-stu-id="57151-103">Adds a service endpoint policy definition to a specified policy.</span></span>

## <span data-ttu-id="57151-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="57151-104">SYNTAX</span></span>

```
Add-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57151-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="57151-105">DESCRIPTION</span></span>
<span data-ttu-id="57151-106">Для **этого к политике добавляется** определение конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="57151-106">The **Add-AzServiceEndpointPolicyDefinition** cmdlet add a service endpoint policy definition to the policy.</span></span>

## <span data-ttu-id="57151-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="57151-107">EXAMPLES</span></span>

### <span data-ttu-id="57151-108">Пример 1. Обновление определения политики конечной точки службы в политике конечных точек службы</span><span class="sxs-lookup"><span data-stu-id="57151-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$policydef= New-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ResourceGroupName "ResourceGroup01" -Service "Microsoft.Storage" -ServiceResources "subscriptions/sub1" -Description "New Definition"
```

<span data-ttu-id="57151-109">Эта команда обновила определение политики конечной точки службы с именами ServiceEndpointPolicyDefinition1, Службой Microsoft.Storage, подписками на ресурсы службы/sub1 и описанием "Новое определение", которое принадлежит группе ресурсов ResourceGroup01 и хранит ее в переменной $policydef.</span><span class="sxs-lookup"><span data-stu-id="57151-109">This command updated the service endpoint policy definition with name ServiceEndpointPolicyDefinition1,  service Microsoft.Storage, service resources subscriptions/sub1 and description "New Definition" that belongs to the resource group named ResourceGroup01 and stores it in the $policydef variable.</span></span>

## <span data-ttu-id="57151-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57151-110">PARAMETERS</span></span>

### <span data-ttu-id="57151-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57151-111">-DefaultProfile</span></span>
<span data-ttu-id="57151-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="57151-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57151-113">-Description</span><span class="sxs-lookup"><span data-stu-id="57151-113">-Description</span></span>
<span data-ttu-id="57151-114">Описание определения</span><span class="sxs-lookup"><span data-stu-id="57151-114">The description of the definition</span></span>

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

### <span data-ttu-id="57151-115">-Name</span><span class="sxs-lookup"><span data-stu-id="57151-115">-Name</span></span>
<span data-ttu-id="57151-116">Имя определения политики конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="57151-116">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="57151-117">-Service</span><span class="sxs-lookup"><span data-stu-id="57151-117">-Service</span></span>
<span data-ttu-id="57151-118">Имя службы</span><span class="sxs-lookup"><span data-stu-id="57151-118">Name of the service</span></span>

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

### <span data-ttu-id="57151-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="57151-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="57151-120">The ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="57151-120">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="57151-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="57151-121">-ServiceResource</span></span>
<span data-ttu-id="57151-122">Список ресурсов службы</span><span class="sxs-lookup"><span data-stu-id="57151-122">List of service resources</span></span>

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

### <span data-ttu-id="57151-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="57151-123">-Confirm</span></span>
<span data-ttu-id="57151-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="57151-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57151-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57151-125">-WhatIf</span></span>
<span data-ttu-id="57151-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57151-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="57151-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="57151-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57151-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57151-128">CommonParameters</span></span>
<span data-ttu-id="57151-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57151-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57151-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57151-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57151-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57151-131">INPUTS</span></span>

### <span data-ttu-id="57151-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="57151-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="57151-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="57151-133">OUTPUTS</span></span>

### <span data-ttu-id="57151-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="57151-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="57151-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="57151-135">NOTES</span></span>

## <span data-ttu-id="57151-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="57151-136">RELATED LINKS</span></span>

[<span data-ttu-id="57151-137">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="57151-137">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="57151-138">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="57151-138">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="57151-139">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="57151-139">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="57151-140">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="57151-140">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
