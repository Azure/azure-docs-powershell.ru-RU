---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 554d3285c80370559bbedfb91430d2b6801a6f51
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959496"
---
# <span data-ttu-id="4a63e-101">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4a63e-101">Get-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="4a63e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a63e-102">SYNOPSIS</span></span>
<span data-ttu-id="4a63e-103">Получает определение политики конечных точек службы.</span><span class="sxs-lookup"><span data-stu-id="4a63e-103">Gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="4a63e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4a63e-104">SYNTAX</span></span>

```
Get-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4a63e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a63e-105">DESCRIPTION</span></span>
<span data-ttu-id="4a63e-106">Для получения определения политики конечной точки службы возвращается **cmdlet Get-AzServiceEndpointPolicyDefinition.**</span><span class="sxs-lookup"><span data-stu-id="4a63e-106">The **Get-AzServiceEndpointPolicyDefinition** cmdlet gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="4a63e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4a63e-107">EXAMPLES</span></span>

### <span data-ttu-id="4a63e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4a63e-108">Example 1</span></span>
```
$policydef= Get-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ServiceEndpointPolicy $Policy
```

<span data-ttu-id="4a63e-109">Эта команда получает определение политики конечной точки службы ServiceEndpointPolicyDefinition1 в ServiceEndpointPolicy $Policy сохраняет его в переменной $policydef службы.</span><span class="sxs-lookup"><span data-stu-id="4a63e-109">This command gets the service endpoint policy definition named ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy stores it in the $policydef variable.</span></span>

## <span data-ttu-id="4a63e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4a63e-110">PARAMETERS</span></span>

### <span data-ttu-id="4a63e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a63e-111">-DefaultProfile</span></span>
<span data-ttu-id="4a63e-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4a63e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a63e-113">-Name</span><span class="sxs-lookup"><span data-stu-id="4a63e-113">-Name</span></span>
<span data-ttu-id="4a63e-114">Имя определения политики конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="4a63e-114">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="4a63e-115">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4a63e-115">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="4a63e-116">Политика конечных точек службы</span><span class="sxs-lookup"><span data-stu-id="4a63e-116">The Service endpoint policy</span></span>

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

### <span data-ttu-id="4a63e-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4a63e-117">-Confirm</span></span>
<span data-ttu-id="4a63e-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a63e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a63e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a63e-119">-WhatIf</span></span>
<span data-ttu-id="4a63e-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a63e-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4a63e-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4a63e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a63e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a63e-122">CommonParameters</span></span>
<span data-ttu-id="4a63e-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a63e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a63e-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4a63e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a63e-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4a63e-125">INPUTS</span></span>

### <span data-ttu-id="4a63e-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4a63e-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="4a63e-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4a63e-127">OUTPUTS</span></span>

### <span data-ttu-id="4a63e-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4a63e-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="4a63e-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4a63e-129">NOTES</span></span>

## <span data-ttu-id="4a63e-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4a63e-130">RELATED LINKS</span></span>

[<span data-ttu-id="4a63e-131">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4a63e-131">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="4a63e-132">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4a63e-132">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="4a63e-133">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4a63e-133">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="4a63e-134">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4a63e-134">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
