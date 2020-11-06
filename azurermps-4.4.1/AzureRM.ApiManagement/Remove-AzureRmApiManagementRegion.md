---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
ms.openlocfilehash: 8bacb26b4e30521ddd840d2a8081365ed9c4c6ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557991"
---
# <span data-ttu-id="b2853-101">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="b2853-101">Remove-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="b2853-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b2853-102">SYNOPSIS</span></span>
<span data-ttu-id="b2853-103">Удаляет существующий регион развертывания из экземпляра PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="b2853-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2853-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b2853-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2853-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2853-105">DESCRIPTION</span></span>
<span data-ttu-id="b2853-106">Командлет **Remove-AzureRmApiManagementRegion** удаляет экземпляр типа **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** из коллекции **AdditionalRegions** предоставленных экземпляров типа **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="b2853-106">The **Remove-AzureRmApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="b2853-107">Этот командлет не изменяет само развертывание, но обновляет экземпляр **PsApiManagement** в памяти.</span><span class="sxs-lookup"><span data-stu-id="b2853-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="b2853-108">Чтобы обновить развертывание управления API, передайте модифицированный **PsApiManagementInstance** на **Update-AzureRmApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="b2853-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Update-AzureRmApiManagement**.</span></span>

## <span data-ttu-id="b2853-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b2853-109">EXAMPLES</span></span>

### <span data-ttu-id="b2853-110">Пример 1: удаление региона из экземпляра PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="b2853-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="b2853-111">Эта команда удаляет из экземпляра **PsApiManagement** регион с именем "Восток США".</span><span class="sxs-lookup"><span data-stu-id="b2853-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="b2853-112">Пример 2: удаление региона из экземпляра PsApiManagement с помощью ряда команд</span><span class="sxs-lookup"><span data-stu-id="b2853-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzureRmApiManagementRegion -Location "East US" | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="b2853-113">Эта первая команда получает экземпляр **PsApiManagement** из группы ресурсов contoso с именем ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="b2853-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="b2853-114">Последняя команда затем удаляет из этого экземпляра регион с именем "Восток США" и обновляет развертывание.</span><span class="sxs-lookup"><span data-stu-id="b2853-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="b2853-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b2853-115">PARAMETERS</span></span>

### <span data-ttu-id="b2853-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="b2853-116">-ApiManagement</span></span>
<span data-ttu-id="b2853-117">Указывает экземпляр **PsApiManagement** , из которого этот командлет удаляет дополнительный регион развертывания.</span><span class="sxs-lookup"><span data-stu-id="b2853-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

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

### <span data-ttu-id="b2853-118">-Location</span><span class="sxs-lookup"><span data-stu-id="b2853-118">-Location</span></span>
<span data-ttu-id="b2853-119">Указывает расположение области, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="b2853-119">Specifies the location of the region that this cmdlet removes.</span></span>

<span data-ttu-id="b2853-120">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="b2853-120">Valid values are:</span></span> 

- <span data-ttu-id="b2853-121">Северный Центральный США</span><span class="sxs-lookup"><span data-stu-id="b2853-121">North Central US</span></span>
- <span data-ttu-id="b2853-122">Южная Центральная американская</span><span class="sxs-lookup"><span data-stu-id="b2853-122">South Central US</span></span>
- <span data-ttu-id="b2853-123">Центральная американская</span><span class="sxs-lookup"><span data-stu-id="b2853-123">Central US</span></span>
- <span data-ttu-id="b2853-124">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="b2853-124">West Europe</span></span>
- <span data-ttu-id="b2853-125">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="b2853-125">North Europe</span></span>
- <span data-ttu-id="b2853-126">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="b2853-126">West US</span></span>
- <span data-ttu-id="b2853-127">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="b2853-127">East US</span></span>
- <span data-ttu-id="b2853-128">Восточная часть 2</span><span class="sxs-lookup"><span data-stu-id="b2853-128">East US 2</span></span>
- <span data-ttu-id="b2853-129">Восточная Япония</span><span class="sxs-lookup"><span data-stu-id="b2853-129">Japan East</span></span>
- <span data-ttu-id="b2853-130">Западная часть Японии</span><span class="sxs-lookup"><span data-stu-id="b2853-130">Japan West</span></span>
- <span data-ttu-id="b2853-131">Южная Бразилия</span><span class="sxs-lookup"><span data-stu-id="b2853-131">Brazil South</span></span>
- <span data-ttu-id="b2853-132">Юго-Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="b2853-132">Southeast Asia</span></span>
- <span data-ttu-id="b2853-133">Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="b2853-133">East Asia</span></span>
- <span data-ttu-id="b2853-134">Восточная Австралия</span><span class="sxs-lookup"><span data-stu-id="b2853-134">Australia East</span></span>
- <span data-ttu-id="b2853-135">Юго-восток Австралии</span><span class="sxs-lookup"><span data-stu-id="b2853-135">Australia Southeast</span></span>

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

### <span data-ttu-id="b2853-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2853-136">-DefaultProfile</span></span>
<span data-ttu-id="b2853-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b2853-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2853-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2853-138">CommonParameters</span></span>
<span data-ttu-id="b2853-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b2853-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2853-140">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2853-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2853-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b2853-141">INPUTS</span></span>

### <span data-ttu-id="b2853-142">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="b2853-142">PsApiManagement</span></span>
<span data-ttu-id="b2853-143">Параметр "ApiManagement" принимает значение типа "PsApiManagement" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="b2853-143">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="b2853-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2853-144">OUTPUTS</span></span>

### <span data-ttu-id="b2853-145">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="b2853-145">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="b2853-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="b2853-146">NOTES</span></span>

## <span data-ttu-id="b2853-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b2853-147">RELATED LINKS</span></span>

[<span data-ttu-id="b2853-148">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="b2853-148">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="b2853-149">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="b2853-149">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)


