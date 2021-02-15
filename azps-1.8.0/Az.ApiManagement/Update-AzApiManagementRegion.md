---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: 3f9c88177d3f791acdd0be5c81eec2fb5bc6911c
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400711"
---
# <span data-ttu-id="2ac57-101">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="2ac57-101">Update-AzApiManagementRegion</span></span>

## <span data-ttu-id="2ac57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ac57-102">SYNOPSIS</span></span>
<span data-ttu-id="2ac57-103">Обновляет существующий регион развертывания в экземпляре PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="2ac57-103">Updates existing deployment region in PsApiManagement instance.</span></span>

## <span data-ttu-id="2ac57-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2ac57-104">SYNTAX</span></span>

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2ac57-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ac57-105">DESCRIPTION</span></span>
<span data-ttu-id="2ac57-106">Командлет **Update-AzApiManagementRegion** обновляет существующий экземпляр типа **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** в коллекции объектов **AdditionalRegions** предоставленного экземпляра **типа Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="2ac57-106">The **Update-AzApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="2ac57-107">Этот cmdlet не развертывает ничего, но обновляет экземпляр **PsApiManagement** в памяти.</span><span class="sxs-lookup"><span data-stu-id="2ac57-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="2ac57-108">Чтобы обновить развертывание управления API, используйте измененный для Set-AzApiManagement **psApiManagementInstance.**</span><span class="sxs-lookup"><span data-stu-id="2ac57-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="2ac57-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2ac57-109">EXAMPLES</span></span>

### <span data-ttu-id="2ac57-110">Пример 1. Увеличение емкости дополнительного региона в экземпляре PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="2ac57-110">Example 1: Increases capacity of Additional Region in a PsApiManagement instance</span></span>
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium

# Set the ApiManagement service and Enable Msi idenity on the service
PS C:\>$updatedService = Set-AzApiManagement -InputObject $apimService -PassThru
```

<span data-ttu-id="2ac57-111">Эта команда получает службу SKU API Management Premium, регионы в юго-центральной части США и северной части США.</span><span class="sxs-lookup"><span data-stu-id="2ac57-111">This command gets the API Management Premium SKU service, having regions in South Central US and North Central US.</span></span> <span data-ttu-id="2ac57-112">Затем с помощью **Update-AzApiManagementRegion (Обновление-AzApiManagementRegion)** емкость региона North Central US увеличивается до 2.</span><span class="sxs-lookup"><span data-stu-id="2ac57-112">It then increases the Capacity of the North Central US region to 2 using the **Update-AzApiManagementRegion**.</span></span> <span data-ttu-id="2ac57-113">Следующий Set-AzApiManagement примещает изменение конфигурации к службе управления Api.</span><span class="sxs-lookup"><span data-stu-id="2ac57-113">The next cmdlet Set-AzApiManagement applies the configuration change to the Api Management service.</span></span>

## <span data-ttu-id="2ac57-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2ac57-114">PARAMETERS</span></span>

### <span data-ttu-id="2ac57-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2ac57-115">-ApiManagement</span></span>
<span data-ttu-id="2ac57-116">Указывает экземпляр **PsApiManagement,** в который нужно обновить существующий регион развертывания.</span><span class="sxs-lookup"><span data-stu-id="2ac57-116">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="2ac57-117">-Capacity</span><span class="sxs-lookup"><span data-stu-id="2ac57-117">-Capacity</span></span>
<span data-ttu-id="2ac57-118">Указывает новое значение емкости SKU для региона развертывания.</span><span class="sxs-lookup"><span data-stu-id="2ac57-118">Specifies the new SKU capacity value for the deployment region.</span></span>

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

### <span data-ttu-id="2ac57-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ac57-119">-DefaultProfile</span></span>
<span data-ttu-id="2ac57-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2ac57-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ac57-121">-Location</span><span class="sxs-lookup"><span data-stu-id="2ac57-121">-Location</span></span>
<span data-ttu-id="2ac57-122">Определяет расположение региона развертывания, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="2ac57-122">Specifies the location of the deployment region to update.</span></span>
<span data-ttu-id="2ac57-123">Указывает расположение нового региона развертывания из поддерживаемого региона для службы управления Api.</span><span class="sxs-lookup"><span data-stu-id="2ac57-123">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="2ac57-124">Чтобы получить допустимые расположения, используйте Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | где {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object Расположения</span><span class="sxs-lookup"><span data-stu-id="2ac57-124">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="2ac57-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="2ac57-125">-Sku</span></span>
<span data-ttu-id="2ac57-126">Указывает значение нового уровня для региона развертывания.</span><span class="sxs-lookup"><span data-stu-id="2ac57-126">Specifies the new tier value for the deployment region.</span></span>
<span data-ttu-id="2ac57-127">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="2ac57-127">Valid values are:</span></span>
- <span data-ttu-id="2ac57-128">Разработчик</span><span class="sxs-lookup"><span data-stu-id="2ac57-128">Developer</span></span>
- <span data-ttu-id="2ac57-129">Стандартный</span><span class="sxs-lookup"><span data-stu-id="2ac57-129">Standard</span></span>
- <span data-ttu-id="2ac57-130">Premium</span><span class="sxs-lookup"><span data-stu-id="2ac57-130">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac57-131">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2ac57-131">-VirtualNetwork</span></span>
<span data-ttu-id="2ac57-132">Определяет конфигурацию виртуальной сети для региона развертывания.</span><span class="sxs-lookup"><span data-stu-id="2ac57-132">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="2ac57-133">Передача $null удалит конфигурацию виртуальной сети для этого региона.</span><span class="sxs-lookup"><span data-stu-id="2ac57-133">Passing $null will remove virtual network configuration for the region.</span></span>

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

### <span data-ttu-id="2ac57-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ac57-134">CommonParameters</span></span>
<span data-ttu-id="2ac57-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ac57-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ac57-136">Дополнительные сведения см. в about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ac57-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ac57-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2ac57-137">INPUTS</span></span>

### <span data-ttu-id="2ac57-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="2ac57-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="2ac57-139">System.String</span><span class="sxs-lookup"><span data-stu-id="2ac57-139">System.String</span></span>

### <span data-ttu-id="2ac57-140">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span><span class="sxs-lookup"><span data-stu-id="2ac57-140">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="2ac57-141">System.Int32</span><span class="sxs-lookup"><span data-stu-id="2ac57-141">System.Int32</span></span>

### <span data-ttu-id="2ac57-142">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2ac57-142">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="2ac57-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2ac57-143">OUTPUTS</span></span>

### <span data-ttu-id="2ac57-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="2ac57-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="2ac57-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2ac57-145">NOTES</span></span>

## <span data-ttu-id="2ac57-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ac57-146">RELATED LINKS</span></span>

[<span data-ttu-id="2ac57-147">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="2ac57-147">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="2ac57-148">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="2ac57-148">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="2ac57-149">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="2ac57-149">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)
