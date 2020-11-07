---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 4556C345-55D0-431C-B980-219D5ED14E5F
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/get-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 9ac1bb863053fc322265613a24d90b700d1846cc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904442"
---
# <span data-ttu-id="99aba-101">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="99aba-101">Get-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="99aba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="99aba-102">SYNOPSIS</span></span>
<span data-ttu-id="99aba-103">Получает конечную точку для профиля диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="99aba-103">Gets an endpoint for a Traffic Manager profile.</span></span>

## <span data-ttu-id="99aba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="99aba-104">SYNTAX</span></span>

### <span data-ttu-id="99aba-105">»</span><span class="sxs-lookup"><span data-stu-id="99aba-105">Fields</span></span>
```
Get-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99aba-106">DataObject</span><span class="sxs-lookup"><span data-stu-id="99aba-106">Object</span></span>
```
Get-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99aba-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="99aba-107">DESCRIPTION</span></span>
<span data-ttu-id="99aba-108">Командлет **Get-AzTrafficManagerEndpoint** получает конечную точку для профиля диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="99aba-108">The **Get-AzTrafficManagerEndpoint** cmdlet gets an endpoint for an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="99aba-109">Вы можете локально изменить этот объект, а затем применить изменения к профилю с помощью командлета Set-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="99aba-109">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="99aba-110">Укажите конечную точку, используя параметры *Name* и *Type* .</span><span class="sxs-lookup"><span data-stu-id="99aba-110">Specify the endpoint by using the *Name* and *Type* parameters.</span></span>
<span data-ttu-id="99aba-111">Профиль диспетчера трафика можно задать с помощью параметров *имя_профиля* и *ResourceGroupName* , либо указав объект **TrafficManagerProfile** .</span><span class="sxs-lookup"><span data-stu-id="99aba-111">You can specify the Traffic Manager profile either by using the *ProfileName* and *ResourceGroupName* parameter, or by specifying a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="99aba-112">Кроме того, вы можете передать это значение с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="99aba-112">Alternatively, you can pass that value by using the pipeline.</span></span>

## <span data-ttu-id="99aba-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="99aba-113">EXAMPLES</span></span>

### <span data-ttu-id="99aba-114">Пример 1: получение конечной точки</span><span class="sxs-lookup"><span data-stu-id="99aba-114">Example 1: Get an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="99aba-115">Эта команда получает конечную точку Azure с именем Contoso из профиля с именем ContosoProfile в группе ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="99aba-115">This command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>

## <span data-ttu-id="99aba-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="99aba-116">PARAMETERS</span></span>

### <span data-ttu-id="99aba-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99aba-117">-DefaultProfile</span></span>
<span data-ttu-id="99aba-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="99aba-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="99aba-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="99aba-119">-Name</span></span>
<span data-ttu-id="99aba-120">Указывает имя конечной точки диспетчера трафика, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="99aba-120">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="99aba-121">-Имя_профиля</span><span class="sxs-lookup"><span data-stu-id="99aba-121">-ProfileName</span></span>
<span data-ttu-id="99aba-122">Указывает имя конечной точки диспетчера трафика, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="99aba-122">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="99aba-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99aba-123">-ResourceGroupName</span></span>
<span data-ttu-id="99aba-124">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="99aba-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="99aba-125">Этот командлет получает конечную точку диспетчера трафика в группе, которую указывает этот параметр.</span><span class="sxs-lookup"><span data-stu-id="99aba-125">This cmdlet gets a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="99aba-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="99aba-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="99aba-127">Указывает конечную точку диспетчера трафика, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="99aba-127">Specifies the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="99aba-128">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="99aba-128">-Type</span></span>
<span data-ttu-id="99aba-129">Указывает тип конечной точки, которую добавляет этот командлет к профилю диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="99aba-129">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="99aba-130">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="99aba-130">Valid values are:</span></span> 

- <span data-ttu-id="99aba-131">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="99aba-131">AzureEndpoints</span></span>
- <span data-ttu-id="99aba-132">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="99aba-132">ExternalEndpoints</span></span>
- <span data-ttu-id="99aba-133">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="99aba-133">NestedEndpoints</span></span>

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

### <span data-ttu-id="99aba-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99aba-134">CommonParameters</span></span>
<span data-ttu-id="99aba-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="99aba-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99aba-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99aba-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99aba-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="99aba-137">INPUTS</span></span>

### <span data-ttu-id="99aba-138">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="99aba-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="99aba-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="99aba-139">OUTPUTS</span></span>

### <span data-ttu-id="99aba-140">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="99aba-140">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="99aba-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="99aba-141">NOTES</span></span>

## <span data-ttu-id="99aba-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="99aba-142">RELATED LINKS</span></span>

[<span data-ttu-id="99aba-143">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="99aba-143">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="99aba-144">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="99aba-144">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="99aba-145">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="99aba-145">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="99aba-146">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="99aba-146">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="99aba-147">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="99aba-147">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)


