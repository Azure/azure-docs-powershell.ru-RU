---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
ms.openlocfilehash: 82e09e146999ce0bd320ba398ab2f196f1115688
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565747"
---
# <span data-ttu-id="2437f-101">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="2437f-101">New-AzureRmApiManagement</span></span>

## <span data-ttu-id="2437f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2437f-102">SYNOPSIS</span></span>
<span data-ttu-id="2437f-103">Создает развертывание управления API.</span><span class="sxs-lookup"><span data-stu-id="2437f-103">Creates an API Management deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2437f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2437f-104">SYNTAX</span></span>

```
New-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2437f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2437f-105">DESCRIPTION</span></span>
<span data-ttu-id="2437f-106">Командлет **New-AzureRmApiManagement** создает развертывание управления API в Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="2437f-106">The **New-AzureRmApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="2437f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2437f-107">EXAMPLES</span></span>

### <span data-ttu-id="2437f-108">Пример 1: создание службы управления API уровня разработчика</span><span class="sxs-lookup"><span data-stu-id="2437f-108">Example 1: Create a Developer tier API Management service</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="2437f-109">Эта команда создает службу управления API уровня разработчика.</span><span class="sxs-lookup"><span data-stu-id="2437f-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="2437f-110">Команда определяет организацию и адрес администратора.</span><span class="sxs-lookup"><span data-stu-id="2437f-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="2437f-111">В команде не указан параметр *SKU* .</span><span class="sxs-lookup"><span data-stu-id="2437f-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="2437f-112">Таким образом, командлет использует значение по умолчанию для разработчика.</span><span class="sxs-lookup"><span data-stu-id="2437f-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="2437f-113">Пример 2: создание стандартной службы уровня с тремя единицами</span><span class="sxs-lookup"><span data-stu-id="2437f-113">Example 2: Create a Standard tier service that has three units</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="2437f-114">Эта команда создает стандартную службу управления многоуровневой ИНТЕРФЕЙСом с тремя единицами.</span><span class="sxs-lookup"><span data-stu-id="2437f-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="2437f-115">Пример 3: создание службы управления API для внешней виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="2437f-115">Example 3: Create an API Management service for an external virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="2437f-116">Эта команда создает службу управления API высшего уровня в подсети виртуальной сети Azure, имеющей внешнюю доступную конечную точку шлюза с главным регионом в регионе "Западная часть США".</span><span class="sxs-lookup"><span data-stu-id="2437f-116">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="2437f-117">Пример 4: создание службы управления API для внутренней виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="2437f-117">Example 4: Create an API Management service for an internal virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="2437f-118">Эта команда создает службу управления API высшего уровня в подсети виртуальной сети Azure, которая имеет внутреннюю доступную конечную точку шлюза с главным регионом в регионе "Западная часть США".</span><span class="sxs-lookup"><span data-stu-id="2437f-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

## <span data-ttu-id="2437f-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2437f-119">PARAMETERS</span></span>

### <span data-ttu-id="2437f-120">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="2437f-120">-AdditionalRegions</span></span>
<span data-ttu-id="2437f-121">Дополнительные области развертывания управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="2437f-121">Additional deployment regions of Azure API Management.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2437f-122">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="2437f-122">-AdminEmail</span></span>
<span data-ttu-id="2437f-123">Указывает исходный адрес электронной почты для всех уведомлений, которые отправляет система управления API.</span><span class="sxs-lookup"><span data-stu-id="2437f-123">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="2437f-124">-Capacity</span><span class="sxs-lookup"><span data-stu-id="2437f-124">-Capacity</span></span>
<span data-ttu-id="2437f-125">Указывает емкость SKU службы управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="2437f-125">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="2437f-126">Значение по умолчанию — One (1).</span><span class="sxs-lookup"><span data-stu-id="2437f-126">The default is one (1).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2437f-127">-Location</span><span class="sxs-lookup"><span data-stu-id="2437f-127">-Location</span></span>
<span data-ttu-id="2437f-128">Указывает расположение, в котором этот командлет создает развертывание управления API.</span><span class="sxs-lookup"><span data-stu-id="2437f-128">Specifies the location in which this cmdlet creates an API Management deployment.</span></span>
<span data-ttu-id="2437f-129">Для получения допустимых местоположений используйте командлеты Get-AzureLocation.</span><span class="sxs-lookup"><span data-stu-id="2437f-129">To obtain valid locations, use the Get-AzureLocation cmdlets.</span></span>

<span data-ttu-id="2437f-130">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="2437f-130">Valid values are:</span></span> 

- <span data-ttu-id="2437f-131">Северный Центральный США</span><span class="sxs-lookup"><span data-stu-id="2437f-131">North Central US</span></span>
- <span data-ttu-id="2437f-132">Южная Центральная американская</span><span class="sxs-lookup"><span data-stu-id="2437f-132">South Central US</span></span>
- <span data-ttu-id="2437f-133">Центральная американская</span><span class="sxs-lookup"><span data-stu-id="2437f-133">Central US</span></span>
- <span data-ttu-id="2437f-134">Западная Европа</span><span class="sxs-lookup"><span data-stu-id="2437f-134">West Europe</span></span>
- <span data-ttu-id="2437f-135">Северная Европа</span><span class="sxs-lookup"><span data-stu-id="2437f-135">North Europe</span></span>
- <span data-ttu-id="2437f-136">Западная часть США</span><span class="sxs-lookup"><span data-stu-id="2437f-136">West US</span></span>
- <span data-ttu-id="2437f-137">Восточная часть США</span><span class="sxs-lookup"><span data-stu-id="2437f-137">East US</span></span>
- <span data-ttu-id="2437f-138">Восточная часть 2</span><span class="sxs-lookup"><span data-stu-id="2437f-138">East US 2</span></span>
- <span data-ttu-id="2437f-139">Восточная Япония</span><span class="sxs-lookup"><span data-stu-id="2437f-139">Japan East</span></span>
- <span data-ttu-id="2437f-140">Западная часть Японии</span><span class="sxs-lookup"><span data-stu-id="2437f-140">Japan West</span></span>
- <span data-ttu-id="2437f-141">Южная Бразилия</span><span class="sxs-lookup"><span data-stu-id="2437f-141">Brazil South</span></span>
- <span data-ttu-id="2437f-142">Юго-Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="2437f-142">Southeast Asia</span></span>
- <span data-ttu-id="2437f-143">Восточная Азия</span><span class="sxs-lookup"><span data-stu-id="2437f-143">East Asia</span></span>
- <span data-ttu-id="2437f-144">Восточная Австралия</span><span class="sxs-lookup"><span data-stu-id="2437f-144">Australia East</span></span>
- <span data-ttu-id="2437f-145">Юго-восток Австралии</span><span class="sxs-lookup"><span data-stu-id="2437f-145">Australia Southeast</span></span>

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

### <span data-ttu-id="2437f-146">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2437f-146">-Name</span></span>
<span data-ttu-id="2437f-147">Указывает имя для развертывания управления API.</span><span class="sxs-lookup"><span data-stu-id="2437f-147">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="2437f-148">-Организация</span><span class="sxs-lookup"><span data-stu-id="2437f-148">-Organization</span></span>
<span data-ttu-id="2437f-149">Указывает название организации.</span><span class="sxs-lookup"><span data-stu-id="2437f-149">Specifies the name of an organization.</span></span>
<span data-ttu-id="2437f-150">Управление API использует этот адрес на портале разработчика в уведомлениях по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="2437f-150">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="2437f-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2437f-151">-ResourceGroupName</span></span>
<span data-ttu-id="2437f-152">Указывает имя группы ресурсов, в которой этот командлет создает развертывание для управления API.</span><span class="sxs-lookup"><span data-stu-id="2437f-152">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="2437f-153">-SKU</span><span class="sxs-lookup"><span data-stu-id="2437f-153">-Sku</span></span>
<span data-ttu-id="2437f-154">Указывает уровень службы управления API.</span><span class="sxs-lookup"><span data-stu-id="2437f-154">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="2437f-155">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="2437f-155">Valid values are:</span></span> 

- <span data-ttu-id="2437f-156">Программист</span><span class="sxs-lookup"><span data-stu-id="2437f-156">Developer</span></span> 
- <span data-ttu-id="2437f-157">Стандартная</span><span class="sxs-lookup"><span data-stu-id="2437f-157">Standard</span></span> 
- <span data-ttu-id="2437f-158">Версию</span><span class="sxs-lookup"><span data-stu-id="2437f-158">Premium</span></span> 

<span data-ttu-id="2437f-159">Значение по умолчанию — разработчик.</span><span class="sxs-lookup"><span data-stu-id="2437f-159">The default is Developer.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2437f-160">-Теги</span><span class="sxs-lookup"><span data-stu-id="2437f-160">-Tags</span></span>
<span data-ttu-id="2437f-161">Указывает словарь тегов.</span><span class="sxs-lookup"><span data-stu-id="2437f-161">Specifies a dictionary of tags.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2437f-162">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2437f-162">-VirtualNetwork</span></span>
<span data-ttu-id="2437f-163">Конфигурация виртуальной сети для главного региона развертывания управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="2437f-163">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

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

### <span data-ttu-id="2437f-164">-VpnType</span><span class="sxs-lookup"><span data-stu-id="2437f-164">-VpnType</span></span>
<span data-ttu-id="2437f-165">Тип виртуальной сети для развертывания ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="2437f-165">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="2437f-166">Допустимые значения</span><span class="sxs-lookup"><span data-stu-id="2437f-166">Valid Values are</span></span> 
- <span data-ttu-id="2437f-167">"Нет" (значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2437f-167">"None" (Default Value.</span></span> <span data-ttu-id="2437f-168">ApiManagement не является частью какой-либо виртуальной сети.)</span><span class="sxs-lookup"><span data-stu-id="2437f-168">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="2437f-169">"External" (развертывание ApiManagement выполняется в виртуальной сети, у которой есть конечная точка, подключенная к Интернету)</span><span class="sxs-lookup"><span data-stu-id="2437f-169">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="2437f-170">"Internal" (развертывание ApiManagement в виртуальной сети, где есть конечная точка, подключенная к интрасети)</span><span class="sxs-lookup"><span data-stu-id="2437f-170">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: (All)
Aliases: 
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2437f-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2437f-171">-DefaultProfile</span></span>
<span data-ttu-id="2437f-172">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2437f-172">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2437f-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2437f-173">CommonParameters</span></span>
<span data-ttu-id="2437f-174">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2437f-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2437f-175">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2437f-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2437f-176">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2437f-176">INPUTS</span></span>

## <span data-ttu-id="2437f-177">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2437f-177">OUTPUTS</span></span>

### <span data-ttu-id="2437f-178">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="2437f-178">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="2437f-179">Пуск</span><span class="sxs-lookup"><span data-stu-id="2437f-179">NOTES</span></span>

## <span data-ttu-id="2437f-180">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2437f-180">RELATED LINKS</span></span>

[<span data-ttu-id="2437f-181">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="2437f-181">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="2437f-182">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="2437f-182">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="2437f-183">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="2437f-183">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="2437f-184">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="2437f-184">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


