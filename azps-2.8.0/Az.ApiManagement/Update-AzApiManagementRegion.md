---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: 7fa565eb16ced9e9146b219d7850354e499ef06e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727911"
---
# <span data-ttu-id="c18be-101">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="c18be-101">Update-AzApiManagementRegion</span></span>

## <span data-ttu-id="c18be-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c18be-102">SYNOPSIS</span></span>
<span data-ttu-id="c18be-103">Обновляет существующий регион развертывания в экземпляре PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="c18be-103">Updates existing deployment region in PsApiManagement instance.</span></span>

## <span data-ttu-id="c18be-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c18be-104">SYNTAX</span></span>

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c18be-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c18be-105">DESCRIPTION</span></span>
<span data-ttu-id="c18be-106">Командлет **Update-AzApiManagementRegion** обновляет существующий экземпляр типа **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** в коллекции объектов **AdditionalRegions** указанного экземпляра типа **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="c18be-106">The **Update-AzApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="c18be-107">Этот командлет не развертывает ничего, но обновляет экземпляр **PsApiManagement** в памяти.</span><span class="sxs-lookup"><span data-stu-id="c18be-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="c18be-108">Чтобы обновить развертывание управления API, используйте модифицированный **PsApiManagementInstance** в командлете Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="c18be-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="c18be-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c18be-109">EXAMPLES</span></span>

### <span data-ttu-id="c18be-110">Пример 1: увеличивает емкость дополнительного региона в экземпляре PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="c18be-110">Example 1: Increases capacity of Additional Region in a PsApiManagement instance</span></span>
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium
PS C:\>$apimService = Set-AzApiManagement -InputObject $apimService -PassThru
```

<span data-ttu-id="c18be-111">Эта команда возвращает службу управления расширенным интерфейсом API, в которой есть регионы в Южной Центральной США и Северной центральной части США.</span><span class="sxs-lookup"><span data-stu-id="c18be-111">This command gets the API Management Premium SKU service, having regions in South Central US and North Central US.</span></span> <span data-ttu-id="c18be-112">Затем он увеличивает емкость центрального региона США до 2 с помощью **Set-AzApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="c18be-112">It then increases the Capacity of the North Central US region to 2 using the **Set-AzApiManagement**.</span></span> <span data-ttu-id="c18be-113">Следующий командлет **Set-AzApiManagement** применяет изменение конфигурации к службе управления API.</span><span class="sxs-lookup"><span data-stu-id="c18be-113">The next cmdlet **Set-AzApiManagement** applies the configuration change to the Api Management service.</span></span>

## <span data-ttu-id="c18be-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c18be-114">PARAMETERS</span></span>

### <span data-ttu-id="c18be-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="c18be-115">-ApiManagement</span></span>
<span data-ttu-id="c18be-116">Указывает экземпляр **PsApiManagement** , который будет обновлять существующий регион развертывания в.</span><span class="sxs-lookup"><span data-stu-id="c18be-116">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="c18be-117">-Capacity</span><span class="sxs-lookup"><span data-stu-id="c18be-117">-Capacity</span></span>
<span data-ttu-id="c18be-118">Указывает новое значение емкости SKU для региона развертывания.</span><span class="sxs-lookup"><span data-stu-id="c18be-118">Specifies the new SKU capacity value for the deployment region.</span></span>

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

### <span data-ttu-id="c18be-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c18be-119">-DefaultProfile</span></span>
<span data-ttu-id="c18be-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c18be-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c18be-121">-Location</span><span class="sxs-lookup"><span data-stu-id="c18be-121">-Location</span></span>
<span data-ttu-id="c18be-122">Указывает расположение области развертывания для обновления.</span><span class="sxs-lookup"><span data-stu-id="c18be-122">Specifies the location of the deployment region to update.</span></span>
<span data-ttu-id="c18be-123">Указывает расположение нового региона развертывания в поддерживаемом регионе для службы управления API.</span><span class="sxs-lookup"><span data-stu-id="c18be-123">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="c18be-124">Для получения допустимых местоположений используйте командлет Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | where {$ _. ResourceTypes [0]. ResourceTypeName-EQ "Service"} | Расположение Select-Object</span><span class="sxs-lookup"><span data-stu-id="c18be-124">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="c18be-125">-SKU</span><span class="sxs-lookup"><span data-stu-id="c18be-125">-Sku</span></span>
<span data-ttu-id="c18be-126">Задает значение нового уровня для области развертывания.</span><span class="sxs-lookup"><span data-stu-id="c18be-126">Specifies the new tier value for the deployment region.</span></span>
<span data-ttu-id="c18be-127">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="c18be-127">Valid values are:</span></span>
- <span data-ttu-id="c18be-128">Программист</span><span class="sxs-lookup"><span data-stu-id="c18be-128">Developer</span></span>
- <span data-ttu-id="c18be-129">Стандартная</span><span class="sxs-lookup"><span data-stu-id="c18be-129">Standard</span></span>
- <span data-ttu-id="c18be-130">Версию</span><span class="sxs-lookup"><span data-stu-id="c18be-130">Premium</span></span>

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

### <span data-ttu-id="c18be-131">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c18be-131">-VirtualNetwork</span></span>
<span data-ttu-id="c18be-132">Указывает конфигурацию виртуальной сети для региона развертывания.</span><span class="sxs-lookup"><span data-stu-id="c18be-132">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="c18be-133">Передача $null приведет к удалению конфигурации виртуальной сети для региона.</span><span class="sxs-lookup"><span data-stu-id="c18be-133">Passing $null will remove virtual network configuration for the region.</span></span>

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

### <span data-ttu-id="c18be-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c18be-134">CommonParameters</span></span>
<span data-ttu-id="c18be-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c18be-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c18be-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c18be-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c18be-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c18be-137">INPUTS</span></span>

### <span data-ttu-id="c18be-138">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="c18be-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="c18be-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c18be-139">System.String</span></span>

### <span data-ttu-id="c18be-140">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSku</span><span class="sxs-lookup"><span data-stu-id="c18be-140">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="c18be-141">System. Int32</span><span class="sxs-lookup"><span data-stu-id="c18be-141">System.Int32</span></span>

### <span data-ttu-id="c18be-142">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c18be-142">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="c18be-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c18be-143">OUTPUTS</span></span>

### <span data-ttu-id="c18be-144">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="c18be-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="c18be-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="c18be-145">NOTES</span></span>

## <span data-ttu-id="c18be-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c18be-146">RELATED LINKS</span></span>

[<span data-ttu-id="c18be-147">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="c18be-147">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="c18be-148">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="c18be-148">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="c18be-149">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="c18be-149">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)
