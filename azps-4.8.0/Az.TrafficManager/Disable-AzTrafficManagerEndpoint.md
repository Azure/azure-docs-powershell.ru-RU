---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/disable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Disable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 037a670c0e96d1a9014cd19b32a7d2ba4da282ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079332"
---
# <span data-ttu-id="94d58-101">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="94d58-101">Disable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="94d58-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="94d58-102">SYNOPSIS</span></span>
<span data-ttu-id="94d58-103">Отключает конечную точку в профиле диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="94d58-103">Disables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="94d58-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="94d58-104">SYNTAX</span></span>

### <span data-ttu-id="94d58-105">»</span><span class="sxs-lookup"><span data-stu-id="94d58-105">Fields</span></span>
```
Disable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="94d58-106">DataObject</span><span class="sxs-lookup"><span data-stu-id="94d58-106">Object</span></span>
```
Disable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94d58-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94d58-107">DESCRIPTION</span></span>
<span data-ttu-id="94d58-108">Командлет **Disable-AzTrafficManagerEndpoint** отключает конечную точку в профиле диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="94d58-108">The **Disable-AzTrafficManagerEndpoint** cmdlet disables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="94d58-109">Вы можете использовать оператор Pipeline для передачи объекта **TrafficManagerEndpoint** в этот командлет или передать объект **TrafficManagerEndpoint** с помощью параметра *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="94d58-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can pass a **TrafficManagerEndpoint** object using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="94d58-110">Кроме того, вы можете указать имя и тип конечной точки, используя параметры *Name* и *Type* вместе с параметрами *filename* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="94d58-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="94d58-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="94d58-111">EXAMPLES</span></span>

### <span data-ttu-id="94d58-112">Пример 1: отключение конечной точки по имени</span><span class="sxs-lookup"><span data-stu-id="94d58-112">Example 1: Disable an endpoint by name</span></span>
```
PS C:\> Disable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="94d58-113">Эта команда отключает внешнюю конечную точку с именем Contoso в профиле с именем ContosoProfile в группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="94d58-113">This command disables the external endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="94d58-114">В командной строке появится запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="94d58-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="94d58-115">Пример 2: отключение конечной точки с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="94d58-115">Example 2: Disable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzTrafficManagerEndpoint -Force
```

<span data-ttu-id="94d58-116">Эта команда получает внешнюю конечную точку с именем Contoso из профиля с именем ContosoProfile в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="94d58-116">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="94d58-117">Затем команда передает эту конечную точку командлету **Disable-AzTrafficManagerEndpoint** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="94d58-117">The command then passes that endpoint to the **Disable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="94d58-118">Этот командлет отключает эту конечную точку.</span><span class="sxs-lookup"><span data-stu-id="94d58-118">That cmdlet disables that endpoint.</span></span>
<span data-ttu-id="94d58-119">Команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="94d58-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="94d58-120">Поэтому он не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="94d58-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="94d58-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="94d58-121">PARAMETERS</span></span>

### <span data-ttu-id="94d58-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94d58-122">-DefaultProfile</span></span>
<span data-ttu-id="94d58-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="94d58-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94d58-124">-Force</span><span class="sxs-lookup"><span data-stu-id="94d58-124">-Force</span></span>
<span data-ttu-id="94d58-125">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="94d58-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="94d58-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="94d58-126">-Name</span></span>
<span data-ttu-id="94d58-127">Указывает имя конечной точки диспетчера трафика, которую отключает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="94d58-127">Specifies the name of the Traffic Manager endpoint that this cmdlet disables.</span></span>

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

### <span data-ttu-id="94d58-128">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="94d58-128">-ProfileName</span></span>
<span data-ttu-id="94d58-129">Указывает имя профиля диспетчера трафика, в котором этот командлет отключает конечную точку.</span><span class="sxs-lookup"><span data-stu-id="94d58-129">Specifies the name of a Traffic Manager profile in which this cmdlet disables an endpoint.</span></span>
<span data-ttu-id="94d58-130">Чтобы получить профиль, используйте командлет Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="94d58-130">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="94d58-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94d58-131">-ResourceGroupName</span></span>
<span data-ttu-id="94d58-132">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94d58-132">Specifies the name of a resource group.</span></span>
<span data-ttu-id="94d58-133">Этот командлет отключает в группе, в которой указан этот параметр, конечную точку диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="94d58-133">This cmdlet disables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="94d58-134">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="94d58-134">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="94d58-135">Указывает конечную точку диспетчера трафика, которую отключает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="94d58-135">Specifies the Traffic Manager endpoint that this cmdlet disables.</span></span>
<span data-ttu-id="94d58-136">Чтобы получить объект **TrafficManagerEndpoint** , используйте командлет Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="94d58-136">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="94d58-137">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="94d58-137">-Type</span></span>
<span data-ttu-id="94d58-138">Указывает тип конечной точки, которую добавляет этот командлет к профилю диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="94d58-138">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="94d58-139">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="94d58-139">Valid values are:</span></span> 

- <span data-ttu-id="94d58-140">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="94d58-140">AzureEndpoints</span></span>
- <span data-ttu-id="94d58-141">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="94d58-141">ExternalEndpoints</span></span>
- <span data-ttu-id="94d58-142">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="94d58-142">NestedEndpoints</span></span>

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

### <span data-ttu-id="94d58-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94d58-143">-Confirm</span></span>
<span data-ttu-id="94d58-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="94d58-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94d58-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94d58-145">-WhatIf</span></span>
<span data-ttu-id="94d58-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="94d58-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94d58-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="94d58-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94d58-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94d58-148">CommonParameters</span></span>
<span data-ttu-id="94d58-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="94d58-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94d58-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94d58-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94d58-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="94d58-151">INPUTS</span></span>

### <span data-ttu-id="94d58-152">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="94d58-152">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="94d58-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="94d58-153">OUTPUTS</span></span>

### <span data-ttu-id="94d58-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="94d58-154">System.Boolean</span></span>

## <span data-ttu-id="94d58-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="94d58-155">NOTES</span></span>

## <span data-ttu-id="94d58-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94d58-156">RELATED LINKS</span></span>

[<span data-ttu-id="94d58-157">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="94d58-157">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="94d58-158">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="94d58-158">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="94d58-159">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="94d58-159">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="94d58-160">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="94d58-160">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="94d58-161">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="94d58-161">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="94d58-162">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="94d58-162">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="94d58-163">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="94d58-163">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


