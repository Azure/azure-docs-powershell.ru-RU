---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: c2e01d4a3f6ee3466151202a1c1d681c9f4e5486
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001912"
---
# <span data-ttu-id="1c25e-101">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="1c25e-101">Update-AzApiManagementRegion</span></span>

## <span data-ttu-id="1c25e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c25e-102">SYNOPSIS</span></span>
<span data-ttu-id="1c25e-103">Обновляет существующий регион развертывания в экземпляре PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="1c25e-103">Updates existing deployment region in PsApiManagement instance.</span></span>

## <span data-ttu-id="1c25e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1c25e-104">SYNTAX</span></span>

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1c25e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1c25e-105">DESCRIPTION</span></span>
<span data-ttu-id="1c25e-106">Командлет **Update-AzApiManagementRegion** обновляет существующий экземпляр типа **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** в коллекции объектов **AdditionalRegions** предоставленного экземпляра **типа Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="1c25e-106">The **Update-AzApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="1c25e-107">Этот cmdlet не развертывает ничего, но обновляет экземпляр **PsApiManagement** в памяти.</span><span class="sxs-lookup"><span data-stu-id="1c25e-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="1c25e-108">Чтобы обновить развертывание управления API, используйте измененный Set-AzApiManagement **PsApiManagementInstance.**</span><span class="sxs-lookup"><span data-stu-id="1c25e-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="1c25e-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1c25e-109">EXAMPLES</span></span>

### <span data-ttu-id="1c25e-110">Пример 1. Увеличение емкости дополнительного региона в экземпляре PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="1c25e-110">Example 1: Increases capacity of Additional Region in a PsApiManagement instance</span></span>
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium
PS C:\>$apimService = Set-AzApiManagement -InputObject $apimService -PassThru
```

<span data-ttu-id="1c25e-111">Эта команда получает службу SKU API Management Premium, регионы в юго-центральной части США и северной части США.</span><span class="sxs-lookup"><span data-stu-id="1c25e-111">This command gets the API Management Premium SKU service, having regions in South Central US and North Central US.</span></span> <span data-ttu-id="1c25e-112">Затем с помощью **set-AzApiManagement** можно увеличить емкость северо-центрального региона США до 2.</span><span class="sxs-lookup"><span data-stu-id="1c25e-112">It then increases the Capacity of the North Central US region to 2 using the **Set-AzApiManagement**.</span></span> <span data-ttu-id="1c25e-113">Следующий cmdlet **Set-AzApiManagement** примещает изменение конфигурации к службе управления Api.</span><span class="sxs-lookup"><span data-stu-id="1c25e-113">The next cmdlet **Set-AzApiManagement** applies the configuration change to the Api Management service.</span></span>

### <span data-ttu-id="1c25e-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="1c25e-114">Example 2</span></span>

<span data-ttu-id="1c25e-115">Обновляет существующий регион развертывания в экземпляре PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="1c25e-115">Updates existing deployment region in PsApiManagement instance.</span></span> <span data-ttu-id="1c25e-116">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="1c25e-116">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Capacity 2 -Location 'North Central US' -Sku Developer -VirtualNetwork <PsApiManagementVirtualNetwork>
```

## <span data-ttu-id="1c25e-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c25e-117">PARAMETERS</span></span>

### <span data-ttu-id="1c25e-118">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="1c25e-118">-ApiManagement</span></span>
<span data-ttu-id="1c25e-119">Указывает экземпляр **PsApiManagement,** в который нужно обновить существующий регион развертывания.</span><span class="sxs-lookup"><span data-stu-id="1c25e-119">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="1c25e-120">-Capacity</span><span class="sxs-lookup"><span data-stu-id="1c25e-120">-Capacity</span></span>
<span data-ttu-id="1c25e-121">Указывает новое значение емкости SKU для региона развертывания.</span><span class="sxs-lookup"><span data-stu-id="1c25e-121">Specifies the new SKU capacity value for the deployment region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c25e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c25e-122">-DefaultProfile</span></span>
<span data-ttu-id="1c25e-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1c25e-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c25e-124">-Location</span><span class="sxs-lookup"><span data-stu-id="1c25e-124">-Location</span></span>
<span data-ttu-id="1c25e-125">Определяет расположение региона развертывания, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="1c25e-125">Specifies the location of the deployment region to update.</span></span>
<span data-ttu-id="1c25e-126">Указывает расположение нового региона развертывания из поддерживаемого региона для службы управления Api.</span><span class="sxs-lookup"><span data-stu-id="1c25e-126">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="1c25e-127">Чтобы получить допустимые расположения, используйте Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | где {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object Расположения</span><span class="sxs-lookup"><span data-stu-id="1c25e-127">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c25e-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="1c25e-128">-Sku</span></span>
<span data-ttu-id="1c25e-129">Указывает значение нового уровня для региона развертывания.</span><span class="sxs-lookup"><span data-stu-id="1c25e-129">Specifies the new tier value for the deployment region.</span></span>
<span data-ttu-id="1c25e-130">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="1c25e-130">Valid values are:</span></span>
- <span data-ttu-id="1c25e-131">Разработчик</span><span class="sxs-lookup"><span data-stu-id="1c25e-131">Developer</span></span>
- <span data-ttu-id="1c25e-132">Стандартный</span><span class="sxs-lookup"><span data-stu-id="1c25e-132">Standard</span></span>
- <span data-ttu-id="1c25e-133">Premium</span><span class="sxs-lookup"><span data-stu-id="1c25e-133">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic, Consumption

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c25e-134">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1c25e-134">-VirtualNetwork</span></span>
<span data-ttu-id="1c25e-135">Определяет конфигурацию виртуальной сети для региона развертывания.</span><span class="sxs-lookup"><span data-stu-id="1c25e-135">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="1c25e-136">Передача $null удалит конфигурацию виртуальной сети для этого региона.</span><span class="sxs-lookup"><span data-stu-id="1c25e-136">Passing $null will remove virtual network configuration for the region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c25e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c25e-137">CommonParameters</span></span>
<span data-ttu-id="1c25e-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c25e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c25e-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c25e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c25e-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1c25e-140">INPUTS</span></span>

### <span data-ttu-id="1c25e-141">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="1c25e-141">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="1c25e-142">System.String</span><span class="sxs-lookup"><span data-stu-id="1c25e-142">System.String</span></span>

### <span data-ttu-id="1c25e-143">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span><span class="sxs-lookup"><span data-stu-id="1c25e-143">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="1c25e-144">System.Int32</span><span class="sxs-lookup"><span data-stu-id="1c25e-144">System.Int32</span></span>

### <span data-ttu-id="1c25e-145">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1c25e-145">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="1c25e-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1c25e-146">OUTPUTS</span></span>

### <span data-ttu-id="1c25e-147">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="1c25e-147">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="1c25e-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1c25e-148">NOTES</span></span>

## <span data-ttu-id="1c25e-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1c25e-149">RELATED LINKS</span></span>

[<span data-ttu-id="1c25e-150">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="1c25e-150">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="1c25e-151">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="1c25e-151">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="1c25e-152">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="1c25e-152">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)
