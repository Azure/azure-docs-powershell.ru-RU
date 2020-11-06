---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 8CC749F1-B961-4F8F-BAD4-2C0F4385D1C2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/disable-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Disable-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: af05a91fe2281d457cff649bf0de6d986f7f413a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563927"
---
# <span data-ttu-id="84458-101">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="84458-101">Disable-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="84458-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="84458-102">SYNOPSIS</span></span>
<span data-ttu-id="84458-103">Отключает конечную точку в профиле диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="84458-103">Disables an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84458-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="84458-104">SYNTAX</span></span>

### <span data-ttu-id="84458-105">»</span><span class="sxs-lookup"><span data-stu-id="84458-105">Fields</span></span>
```
Disable-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84458-106">DataObject</span><span class="sxs-lookup"><span data-stu-id="84458-106">Object</span></span>
```
Disable-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84458-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="84458-107">DESCRIPTION</span></span>
<span data-ttu-id="84458-108">Командлет **Disable-AzureRmTrafficManagerEndpoint** отключает конечную точку в профиле диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="84458-108">The **Disable-AzureRmTrafficManagerEndpoint** cmdlet disables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="84458-109">Вы можете использовать оператор Pipeline для передачи объекта **TrafficManagerEndpoint** в этот командлет или передать объект **TrafficManagerEndpoint** с помощью параметра *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="84458-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can pass a **TrafficManagerEndpoint** object using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="84458-110">Кроме того, вы можете указать имя и тип конечной точки, используя параметры *Name* и *Type* вместе с параметрами *filename* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="84458-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="84458-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="84458-111">EXAMPLES</span></span>

### <span data-ttu-id="84458-112">Пример 1: отключение конечной точки по имени</span><span class="sxs-lookup"><span data-stu-id="84458-112">Example 1: Disable an endpoint by name</span></span>
```
PS C:\> Disable-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="84458-113">Эта команда отключает внешнюю конечную точку с именем Contoso в профиле с именем ContosoProfile в группе ресурсов ResouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="84458-113">This command disables the external endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>
<span data-ttu-id="84458-114">В командной строке появится запрос на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="84458-114">The command prompts you for confirmation.</span></span>

### <span data-ttu-id="84458-115">Пример 2: отключение конечной точки с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="84458-115">Example 2: Disable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Disable-AzureRmTrafficManagerEndpoint -Force
```

<span data-ttu-id="84458-116">Эта команда получает внешнюю конечную точку с именем Contoso из профиля с именем ContosoProfile в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="84458-116">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="84458-117">Затем команда передает эту конечную точку командлету **Disable-AzureRmTrafficManagerEndpoint** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="84458-117">The command then passes that endpoint to the **Disable-AzureRmTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="84458-118">Этот командлет отключает эту конечную точку.</span><span class="sxs-lookup"><span data-stu-id="84458-118">That cmdlet disables that endpoint.</span></span>
<span data-ttu-id="84458-119">Команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="84458-119">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="84458-120">Поэтому он не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="84458-120">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="84458-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="84458-121">PARAMETERS</span></span>

### <span data-ttu-id="84458-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84458-122">-DefaultProfile</span></span>
<span data-ttu-id="84458-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="84458-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84458-124">-Force</span><span class="sxs-lookup"><span data-stu-id="84458-124">-Force</span></span>
<span data-ttu-id="84458-125">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="84458-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="84458-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="84458-126">-Name</span></span>
<span data-ttu-id="84458-127">Указывает имя конечной точки диспетчера трафика, которую отключает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="84458-127">Specifies the name of the Traffic Manager endpoint that this cmdlet disables.</span></span>

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

### <span data-ttu-id="84458-128">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="84458-128">-ProfileName</span></span>
<span data-ttu-id="84458-129">Указывает имя профиля диспетчера трафика, в котором этот командлет отключает конечную точку.</span><span class="sxs-lookup"><span data-stu-id="84458-129">Specifies the name of a Traffic Manager profile in which this cmdlet disables an endpoint.</span></span>
<span data-ttu-id="84458-130">Чтобы получить профиль, используйте командлет Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="84458-130">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="84458-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84458-131">-ResourceGroupName</span></span>
<span data-ttu-id="84458-132">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="84458-132">Specifies the name of a resource group.</span></span>
<span data-ttu-id="84458-133">Этот командлет отключает в группе, в которой указан этот параметр, конечную точку диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="84458-133">This cmdlet disables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="84458-134">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="84458-134">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="84458-135">Указывает конечную точку диспетчера трафика, которую отключает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="84458-135">Specifies the Traffic Manager endpoint that this cmdlet disables.</span></span>
<span data-ttu-id="84458-136">Чтобы получить объект **TrafficManagerEndpoint** , используйте командлет Get-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="84458-136">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="84458-137">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="84458-137">-Type</span></span>
<span data-ttu-id="84458-138">Указывает тип конечной точки, которую добавляет этот командлет к профилю диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="84458-138">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="84458-139">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="84458-139">Valid values are:</span></span> 

- <span data-ttu-id="84458-140">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="84458-140">AzureEndpoints</span></span>
- <span data-ttu-id="84458-141">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="84458-141">ExternalEndpoints</span></span>
- <span data-ttu-id="84458-142">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="84458-142">NestedEndpoints</span></span>

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

### <span data-ttu-id="84458-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84458-143">-Confirm</span></span>
<span data-ttu-id="84458-144">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="84458-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84458-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84458-145">-WhatIf</span></span>
<span data-ttu-id="84458-146">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="84458-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84458-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="84458-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84458-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84458-148">CommonParameters</span></span>
<span data-ttu-id="84458-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="84458-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84458-150">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84458-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84458-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="84458-151">INPUTS</span></span>

### <span data-ttu-id="84458-152">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="84458-152">TrafficManagerEndpoint</span></span>
<span data-ttu-id="84458-153">Параметр "TrafficManagerEndpoint" принимает значение типа "TrafficManagerEndpoint" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="84458-153">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="84458-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="84458-154">OUTPUTS</span></span>

### <span data-ttu-id="84458-155">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="84458-155">System.Boolean</span></span>

## <span data-ttu-id="84458-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="84458-156">NOTES</span></span>

## <span data-ttu-id="84458-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="84458-157">RELATED LINKS</span></span>

[<span data-ttu-id="84458-158">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="84458-158">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="84458-159">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="84458-159">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="84458-160">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="84458-160">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="84458-161">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="84458-161">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="84458-162">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="84458-162">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="84458-163">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="84458-163">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="84458-164">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="84458-164">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


