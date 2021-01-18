---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 46d86b6a910abcd00257277f61bb44dd426ab945
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98517913"
---
# <span data-ttu-id="1292f-101">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1292f-101">Set-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="1292f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1292f-102">SYNOPSIS</span></span>
<span data-ttu-id="1292f-103">Обновляет определение политики конечных точек службы.</span><span class="sxs-lookup"><span data-stu-id="1292f-103">Updates a service endpoint policy definition.</span></span>

## <span data-ttu-id="1292f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1292f-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1292f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1292f-105">DESCRIPTION</span></span>
<span data-ttu-id="1292f-106">Для создания определения политики конечной точки службы будет создан **cmdlet Set-AzServiceEndpointPolicyDefinition.**</span><span class="sxs-lookup"><span data-stu-id="1292f-106">The **Set-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="1292f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1292f-107">EXAMPLES</span></span>

### <span data-ttu-id="1292f-108">Пример 1. Обновление определения политики конечной точки службы в политике конечных точек службы</span><span class="sxs-lookup"><span data-stu-id="1292f-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="1292f-109">Эта команда обновляет определение политики конечной точки службы с именем Policydef1 в политике конечных точек службы, заданной объектом $ServiceEndpointPolicy.</span><span class="sxs-lookup"><span data-stu-id="1292f-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="1292f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1292f-110">PARAMETERS</span></span>

### <span data-ttu-id="1292f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1292f-111">-DefaultProfile</span></span>
<span data-ttu-id="1292f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1292f-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1292f-113">-Description</span><span class="sxs-lookup"><span data-stu-id="1292f-113">-Description</span></span>
<span data-ttu-id="1292f-114">Описание определения</span><span class="sxs-lookup"><span data-stu-id="1292f-114">The description of the definition</span></span>

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

### <span data-ttu-id="1292f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1292f-115">-Name</span></span>
<span data-ttu-id="1292f-116">Имя правила</span><span class="sxs-lookup"><span data-stu-id="1292f-116">The name of the rule</span></span>

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

### <span data-ttu-id="1292f-117">-Service</span><span class="sxs-lookup"><span data-stu-id="1292f-117">-Service</span></span>
<span data-ttu-id="1292f-118">Имя службы</span><span class="sxs-lookup"><span data-stu-id="1292f-118">Name of the service</span></span>

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

### <span data-ttu-id="1292f-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="1292f-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="1292f-120">The NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="1292f-120">The NetworkSecurityGroup</span></span>

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

### <span data-ttu-id="1292f-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="1292f-121">-ServiceResource</span></span>
<span data-ttu-id="1292f-122">Список ресурсов службы</span><span class="sxs-lookup"><span data-stu-id="1292f-122">List of service resources</span></span>

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

### <span data-ttu-id="1292f-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1292f-123">-Confirm</span></span>
<span data-ttu-id="1292f-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="1292f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1292f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1292f-125">-WhatIf</span></span>
<span data-ttu-id="1292f-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1292f-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1292f-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1292f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1292f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1292f-128">CommonParameters</span></span>
<span data-ttu-id="1292f-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1292f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1292f-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1292f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1292f-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1292f-131">INPUTS</span></span>

### <span data-ttu-id="1292f-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="1292f-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="1292f-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1292f-133">OUTPUTS</span></span>

### <span data-ttu-id="1292f-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="1292f-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="1292f-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1292f-135">NOTES</span></span>

## <span data-ttu-id="1292f-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1292f-136">RELATED LINKS</span></span>

[<span data-ttu-id="1292f-137">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1292f-137">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="1292f-138">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1292f-138">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="1292f-139">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1292f-139">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="1292f-140">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1292f-140">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)
