---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 32263236-C207-4FE0-AB8A-018118FC7729
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/enable-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 9412a75ff595424637b36fb64db82ba556c9a057
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566876"
---
# <span data-ttu-id="3b7a9-101">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3b7a9-101">Enable-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="3b7a9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3b7a9-102">SYNOPSIS</span></span>
<span data-ttu-id="3b7a9-103">Включает конечную точку в профиле диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="3b7a9-103">Enables an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b7a9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3b7a9-104">SYNTAX</span></span>

### <span data-ttu-id="3b7a9-105">»</span><span class="sxs-lookup"><span data-stu-id="3b7a9-105">Fields</span></span>
```
Enable-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3b7a9-106">DataObject</span><span class="sxs-lookup"><span data-stu-id="3b7a9-106">Object</span></span>
```
Enable-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b7a9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b7a9-107">DESCRIPTION</span></span>
<span data-ttu-id="3b7a9-108">Командлет **Enable-AzureRmTrafficManagerEndpoint** включает конечную точку в профиле диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="3b7a9-108">The **Enable-AzureRmTrafficManagerEndpoint** cmdlet enables an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="3b7a9-109">Вы можете использовать оператор Pipeline для передачи объекта **TrafficManagerEndpoint** в этот командлет или задать объект **TrafficManagerEndpoint** с помощью параметра *TrafficManagerEndpoint* .</span><span class="sxs-lookup"><span data-stu-id="3b7a9-109">You can use the pipeline operator to pass a **TrafficManagerEndpoint** object to this cmdlet, or you can specify a **TrafficManagerEndpoint** object by using the *TrafficManagerEndpoint* parameter.</span></span>

<span data-ttu-id="3b7a9-110">Кроме того, вы можете указать имя и тип конечной точки, используя параметры *Name* и *Type* вместе с параметрами *filename* и *ResourceGroupName* .</span><span class="sxs-lookup"><span data-stu-id="3b7a9-110">Alternatively, you can specify the endpoint name and type by using the *Name* and *Type* parameters, together with the *ProfileName* and *ResourceGroupName* parameters.</span></span>

## <span data-ttu-id="3b7a9-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3b7a9-111">EXAMPLES</span></span>

### <span data-ttu-id="3b7a9-112">Пример 1: включение конечной точки из профиля</span><span class="sxs-lookup"><span data-stu-id="3b7a9-112">Example 1: Enable an endpoint from a profile</span></span>
```
PS C:\>Enable-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName ResourceGroup11 -Type ExternalEndpoints
```

<span data-ttu-id="3b7a9-113">Эта команда включает внешнюю конечную точку с именем Contoso в профиле с именем ContosoProfile в группе ресурсов ResouceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3b7a9-113">This command enables the external endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>

### <span data-ttu-id="3b7a9-114">Пример 2: включение конечной точки с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="3b7a9-114">Example 2: Enable an endpoint by using the pipeline</span></span>
```
PS C:\>Get-AzureRmTrafficManagerEndpoint -Name "contoso" -Type ExternalEndpoints -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzureRmTrafficManagerEndpoint
```

<span data-ttu-id="3b7a9-115">Эта команда получает внешнюю конечную точку с именем Contoso из профиля с именем ContosoProfile в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="3b7a9-115">This command gets the external endpoint named Contoso from the profile named ContosoProfile in ResourceGroup11.</span></span>
<span data-ttu-id="3b7a9-116">Затем команда передает эту конечную точку командлету **Enable-AzureRmTrafficManagerEndpoint** с помощью оператора Pipeline.</span><span class="sxs-lookup"><span data-stu-id="3b7a9-116">The command then passes that endpoint to the **Enable-AzureRmTrafficManagerEndpoint** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3b7a9-117">Этот командлет включает эту конечную точку.</span><span class="sxs-lookup"><span data-stu-id="3b7a9-117">That cmdlet enables that endpoint.</span></span>

## <span data-ttu-id="3b7a9-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3b7a9-118">PARAMETERS</span></span>

### <span data-ttu-id="3b7a9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b7a9-119">-DefaultProfile</span></span>
<span data-ttu-id="3b7a9-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3b7a9-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b7a9-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3b7a9-121">-Name</span></span>
<span data-ttu-id="3b7a9-122">Указывает имя конечной точки диспетчера трафика, которую включает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3b7a9-122">Specifies the name of the Traffic Manager endpoint that this cmdlet enables.</span></span>

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

### <span data-ttu-id="3b7a9-123">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="3b7a9-123">-ProfileName</span></span>
<span data-ttu-id="3b7a9-124">Указывает имя профиля диспетчера трафика, в котором этот командлет включит конечную точку.</span><span class="sxs-lookup"><span data-stu-id="3b7a9-124">Specifies the name of a Traffic Manager profile in which this cmdlet enables an endpoint.</span></span>
<span data-ttu-id="3b7a9-125">Чтобы получить профиль, используйте командлет Get-AzureRmTrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="3b7a9-125">To obtain a profile, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="3b7a9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b7a9-126">-ResourceGroupName</span></span>
<span data-ttu-id="3b7a9-127">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3b7a9-127">Specifies the name of a resource group.</span></span>
<span data-ttu-id="3b7a9-128">Этот командлет включает в группе, в которой указан этот параметр, конечную точку диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="3b7a9-128">This cmdlet enables a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="3b7a9-129">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3b7a9-129">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="3b7a9-130">Указывает конечную точку диспетчера трафика, которую включает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3b7a9-130">Specifies the Traffic Manager endpoint that this cmdlet enables.</span></span>
<span data-ttu-id="3b7a9-131">Чтобы получить объект **TrafficManagerEndpoint** , используйте командлет Get-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="3b7a9-131">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="3b7a9-132">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="3b7a9-132">-Type</span></span>
<span data-ttu-id="3b7a9-133">Указывает тип конечной точки, которую этот командлет отключает в профиле диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="3b7a9-133">Specifies the type of endpoint that this cmdlet disables in the Traffic Manager profile.</span></span>
<span data-ttu-id="3b7a9-134">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="3b7a9-134">Valid values are:</span></span> 

- <span data-ttu-id="3b7a9-135">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="3b7a9-135">AzureEndpoints</span></span>
- <span data-ttu-id="3b7a9-136">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="3b7a9-136">ExternalEndpoints</span></span>
- <span data-ttu-id="3b7a9-137">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="3b7a9-137">NestedEndpoints</span></span>

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

### <span data-ttu-id="3b7a9-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b7a9-138">CommonParameters</span></span>
<span data-ttu-id="3b7a9-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3b7a9-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b7a9-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b7a9-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b7a9-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3b7a9-141">INPUTS</span></span>

### <span data-ttu-id="3b7a9-142">TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3b7a9-142">TrafficManagerEndpoint</span></span>
<span data-ttu-id="3b7a9-143">Параметр "TrafficManagerEndpoint" принимает значение типа "TrafficManagerEndpoint" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="3b7a9-143">Parameter 'TrafficManagerEndpoint' accepts value of type 'TrafficManagerEndpoint' from the pipeline</span></span>

## <span data-ttu-id="3b7a9-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b7a9-144">OUTPUTS</span></span>

### <span data-ttu-id="3b7a9-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3b7a9-145">System.Boolean</span></span>

## <span data-ttu-id="3b7a9-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="3b7a9-146">NOTES</span></span>

## <span data-ttu-id="3b7a9-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b7a9-147">RELATED LINKS</span></span>

[<span data-ttu-id="3b7a9-148">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3b7a9-148">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="3b7a9-149">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3b7a9-149">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="3b7a9-150">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3b7a9-150">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="3b7a9-151">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3b7a9-151">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="3b7a9-152">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3b7a9-152">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="3b7a9-153">Remove-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3b7a9-153">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="3b7a9-154">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3b7a9-154">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


