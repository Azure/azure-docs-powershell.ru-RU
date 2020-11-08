---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 164fc5edb4bac3b90debde0aaf6205c719f5c95c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235520"
---
# <span data-ttu-id="fc59b-101">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="fc59b-101">Get-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="fc59b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fc59b-102">SYNOPSIS</span></span>
<span data-ttu-id="fc59b-103">Получает определение политики конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="fc59b-103">Gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="fc59b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fc59b-104">SYNTAX</span></span>

```
Get-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc59b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc59b-105">DESCRIPTION</span></span>
<span data-ttu-id="fc59b-106">Командлет **Get-AzServiceEndpointPolicyDefinition** получает определение политики конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="fc59b-106">The **Get-AzServiceEndpointPolicyDefinition** cmdlet gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="fc59b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fc59b-107">EXAMPLES</span></span>

### <span data-ttu-id="fc59b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fc59b-108">Example 1</span></span>
```
$policydef= Get-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ServiceEndpointPolicy $Policy
```

<span data-ttu-id="fc59b-109">Эта команда получает определение политики конечной точки службы с именем ServiceEndpointPolicyDefinition1 в ServiceEndpointPolicy $Policy сохраняет его в переменной $policydef.</span><span class="sxs-lookup"><span data-stu-id="fc59b-109">This command gets the service endpoint policy definition named ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy stores it in the $policydef variable.</span></span>

## <span data-ttu-id="fc59b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fc59b-110">PARAMETERS</span></span>

### <span data-ttu-id="fc59b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc59b-111">-DefaultProfile</span></span>
<span data-ttu-id="fc59b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fc59b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc59b-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fc59b-113">-Name</span></span>
<span data-ttu-id="fc59b-114">Имя определения политики конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="fc59b-114">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="fc59b-115">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="fc59b-115">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="fc59b-116">Политика конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="fc59b-116">The Service endpoint policy</span></span>

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

### <span data-ttu-id="fc59b-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc59b-117">-Confirm</span></span>
<span data-ttu-id="fc59b-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fc59b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc59b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc59b-119">-WhatIf</span></span>
<span data-ttu-id="fc59b-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fc59b-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fc59b-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fc59b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc59b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc59b-122">CommonParameters</span></span>
<span data-ttu-id="fc59b-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fc59b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc59b-124">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc59b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc59b-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fc59b-125">INPUTS</span></span>

### <span data-ttu-id="fc59b-126">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="fc59b-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="fc59b-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc59b-127">OUTPUTS</span></span>

### <span data-ttu-id="fc59b-128">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="fc59b-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="fc59b-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="fc59b-129">NOTES</span></span>

## <span data-ttu-id="fc59b-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fc59b-130">RELATED LINKS</span></span>

[<span data-ttu-id="fc59b-131">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="fc59b-131">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="fc59b-132">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="fc59b-132">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="fc59b-133">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="fc59b-133">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="fc59b-134">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="fc59b-134">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)