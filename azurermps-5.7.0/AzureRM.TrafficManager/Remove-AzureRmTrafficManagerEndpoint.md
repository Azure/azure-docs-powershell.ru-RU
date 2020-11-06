---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2129C457-592B-484C-A148-828BFD5895D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 3b3eb2fb0539be4750f4cce7dedb7cd2f26931a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563232"
---
# <span data-ttu-id="f7eae-101">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f7eae-101">Remove-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="f7eae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7eae-102">SYNOPSIS</span></span>
<span data-ttu-id="f7eae-103">Удаляет конечную точку из диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="f7eae-103">Removes an endpoint from Traffic Manager.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7eae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7eae-104">SYNTAX</span></span>

### <span data-ttu-id="f7eae-105">»</span><span class="sxs-lookup"><span data-stu-id="f7eae-105">Fields</span></span>
```
Remove-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f7eae-106">DataObject</span><span class="sxs-lookup"><span data-stu-id="f7eae-106">Object</span></span>
```
Remove-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7eae-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7eae-107">DESCRIPTION</span></span>
<span data-ttu-id="f7eae-108">Командлет **Remove-AzureRmTrafficManagerEndpoint** удаляет конечную точку из диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="f7eae-108">The **Remove-AzureRmTrafficManagerEndpoint** cmdlet removes an endpoint from Azure Traffic Manager.</span></span>

<span data-ttu-id="f7eae-109">Этот командлет фиксирует каждое изменение в службе диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="f7eae-109">This cmdlet commits each change to the Traffic Manager service.</span></span>
<span data-ttu-id="f7eae-110">Для удаления нескольких конечных точек из объекта профиля диспетчера локальных данных и фиксации изменений в одной операции используйте командлет Remove-AzureRmTrafficManagerEndpointConfig.</span><span class="sxs-lookup"><span data-stu-id="f7eae-110">To remove multiple endpoints from a local Traffic Manager profile object and commit changes in a single operation, use the Remove-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>

<span data-ttu-id="f7eae-111">Вы можете использовать оператор Pipeline для передачи объекта **TrafficManagerEndpoint** в этот командлет или задать объект **TrafficManagerEndpoint** с помощью параметра *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="f7eae-111">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="f7eae-112">Кроме того, вы можете указать имя и тип конечной точки, используя параметры *Name* и *Type* вместе с параметрами *filename* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="f7eae-112">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="f7eae-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7eae-113">EXAMPLES</span></span>

### <span data-ttu-id="f7eae-114">Пример 1: Удаление конечной точки из профиля</span><span class="sxs-lookup"><span data-stu-id="f7eae-114">Example 1: Remove an endpoint from a profile</span></span>
```
PS C:\>Remove-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="f7eae-115">Эта команда удаляет конечную точку Azure с именем Contoso из профиля с именем ContosoProfile в группе ресурсов с именем ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="f7eae-115">This command removes the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="f7eae-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7eae-116">PARAMETERS</span></span>

### <span data-ttu-id="f7eae-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7eae-117">-DefaultProfile</span></span>
<span data-ttu-id="f7eae-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f7eae-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7eae-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f7eae-119">-Force</span></span>
<span data-ttu-id="f7eae-120">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f7eae-120">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7eae-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f7eae-121">-Name</span></span>
<span data-ttu-id="f7eae-122">Указывает имя конечной точки диспетчера трафика, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f7eae-122">Specifies the name of the Traffic Manager endpoint that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7eae-123">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="f7eae-123">-ProfileName</span></span>
<span data-ttu-id="f7eae-124">Указывает имя профиля диспетчера трафика, из которого этот командлет удаляет конечную точку.</span><span class="sxs-lookup"><span data-stu-id="f7eae-124">Specifies the name of a Traffic Manager profile from which this cmdlet removes an endpoint.</span></span>
<span data-ttu-id="f7eae-125">Чтобы получить профиль, используйте командлет Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f7eae-125">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7eae-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7eae-126">-ResourceGroupName</span></span>
<span data-ttu-id="f7eae-127">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f7eae-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="f7eae-128">Этот командлет удаляет конечную точку диспетчера трафика из профиля диспетчера трафика в группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="f7eae-128">This cmdlet removes a Traffic Manager endpoint from a Traffic Manager profile in the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7eae-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f7eae-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="f7eae-130">Указывает конечную точку диспетчера трафика, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f7eae-130">Specifies the Traffic Manager endpoint that this cmdlet removes.</span></span>
<span data-ttu-id="f7eae-131">Чтобы получить объект **TrafficManagerEndpoint** , используйте командлет Get-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="f7eae-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: TrafficManagerEndpoint
Parameter Sets: Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7eae-132">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="f7eae-132">-Type</span></span>
<span data-ttu-id="f7eae-133">Указывает тип конечной точки, которую добавляет этот командлет к профилю диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="f7eae-133">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="f7eae-134">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="f7eae-134">Valid values are:</span></span> 

- <span data-ttu-id="f7eae-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="f7eae-135">AzureEndpoints</span></span>
- <span data-ttu-id="f7eae-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="f7eae-136">ExternalEndpoints</span></span>
- <span data-ttu-id="f7eae-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="f7eae-137">NestedEndpoints</span></span>

```yaml
Type: String
Parameter Sets: Fields
Aliases: 
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7eae-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7eae-138">-Confirm</span></span>
<span data-ttu-id="f7eae-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f7eae-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7eae-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7eae-140">-WhatIf</span></span>
<span data-ttu-id="f7eae-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f7eae-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7eae-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f7eae-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7eae-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7eae-143">CommonParameters</span></span>
<span data-ttu-id="f7eae-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7eae-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7eae-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7eae-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7eae-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7eae-146">INPUTS</span></span>

### <span data-ttu-id="f7eae-147">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f7eae-147">TrafficManagerEndpoint</span></span>
<span data-ttu-id="f7eae-148">Параметр "TrafficManagerEndpoint" принимает значение типа "TrafficManagerEndpoint" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="f7eae-148">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="f7eae-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7eae-149">OUTPUTS</span></span>

### <span data-ttu-id="f7eae-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f7eae-150">System.Boolean</span></span>

## <span data-ttu-id="f7eae-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7eae-151">NOTES</span></span>

## <span data-ttu-id="f7eae-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7eae-152">RELATED LINKS</span></span>

[<span data-ttu-id="f7eae-153">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f7eae-153">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="f7eae-154">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f7eae-154">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="f7eae-155">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f7eae-155">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="f7eae-156">Remove-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="f7eae-156">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="f7eae-157">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f7eae-157">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


