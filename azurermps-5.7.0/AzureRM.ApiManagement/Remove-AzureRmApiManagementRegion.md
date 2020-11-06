---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
ms.openlocfilehash: 0376c80e769153c448cdc23d8465966026584fcf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570323"
---
# <span data-ttu-id="3c395-101">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="3c395-101">Remove-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="3c395-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3c395-102">SYNOPSIS</span></span>
<span data-ttu-id="3c395-103">Удаляет существующий регион развертывания из экземпляра PsApiManagement.</span><span class="sxs-lookup"><span data-stu-id="3c395-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c395-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3c395-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c395-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c395-105">DESCRIPTION</span></span>
<span data-ttu-id="3c395-106">Командлет **Remove-AzureRmApiManagementRegion** удаляет экземпляр типа **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion** из коллекции **AdditionalRegions** предоставленных экземпляров типа **Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="3c395-106">The **Remove-AzureRmApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="3c395-107">Этот командлет не изменяет само развертывание, но обновляет экземпляр **PsApiManagement** в памяти.</span><span class="sxs-lookup"><span data-stu-id="3c395-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="3c395-108">Чтобы обновить развертывание управления API, передайте модифицированный **PsApiManagementInstance** на **Update-AzureRmApiManagement**.</span><span class="sxs-lookup"><span data-stu-id="3c395-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Update-AzureRmApiManagement**.</span></span>

## <span data-ttu-id="3c395-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3c395-109">EXAMPLES</span></span>

### <span data-ttu-id="3c395-110">Пример 1: удаление региона из экземпляра PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="3c395-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="3c395-111">Эта команда удаляет из экземпляра **PsApiManagement** регион с именем "Восток США".</span><span class="sxs-lookup"><span data-stu-id="3c395-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="3c395-112">Пример 2: удаление региона из экземпляра PsApiManagement с помощью ряда команд</span><span class="sxs-lookup"><span data-stu-id="3c395-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzureRmApiManagementRegion -Location "East US" | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="3c395-113">Эта первая команда получает экземпляр **PsApiManagement** из группы ресурсов contoso с именем ContosoApi.</span><span class="sxs-lookup"><span data-stu-id="3c395-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="3c395-114">Последняя команда затем удаляет из этого экземпляра регион с именем "Восток США" и обновляет развертывание.</span><span class="sxs-lookup"><span data-stu-id="3c395-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="3c395-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3c395-115">PARAMETERS</span></span>

### <span data-ttu-id="3c395-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="3c395-116">-ApiManagement</span></span>
<span data-ttu-id="3c395-117">Указывает экземпляр **PsApiManagement** , из которого этот командлет удаляет дополнительный регион развертывания.</span><span class="sxs-lookup"><span data-stu-id="3c395-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

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

### <span data-ttu-id="3c395-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c395-118">-DefaultProfile</span></span>
<span data-ttu-id="3c395-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3c395-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="3c395-120">-Location</span><span class="sxs-lookup"><span data-stu-id="3c395-120">-Location</span></span>
<span data-ttu-id="3c395-121">Указывает расположение области, которую удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3c395-121">Specifies the location of the region that this cmdlet removes.</span></span>

<span data-ttu-id="3c395-122">Указывает расположение нового региона развертывания в поддерживаемом регионе для службы управления API.</span><span class="sxs-lookup"><span data-stu-id="3c395-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="3c395-123">Для получения допустимых местоположений используйте командлет Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | where {$ _. ResourceTypes [0]. ResourceTypeName-EQ "Service"} | Расположение Select-Object</span><span class="sxs-lookup"><span data-stu-id="3c395-123">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="3c395-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c395-124">CommonParameters</span></span>
<span data-ttu-id="3c395-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3c395-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c395-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c395-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c395-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3c395-127">INPUTS</span></span>

### <span data-ttu-id="3c395-128">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="3c395-128">PsApiManagement</span></span>
<span data-ttu-id="3c395-129">Параметр "ApiManagement" принимает значение типа "PsApiManagement" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="3c395-129">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="3c395-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c395-130">OUTPUTS</span></span>

### <span data-ttu-id="3c395-131">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="3c395-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="3c395-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="3c395-132">NOTES</span></span>

## <span data-ttu-id="3c395-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c395-133">RELATED LINKS</span></span>

[<span data-ttu-id="3c395-134">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="3c395-134">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="3c395-135">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="3c395-135">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)


