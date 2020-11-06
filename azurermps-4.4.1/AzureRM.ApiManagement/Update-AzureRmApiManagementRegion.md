---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
ms.openlocfilehash: 29dd6d1938228d3e76c0393ca27f49a3a9fe2564
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557967"
---
# <span data-ttu-id="fe1c3-101">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="fe1c3-101">Update-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="fe1c3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fe1c3-102">SYNOPSIS</span></span>
<span data-ttu-id="fe1c3-103">Обновляет существующий регион развертывания в экземпляре PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="fe1c3-103">Updates existing deployment region in PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe1c3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fe1c3-104">SYNTAX</span></span>

```
Update-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fe1c3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe1c3-105">DESCRIPTION</span></span>
<span data-ttu-id="fe1c3-106">Командлет **Update-AzureRmApiManagementRegion** обновляет существующий экземпляр типа **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** в коллекции объектов **AdditionalRegions** указанного экземпляра типа **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="fe1c3-106">The **Update-AzureRmApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="fe1c3-107">Этот командлет не развертывает ничего, но обновляет экземпляр **PsApiManagement** в памяти.</span><span class="sxs-lookup"><span data-stu-id="fe1c3-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="fe1c3-108">Чтобы обновить развертывание управления API, используйте модифицированный **PsApiManagementInstance** в командлете Update-AzureRmApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="fe1c3-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Update-AzureRmApiManagementDeployment cmdlet.</span></span>

## <span data-ttu-id="fe1c3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fe1c3-109">EXAMPLES</span></span>

## <span data-ttu-id="fe1c3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fe1c3-110">PARAMETERS</span></span>

### <span data-ttu-id="fe1c3-111">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fe1c3-111">-ApiManagement</span></span>
<span data-ttu-id="fe1c3-112">Указывает экземпляр **PsApiManagement** , который будет обновлять существующий регион развертывания в.</span><span class="sxs-lookup"><span data-stu-id="fe1c3-112">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="fe1c3-113">-Capacity</span><span class="sxs-lookup"><span data-stu-id="fe1c3-113">-Capacity</span></span>
<span data-ttu-id="fe1c3-114">Указывает новое значение емкости SKU для региона развертывания.</span><span class="sxs-lookup"><span data-stu-id="fe1c3-114">Specifies the new SKU capacity value for the deployment region.</span></span>

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

### <span data-ttu-id="fe1c3-115">-Location</span><span class="sxs-lookup"><span data-stu-id="fe1c3-115">-Location</span></span>
<span data-ttu-id="fe1c3-116">Указывает расположение области развертывания для обновления.</span><span class="sxs-lookup"><span data-stu-id="fe1c3-116">Specifies the location of the deployment region to update.</span></span>

<span data-ttu-id="fe1c3-117">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="fe1c3-117">Valid values are:</span></span>

- <span data-ttu-id="fe1c3-118">Северный Центральный США</span><span class="sxs-lookup"><span data-stu-id="fe1c3-118">North Central US</span></span>
- <span data-ttu-id="fe1c3-119">Южная Центральная американская</span><span class="sxs-lookup"><span data-stu-id="fe1c3-119">South Central US</span></span>
- <span data-ttu-id="fe1c3-120">Центральная американская</span><span class="sxs-lookup"><span data-stu-id="fe1c3-120">Central US</span></span>
- <span data-ttu-id="fe1c3-121">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="fe1c3-121">West Europe</span></span>
- <span data-ttu-id="fe1c3-122">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="fe1c3-122">North Europe</span></span>
- <span data-ttu-id="fe1c3-123">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="fe1c3-123">West US</span></span>
- <span data-ttu-id="fe1c3-124">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="fe1c3-124">East US</span></span>
- <span data-ttu-id="fe1c3-125">Восточная часть 2</span><span class="sxs-lookup"><span data-stu-id="fe1c3-125">East US 2</span></span>
- <span data-ttu-id="fe1c3-126">Восточная Япония</span><span class="sxs-lookup"><span data-stu-id="fe1c3-126">Japan East</span></span>
- <span data-ttu-id="fe1c3-127">Западная часть Японии</span><span class="sxs-lookup"><span data-stu-id="fe1c3-127">Japan West</span></span>
- <span data-ttu-id="fe1c3-128">Южная Бразилия</span><span class="sxs-lookup"><span data-stu-id="fe1c3-128">Brazil South</span></span>
- <span data-ttu-id="fe1c3-129">Юго-Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="fe1c3-129">Southeast Asia</span></span>
- <span data-ttu-id="fe1c3-130">Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="fe1c3-130">East Asia</span></span>
- <span data-ttu-id="fe1c3-131">Восточная Австралия</span><span class="sxs-lookup"><span data-stu-id="fe1c3-131">Australia East</span></span>
- <span data-ttu-id="fe1c3-132">Юго-восток Австралии</span><span class="sxs-lookup"><span data-stu-id="fe1c3-132">Australia Southeast</span></span>

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

### <span data-ttu-id="fe1c3-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="fe1c3-133">-Sku</span></span>
<span data-ttu-id="fe1c3-134">Задает значение нового уровня для области развертывания.</span><span class="sxs-lookup"><span data-stu-id="fe1c3-134">Specifies the new tier value for the deployment region.</span></span>

<span data-ttu-id="fe1c3-135">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="fe1c3-135">Valid values are:</span></span>

- <span data-ttu-id="fe1c3-136">Программист</span><span class="sxs-lookup"><span data-stu-id="fe1c3-136">Developer</span></span>
- <span data-ttu-id="fe1c3-137">Стандартная</span><span class="sxs-lookup"><span data-stu-id="fe1c3-137">Standard</span></span>
- <span data-ttu-id="fe1c3-138">Версию</span><span class="sxs-lookup"><span data-stu-id="fe1c3-138">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe1c3-139">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fe1c3-139">-VirtualNetwork</span></span>
<span data-ttu-id="fe1c3-140">Указывает конфигурацию виртуальной сети для региона развертывания.</span><span class="sxs-lookup"><span data-stu-id="fe1c3-140">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="fe1c3-141">Передача $null приведет к удалению конфигурации виртуальной сети для региона.</span><span class="sxs-lookup"><span data-stu-id="fe1c3-141">Passing $null will remove virtual network configuration for the region.</span></span>

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

### <span data-ttu-id="fe1c3-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe1c3-142">-DefaultProfile</span></span>
<span data-ttu-id="fe1c3-143">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fe1c3-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe1c3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe1c3-144">CommonParameters</span></span>
<span data-ttu-id="fe1c3-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fe1c3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe1c3-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe1c3-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe1c3-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fe1c3-147">INPUTS</span></span>

### <span data-ttu-id="fe1c3-148">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="fe1c3-148">PsApiManagement</span></span>
<span data-ttu-id="fe1c3-149">Параметр "ApiManagement" принимает значение типа "PsApiManagement" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="fe1c3-149">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="fe1c3-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe1c3-150">OUTPUTS</span></span>

### <span data-ttu-id="fe1c3-151">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="fe1c3-151">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="fe1c3-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="fe1c3-152">NOTES</span></span>

## <span data-ttu-id="fe1c3-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe1c3-153">RELATED LINKS</span></span>

[<span data-ttu-id="fe1c3-154">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="fe1c3-154">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="fe1c3-155">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="fe1c3-155">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="fe1c3-156">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="fe1c3-156">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)
