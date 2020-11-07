---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzServiceEndpointPolicy.md
ms.openlocfilehash: 9b03a33ebea52e57950e46c894e95ffefe520b4e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93902082"
---
# <span data-ttu-id="63ebc-101">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="63ebc-101">New-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="63ebc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="63ebc-102">SYNOPSIS</span></span>
<span data-ttu-id="63ebc-103">Создание политики конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="63ebc-103">Creates a service endpoint policy.</span></span>

## <span data-ttu-id="63ebc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="63ebc-104">SYNTAX</span></span>

```
New-AzServiceEndpointPolicy -Name <String>
 [-ServiceEndpointPolicyDefinition <PSServiceEndpointPolicyDefinition[]>] -ResourceGroupName <String>
 -Location <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="63ebc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63ebc-105">DESCRIPTION</span></span>
<span data-ttu-id="63ebc-106">Командлет **New-AzServiceEndpointPolicy** создает политику конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="63ebc-106">The **New-AzServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="63ebc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="63ebc-107">EXAMPLES</span></span>

### <span data-ttu-id="63ebc-108">Пример 1: Создание политики конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="63ebc-108">Example 1: Creates a service endpoint policy</span></span>
```
$serviceEndpointPolicy = New-AzServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicyDefinition $serviceEndpointDefinition -Location "location";
```

<span data-ttu-id="63ebc-109">Эта команда создает политику конечной точки службы с именем Policy1 с определениями, определенными объектом, $serviceEndpointDefinition и сохраняет их в переменной $serviceEndpointPolicy.</span><span class="sxs-lookup"><span data-stu-id="63ebc-109">This command creates a service endpoint policy named Policy1 with definitions defined by the object $serviceEndpointDefinition and stores it in the $serviceEndpointPolicy variable.</span></span>

## <span data-ttu-id="63ebc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="63ebc-110">PARAMETERS</span></span>

### <span data-ttu-id="63ebc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63ebc-111">-DefaultProfile</span></span>
<span data-ttu-id="63ebc-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63ebc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63ebc-113">-Force</span><span class="sxs-lookup"><span data-stu-id="63ebc-113">-Force</span></span>
<span data-ttu-id="63ebc-114">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="63ebc-114">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="63ebc-115">-Location</span><span class="sxs-lookup"><span data-stu-id="63ebc-115">-Location</span></span>
<span data-ttu-id="63ebc-116">поиска.</span><span class="sxs-lookup"><span data-stu-id="63ebc-116">location.</span></span>

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

### <span data-ttu-id="63ebc-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="63ebc-117">-Name</span></span>
<span data-ttu-id="63ebc-118">Имя подсети.</span><span class="sxs-lookup"><span data-stu-id="63ebc-118">The name of the subnet</span></span>

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

### <span data-ttu-id="63ebc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63ebc-119">-ResourceGroupName</span></span>
<span data-ttu-id="63ebc-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63ebc-120">The resource group name.</span></span>

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

### <span data-ttu-id="63ebc-121">-ServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="63ebc-121">-ServiceEndpointPolicyDefinition</span></span>
<span data-ttu-id="63ebc-122">Список определений конечной точки службы</span><span class="sxs-lookup"><span data-stu-id="63ebc-122">List of service endpoint definitions</span></span>

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

### <span data-ttu-id="63ebc-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63ebc-123">-Confirm</span></span>
<span data-ttu-id="63ebc-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="63ebc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63ebc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63ebc-125">-WhatIf</span></span>
<span data-ttu-id="63ebc-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="63ebc-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63ebc-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="63ebc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63ebc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63ebc-128">CommonParameters</span></span>
<span data-ttu-id="63ebc-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="63ebc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63ebc-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63ebc-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63ebc-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="63ebc-131">INPUTS</span></span>

### <span data-ttu-id="63ebc-132">System. String</span><span class="sxs-lookup"><span data-stu-id="63ebc-132">System.String</span></span>

## <span data-ttu-id="63ebc-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="63ebc-133">OUTPUTS</span></span>

### <span data-ttu-id="63ebc-134">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="63ebc-134">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="63ebc-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="63ebc-135">NOTES</span></span>

## <span data-ttu-id="63ebc-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63ebc-136">RELATED LINKS</span></span>

[<span data-ttu-id="63ebc-137">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="63ebc-137">Get-AzServiceEndpointPolicy</span></span>](./Get-AzServiceEndpointPolicy.md)

[<span data-ttu-id="63ebc-138">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="63ebc-138">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="63ebc-139">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="63ebc-139">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
