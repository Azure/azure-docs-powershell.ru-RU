---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 69a9fd259350238175016b3245d22022845a9f51
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904382"
---
# <span data-ttu-id="311bc-101">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="311bc-101">Set-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="311bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="311bc-102">SYNOPSIS</span></span>
<span data-ttu-id="311bc-103">Обновляет определение политики конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="311bc-103">Updates a service endpoint policy definition.</span></span>

## <span data-ttu-id="311bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="311bc-104">SYNTAX</span></span>

```
Set-AzServiceEndpointPolicyDefinition -Name <String> -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-Description <String>] [-ServiceResource <String[]>] [-Service <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="311bc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="311bc-105">DESCRIPTION</span></span>
<span data-ttu-id="311bc-106">Командлет **Set-AzServiceEndpointPolicyDefinition** создает определение политики конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="311bc-106">The **Set-AzServiceEndpointPolicyDefinition** cmdlet create a service endpoint policy definition.</span></span>

## <span data-ttu-id="311bc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="311bc-107">EXAMPLES</span></span>

### <span data-ttu-id="311bc-108">Пример 1: обновление определения политики конечной точки службы в политике конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="311bc-108">Example 1: Updates a service endpoint policy definition in a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzServiceEndpointPolicyDefinition -Name "Policydef1" -ServiceEndpointPolicy $serviceEndpointPolicy
```

<span data-ttu-id="311bc-109">Эта команда обновляет определение политики конечной точки службы с именем Policydef1 в политике конечной точки службы, определенной объектом $ServiceEndpointPolicy.</span><span class="sxs-lookup"><span data-stu-id="311bc-109">This command updates a service endpoint policy definition named Policydef1 in the service endpoint policy defined by the object $ServiceEndpointPolicy.</span></span>

## <span data-ttu-id="311bc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="311bc-110">PARAMETERS</span></span>

### <span data-ttu-id="311bc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="311bc-111">-DefaultProfile</span></span>
<span data-ttu-id="311bc-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="311bc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="311bc-113">-Описание</span><span class="sxs-lookup"><span data-stu-id="311bc-113">-Description</span></span>
<span data-ttu-id="311bc-114">Описание определения</span><span class="sxs-lookup"><span data-stu-id="311bc-114">The description of the definition</span></span>

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

### <span data-ttu-id="311bc-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="311bc-115">-Name</span></span>
<span data-ttu-id="311bc-116">Имя правила.</span><span class="sxs-lookup"><span data-stu-id="311bc-116">The name of the rule</span></span>

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

### <span data-ttu-id="311bc-117">-Служба</span><span class="sxs-lookup"><span data-stu-id="311bc-117">-Service</span></span>
<span data-ttu-id="311bc-118">Имя службы</span><span class="sxs-lookup"><span data-stu-id="311bc-118">Name of the service</span></span>

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

### <span data-ttu-id="311bc-119">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="311bc-119">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="311bc-120">NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="311bc-120">The NetworkSecurityGroup</span></span>

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

### <span data-ttu-id="311bc-121">-ServiceResource</span><span class="sxs-lookup"><span data-stu-id="311bc-121">-ServiceResource</span></span>
<span data-ttu-id="311bc-122">Список ресурсов служб</span><span class="sxs-lookup"><span data-stu-id="311bc-122">List of service resources</span></span>

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

### <span data-ttu-id="311bc-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="311bc-123">-Confirm</span></span>
<span data-ttu-id="311bc-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="311bc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="311bc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="311bc-125">-WhatIf</span></span>
<span data-ttu-id="311bc-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="311bc-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="311bc-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="311bc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="311bc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="311bc-128">CommonParameters</span></span>
<span data-ttu-id="311bc-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="311bc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="311bc-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="311bc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="311bc-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="311bc-131">INPUTS</span></span>

### <span data-ttu-id="311bc-132">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="311bc-132">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="311bc-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="311bc-133">OUTPUTS</span></span>

### <span data-ttu-id="311bc-134">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="311bc-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="311bc-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="311bc-135">NOTES</span></span>

## <span data-ttu-id="311bc-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="311bc-136">RELATED LINKS</span></span>

[<span data-ttu-id="311bc-137">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="311bc-137">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="311bc-138">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="311bc-138">Get-AzServiceEndpointPolicyDefinition</span></span>](./Get-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="311bc-139">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="311bc-139">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="311bc-140">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="311bc-140">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)
