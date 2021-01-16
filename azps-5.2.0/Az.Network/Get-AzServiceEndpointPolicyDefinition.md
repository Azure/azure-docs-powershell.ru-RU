---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 164fc5edb4bac3b90debde0aaf6205c719f5c95c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399671"
---
# <span data-ttu-id="1e0f7-101">Get-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1e0f7-101">Get-AzServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="1e0f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e0f7-102">SYNOPSIS</span></span>
<span data-ttu-id="1e0f7-103">Возвращает определение политики конечных точек службы.</span><span class="sxs-lookup"><span data-stu-id="1e0f7-103">Gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="1e0f7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1e0f7-104">SYNTAX</span></span>

```
Get-AzServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e0f7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e0f7-105">DESCRIPTION</span></span>
<span data-ttu-id="1e0f7-106">Для получения определения политики конечной точки службы возвращается **cmdlet Get-AzServiceEndpointPolicyDefinition.**</span><span class="sxs-lookup"><span data-stu-id="1e0f7-106">The **Get-AzServiceEndpointPolicyDefinition** cmdlet gets a service endpoint policy definition.</span></span>

## <span data-ttu-id="1e0f7-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1e0f7-107">EXAMPLES</span></span>

### <span data-ttu-id="1e0f7-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1e0f7-108">Example 1</span></span>
```
$policydef= Get-AzServiceEndpointPolicyDefinition -Name "ServiceEndpointPolicyDefinition1" -ServiceEndpointPolicy $Policy
```

<span data-ttu-id="1e0f7-109">Эта команда получает определение политики конечной точки службы ServiceEndpointPolicyDefinition1 в ServiceEndpointPolicy $Policy сохраняет его в переменной $policydef службы.</span><span class="sxs-lookup"><span data-stu-id="1e0f7-109">This command gets the service endpoint policy definition named ServiceEndpointPolicyDefinition1 in ServiceEndpointPolicy $Policy stores it in the $policydef variable.</span></span>

## <span data-ttu-id="1e0f7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e0f7-110">PARAMETERS</span></span>

### <span data-ttu-id="1e0f7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e0f7-111">-DefaultProfile</span></span>
<span data-ttu-id="1e0f7-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1e0f7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e0f7-113">-Name</span><span class="sxs-lookup"><span data-stu-id="1e0f7-113">-Name</span></span>
<span data-ttu-id="1e0f7-114">Имя определения политики конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="1e0f7-114">The name of the service endpoint policy definition</span></span>

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

### <span data-ttu-id="1e0f7-115">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="1e0f7-115">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="1e0f7-116">Политика конечных точек службы</span><span class="sxs-lookup"><span data-stu-id="1e0f7-116">The Service endpoint policy</span></span>

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

### <span data-ttu-id="1e0f7-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e0f7-117">-Confirm</span></span>
<span data-ttu-id="1e0f7-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e0f7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e0f7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e0f7-119">-WhatIf</span></span>
<span data-ttu-id="1e0f7-120">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e0f7-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e0f7-121">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1e0f7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e0f7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e0f7-122">CommonParameters</span></span>
<span data-ttu-id="1e0f7-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e0f7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e0f7-124">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e0f7-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e0f7-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1e0f7-125">INPUTS</span></span>

### <span data-ttu-id="1e0f7-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="1e0f7-126">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="1e0f7-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1e0f7-127">OUTPUTS</span></span>

### <span data-ttu-id="1e0f7-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1e0f7-128">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="1e0f7-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1e0f7-129">NOTES</span></span>

## <span data-ttu-id="1e0f7-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1e0f7-130">RELATED LINKS</span></span>

[<span data-ttu-id="1e0f7-131">Add-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1e0f7-131">Add-AzServiceEndpointPolicyDefinition</span></span>](./Add-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="1e0f7-132">New-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1e0f7-132">New-AzServiceEndpointPolicyDefinition</span></span>](./New-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="1e0f7-133">Remove-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1e0f7-133">Remove-AzServiceEndpointPolicyDefinition</span></span>](./Remove-AzServiceEndpointPolicyDefinition.md)

[<span data-ttu-id="1e0f7-134">Set-AzServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1e0f7-134">Set-AzServiceEndpointPolicyDefinition</span></span>](./Set-AzServiceEndpointPolicyDefinition.md)
