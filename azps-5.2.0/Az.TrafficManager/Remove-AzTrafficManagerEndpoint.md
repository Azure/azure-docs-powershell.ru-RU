---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2129C457-592B-484C-A148-828BFD5895D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 6f2884a6d4cefaf52b06ec653db85c9e9ae59f54
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391388"
---
# <span data-ttu-id="f8fee-101">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f8fee-101">Remove-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="f8fee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8fee-102">SYNOPSIS</span></span>
<span data-ttu-id="f8fee-103">Удаляет конечную точку из Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="f8fee-103">Removes an endpoint from Traffic Manager.</span></span>

## <span data-ttu-id="f8fee-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f8fee-104">SYNTAX</span></span>

### <span data-ttu-id="f8fee-105">Поля</span><span class="sxs-lookup"><span data-stu-id="f8fee-105">Fields</span></span>
```
Remove-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8fee-106">Объект</span><span class="sxs-lookup"><span data-stu-id="f8fee-106">Object</span></span>
```
Remove-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8fee-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8fee-107">DESCRIPTION</span></span>
<span data-ttu-id="f8fee-108">Для **удаления конечной** точки из Диспетчера трафика Azure удаляется конечная точка.</span><span class="sxs-lookup"><span data-stu-id="f8fee-108">The **Remove-AzTrafficManagerEndpoint** cmdlet removes an endpoint from Azure Traffic Manager.</span></span>

<span data-ttu-id="f8fee-109">Этот cmdlet зафиксировать каждое изменение в службе Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="f8fee-109">This cmdlet commits each change to the Traffic Manager service.</span></span>
<span data-ttu-id="f8fee-110">Чтобы удалить несколько конечных точек из локального объекта профиля Диспетчера трафика и зафиксировать изменения за одну операцию, воспользуйтесь Remove-AzTrafficManagerEndpointConfig управления.</span><span class="sxs-lookup"><span data-stu-id="f8fee-110">To remove multiple endpoints from a local Traffic Manager profile object and commit changes in a single operation, use the Remove-AzTrafficManagerEndpointConfig cmdlet.</span></span>

<span data-ttu-id="f8fee-111">Для этого cmdlet можно использовать оператор конвейера, чтобы передать объект **TrafficManagerEndpoint,** или указать объект **TrafficManagerEndpoint** с помощью параметра *TrafficManagerEndpoint.*</span><span class="sxs-lookup"><span data-stu-id="f8fee-111">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="f8fee-112">Кроме того, можно указать имя и тип конечной точки с помощью параметров *"Имя"* и "Тип" вместе с параметрами *ProfileName* и  *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="f8fee-112">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="f8fee-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f8fee-113">EXAMPLES</span></span>

### <span data-ttu-id="f8fee-114">Пример 1. Удаление конечной точки из профиля</span><span class="sxs-lookup"><span data-stu-id="f8fee-114">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>Remove-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="f8fee-115">Эта команда удаляет конечную точку Azure contoso из профиля ContosoProfile в группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f8fee-115">This command removes the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="f8fee-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8fee-116">PARAMETERS</span></span>

### <span data-ttu-id="f8fee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8fee-117">-DefaultProfile</span></span>
<span data-ttu-id="f8fee-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f8fee-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8fee-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f8fee-119">-Force</span></span>
<span data-ttu-id="f8fee-120">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="f8fee-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f8fee-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f8fee-121">-Name</span></span>
<span data-ttu-id="f8fee-122">Указывает имя конечной точки Диспетчера трафика, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8fee-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8fee-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="f8fee-123">-ProfileName</span></span>
<span data-ttu-id="f8fee-124">Указывает имя профиля Диспетчера трафика, из которого этот cmdlet удаляет конечную точку.</span><span class="sxs-lookup"><span data-stu-id="f8fee-124">Specifies the name of a Traffic Manager profile from which this cmdlet removes an endpoint.</span></span>
<span data-ttu-id="f8fee-125">Чтобы получить профиль, воспользуйтесь Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f8fee-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8fee-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8fee-126">-ResourceGroupName</span></span>
<span data-ttu-id="f8fee-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f8fee-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="f8fee-128">Этот cmdlet удаляет конечную точку Диспетчера трафика из профиля Диспетчера трафика в группе, заданной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="f8fee-128">This cmdlet removes a Traffic Manager endpoint from a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8fee-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f8fee-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="f8fee-130">Указывает конечную точку диспетчера трафика, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8fee-130">Specifies the Traffic Manager endpoint that this cmdlet removes.</span></span>
<span data-ttu-id="f8fee-131">Чтобы получить объект **TrafficManagerEndpoint,** воспользуйтесь Get-AzTrafficManagerEndpoint управления.</span><span class="sxs-lookup"><span data-stu-id="f8fee-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8fee-132">-Type</span><span class="sxs-lookup"><span data-stu-id="f8fee-132">-Type</span></span>
<span data-ttu-id="f8fee-133">Определяет тип конечной точки, которую этот cmdlet добавляет в профиль Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="f8fee-133">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="f8fee-134">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="f8fee-134">Valid values are:</span></span> 

- <span data-ttu-id="f8fee-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="f8fee-135">AzureEndpoints</span></span>
- <span data-ttu-id="f8fee-136">Внешниеendpoints</span><span class="sxs-lookup"><span data-stu-id="f8fee-136">ExternalEndpoints</span></span>
- <span data-ttu-id="f8fee-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="f8fee-137">NestedEndpoints</span></span>

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8fee-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8fee-138">-Confirm</span></span>
<span data-ttu-id="f8fee-139">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f8fee-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8fee-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8fee-140">-WhatIf</span></span>
<span data-ttu-id="f8fee-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8fee-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8fee-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f8fee-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8fee-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8fee-143">CommonParameters</span></span>
<span data-ttu-id="f8fee-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8fee-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8fee-145">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8fee-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8fee-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f8fee-146">INPUTS</span></span>

### <span data-ttu-id="f8fee-147">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f8fee-147">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="f8fee-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f8fee-148">OUTPUTS</span></span>

### <span data-ttu-id="f8fee-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f8fee-149">System.Boolean</span></span>

## <span data-ttu-id="f8fee-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f8fee-150">NOTES</span></span>

## <span data-ttu-id="f8fee-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8fee-151">RELATED LINKS</span></span>

[<span data-ttu-id="f8fee-152">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f8fee-152">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="f8fee-153">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f8fee-153">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="f8fee-154">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f8fee-154">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="f8fee-155">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="f8fee-155">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="f8fee-156">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f8fee-156">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


