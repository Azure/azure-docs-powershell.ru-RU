---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: fff6145adaa909bcadde90f36802072b812ba0ae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074158"
---
# <span data-ttu-id="901bc-101">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="901bc-101">Update-AzApiManagementRegion</span></span>

## <span data-ttu-id="901bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="901bc-102">SYNOPSIS</span></span>
<span data-ttu-id="901bc-103">Обновляет существующий регион развертывания в экземпляре PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="901bc-103">Updates existing deployment region in PsApiManagement instance.</span></span>

## <span data-ttu-id="901bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="901bc-104">SYNTAX</span></span>

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="901bc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="901bc-105">DESCRIPTION</span></span>
<span data-ttu-id="901bc-106">Командлет **Update-AzApiManagementRegion** обновляет существующий экземпляр типа **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** в коллекции объектов **AdditionalRegions** указанного экземпляра типа **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="901bc-106">The **Update-AzApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="901bc-107">Этот командлет не развертывает ничего, но обновляет экземпляр **PsApiManagement** в памяти.</span><span class="sxs-lookup"><span data-stu-id="901bc-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="901bc-108">Чтобы обновить развертывание управления API, используйте модифицированный **PsApiManagementInstance** в командлете Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="901bc-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="901bc-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="901bc-109">EXAMPLES</span></span>

### <span data-ttu-id="901bc-110">Пример 1: увеличивает емкость дополнительного региона в экземпляре PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="901bc-110">Example 1: Increases capacity of Additional Region in a PsApiManagement instance</span></span>
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium
PS C:\>$apimService = Set-AzApiManagement -InputObject $apimService -PassThru
```

<span data-ttu-id="901bc-111">Эта команда возвращает службу управления расширенным интерфейсом API, в которой есть регионы в Южной Центральной США и Северной центральной части США.</span><span class="sxs-lookup"><span data-stu-id="901bc-111">This command gets the API Management Premium SKU service, having regions in South Central US and North Central US.</span></span> <span data-ttu-id="901bc-112">Затем он увеличивает емкость центрального региона США до 2 с помощью **Set-AzApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="901bc-112">It then increases the Capacity of the North Central US region to 2 using the **Set-AzApiManagement**.</span></span> <span data-ttu-id="901bc-113">Следующий командлет **Set-AzApiManagement** применяет изменение конфигурации к службе управления API.</span><span class="sxs-lookup"><span data-stu-id="901bc-113">The next cmdlet **Set-AzApiManagement** applies the configuration change to the Api Management service.</span></span>

## <span data-ttu-id="901bc-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="901bc-114">PARAMETERS</span></span>

### <span data-ttu-id="901bc-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="901bc-115">-ApiManagement</span></span>
<span data-ttu-id="901bc-116">Указывает экземпляр **PsApiManagement** , который будет обновлять существующий регион развертывания в.</span><span class="sxs-lookup"><span data-stu-id="901bc-116">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="901bc-117">-Capacity</span><span class="sxs-lookup"><span data-stu-id="901bc-117">-Capacity</span></span>
<span data-ttu-id="901bc-118">Указывает новое значение емкости SKU для региона развертывания.</span><span class="sxs-lookup"><span data-stu-id="901bc-118">Specifies the new SKU capacity value for the deployment region.</span></span>

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

### <span data-ttu-id="901bc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="901bc-119">-DefaultProfile</span></span>
<span data-ttu-id="901bc-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="901bc-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="901bc-121">-Location</span><span class="sxs-lookup"><span data-stu-id="901bc-121">-Location</span></span>
<span data-ttu-id="901bc-122">Указывает расположение области развертывания для обновления.</span><span class="sxs-lookup"><span data-stu-id="901bc-122">Specifies the location of the deployment region to update.</span></span>
<span data-ttu-id="901bc-123">Указывает расположение нового региона развертывания в поддерживаемом регионе для службы управления API.</span><span class="sxs-lookup"><span data-stu-id="901bc-123">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="901bc-124">Для получения допустимых местоположений используйте командлет Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | where {$ _. ResourceTypes [0]. ResourceTypeName-EQ "Service"} | Расположение Select-Object</span><span class="sxs-lookup"><span data-stu-id="901bc-124">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="901bc-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="901bc-125">-Sku</span></span>
<span data-ttu-id="901bc-126">Задает значение нового уровня для области развертывания.</span><span class="sxs-lookup"><span data-stu-id="901bc-126">Specifies the new tier value for the deployment region.</span></span>
<span data-ttu-id="901bc-127">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="901bc-127">Valid values are:</span></span>
- <span data-ttu-id="901bc-128">Программист</span><span class="sxs-lookup"><span data-stu-id="901bc-128">Developer</span></span>
- <span data-ttu-id="901bc-129">Стандартная</span><span class="sxs-lookup"><span data-stu-id="901bc-129">Standard</span></span>
- <span data-ttu-id="901bc-130">Версию</span><span class="sxs-lookup"><span data-stu-id="901bc-130">Premium</span></span>

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

### <span data-ttu-id="901bc-131">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="901bc-131">-VirtualNetwork</span></span>
<span data-ttu-id="901bc-132">Указывает конфигурацию виртуальной сети для региона развертывания.</span><span class="sxs-lookup"><span data-stu-id="901bc-132">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="901bc-133">Передача $null приведет к удалению конфигурации виртуальной сети для региона.</span><span class="sxs-lookup"><span data-stu-id="901bc-133">Passing $null will remove virtual network configuration for the region.</span></span>

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

### <span data-ttu-id="901bc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="901bc-134">CommonParameters</span></span>
<span data-ttu-id="901bc-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="901bc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="901bc-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="901bc-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="901bc-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="901bc-137">INPUTS</span></span>

### <span data-ttu-id="901bc-138">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="901bc-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="901bc-139">System. String</span><span class="sxs-lookup"><span data-stu-id="901bc-139">System.String</span></span>

### <span data-ttu-id="901bc-140">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSku</span><span class="sxs-lookup"><span data-stu-id="901bc-140">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="901bc-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="901bc-141">System.Int32</span></span>

### <span data-ttu-id="901bc-142">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="901bc-142">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="901bc-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="901bc-143">OUTPUTS</span></span>

### <span data-ttu-id="901bc-144">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="901bc-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="901bc-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="901bc-145">NOTES</span></span>

## <span data-ttu-id="901bc-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="901bc-146">RELATED LINKS</span></span>

[<span data-ttu-id="901bc-147">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="901bc-147">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="901bc-148">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="901bc-148">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="901bc-149">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="901bc-149">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)
