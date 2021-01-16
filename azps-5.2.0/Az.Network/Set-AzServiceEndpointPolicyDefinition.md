---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 46d86b6a910abcd00257277f61bb44dd426ab945
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98409335"
---
# <span data-ttu-id="e60b8-101">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e60b8-101">Set-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="e60b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e60b8-102">SYNOPSIS</span></span>
<span data-ttu-id="e60b8-103">Обновляет определение политики конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="e60b8-103">Updates a service endpoint policy definition.</span></span>

## <span data-ttu-id="e60b8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e60b8-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e60b8-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e60b8-105">DESCRIPTION</span></span>
<span data-ttu-id="e60b8-106">Для создания определения политики конечной точки службы будет создан **cmdlet Set-AzServiceEndpointPolicyDefinition.**</span><span class="sxs-lookup"><span data-stu-id="e60b8-106">The **Set-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="e60b8-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e60b8-107">EXAMPLES</span></span>

### <span data-ttu-id="e60b8-108">Пример 1. Обновление определения политики конечной точки службы в политике конечных точек службы</span><span class="sxs-lookup"><span data-stu-id="e60b8-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="e60b8-109">Эта команда обновляет определение политики конечной точки службы с именем Policydef1 в политике конечных точек службы, заданной объектом $ServiceEndpointPolicy.</span><span class="sxs-lookup"><span data-stu-id="e60b8-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="e60b8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e60b8-110">PARAMETERS</span></span>

### <span data-ttu-id="e60b8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e60b8-111">-DefaultProfile</span></span>
<span data-ttu-id="e60b8-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e60b8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e60b8-113">-Description</span><span class="sxs-lookup"><span data-stu-id="e60b8-113">-Description</span></span>
<span data-ttu-id="e60b8-114">Описание определения</span><span class="sxs-lookup"><span data-stu-id="e60b8-114">The description of the definition</span></span>

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

### <span data-ttu-id="e60b8-115">-Name</span><span class="sxs-lookup"><span data-stu-id="e60b8-115">-Name</span></span>
<span data-ttu-id="e60b8-116">Имя правила</span><span class="sxs-lookup"><span data-stu-id="e60b8-116">The name of the rule</span></span>

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

### <span data-ttu-id="e60b8-117">-Service</span><span class="sxs-lookup"><span data-stu-id="e60b8-117">-Service</span></span>
<span data-ttu-id="e60b8-118">Имя службы</span><span class="sxs-lookup"><span data-stu-id="e60b8-118">Name of the service</span></span>

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

### <span data-ttu-id="e60b8-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e60b8-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="e60b8-120">The NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="e60b8-120">The NetworkSecurityGroup</span></span>

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

### <span data-ttu-id="e60b8-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="e60b8-121">-ServiceResource</span></span>
<span data-ttu-id="e60b8-122">Список ресурсов службы</span><span class="sxs-lookup"><span data-stu-id="e60b8-122">List of service resources</span></span>

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

### <span data-ttu-id="e60b8-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e60b8-123">-Confirm</span></span>
<span data-ttu-id="e60b8-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e60b8-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e60b8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e60b8-125">-WhatIf</span></span>
<span data-ttu-id="e60b8-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e60b8-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e60b8-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e60b8-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e60b8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e60b8-128">CommonParameters</span></span>
<span data-ttu-id="e60b8-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e60b8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e60b8-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e60b8-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e60b8-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e60b8-131">INPUTS</span></span>

### <span data-ttu-id="e60b8-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e60b8-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="e60b8-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e60b8-133">OUTPUTS</span></span>

### <span data-ttu-id="e60b8-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="e60b8-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="e60b8-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e60b8-135">NOTES</span></span>

## <span data-ttu-id="e60b8-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e60b8-136">RELATED LINKS</span></span>

[<span data-ttu-id="e60b8-137">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e60b8-137">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="e60b8-138">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e60b8-138">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="e60b8-139">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e60b8-139">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="e60b8-140">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e60b8-140">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)
