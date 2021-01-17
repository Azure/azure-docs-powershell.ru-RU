---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 4556C345-55D0-431C-B980-219D5ED14E5F
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/get-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Get-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 3a24063e7b3d74704aa8d409b5bec6d87e35d095
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98423847"
---
# <span data-ttu-id="20ed1-101">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="20ed1-101">Get-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="20ed1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20ed1-102">SYNOPSIS</span></span>
<span data-ttu-id="20ed1-103">Получает конечную точку для профиля Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="20ed1-103">Gets an endpoint for a Traffic Manager profile.</span></span>

## <span data-ttu-id="20ed1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="20ed1-104">SYNTAX</span></span>

### <span data-ttu-id="20ed1-105">Поля</span><span class="sxs-lookup"><span data-stu-id="20ed1-105">Fields</span></span>
```
Get-AzTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20ed1-106">Объект</span><span class="sxs-lookup"><span data-stu-id="20ed1-106">Object</span></span>
```
Get-AzTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20ed1-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="20ed1-107">DESCRIPTION</span></span>
<span data-ttu-id="20ed1-108">Cmdlet **Get-AzTrafficManagerEndpoint** получает конечную точку для профиля Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="20ed1-108">The **Get-AzTrafficManagerEndpoint** cmdlet gets an endpoint for an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="20ed1-109">Вы можете изменить этот объект локально, а затем применить изменения к профилю с помощью Set-AzTrafficManagerEndpoint-Set-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="20ed1-109">You can modify this object locally, and then apply changes to the profile by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="20ed1-110">Укажите конечную точку с помощью параметров *"Имя"* и *"Тип".*</span><span class="sxs-lookup"><span data-stu-id="20ed1-110">Specify the endpoint by using the *Name* and *Type* parameters.</span></span>
<span data-ttu-id="20ed1-111">Вы можете указать профиль Диспетчера трафика с помощью параметра *ProfileName* и *ResourceGroupName* или объекта **TrafficManagerProfile.**</span><span class="sxs-lookup"><span data-stu-id="20ed1-111">You can specify the Traffic Manager profile either by using the *ProfileName* and *ResourceGroupName* parameter, or by specifying a **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="20ed1-112">Кроме того, это значение можно передать с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="20ed1-112">Alternatively, you can pass that value by using the pipeline.</span></span>

## <span data-ttu-id="20ed1-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="20ed1-113">EXAMPLES</span></span>

### <span data-ttu-id="20ed1-114">Пример 1. Получить конечную точку</span><span class="sxs-lookup"><span data-stu-id="20ed1-114">Example 1: Get an endpoint</span></span>
```
PS C:\>$TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

<span data-ttu-id="20ed1-115">Эта команда получает конечную точку Azure contoso из профиля ContosoProfile в группе ресурсов ResourceGroup11, а затем сохраняет объект в переменной $TrafficManagerEndpoint ресурса.</span><span class="sxs-lookup"><span data-stu-id="20ed1-115">This command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>

## <span data-ttu-id="20ed1-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20ed1-116">PARAMETERS</span></span>

### <span data-ttu-id="20ed1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20ed1-117">-DefaultProfile</span></span>
<span data-ttu-id="20ed1-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="20ed1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20ed1-119">-Name</span><span class="sxs-lookup"><span data-stu-id="20ed1-119">-Name</span></span>
<span data-ttu-id="20ed1-120">Указывает имя конечной точки Диспетчера трафика, которую получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20ed1-120">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="20ed1-121">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="20ed1-121">-ProfileName</span></span>
<span data-ttu-id="20ed1-122">Указывает имя конечной точки Диспетчера трафика, которую получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20ed1-122">Specifies the name of the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="20ed1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20ed1-123">-ResourceGroupName</span></span>
<span data-ttu-id="20ed1-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="20ed1-124">Specifies the name of a resource group.</span></span>
<span data-ttu-id="20ed1-125">Этот cmdlet получает конечную точку Диспетчера трафика в группе, указанной этим параметром.</span><span class="sxs-lookup"><span data-stu-id="20ed1-125">This cmdlet gets a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="20ed1-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="20ed1-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="20ed1-127">Указывает конечную точку диспетчера трафика, которая получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20ed1-127">Specifies the Traffic Manager endpoint that this cmdlet gets.</span></span>

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

### <span data-ttu-id="20ed1-128">-Type</span><span class="sxs-lookup"><span data-stu-id="20ed1-128">-Type</span></span>
<span data-ttu-id="20ed1-129">Тип конечной точки, которую этот cmdlet добавляет в профиль Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="20ed1-129">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="20ed1-130">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="20ed1-130">Valid values are:</span></span> 

- <span data-ttu-id="20ed1-131">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="20ed1-131">AzureEndpoints</span></span>
- <span data-ttu-id="20ed1-132">Внешниеendpoints</span><span class="sxs-lookup"><span data-stu-id="20ed1-132">ExternalEndpoints</span></span>
- <span data-ttu-id="20ed1-133">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="20ed1-133">NestedEndpoints</span></span>

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

### <span data-ttu-id="20ed1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20ed1-134">CommonParameters</span></span>
<span data-ttu-id="20ed1-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20ed1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20ed1-136">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20ed1-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20ed1-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="20ed1-137">INPUTS</span></span>

### <span data-ttu-id="20ed1-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="20ed1-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="20ed1-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="20ed1-139">OUTPUTS</span></span>

### <span data-ttu-id="20ed1-140">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="20ed1-140">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="20ed1-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="20ed1-141">NOTES</span></span>

## <span data-ttu-id="20ed1-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="20ed1-142">RELATED LINKS</span></span>

[<span data-ttu-id="20ed1-143">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="20ed1-143">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="20ed1-144">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="20ed1-144">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="20ed1-145">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="20ed1-145">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="20ed1-146">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="20ed1-146">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="20ed1-147">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="20ed1-147">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)


