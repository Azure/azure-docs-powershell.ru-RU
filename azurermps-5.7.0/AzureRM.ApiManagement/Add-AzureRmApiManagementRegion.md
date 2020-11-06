---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
ms.openlocfilehash: f7a2952bf466a0d964a8b9075832635d2560b6fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570020"
---
# <span data-ttu-id="4be02-101">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="4be02-101">Add-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="4be02-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4be02-102">SYNOPSIS</span></span>
<span data-ttu-id="4be02-103">Добавляет новые области развертывания в экземпляр PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="4be02-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4be02-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4be02-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4be02-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4be02-105">DESCRIPTION</span></span>
<span data-ttu-id="4be02-106">Командлет **Add-AzureRmApiManagementRegion** добавляет новый экземпляр типа **PsApiManagementRegion** в коллекцию **AdditionalRegions** указанного экземпляра типа **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="4be02-106">The **Add-AzureRmApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="4be02-107">Этот командлет не развертывает ничего отдельно, но обновляет экземпляр **PsApiManagement** в памяти.</span><span class="sxs-lookup"><span data-stu-id="4be02-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="4be02-108">Чтобы обновить развертывание управления API, передайте измененный экземпляр **PsApiManagement** на Update-AzureRmApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="4be02-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Update-AzureRmApiManagementDeployment.</span></span>

## <span data-ttu-id="4be02-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4be02-109">EXAMPLES</span></span>

### <span data-ttu-id="4be02-110">Пример 1: Добавление новых областей развертывания в экземпляр PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="4be02-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="4be02-111">Эта команда добавляет два единицы измерения Premium и регион с именем "Восток США" в экземпляр **PsApiManagement** .</span><span class="sxs-lookup"><span data-stu-id="4be02-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="4be02-112">Пример 2: Добавление новых областей развертывания в экземпляр PsApiManagement и последующее обновление развертывания</span><span class="sxs-lookup"><span data-stu-id="4be02-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi" | Add-AzureRmApiManagementRegion -Location "East US" -Sku "Premium" -Capacity 2 | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="4be02-113">Эта команда получает объект **PsApiManagement** , добавляя два единицы измерения Premium для региона "Восток США", а затем обновляет развертывание.</span><span class="sxs-lookup"><span data-stu-id="4be02-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="4be02-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4be02-114">PARAMETERS</span></span>

### <span data-ttu-id="4be02-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="4be02-115">-ApiManagement</span></span>
<span data-ttu-id="4be02-116">Указывает экземпляр **PsApiManagement** , к которому этот командлет добавляет дополнительные области развертывания.</span><span class="sxs-lookup"><span data-stu-id="4be02-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

```yaml
Type: PsApiManagement
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4be02-117">-Capacity</span><span class="sxs-lookup"><span data-stu-id="4be02-117">-Capacity</span></span>
<span data-ttu-id="4be02-118">Указывает емкость SKU области развертывания.</span><span class="sxs-lookup"><span data-stu-id="4be02-118">Specifies the SKU capacity of the deployment region.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4be02-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4be02-119">-DefaultProfile</span></span>
<span data-ttu-id="4be02-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4be02-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4be02-121">-Location</span><span class="sxs-lookup"><span data-stu-id="4be02-121">-Location</span></span>
<span data-ttu-id="4be02-122">Указывает расположение нового региона развертывания в поддерживаемом регионе для службы управления API.</span><span class="sxs-lookup"><span data-stu-id="4be02-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>

<span data-ttu-id="4be02-123">Для получения допустимых местоположений используйте командлет Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | where {$ _. ResourceTypes [0]. ResourceTypeName-EQ "Service"} | Расположение Select-Object</span><span class="sxs-lookup"><span data-stu-id="4be02-123">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4be02-124">-SKU</span><span class="sxs-lookup"><span data-stu-id="4be02-124">-Sku</span></span>
<span data-ttu-id="4be02-125">Указывает уровень области развертывания.</span><span class="sxs-lookup"><span data-stu-id="4be02-125">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="4be02-126">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="4be02-126">Valid values are:</span></span> 

- <span data-ttu-id="4be02-127">Программист</span><span class="sxs-lookup"><span data-stu-id="4be02-127">Developer</span></span>
- <span data-ttu-id="4be02-128">Стандартная</span><span class="sxs-lookup"><span data-stu-id="4be02-128">Standard</span></span>
- <span data-ttu-id="4be02-129">Версию</span><span class="sxs-lookup"><span data-stu-id="4be02-129">Premium</span></span>

```yaml
Type: PsApiManagementSku
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4be02-130">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4be02-130">-VirtualNetwork</span></span>
<span data-ttu-id="4be02-131">Указывает конфигурацию виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="4be02-131">Specifies a virtual network configuration.</span></span>

```yaml
Type: PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4be02-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4be02-132">CommonParameters</span></span>
<span data-ttu-id="4be02-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4be02-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4be02-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4be02-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4be02-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4be02-135">INPUTS</span></span>

### <span data-ttu-id="4be02-136">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="4be02-136">PsApiManagement</span></span>
<span data-ttu-id="4be02-137">Параметр "ApiManagement" принимает значение типа "PsApiManagement" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="4be02-137">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="4be02-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4be02-138">OUTPUTS</span></span>

### <span data-ttu-id="4be02-139">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="4be02-139">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="4be02-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="4be02-140">NOTES</span></span>
* <span data-ttu-id="4be02-141">Командлет записывает обновленный экземпляр **PsApiManagement** в конвейер.</span><span class="sxs-lookup"><span data-stu-id="4be02-141">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="4be02-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4be02-142">RELATED LINKS</span></span>

[<span data-ttu-id="4be02-143">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="4be02-143">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="4be02-144">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="4be02-144">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)

[<span data-ttu-id="4be02-145">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="4be02-145">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)


