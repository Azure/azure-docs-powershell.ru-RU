---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
ms.openlocfilehash: f9b4aad305abd414e95a237b95ce339c583d8600
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728142"
---
# <span data-ttu-id="3902d-101">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="3902d-101">Add-AzApiManagementRegion</span></span>

## <span data-ttu-id="3902d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3902d-102">SYNOPSIS</span></span>
<span data-ttu-id="3902d-103">Добавляет новые области развертывания в экземпляр PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="3902d-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

## <span data-ttu-id="3902d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3902d-104">SYNTAX</span></span>

```
Add-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3902d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3902d-105">DESCRIPTION</span></span>
<span data-ttu-id="3902d-106">Командлет **Add-AzApiManagementRegion** добавляет новый экземпляр типа **PsApiManagementRegion** в коллекцию **AdditionalRegions** указанного экземпляра типа **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="3902d-106">The **Add-AzApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="3902d-107">Этот командлет не развертывает ничего отдельно, но обновляет экземпляр **PsApiManagement** в памяти.</span><span class="sxs-lookup"><span data-stu-id="3902d-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="3902d-108">Чтобы обновить развертывание управления API, передайте модифицированный экземпляр **PsApiManagement** в Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="3902d-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Set-AzApiManagement.</span></span>

## <span data-ttu-id="3902d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3902d-109">EXAMPLES</span></span>

### <span data-ttu-id="3902d-110">Пример 1: Добавление новых областей развертывания в экземпляр PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="3902d-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="3902d-111">Эта команда добавляет два единицы измерения Premium и регион с именем "Восток США" в экземпляр **PsApiManagement** .</span><span class="sxs-lookup"><span data-stu-id="3902d-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="3902d-112">Пример 2: Добавление новых областей развертывания в экземпляр PsApiManagement и последующее обновление развертывания</span><span class="sxs-lookup"><span data-stu-id="3902d-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```powershell
PS C:\>$service = Get-AzApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\>$service = Add-AzApiManagementRegion -ApiManagement $service -Location $secondarylocation -VirtualNetwork $additionalRegionVirtualNetwork
PS C:\>$service = Set-AzApiManagement -InputObject $service -PassThru 
```

<span data-ttu-id="3902d-113">Эта команда получает объект **PsApiManagement** , добавляя два единицы измерения Premium для региона "Восток США", а затем обновляет развертывание.</span><span class="sxs-lookup"><span data-stu-id="3902d-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="3902d-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3902d-114">PARAMETERS</span></span>

### <span data-ttu-id="3902d-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3902d-115">-ApiManagement</span></span>
<span data-ttu-id="3902d-116">Указывает экземпляр **PsApiManagement** , к которому этот командлет добавляет дополнительные области развертывания.</span><span class="sxs-lookup"><span data-stu-id="3902d-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

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

### <span data-ttu-id="3902d-117">-Capacity</span><span class="sxs-lookup"><span data-stu-id="3902d-117">-Capacity</span></span>
<span data-ttu-id="3902d-118">Указывает емкость SKU области развертывания.</span><span class="sxs-lookup"><span data-stu-id="3902d-118">Specifies the SKU capacity of the deployment region.</span></span>

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

### <span data-ttu-id="3902d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3902d-119">-DefaultProfile</span></span>
<span data-ttu-id="3902d-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3902d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3902d-121">-Location</span><span class="sxs-lookup"><span data-stu-id="3902d-121">-Location</span></span>
<span data-ttu-id="3902d-122">Указывает расположение нового региона развертывания в поддерживаемом регионе для службы управления API.</span><span class="sxs-lookup"><span data-stu-id="3902d-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="3902d-123">Для получения допустимых местоположений используйте командлет Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | where {$ _. ResourceTypes [0]. ResourceTypeName-EQ "Service"} | Расположение Select-Object</span><span class="sxs-lookup"><span data-stu-id="3902d-123">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="3902d-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="3902d-124">-Sku</span></span>
<span data-ttu-id="3902d-125">Указывает уровень области развертывания.</span><span class="sxs-lookup"><span data-stu-id="3902d-125">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="3902d-126">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="3902d-126">Valid values are:</span></span> 
- <span data-ttu-id="3902d-127">Программист</span><span class="sxs-lookup"><span data-stu-id="3902d-127">Developer</span></span>
- <span data-ttu-id="3902d-128">Стандартная</span><span class="sxs-lookup"><span data-stu-id="3902d-128">Standard</span></span>
- <span data-ttu-id="3902d-129">Версию</span><span class="sxs-lookup"><span data-stu-id="3902d-129">Premium</span></span>

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

### <span data-ttu-id="3902d-130">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3902d-130">-VirtualNetwork</span></span>
<span data-ttu-id="3902d-131">Указывает конфигурацию виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="3902d-131">Specifies a virtual network configuration.</span></span>

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

### <span data-ttu-id="3902d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3902d-132">CommonParameters</span></span>
<span data-ttu-id="3902d-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3902d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3902d-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3902d-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3902d-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3902d-135">INPUTS</span></span>

### <span data-ttu-id="3902d-136">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="3902d-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="3902d-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3902d-137">OUTPUTS</span></span>

### <span data-ttu-id="3902d-138">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="3902d-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="3902d-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="3902d-139">NOTES</span></span>
* <span data-ttu-id="3902d-140">Командлет записывает обновленный экземпляр **PsApiManagement** в конвейер.</span><span class="sxs-lookup"><span data-stu-id="3902d-140">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="3902d-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3902d-141">RELATED LINKS</span></span>

[<span data-ttu-id="3902d-142">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="3902d-142">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="3902d-143">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="3902d-143">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)

[<span data-ttu-id="3902d-144">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="3902d-144">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)


