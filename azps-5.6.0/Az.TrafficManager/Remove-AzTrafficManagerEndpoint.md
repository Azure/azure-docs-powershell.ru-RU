---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2129C457-592B-484C-A148-828BFD5895D4
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 1864cc9d5975c9f959edb6be470e63a10cfa63f2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987283"
---
# <span data-ttu-id="19445-101">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="19445-101">Remove-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="19445-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19445-102">SYNOPSIS</span></span>
<span data-ttu-id="19445-103">Удаляет конечную точку из Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="19445-103">Removes an endpoint from Traffic Manager.</span></span>

## <span data-ttu-id="19445-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="19445-104">SYNTAX</span></span>

### <span data-ttu-id="19445-105">Поля</span><span class="sxs-lookup"><span data-stu-id="19445-105">Fields</span></span>
```
Remove-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19445-106">Объект</span><span class="sxs-lookup"><span data-stu-id="19445-106">Object</span></span>
```
Remove-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19445-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="19445-107">DESCRIPTION</span></span>
<span data-ttu-id="19445-108">Для **удаления конечной** точки из Диспетчера трафика Azure удаляется конечная точка.</span><span class="sxs-lookup"><span data-stu-id="19445-108">The **Remove-AzTrafficManagerEndpoint** cmdlet removes an endpoint from Azure Traffic Manager.</span></span>

<span data-ttu-id="19445-109">Этот cmdlet зафиксировать каждое изменение в службе Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="19445-109">This cmdlet commits each change to the Traffic Manager service.</span></span>
<span data-ttu-id="19445-110">Чтобы удалить несколько конечных точек из локального объекта профиля Диспетчера трафика и зафиксировать изменения за одну операцию, используйте Remove-AzTrafficManagerEndpointConfig управления.</span><span class="sxs-lookup"><span data-stu-id="19445-110">To remove multiple endpoints from a local Traffic Manager profile object and commit changes in a single operation, use the Remove-AzTrafficManagerEndpointConfig cmdlet.</span></span>

<span data-ttu-id="19445-111">С помощью оператора конвейера можно передать объект **TrafficManagerEndpoint** этому cmdlet или указать объект **TrafficManagerEndpoint** с помощью параметра *TrafficManagerEndpoint.*</span><span class="sxs-lookup"><span data-stu-id="19445-111">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="19445-112">Кроме того, можно указать имя и тип конечной точки с помощью параметров *"Имя"* и "Тип" вместе с параметрами *ProfileName* и  *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="19445-112">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="19445-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="19445-113">EXAMPLES</span></span>

### <span data-ttu-id="19445-114">Пример 1. Удаление конечной точки из профиля</span><span class="sxs-lookup"><span data-stu-id="19445-114">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>Remove-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="19445-115">Эта команда удаляет конечную точку Azure contoso из профиля ContosoProfile в группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="19445-115">This command removes the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="19445-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19445-116">PARAMETERS</span></span>

### <span data-ttu-id="19445-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19445-117">-DefaultProfile</span></span>
<span data-ttu-id="19445-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="19445-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19445-119">-Force</span><span class="sxs-lookup"><span data-stu-id="19445-119">-Force</span></span>
<span data-ttu-id="19445-120">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="19445-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="19445-121">-Name</span><span class="sxs-lookup"><span data-stu-id="19445-121">-Name</span></span>
<span data-ttu-id="19445-122">Указывает имя конечной точки Диспетчера трафика, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19445-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="19445-123">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="19445-123">-ProfileName</span></span>
<span data-ttu-id="19445-124">Указывает имя профиля Диспетчера трафика, из которого этот cmdlet удаляет конечную точку.</span><span class="sxs-lookup"><span data-stu-id="19445-124">Specifies the name of a Traffic Manager profile from which this cmdlet removes an endpoint.</span></span>
<span data-ttu-id="19445-125">Чтобы получить профиль, воспользуйтесь Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="19445-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="19445-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19445-126">-ResourceGroupName</span></span>
<span data-ttu-id="19445-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="19445-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="19445-128">Этот cmdlet удаляет конечную точку Диспетчера трафика из профиля Диспетчера трафика в группе, заданной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="19445-128">This cmdlet removes a Traffic Manager endpoint from a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="19445-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="19445-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="19445-130">Указывает конечную точку диспетчера трафика, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19445-130">Specifies the Traffic Manager endpoint that this cmdlet removes.</span></span>
<span data-ttu-id="19445-131">Чтобы получить объект **TrafficManagerEndpoint,** воспользуйтесь Get-AzTrafficManagerEndpoint управления.</span><span class="sxs-lookup"><span data-stu-id="19445-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="19445-132">-Type</span><span class="sxs-lookup"><span data-stu-id="19445-132">-Type</span></span>
<span data-ttu-id="19445-133">Определяет тип конечной точки, которую этот cmdlet добавляет в профиль Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="19445-133">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="19445-134">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="19445-134">Valid values are:</span></span> 

- <span data-ttu-id="19445-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="19445-135">AzureEndpoints</span></span>
- <span data-ttu-id="19445-136">Внешниеendpoints</span><span class="sxs-lookup"><span data-stu-id="19445-136">ExternalEndpoints</span></span>
- <span data-ttu-id="19445-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="19445-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="19445-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19445-138">-Confirm</span></span>
<span data-ttu-id="19445-139">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19445-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19445-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19445-140">-WhatIf</span></span>
<span data-ttu-id="19445-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19445-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19445-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="19445-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19445-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19445-143">CommonParameters</span></span>
<span data-ttu-id="19445-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19445-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19445-145">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19445-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19445-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19445-146">INPUTS</span></span>

### <span data-ttu-id="19445-147">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="19445-147">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="19445-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="19445-148">OUTPUTS</span></span>

### <span data-ttu-id="19445-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="19445-149">System.Boolean</span></span>

## <span data-ttu-id="19445-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="19445-150">NOTES</span></span>

## <span data-ttu-id="19445-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="19445-151">RELATED LINKS</span></span>

[<span data-ttu-id="19445-152">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="19445-152">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="19445-153">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="19445-153">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="19445-154">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="19445-154">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="19445-155">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="19445-155">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="19445-156">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="19445-156">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


