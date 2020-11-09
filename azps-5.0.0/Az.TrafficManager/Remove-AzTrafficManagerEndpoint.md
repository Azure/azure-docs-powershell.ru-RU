---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2129C457-592B-484C-A148-828BFD5895D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 6f2884a6d4cefaf52b06ec653db85c9e9ae59f54
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248449"
---
# <span data-ttu-id="cc4fc-101">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="cc4fc-101">Remove-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="cc4fc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cc4fc-102">SYNOPSIS</span></span>
<span data-ttu-id="cc4fc-103">Удаляет конечную точку из диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="cc4fc-103">Removes an endpoint from Traffic Manager.</span></span>

## <span data-ttu-id="cc4fc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cc4fc-104">SYNTAX</span></span>

### <span data-ttu-id="cc4fc-105">»</span><span class="sxs-lookup"><span data-stu-id="cc4fc-105">Fields</span></span>
```
Remove-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc4fc-106">DataObject</span><span class="sxs-lookup"><span data-stu-id="cc4fc-106">Object</span></span>
```
Remove-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc4fc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc4fc-107">DESCRIPTION</span></span>
<span data-ttu-id="cc4fc-108">Командлет **Remove-AzTrafficManagerEndpoint** удаляет конечную точку из диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="cc4fc-108">The **Remove-AzTrafficManagerEndpoint** cmdlet removes an endpoint from Azure Traffic Manager.</span></span>

<span data-ttu-id="cc4fc-109">Этот командлет фиксирует каждое изменение в службе диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="cc4fc-109">This cmdlet commits each change to the Traffic Manager service.</span></span>
<span data-ttu-id="cc4fc-110">Для удаления нескольких конечных точек из объекта профиля диспетчера локальных данных и фиксации изменений в одной операции используйте командлет Remove-AzTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="cc4fc-110">To remove multiple endpoints from a local Traffic Manager profile object and commit changes in a single operation, use the Remove-AzTrafficManagerEndpointConfig cmdlet.</span></span>

<span data-ttu-id="cc4fc-111">Вы можете использовать оператор Pipeline для передачи объекта **TrafficManagerEndpoint** в этот командлет или задать объект **TrafficManagerEndpoint** с помощью параметра *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="cc4fc-111">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="cc4fc-112">Кроме того, вы можете указать имя и тип конечной точки, используя параметры *Name* и *Type* вместе с параметрами *filename* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="cc4fc-112">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="cc4fc-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cc4fc-113">EXAMPLES</span></span>

### <span data-ttu-id="cc4fc-114">Пример 1: Удаление конечной точки из профиля</span><span class="sxs-lookup"><span data-stu-id="cc4fc-114">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>Remove-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="cc4fc-115">Эта команда удаляет конечную точку Azure с именем Contoso из профиля с именем ContosoProfile в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="cc4fc-115">This command removes the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="cc4fc-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cc4fc-116">PARAMETERS</span></span>

### <span data-ttu-id="cc4fc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc4fc-117">-DefaultProfile</span></span>
<span data-ttu-id="cc4fc-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cc4fc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cc4fc-119">-Force</span><span class="sxs-lookup"><span data-stu-id="cc4fc-119">-Force</span></span>
<span data-ttu-id="cc4fc-120">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="cc4fc-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cc4fc-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cc4fc-121">-Name</span></span>
<span data-ttu-id="cc4fc-122">Указывает имя конечной точки диспетчера трафика, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="cc4fc-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

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

### <span data-ttu-id="cc4fc-123">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="cc4fc-123">-ProfileName</span></span>
<span data-ttu-id="cc4fc-124">Указывает имя профиля диспетчера трафика, из которого этот командлет удаляет конечную точку.</span><span class="sxs-lookup"><span data-stu-id="cc4fc-124">Specifies the name of a Traffic Manager profile from which this cmdlet removes an endpoint.</span></span>
<span data-ttu-id="cc4fc-125">Чтобы получить профиль, используйте командлет Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="cc4fc-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="cc4fc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc4fc-126">-ResourceGroupName</span></span>
<span data-ttu-id="cc4fc-127">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cc4fc-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="cc4fc-128">Этот командлет удаляет конечную точку диспетчера трафика из профиля диспетчера трафика в группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="cc4fc-128">This cmdlet removes a Traffic Manager endpoint from a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="cc4fc-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="cc4fc-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="cc4fc-130">Указывает конечную точку диспетчера трафика, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="cc4fc-130">Specifies the Traffic Manager endpoint that this cmdlet removes.</span></span>
<span data-ttu-id="cc4fc-131">Чтобы получить объект **TrafficManagerEndpoint** , используйте командлет Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="cc4fc-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="cc4fc-132">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="cc4fc-132">-Type</span></span>
<span data-ttu-id="cc4fc-133">Указывает тип конечной точки, которую добавляет этот командлет к профилю диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="cc4fc-133">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="cc4fc-134">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="cc4fc-134">Valid values are:</span></span> 

- <span data-ttu-id="cc4fc-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="cc4fc-135">AzureEndpoints</span></span>
- <span data-ttu-id="cc4fc-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="cc4fc-136">ExternalEndpoints</span></span>
- <span data-ttu-id="cc4fc-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="cc4fc-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="cc4fc-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc4fc-138">-Confirm</span></span>
<span data-ttu-id="cc4fc-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cc4fc-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc4fc-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc4fc-140">-WhatIf</span></span>
<span data-ttu-id="cc4fc-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cc4fc-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc4fc-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cc4fc-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc4fc-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc4fc-143">CommonParameters</span></span>
<span data-ttu-id="cc4fc-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cc4fc-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc4fc-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc4fc-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc4fc-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cc4fc-146">INPUTS</span></span>

### <span data-ttu-id="cc4fc-147">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="cc4fc-147">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="cc4fc-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc4fc-148">OUTPUTS</span></span>

### <span data-ttu-id="cc4fc-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cc4fc-149">System.Boolean</span></span>

## <span data-ttu-id="cc4fc-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="cc4fc-150">NOTES</span></span>

## <span data-ttu-id="cc4fc-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cc4fc-151">RELATED LINKS</span></span>

[<span data-ttu-id="cc4fc-152">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="cc4fc-152">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="cc4fc-153">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cc4fc-153">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="cc4fc-154">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="cc4fc-154">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="cc4fc-155">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="cc4fc-155">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="cc4fc-156">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="cc4fc-156">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

