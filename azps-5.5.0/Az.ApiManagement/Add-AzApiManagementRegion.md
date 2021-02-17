---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
ms.openlocfilehash: 172bd1490b105b942dc706afe9440030d39d5c49
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100221849"
---
# <span data-ttu-id="144dd-101">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="144dd-101">Add-AzApiManagementRegion</span></span>

## <span data-ttu-id="144dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="144dd-102">SYNOPSIS</span></span>
<span data-ttu-id="144dd-103">Добавляет новые регионы развертывания в экземпляр PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="144dd-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

## <span data-ttu-id="144dd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="144dd-104">SYNTAX</span></span>

```
Add-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="144dd-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="144dd-105">DESCRIPTION</span></span>
<span data-ttu-id="144dd-106">Командлет **Add-AzApiManagementRegion** добавляет новый экземпляр типа **PsApiManagementRegion** в коллекцию **AdditionalRegions** предоставленного экземпляра **microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="144dd-106">The **Add-AzApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="144dd-107">Этот cmdlet не развертывает ничего сами по себе, но обновляет экземпляр **PsApiManagement** в памяти.</span><span class="sxs-lookup"><span data-stu-id="144dd-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="144dd-108">Чтобы обновить развертывание управления API, измененный экземпляр **PsApiManagement** передается в set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="144dd-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Set-AzApiManagement.</span></span>

## <span data-ttu-id="144dd-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="144dd-109">EXAMPLES</span></span>

### <span data-ttu-id="144dd-110">Пример 1. Добавление новых областей развертывания в экземпляр PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="144dd-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="144dd-111">Эта команда добавляет два единицы SKU премиум-класса и регион Восточной США в экземпляр **PsApiManagement.**</span><span class="sxs-lookup"><span data-stu-id="144dd-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="144dd-112">Пример 2. Добавление новых областей развертывания в экземпляр PsApiManagement и обновление развертывания</span><span class="sxs-lookup"><span data-stu-id="144dd-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```powershell
PS C:\>$service = Get-AzApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\>$service = Add-AzApiManagementRegion -ApiManagement $service -Location $secondarylocation -VirtualNetwork $additionalRegionVirtualNetwork
PS C:\>$service = Set-AzApiManagement -InputObject $service -PassThru
```

<span data-ttu-id="144dd-113">Эта команда получает объект **PsApiManagement,** добавляет два единицы SKU премиум для восточноазиатских регионов, а затем обновляет развертывание.</span><span class="sxs-lookup"><span data-stu-id="144dd-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="144dd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="144dd-114">PARAMETERS</span></span>

### <span data-ttu-id="144dd-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="144dd-115">-ApiManagement</span></span>
<span data-ttu-id="144dd-116">Указывает экземпляр **PsApiManagement,** в который этот cmdlet добавляет дополнительные регионы развертывания.</span><span class="sxs-lookup"><span data-stu-id="144dd-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="144dd-117">-Capacity</span><span class="sxs-lookup"><span data-stu-id="144dd-117">-Capacity</span></span>
<span data-ttu-id="144dd-118">Определяет емкость SKU в регионе развертывания.</span><span class="sxs-lookup"><span data-stu-id="144dd-118">Specifies the SKU capacity of the deployment region.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="144dd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="144dd-119">-DefaultProfile</span></span>
<span data-ttu-id="144dd-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="144dd-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="144dd-121">-Location</span><span class="sxs-lookup"><span data-stu-id="144dd-121">-Location</span></span>
<span data-ttu-id="144dd-122">Указывает расположение нового региона развертывания из поддерживаемого региона для службы управления Api.</span><span class="sxs-lookup"><span data-stu-id="144dd-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="144dd-123">Чтобы получить допустимые расположения, используйте Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | где {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object Расположения</span><span class="sxs-lookup"><span data-stu-id="144dd-123">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="144dd-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="144dd-124">-Sku</span></span>
<span data-ttu-id="144dd-125">Определяет уровень региона развертывания.</span><span class="sxs-lookup"><span data-stu-id="144dd-125">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="144dd-126">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="144dd-126">Valid values are:</span></span> 
- <span data-ttu-id="144dd-127">Разработчик</span><span class="sxs-lookup"><span data-stu-id="144dd-127">Developer</span></span>
- <span data-ttu-id="144dd-128">Стандартный</span><span class="sxs-lookup"><span data-stu-id="144dd-128">Standard</span></span>
- <span data-ttu-id="144dd-129">Premium</span><span class="sxs-lookup"><span data-stu-id="144dd-129">Premium</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic, Consumption

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="144dd-130">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="144dd-130">-VirtualNetwork</span></span>
<span data-ttu-id="144dd-131">Указывает конфигурацию виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="144dd-131">Specifies a virtual network configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="144dd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="144dd-132">CommonParameters</span></span>
<span data-ttu-id="144dd-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="144dd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="144dd-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="144dd-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="144dd-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="144dd-135">INPUTS</span></span>

### <span data-ttu-id="144dd-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="144dd-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="144dd-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="144dd-137">OUTPUTS</span></span>

### <span data-ttu-id="144dd-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="144dd-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="144dd-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="144dd-139">NOTES</span></span>
* <span data-ttu-id="144dd-140">Он записывает обновленный **экземпляр PsApiManagement для** конвейера.</span><span class="sxs-lookup"><span data-stu-id="144dd-140">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="144dd-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="144dd-141">RELATED LINKS</span></span>

[<span data-ttu-id="144dd-142">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="144dd-142">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="144dd-143">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="144dd-143">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)

[<span data-ttu-id="144dd-144">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="144dd-144">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)


