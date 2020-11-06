---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
ms.openlocfilehash: ebf95d8e809731bdca2f288bc09054fd14353686
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568658"
---
# <span data-ttu-id="2aaf1-101">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="2aaf1-101">New-AzureRmApiManagement</span></span>

## <span data-ttu-id="2aaf1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2aaf1-102">SYNOPSIS</span></span>
<span data-ttu-id="2aaf1-103">Создает развертывание управления API.</span><span class="sxs-lookup"><span data-stu-id="2aaf1-103">Creates an API Management deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2aaf1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2aaf1-104">SYNTAX</span></span>

```
New-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2aaf1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2aaf1-105">DESCRIPTION</span></span>
<span data-ttu-id="2aaf1-106">Командлет **New-AzureRmApiManagement** создает развертывание управления API в Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="2aaf1-106">The **New-AzureRmApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="2aaf1-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2aaf1-107">EXAMPLES</span></span>

### <span data-ttu-id="2aaf1-108">Пример 1: создание службы управления API уровня разработчика</span><span class="sxs-lookup"><span data-stu-id="2aaf1-108">Example 1: Create a Developer tier API Management service</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="2aaf1-109">Эта команда создает службу управления API уровня разработчика.</span><span class="sxs-lookup"><span data-stu-id="2aaf1-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="2aaf1-110">Команда определяет организацию и адрес администратора.</span><span class="sxs-lookup"><span data-stu-id="2aaf1-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="2aaf1-111">В команде не указан параметр *SKU* .</span><span class="sxs-lookup"><span data-stu-id="2aaf1-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="2aaf1-112">Таким образом, командлет использует значение по умолчанию для разработчика.</span><span class="sxs-lookup"><span data-stu-id="2aaf1-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="2aaf1-113">Пример 2: создание стандартной службы уровня с тремя единицами</span><span class="sxs-lookup"><span data-stu-id="2aaf1-113">Example 2: Create a Standard tier service that has three units</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="2aaf1-114">Эта команда создает стандартную службу управления многоуровневой ИНТЕРФЕЙСом с тремя единицами.</span><span class="sxs-lookup"><span data-stu-id="2aaf1-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="2aaf1-115">Пример 3: создание службы управления API для внешней виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="2aaf1-115">Example 3: Create an API Management service for an external virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="2aaf1-116">Эта команда создает службу управления API высшего уровня в подсети виртуальной сети Azure, имеющей внешнюю доступную конечную точку шлюза с главным регионом в регионе "Западная часть США".</span><span class="sxs-lookup"><span data-stu-id="2aaf1-116">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="2aaf1-117">Пример 4: создание службы управления API для внутренней виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="2aaf1-117">Example 4: Create an API Management service for an internal virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="2aaf1-118">Эта команда создает службу управления API высшего уровня в подсети виртуальной сети Azure, которая имеет внутреннюю доступную конечную точку шлюза с главным регионом в регионе "Западная часть США".</span><span class="sxs-lookup"><span data-stu-id="2aaf1-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

## <span data-ttu-id="2aaf1-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2aaf1-119">PARAMETERS</span></span>

### <span data-ttu-id="2aaf1-120">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="2aaf1-120">-AdditionalRegions</span></span>
<span data-ttu-id="2aaf1-121">Дополнительные области развертывания управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="2aaf1-121">Additional deployment regions of Azure API Management.</span></span>

```yaml
Type: PsApiManagementRegion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2aaf1-122">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="2aaf1-122">-AdminEmail</span></span>
<span data-ttu-id="2aaf1-123">Указывает исходный адрес электронной почты для всех уведомлений, которые отправляет система управления API.</span><span class="sxs-lookup"><span data-stu-id="2aaf1-123">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="2aaf1-124">-Capacity</span><span class="sxs-lookup"><span data-stu-id="2aaf1-124">-Capacity</span></span>
<span data-ttu-id="2aaf1-125">Указывает емкость SKU службы управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="2aaf1-125">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="2aaf1-126">Значение по умолчанию — One (1).</span><span class="sxs-lookup"><span data-stu-id="2aaf1-126">The default is one (1).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2aaf1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aaf1-127">-DefaultProfile</span></span>
<span data-ttu-id="2aaf1-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2aaf1-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="2aaf1-129">-Location</span><span class="sxs-lookup"><span data-stu-id="2aaf1-129">-Location</span></span>
<span data-ttu-id="2aaf1-130">Указывает расположение для создания службы управления API.</span><span class="sxs-lookup"><span data-stu-id="2aaf1-130">Specifies the location to create the Api Management service.</span></span>

<span data-ttu-id="2aaf1-131">Для получения допустимых местоположений используйте командлет Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | where {$ _. ResourceTypes [0]. ResourceTypeName-EQ "Service"} | Расположение Select-Object</span><span class="sxs-lookup"><span data-stu-id="2aaf1-131">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="2aaf1-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2aaf1-132">-Name</span></span>
<span data-ttu-id="2aaf1-133">Указывает имя для развертывания управления API.</span><span class="sxs-lookup"><span data-stu-id="2aaf1-133">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="2aaf1-134">-Организация</span><span class="sxs-lookup"><span data-stu-id="2aaf1-134">-Organization</span></span>
<span data-ttu-id="2aaf1-135">Указывает название организации.</span><span class="sxs-lookup"><span data-stu-id="2aaf1-135">Specifies the name of an organization.</span></span>
<span data-ttu-id="2aaf1-136">Управление API использует этот адрес на портале разработчика в уведомлениях по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="2aaf1-136">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="2aaf1-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2aaf1-137">-ResourceGroupName</span></span>
<span data-ttu-id="2aaf1-138">Указывает имя группы ресурсов, в которой этот командлет создает развертывание для управления API.</span><span class="sxs-lookup"><span data-stu-id="2aaf1-138">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="2aaf1-139">-SKU</span><span class="sxs-lookup"><span data-stu-id="2aaf1-139">-Sku</span></span>
<span data-ttu-id="2aaf1-140">Указывает уровень службы управления API.</span><span class="sxs-lookup"><span data-stu-id="2aaf1-140">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="2aaf1-141">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="2aaf1-141">Valid values are:</span></span> 

- <span data-ttu-id="2aaf1-142">Программист</span><span class="sxs-lookup"><span data-stu-id="2aaf1-142">Developer</span></span> 
- <span data-ttu-id="2aaf1-143">Стандартная</span><span class="sxs-lookup"><span data-stu-id="2aaf1-143">Standard</span></span> 
- <span data-ttu-id="2aaf1-144">Версию</span><span class="sxs-lookup"><span data-stu-id="2aaf1-144">Premium</span></span> 

<span data-ttu-id="2aaf1-145">Значение по умолчанию — разработчик.</span><span class="sxs-lookup"><span data-stu-id="2aaf1-145">The default is Developer.</span></span>

```yaml
Type: PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2aaf1-146">-Тег</span><span class="sxs-lookup"><span data-stu-id="2aaf1-146">-Tag</span></span>
<span data-ttu-id="2aaf1-147">Словарь тегов.</span><span class="sxs-lookup"><span data-stu-id="2aaf1-147">Tags dictionary.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2aaf1-148">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2aaf1-148">-VirtualNetwork</span></span>
<span data-ttu-id="2aaf1-149">Конфигурация виртуальной сети для главного региона развертывания управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="2aaf1-149">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

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

### <span data-ttu-id="2aaf1-150">-VpnType</span><span class="sxs-lookup"><span data-stu-id="2aaf1-150">-VpnType</span></span>
<span data-ttu-id="2aaf1-151">Тип виртуальной сети для развертывания ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="2aaf1-151">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="2aaf1-152">Допустимые значения</span><span class="sxs-lookup"><span data-stu-id="2aaf1-152">Valid Values are</span></span> 
- <span data-ttu-id="2aaf1-153">"Нет" (значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2aaf1-153">"None" (Default Value.</span></span> <span data-ttu-id="2aaf1-154">ApiManagement не является частью какой-либо виртуальной сети.)</span><span class="sxs-lookup"><span data-stu-id="2aaf1-154">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="2aaf1-155">"External" (развертывание ApiManagement выполняется в виртуальной сети, у которой есть конечная точка, подключенная к Интернету)</span><span class="sxs-lookup"><span data-stu-id="2aaf1-155">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="2aaf1-156">"Internal" (развертывание ApiManagement в виртуальной сети, где есть конечная точка, подключенная к интрасети)</span><span class="sxs-lookup"><span data-stu-id="2aaf1-156">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

```yaml
Type: PsApiManagementVpnType
Parameter Sets: (All)
Aliases:
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aaf1-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aaf1-157">CommonParameters</span></span>
<span data-ttu-id="2aaf1-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2aaf1-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aaf1-159">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2aaf1-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aaf1-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2aaf1-160">INPUTS</span></span>

### <span data-ttu-id="2aaf1-161">Ничего</span><span class="sxs-lookup"><span data-stu-id="2aaf1-161">None</span></span>
<span data-ttu-id="2aaf1-162">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="2aaf1-162">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2aaf1-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2aaf1-163">OUTPUTS</span></span>

### <span data-ttu-id="2aaf1-164">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="2aaf1-164">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="2aaf1-165">Пуск</span><span class="sxs-lookup"><span data-stu-id="2aaf1-165">NOTES</span></span>

## <span data-ttu-id="2aaf1-166">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2aaf1-166">RELATED LINKS</span></span>

[<span data-ttu-id="2aaf1-167">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="2aaf1-167">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="2aaf1-168">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="2aaf1-168">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="2aaf1-169">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="2aaf1-169">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="2aaf1-170">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="2aaf1-170">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


