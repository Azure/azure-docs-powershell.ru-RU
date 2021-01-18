---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzServiceEndpointPolicy.md
ms.openlocfilehash: a74edbec0051e3a77ab3ac10595f787dd45a2dfc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518826"
---
# <span data-ttu-id="19b34-101">Get-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="19b34-101">Get-AzServiceEndpointPolicy</span></span>

## <span data-ttu-id="19b34-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19b34-102">SYNOPSIS</span></span>
<span data-ttu-id="19b34-103">Возвращает политику конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="19b34-103">Gets a service endpoint policy.</span></span>

## <span data-ttu-id="19b34-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="19b34-104">SYNTAX</span></span>

### <span data-ttu-id="19b34-105">ListParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="19b34-105">ListParameterSet (Default)</span></span>
```
Get-AzServiceEndpointPolicy [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19b34-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="19b34-106">GetByResourceIdParameterSet</span></span>
```
Get-AzServiceEndpointPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19b34-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19b34-107">DESCRIPTION</span></span>
<span data-ttu-id="19b34-108">Для получения политики конечной точки обслуживания возвращается поле **Get-AzServiceEndpointPolicy.**</span><span class="sxs-lookup"><span data-stu-id="19b34-108">The **Get-AzServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="19b34-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="19b34-109">EXAMPLES</span></span>

### <span data-ttu-id="19b34-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="19b34-110">Example 1</span></span>
```
$policy = Get-AzServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="19b34-111">Эта команда получает политику конечной точки службы ServiceEndpointPolicy1, которая принадлежит к группе ресурсов ResourceGroup01, и сохраняет ее в переменной $policy ресурса.</span><span class="sxs-lookup"><span data-stu-id="19b34-111">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="19b34-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="19b34-112">Example 2</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="19b34-113">Эта команда получает список всех политик конечной точки службы в группе ресурсов ResourceGroup01 и сохраняет ее в переменной $policyList ресурса.</span><span class="sxs-lookup"><span data-stu-id="19b34-113">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

### <span data-ttu-id="19b34-114">Пример 3</span><span class="sxs-lookup"><span data-stu-id="19b34-114">Example 3</span></span>
```
$policyList = Get-AzServiceEndpointPolicy -ResourceGroupName "ServiceEndpointPolicy*"
```

<span data-ttu-id="19b34-115">Эта команда возвращает список всех политик конечной точки службы, которые начинаются с "ServiceEndpointPolicy".</span><span class="sxs-lookup"><span data-stu-id="19b34-115">This command gets a list of all the service endpoint policies that start with "ServiceEndpointPolicy".</span></span>

## <span data-ttu-id="19b34-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19b34-116">PARAMETERS</span></span>

### <span data-ttu-id="19b34-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19b34-117">-DefaultProfile</span></span>
<span data-ttu-id="19b34-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="19b34-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19b34-119">-Name</span><span class="sxs-lookup"><span data-stu-id="19b34-119">-Name</span></span>
<span data-ttu-id="19b34-120">Имя политики конечных точек службы</span><span class="sxs-lookup"><span data-stu-id="19b34-120">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="19b34-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19b34-121">-ResourceGroupName</span></span>
<span data-ttu-id="19b34-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="19b34-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="19b34-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19b34-123">-ResourceId</span></span>
<span data-ttu-id="19b34-124">ИД политики конечных точек службы.</span><span class="sxs-lookup"><span data-stu-id="19b34-124">The ID of the service endpoint policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19b34-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19b34-125">-Confirm</span></span>
<span data-ttu-id="19b34-126">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19b34-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19b34-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19b34-127">-WhatIf</span></span>
<span data-ttu-id="19b34-128">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19b34-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19b34-129">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="19b34-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19b34-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19b34-130">CommonParameters</span></span>
<span data-ttu-id="19b34-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19b34-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19b34-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19b34-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19b34-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19b34-133">INPUTS</span></span>

### <span data-ttu-id="19b34-134">System.String</span><span class="sxs-lookup"><span data-stu-id="19b34-134">System.String</span></span>

## <span data-ttu-id="19b34-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="19b34-135">OUTPUTS</span></span>

### <span data-ttu-id="19b34-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="19b34-136">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>

## <span data-ttu-id="19b34-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="19b34-137">NOTES</span></span>

## <span data-ttu-id="19b34-138">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19b34-138">RELATED LINKS</span></span>

[<span data-ttu-id="19b34-139">New-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="19b34-139">New-AzServiceEndpointPolicy</span></span>](./New-AzServiceEndpointPolicy.md)

[<span data-ttu-id="19b34-140">Remove-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="19b34-140">Remove-AzServiceEndpointPolicy</span></span>](./Remove-AzServiceEndpointPolicy.md)

[<span data-ttu-id="19b34-141">Set-AzServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="19b34-141">Set-AzServiceEndpointPolicy</span></span>](./Set-AzServiceEndpointPolicy.md)
