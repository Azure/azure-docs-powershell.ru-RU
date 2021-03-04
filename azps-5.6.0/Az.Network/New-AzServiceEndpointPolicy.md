---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
ms.openlocfilehash: b5f555a0df848c86dbbc0a04297d45b4132e6972
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953795"
---
# <span data-ttu-id="ff2f5-101">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ff2f5-101">New-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="ff2f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff2f5-102">SYNOPSIS</span></span>
<span data-ttu-id="ff2f5-103">Создает политику конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="ff2f5-103">Creates a service endpoint policy.</span></span>

## <span data-ttu-id="ff2f5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ff2f5-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicy -Name <String>
 [-ServiceEndpointPolicyDefinition <PSServiceEndpointPolicyDefinition[]>] -ResourceGroupName <String>
 -Location <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ff2f5-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff2f5-105">DESCRIPTION</span></span>
<span data-ttu-id="ff2f5-106">Для создания политики конечных точек службы будет создаваться cmdlet **New-AzServiceEndpointPolicy.**</span><span class="sxs-lookup"><span data-stu-id="ff2f5-106">The **New-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="ff2f5-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ff2f5-107">EXAMPLES</span></span>

### <span data-ttu-id="ff2f5-108">Пример 1. Создание политики конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="ff2f5-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="ff2f5-109">Эта команда создает политику конечной точки службы с именем "Политика1" с определениями, определенными объектом $serviceEndpointDefinition, и хранит ее в переменной $serviceEndpointPolicy службы.</span><span class="sxs-lookup"><span data-stu-id="ff2f5-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="ff2f5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff2f5-110">PARAMETERS</span></span>

### <span data-ttu-id="ff2f5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff2f5-111">-DefaultProfile</span></span>
<span data-ttu-id="ff2f5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ff2f5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff2f5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ff2f5-113">-Force</span></span>
<span data-ttu-id="ff2f5-114">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="ff2f5-114">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff2f5-115">-Location</span><span class="sxs-lookup"><span data-stu-id="ff2f5-115">-Location</span></span>
<span data-ttu-id="ff2f5-116">расположение.</span><span class="sxs-lookup"><span data-stu-id="ff2f5-116">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff2f5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="ff2f5-117">-Name</span></span>
<span data-ttu-id="ff2f5-118">Имя подсети</span><span class="sxs-lookup"><span data-stu-id="ff2f5-118">The name of the subnet</span></span>

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

### <span data-ttu-id="ff2f5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff2f5-119">-ResourceGroupName</span></span>
<span data-ttu-id="ff2f5-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ff2f5-120">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff2f5-121">-ServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="ff2f5-121">-ServiceEndpointPolicyDefinition</span></span>
<span data-ttu-id="ff2f5-122">Список определений конечных точек службы</span><span class="sxs-lookup"><span data-stu-id="ff2f5-122">List of service endpoint definitions</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicyDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff2f5-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff2f5-123">-Confirm</span></span>
<span data-ttu-id="ff2f5-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff2f5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff2f5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff2f5-125">-WhatIf</span></span>
<span data-ttu-id="ff2f5-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff2f5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff2f5-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ff2f5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff2f5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff2f5-128">CommonParameters</span></span>
<span data-ttu-id="ff2f5-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff2f5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff2f5-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff2f5-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff2f5-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ff2f5-131">INPUTS</span></span>

### <span data-ttu-id="ff2f5-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ff2f5-132">System.String</span></span>

## <span data-ttu-id="ff2f5-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ff2f5-133">OUTPUTS</span></span>

### <span data-ttu-id="ff2f5-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ff2f5-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="ff2f5-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ff2f5-135">NOTES</span></span>

## <span data-ttu-id="ff2f5-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff2f5-136">RELATED LINKS</span></span>

[<span data-ttu-id="ff2f5-137">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ff2f5-137">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="ff2f5-138">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ff2f5-138">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="ff2f5-139">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="ff2f5-139">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
