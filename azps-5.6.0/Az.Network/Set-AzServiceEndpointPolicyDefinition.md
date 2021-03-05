---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: bc68a57437bae2af10b5ee39221459aebf82a2df
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010296"
---
# <span data-ttu-id="ea912-101">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ea912-101">Set-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="ea912-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea912-102">SYNOPSIS</span></span>
<span data-ttu-id="ea912-103">Обновляет определение политики конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="ea912-103">Updates a service endpoint policy definition.</span></span>

## <span data-ttu-id="ea912-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ea912-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea912-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea912-105">DESCRIPTION</span></span>
<span data-ttu-id="ea912-106">Для создания определения политики конечной точки службы будет создан **cmdlet Set-AzServiceEndpointPolicyDefinition.**</span><span class="sxs-lookup"><span data-stu-id="ea912-106">The **Set-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="ea912-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ea912-107">EXAMPLES</span></span>

### <span data-ttu-id="ea912-108">Пример 1. Обновление определения политики конечной точки службы в политике конечных точек службы</span><span class="sxs-lookup"><span data-stu-id="ea912-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="ea912-109">Эта команда обновляет определение политики конечной точки службы с именем Policydef1 в политике конечных точек службы, заданной объектом $ServiceEndpointPolicy.</span><span class="sxs-lookup"><span data-stu-id="ea912-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="ea912-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea912-110">PARAMETERS</span></span>

### <span data-ttu-id="ea912-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea912-111">-DefaultProfile</span></span>
<span data-ttu-id="ea912-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ea912-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea912-113">-Description</span><span class="sxs-lookup"><span data-stu-id="ea912-113">-Description</span></span>
<span data-ttu-id="ea912-114">Описание определения</span><span class="sxs-lookup"><span data-stu-id="ea912-114">The description of the definition</span></span>

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

### <span data-ttu-id="ea912-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ea912-115">-Name</span></span>
<span data-ttu-id="ea912-116">Имя правила</span><span class="sxs-lookup"><span data-stu-id="ea912-116">The name of the rule</span></span>

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

### <span data-ttu-id="ea912-117">-Service</span><span class="sxs-lookup"><span data-stu-id="ea912-117">-Service</span></span>
<span data-ttu-id="ea912-118">Имя службы</span><span class="sxs-lookup"><span data-stu-id="ea912-118">Name of the service</span></span>

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

### <span data-ttu-id="ea912-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ea912-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="ea912-120">The NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ea912-120">The NetworkSecurityGroup</span></span>

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

### <span data-ttu-id="ea912-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="ea912-121">-ServiceResource</span></span>
<span data-ttu-id="ea912-122">Список ресурсов службы</span><span class="sxs-lookup"><span data-stu-id="ea912-122">List of service resources</span></span>

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

### <span data-ttu-id="ea912-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea912-123">-Confirm</span></span>
<span data-ttu-id="ea912-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ea912-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea912-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea912-125">-WhatIf</span></span>
<span data-ttu-id="ea912-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea912-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ea912-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ea912-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea912-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea912-128">CommonParameters</span></span>
<span data-ttu-id="ea912-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea912-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea912-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea912-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea912-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ea912-131">INPUTS</span></span>

### <span data-ttu-id="ea912-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ea912-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="ea912-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ea912-133">OUTPUTS</span></span>

### <span data-ttu-id="ea912-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ea912-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="ea912-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ea912-135">NOTES</span></span>

## <span data-ttu-id="ea912-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea912-136">RELATED LINKS</span></span>

[<span data-ttu-id="ea912-137">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ea912-137">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="ea912-138">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ea912-138">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="ea912-139">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ea912-139">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="ea912-140">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ea912-140">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)
