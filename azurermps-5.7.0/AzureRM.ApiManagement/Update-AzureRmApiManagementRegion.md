---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
ms.openlocfilehash: d6c97ac0fc948ba3ee4f86a2e657a1386c693f73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734041"
---
# <span data-ttu-id="76cac-101">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="76cac-101">Update-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="76cac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="76cac-102">SYNOPSIS</span></span>
<span data-ttu-id="76cac-103">Обновляет существующий регион развертывания в экземпляре PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="76cac-103">Updates existing deployment region in PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76cac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="76cac-104">SYNTAX</span></span>

```
Update-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="76cac-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="76cac-105">DESCRIPTION</span></span>
<span data-ttu-id="76cac-106">Командлет **Update-AzureRmApiManagementRegion** обновляет существующий экземпляр типа **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** в коллекции объектов **AdditionalRegions** указанного экземпляра типа **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="76cac-106">The **Update-AzureRmApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="76cac-107">Этот командлет не развертывает ничего, но обновляет экземпляр **PsApiManagement** в памяти.</span><span class="sxs-lookup"><span data-stu-id="76cac-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="76cac-108">Чтобы обновить развертывание управления API, используйте модифицированный **PsApiManagementInstance** в командлете Update-AzureRmApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="76cac-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Update-AzureRmApiManagementDeployment cmdlet.</span></span>

## <span data-ttu-id="76cac-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="76cac-109">EXAMPLES</span></span>

## <span data-ttu-id="76cac-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="76cac-110">PARAMETERS</span></span>

### <span data-ttu-id="76cac-111">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="76cac-111">-ApiManagement</span></span>
<span data-ttu-id="76cac-112">Указывает экземпляр **PsApiManagement** , который будет обновлять существующий регион развертывания в.</span><span class="sxs-lookup"><span data-stu-id="76cac-112">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="76cac-113">-Capacity</span><span class="sxs-lookup"><span data-stu-id="76cac-113">-Capacity</span></span>
<span data-ttu-id="76cac-114">Указывает новое значение емкости SKU для региона развертывания.</span><span class="sxs-lookup"><span data-stu-id="76cac-114">Specifies the new SKU capacity value for the deployment region.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76cac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76cac-115">-DefaultProfile</span></span>
<span data-ttu-id="76cac-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="76cac-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="76cac-117">-Location</span><span class="sxs-lookup"><span data-stu-id="76cac-117">-Location</span></span>
<span data-ttu-id="76cac-118">Указывает расположение области развертывания для обновления.</span><span class="sxs-lookup"><span data-stu-id="76cac-118">Specifies the location of the deployment region to update.</span></span>

<span data-ttu-id="76cac-119">Указывает расположение нового региона развертывания в поддерживаемом регионе для службы управления API.</span><span class="sxs-lookup"><span data-stu-id="76cac-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="76cac-120">Для получения допустимых местоположений используйте командлет Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | where {$ _. ResourceTypes [0]. ResourceTypeName-EQ "Service"} | Расположение Select-Object</span><span class="sxs-lookup"><span data-stu-id="76cac-120">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76cac-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="76cac-121">-Sku</span></span>
<span data-ttu-id="76cac-122">Задает значение нового уровня для области развертывания.</span><span class="sxs-lookup"><span data-stu-id="76cac-122">Specifies the new tier value for the deployment region.</span></span>

<span data-ttu-id="76cac-123">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="76cac-123">Valid values are:</span></span>

- <span data-ttu-id="76cac-124">Программист</span><span class="sxs-lookup"><span data-stu-id="76cac-124">Developer</span></span>
- <span data-ttu-id="76cac-125">Стандартная</span><span class="sxs-lookup"><span data-stu-id="76cac-125">Standard</span></span>
- <span data-ttu-id="76cac-126">Версию</span><span class="sxs-lookup"><span data-stu-id="76cac-126">Premium</span></span>

```yaml
Type: PsApiManagementSku
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76cac-127">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="76cac-127">-VirtualNetwork</span></span>
<span data-ttu-id="76cac-128">Указывает конфигурацию виртуальной сети для региона развертывания.</span><span class="sxs-lookup"><span data-stu-id="76cac-128">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="76cac-129">Передача $null приведет к удалению конфигурации виртуальной сети для региона.</span><span class="sxs-lookup"><span data-stu-id="76cac-129">Passing $null will remove virtual network configuration for the region.</span></span>

```yaml
Type: PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76cac-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76cac-130">CommonParameters</span></span>
<span data-ttu-id="76cac-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="76cac-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76cac-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76cac-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76cac-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="76cac-133">INPUTS</span></span>

### <span data-ttu-id="76cac-134">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="76cac-134">PsApiManagement</span></span>
<span data-ttu-id="76cac-135">Параметр "ApiManagement" принимает значение типа "PsApiManagement" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="76cac-135">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="76cac-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="76cac-136">OUTPUTS</span></span>

### <span data-ttu-id="76cac-137">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="76cac-137">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="76cac-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="76cac-138">NOTES</span></span>

## <span data-ttu-id="76cac-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="76cac-139">RELATED LINKS</span></span>

[<span data-ttu-id="76cac-140">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="76cac-140">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="76cac-141">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="76cac-141">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="76cac-142">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="76cac-142">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)
