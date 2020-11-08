---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 5d7ef8e2fd778b5bcaaea1413bddd85eceb0582c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066111"
---
# <span data-ttu-id="49c43-101">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="49c43-101">Enable-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="49c43-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="49c43-102">SYNOPSIS</span></span>
<span data-ttu-id="49c43-103">Включает конечную точку в профиле диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="49c43-103">Enables an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="49c43-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="49c43-104">SYNTAX</span></span>

### <span data-ttu-id="49c43-105">»</span><span class="sxs-lookup"><span data-stu-id="49c43-105">Fields</span></span>
```
Enable-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49c43-106">DataObject</span><span class="sxs-lookup"><span data-stu-id="49c43-106">Object</span></span>
```
Enable-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49c43-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49c43-107">DESCRIPTION</span></span>
<span data-ttu-id="49c43-108">Командлет **Enable-AzTrafficManagerEndpoint** включает конечную точку в профиле диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="49c43-108">The **Enable-AzTrafficManagerEndpoint** cmdlet enables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="49c43-109">Вы можете использовать оператор Pipeline для передачи объекта **TrafficManagerEndpoint** в этот командлет или задать объект **TrafficManagerEndpoint** с помощью параметра *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="49c43-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="49c43-110">Кроме того, вы можете указать имя и тип конечной точки, используя параметры *Name* и *Type* вместе с параметрами *filename* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="49c43-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="49c43-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="49c43-111">EXAMPLES</span></span>

### <span data-ttu-id="49c43-112">Пример 1: включение конечной точки из профиля</span><span class="sxs-lookup"><span data-stu-id="49c43-112">Example 1: Enable an endpoint from a profile</span></span>
```
PS C:\>Enable-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="49c43-113">Эта команда включает внешнюю конечную точку с именем Contoso в профиле с именем ContosoProfile в группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="49c43-113">This command enables the external endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>

### <span data-ttu-id="49c43-114">Пример 2: включение конечной точки с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="49c43-114">Example 2: Enable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerEndpoint
```

<span data-ttu-id="49c43-115">Эта команда получает внешнюю конечную точку с именем Contoso из профиля с именем ContosoProfile в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="49c43-115">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="49c43-116">Затем команда передает эту конечную точку командлету **Enable-AzTrafficManagerEndpoint** с помощью оператора Pipeline.</span><span class="sxs-lookup"><span data-stu-id="49c43-116">The command then passes that endpoint to the **Enable-AzTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="49c43-117">Этот командлет включает эту конечную точку.</span><span class="sxs-lookup"><span data-stu-id="49c43-117">That cmdlet enables that endpoint.</span></span>

## <span data-ttu-id="49c43-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="49c43-118">PARAMETERS</span></span>

### <span data-ttu-id="49c43-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49c43-119">-DefaultProfile</span></span>
<span data-ttu-id="49c43-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49c43-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49c43-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="49c43-121">-Name</span></span>
<span data-ttu-id="49c43-122">Указывает имя конечной точки диспетчера трафика, которую включает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="49c43-122">Specifies the name of the Traffic Manager endpoint that this cmdlet enables.</span></span>

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

### <span data-ttu-id="49c43-123">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="49c43-123">-ProfileName</span></span>
<span data-ttu-id="49c43-124">Указывает имя профиля диспетчера трафика, в котором этот командлет включит конечную точку.</span><span class="sxs-lookup"><span data-stu-id="49c43-124">Specifies the name of a Traffic Manager profile in which this cmdlet enables an endpoint.</span></span>
<span data-ttu-id="49c43-125">Чтобы получить профиль, используйте командлет Get-AzTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="49c43-125">To obtain a profile, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="49c43-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49c43-126">-ResourceGroupName</span></span>
<span data-ttu-id="49c43-127">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="49c43-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="49c43-128">Этот командлет включает в группе, в которой указан этот параметр, конечную точку диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="49c43-128">This cmdlet enables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="49c43-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="49c43-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="49c43-130">Указывает конечную точку диспетчера трафика, которую включает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="49c43-130">Specifies the Traffic Manager endpoint that this cmdlet enables.</span></span>
<span data-ttu-id="49c43-131">Чтобы получить объект **TrafficManagerEndpoint** , используйте командлет Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="49c43-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="49c43-132">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="49c43-132">-Type</span></span>
<span data-ttu-id="49c43-133">Указывает тип конечной точки, которую этот командлет отключает в профиле диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="49c43-133">Specifies the type of endpoint that this cmdlet disables in the Traffic Manager profile.</span></span>
<span data-ttu-id="49c43-134">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="49c43-134">Valid values are:</span></span> 

- <span data-ttu-id="49c43-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="49c43-135">AzureEndpoints</span></span>
- <span data-ttu-id="49c43-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="49c43-136">ExternalEndpoints</span></span>
- <span data-ttu-id="49c43-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="49c43-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="49c43-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49c43-138">CommonParameters</span></span>
<span data-ttu-id="49c43-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="49c43-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49c43-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49c43-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49c43-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="49c43-141">INPUTS</span></span>

### <span data-ttu-id="49c43-142">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="49c43-142">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="49c43-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="49c43-143">OUTPUTS</span></span>

### <span data-ttu-id="49c43-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="49c43-144">System.Boolean</span></span>

## <span data-ttu-id="49c43-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="49c43-145">NOTES</span></span>

## <span data-ttu-id="49c43-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49c43-146">RELATED LINKS</span></span>

[<span data-ttu-id="49c43-147">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="49c43-147">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="49c43-148">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="49c43-148">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="49c43-149">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="49c43-149">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="49c43-150">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="49c43-150">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="49c43-151">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="49c43-151">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="49c43-152">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="49c43-152">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="49c43-153">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="49c43-153">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


