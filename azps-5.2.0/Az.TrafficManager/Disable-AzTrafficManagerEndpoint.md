---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 037a670c0e96d1a9014cd19b32a7d2ba4da282ba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397012"
---
# <span data-ttu-id="eff5b-101">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="eff5b-101">Disable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="eff5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eff5b-102">SYNOPSIS</span></span>
<span data-ttu-id="eff5b-103">Отключает конечную точку в профиле Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="eff5b-103">Disables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="eff5b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="eff5b-104">SYNTAX</span></span>

### <span data-ttu-id="eff5b-105">Поля</span><span class="sxs-lookup"><span data-stu-id="eff5b-105">Fields</span></span>
```
Disable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eff5b-106">Объект</span><span class="sxs-lookup"><span data-stu-id="eff5b-106">Object</span></span>
```
Disable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eff5b-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eff5b-107">DESCRIPTION</span></span>
<span data-ttu-id="eff5b-108">**Cmdlet Disable-AzTrafficManagerEndpoint** отключает конечную точку в профиле Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="eff5b-108">The **Disable-AzTrafficManagerEndpoint** cmdlet disables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="eff5b-109">Вы можете использовать оператор конвейера, чтобы передать объект **TrafficManagerEndpoint** этому cmdlet, или передать объект **TrafficManagerEndpoint** с помощью параметра *TrafficManagerEndpoint.*</span><span class="sxs-lookup"><span data-stu-id="eff5b-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can pass a **TrafficManagerEndpoint** object using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="eff5b-110">Кроме того, можно указать имя и тип конечной точки с помощью параметров *"Имя"* и "Тип" вместе с параметрами *ProfileName* и  *ResourceGroupName.*</span><span class="sxs-lookup"><span data-stu-id="eff5b-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="eff5b-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="eff5b-111">EXAMPLES</span></span>

### <span data-ttu-id="eff5b-112">Пример 1. Отключение конечной точки по имени</span><span class="sxs-lookup"><span data-stu-id="eff5b-112">Example 1: Disable an endpoint by name</span></span>
```
PS C:\> Disable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="eff5b-113">Эта команда отключает внешнюю конечную точку contoso в профиле ContosoProfile в группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="eff5b-113">This command disables the external endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="eff5b-114">Команда запросит подтверждение.</span><span class="sxs-lookup"><span data-stu-id="eff5b-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="eff5b-115">Пример 2. Отключение конечной точки с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="eff5b-115">Example 2: Disable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerEndpoint -Force
```

<span data-ttu-id="eff5b-116">Эта команда получает внешнюю конечную точку Contoso из профиля ContosoProfile в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="eff5b-116">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="eff5b-117">Затем эта команда передает ее **командлету Disable-AzTrafficManagerEndpoint** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="eff5b-117">The command then passes that endpoint to the **Disable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="eff5b-118">Этот cmdlet отключает эту конечную точку.</span><span class="sxs-lookup"><span data-stu-id="eff5b-118">That cmdlet disables that endpoint.</span></span>
<span data-ttu-id="eff5b-119">Команда определяет параметр *Force.*</span><span class="sxs-lookup"><span data-stu-id="eff5b-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="eff5b-120">Поэтому запрос на подтверждение не будет.</span><span class="sxs-lookup"><span data-stu-id="eff5b-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="eff5b-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eff5b-121">PARAMETERS</span></span>

### <span data-ttu-id="eff5b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eff5b-122">-DefaultProfile</span></span>
<span data-ttu-id="eff5b-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eff5b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eff5b-124">-Force</span><span class="sxs-lookup"><span data-stu-id="eff5b-124">-Force</span></span>
<span data-ttu-id="eff5b-125">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="eff5b-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="eff5b-126">-Name</span><span class="sxs-lookup"><span data-stu-id="eff5b-126">-Name</span></span>
<span data-ttu-id="eff5b-127">Указывает имя конечной точки Диспетчера трафика, которую отключает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eff5b-127">Specifies the name of the Traffic Manager endpoint that this cmdlet disables.</span></span>

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

### <span data-ttu-id="eff5b-128">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="eff5b-128">-ProfileName</span></span>
<span data-ttu-id="eff5b-129">Указывает имя профиля Диспетчера трафика, для которого этот cmdlet отключает конечную точку.</span><span class="sxs-lookup"><span data-stu-id="eff5b-129">Specifies the name of a Traffic Manager profile in which this cmdlet disables an endpoint.</span></span>
<span data-ttu-id="eff5b-130">Чтобы получить профиль, воспользуйтесь Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="eff5b-130">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="eff5b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eff5b-131">-ResourceGroupName</span></span>
<span data-ttu-id="eff5b-132">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eff5b-132">Specifies the name of a resource group.</span></span>
<span data-ttu-id="eff5b-133">Этот cmdlet отключает конечную точку Диспетчера трафика в группе, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="eff5b-133">This cmdlet disables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="eff5b-134">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="eff5b-134">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="eff5b-135">Указывает конечную точку диспетчера трафика, которую этот cmdlet отключает.</span><span class="sxs-lookup"><span data-stu-id="eff5b-135">Specifies the Traffic Manager endpoint that this cmdlet disables.</span></span>
<span data-ttu-id="eff5b-136">Чтобы получить объект **TrafficManagerEndpoint,** воспользуйтесь Get-AzTrafficManagerEndpoint управления.</span><span class="sxs-lookup"><span data-stu-id="eff5b-136">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="eff5b-137">-Type</span><span class="sxs-lookup"><span data-stu-id="eff5b-137">-Type</span></span>
<span data-ttu-id="eff5b-138">Тип конечной точки, которую этот cmdlet добавляет в профиль Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="eff5b-138">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="eff5b-139">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="eff5b-139">Valid values are:</span></span> 

- <span data-ttu-id="eff5b-140">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="eff5b-140">AzureEndpoints</span></span>
- <span data-ttu-id="eff5b-141">Внешниеendpoints</span><span class="sxs-lookup"><span data-stu-id="eff5b-141">ExternalEndpoints</span></span>
- <span data-ttu-id="eff5b-142">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="eff5b-142">NestedEndpoints</span></span>

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

### <span data-ttu-id="eff5b-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="eff5b-143">-Confirm</span></span>
<span data-ttu-id="eff5b-144">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eff5b-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eff5b-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eff5b-145">-WhatIf</span></span>
<span data-ttu-id="eff5b-146">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eff5b-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eff5b-147">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="eff5b-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eff5b-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eff5b-148">CommonParameters</span></span>
<span data-ttu-id="eff5b-149">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eff5b-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eff5b-150">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eff5b-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eff5b-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eff5b-151">INPUTS</span></span>

### <span data-ttu-id="eff5b-152">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="eff5b-152">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="eff5b-153">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eff5b-153">OUTPUTS</span></span>

### <span data-ttu-id="eff5b-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="eff5b-154">System.Boolean</span></span>

## <span data-ttu-id="eff5b-155">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="eff5b-155">NOTES</span></span>

## <span data-ttu-id="eff5b-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eff5b-156">RELATED LINKS</span></span>

[<span data-ttu-id="eff5b-157">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="eff5b-157">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="eff5b-158">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="eff5b-158">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="eff5b-159">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="eff5b-159">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="eff5b-160">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="eff5b-160">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="eff5b-161">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="eff5b-161">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="eff5b-162">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="eff5b-162">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="eff5b-163">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="eff5b-163">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


