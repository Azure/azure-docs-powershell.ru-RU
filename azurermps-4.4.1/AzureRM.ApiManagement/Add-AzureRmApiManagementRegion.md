---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
ms.openlocfilehash: 7edf16a6970f831235f76c64ef5cb5181a49bf98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568364"
---
# <span data-ttu-id="eb750-101">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="eb750-101">Add-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="eb750-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="eb750-102">SYNOPSIS</span></span>
<span data-ttu-id="eb750-103">Добавляет новые области развертывания в экземпляр PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="eb750-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb750-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="eb750-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb750-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb750-105">DESCRIPTION</span></span>
<span data-ttu-id="eb750-106">Командлет **Add-AzureRmApiManagementRegion** добавляет новый экземпляр типа **PsApiManagementRegion** в коллекцию **AdditionalRegions** указанного экземпляра типа **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="eb750-106">The **Add-AzureRmApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="eb750-107">Этот командлет не развертывает ничего отдельно, но обновляет экземпляр **PsApiManagement** в памяти.</span><span class="sxs-lookup"><span data-stu-id="eb750-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="eb750-108">Чтобы обновить развертывание управления API, передайте измененный экземпляр **PsApiManagement** на Update-AzureRmApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="eb750-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Update-AzureRmApiManagementDeployment.</span></span>

## <span data-ttu-id="eb750-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="eb750-109">EXAMPLES</span></span>

### <span data-ttu-id="eb750-110">Пример 1: Добавление новых областей развертывания в экземпляр PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="eb750-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="eb750-111">Эта команда добавляет два единицы измерения Premium и регион с именем "Восток США" в экземпляр **PsApiManagement** .</span><span class="sxs-lookup"><span data-stu-id="eb750-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="eb750-112">Пример 2: Добавление новых областей развертывания в экземпляр PsApiManagement и последующее обновление развертывания</span><span class="sxs-lookup"><span data-stu-id="eb750-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi" | Add-AzureRmApiManagementRegion -Location "East US" -Sku "Premium" -Capacity 2 | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="eb750-113">Эта команда получает объект **PsApiManagement** , добавляя два единицы измерения Premium для региона "Восток США", а затем обновляет развертывание.</span><span class="sxs-lookup"><span data-stu-id="eb750-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="eb750-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="eb750-114">PARAMETERS</span></span>

### <span data-ttu-id="eb750-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="eb750-115">-ApiManagement</span></span>
<span data-ttu-id="eb750-116">Указывает экземпляр **PsApiManagement** , к которому этот командлет добавляет дополнительные области развертывания.</span><span class="sxs-lookup"><span data-stu-id="eb750-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

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

### <span data-ttu-id="eb750-117">-Capacity</span><span class="sxs-lookup"><span data-stu-id="eb750-117">-Capacity</span></span>
<span data-ttu-id="eb750-118">Указывает емкость SKU области развертывания.</span><span class="sxs-lookup"><span data-stu-id="eb750-118">Specifies the SKU capacity of the deployment region.</span></span>

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

### <span data-ttu-id="eb750-119">-Location</span><span class="sxs-lookup"><span data-stu-id="eb750-119">-Location</span></span>
<span data-ttu-id="eb750-120">Указывает расположение нового региона развертывания.</span><span class="sxs-lookup"><span data-stu-id="eb750-120">Specifies the location of the new deployment region.</span></span>

<span data-ttu-id="eb750-121">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="eb750-121">Valid values are:</span></span> 

- <span data-ttu-id="eb750-122">Северный Центральный США</span><span class="sxs-lookup"><span data-stu-id="eb750-122">North Central US</span></span>
- <span data-ttu-id="eb750-123">Южная Центральная американская</span><span class="sxs-lookup"><span data-stu-id="eb750-123">South Central US</span></span>
- <span data-ttu-id="eb750-124">Центральная американская</span><span class="sxs-lookup"><span data-stu-id="eb750-124">Central US</span></span>
- <span data-ttu-id="eb750-125">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="eb750-125">West Europe</span></span>
- <span data-ttu-id="eb750-126">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="eb750-126">North Europe</span></span>
- <span data-ttu-id="eb750-127">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="eb750-127">West US</span></span>
- <span data-ttu-id="eb750-128">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="eb750-128">East US</span></span>
- <span data-ttu-id="eb750-129">Восточная часть 2</span><span class="sxs-lookup"><span data-stu-id="eb750-129">East US 2</span></span>
- <span data-ttu-id="eb750-130">Восточная Япония</span><span class="sxs-lookup"><span data-stu-id="eb750-130">Japan East</span></span>
- <span data-ttu-id="eb750-131">Западная часть Японии</span><span class="sxs-lookup"><span data-stu-id="eb750-131">Japan West</span></span>
- <span data-ttu-id="eb750-132">Южная Бразилия</span><span class="sxs-lookup"><span data-stu-id="eb750-132">Brazil South</span></span>
- <span data-ttu-id="eb750-133">Юго-Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="eb750-133">Southeast Asia</span></span>
- <span data-ttu-id="eb750-134">Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="eb750-134">East Asia</span></span>
- <span data-ttu-id="eb750-135">Восточная Австралия</span><span class="sxs-lookup"><span data-stu-id="eb750-135">Australia East</span></span>
- <span data-ttu-id="eb750-136">Юго-восток Австралии</span><span class="sxs-lookup"><span data-stu-id="eb750-136">Australia Southeast</span></span>

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

### <span data-ttu-id="eb750-137">-SKU</span><span class="sxs-lookup"><span data-stu-id="eb750-137">-Sku</span></span>
<span data-ttu-id="eb750-138">Указывает уровень области развертывания.</span><span class="sxs-lookup"><span data-stu-id="eb750-138">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="eb750-139">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="eb750-139">Valid values are:</span></span> 

- <span data-ttu-id="eb750-140">Программист</span><span class="sxs-lookup"><span data-stu-id="eb750-140">Developer</span></span>
- <span data-ttu-id="eb750-141">Стандартная</span><span class="sxs-lookup"><span data-stu-id="eb750-141">Standard</span></span>
- <span data-ttu-id="eb750-142">Версию</span><span class="sxs-lookup"><span data-stu-id="eb750-142">Premium</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb750-143">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="eb750-143">-VirtualNetwork</span></span>
<span data-ttu-id="eb750-144">Указывает конфигурацию виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="eb750-144">Specifies a virtual network configuration.</span></span>

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

### <span data-ttu-id="eb750-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb750-145">-DefaultProfile</span></span>
<span data-ttu-id="eb750-146">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="eb750-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eb750-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb750-147">CommonParameters</span></span>
<span data-ttu-id="eb750-148">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="eb750-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb750-149">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb750-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb750-150">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="eb750-150">INPUTS</span></span>

### <span data-ttu-id="eb750-151">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="eb750-151">PsApiManagement</span></span>
<span data-ttu-id="eb750-152">Параметр "ApiManagement" принимает значение типа "PsApiManagement" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="eb750-152">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="eb750-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="eb750-153">OUTPUTS</span></span>

### <span data-ttu-id="eb750-154">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="eb750-154">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="eb750-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="eb750-155">NOTES</span></span>
* <span data-ttu-id="eb750-156">Командлет записывает обновленный экземпляр **PsApiManagement** в конвейер.</span><span class="sxs-lookup"><span data-stu-id="eb750-156">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="eb750-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="eb750-157">RELATED LINKS</span></span>

[<span data-ttu-id="eb750-158">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="eb750-158">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="eb750-159">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="eb750-159">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)

[<span data-ttu-id="eb750-160">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="eb750-160">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)


