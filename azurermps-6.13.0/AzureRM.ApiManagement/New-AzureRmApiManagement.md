---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
ms.openlocfilehash: 98e90b4c8275028ab3e62e7383505775271e8d09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732810"
---
# <span data-ttu-id="36d40-101">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="36d40-101">New-AzureRmApiManagement</span></span>

## <span data-ttu-id="36d40-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="36d40-102">SYNOPSIS</span></span>
<span data-ttu-id="36d40-103">Создает развертывание управления API.</span><span class="sxs-lookup"><span data-stu-id="36d40-103">Creates an API Management deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36d40-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="36d40-104">SYNTAX</span></span>

```
New-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>]
 [-CustomHostnameConfiguration <PsApiManagementCustomHostNameConfiguration[]>]
 [-SystemCertificateConfiguration <PsApiManagementSystemCertificate[]>] [-AssignIdentity]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36d40-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36d40-105">DESCRIPTION</span></span>
<span data-ttu-id="36d40-106">Командлет **New-AzureRmApiManagement** создает развертывание управления API в Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="36d40-106">The **New-AzureRmApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="36d40-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="36d40-107">EXAMPLES</span></span>

### <span data-ttu-id="36d40-108">Пример 1: создание службы управления API уровня разработчика</span><span class="sxs-lookup"><span data-stu-id="36d40-108">Example 1: Create a Developer tier API Management service</span></span>
```powershell
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="36d40-109">Эта команда создает службу управления API уровня разработчика.</span><span class="sxs-lookup"><span data-stu-id="36d40-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="36d40-110">Команда определяет организацию и адрес администратора.</span><span class="sxs-lookup"><span data-stu-id="36d40-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="36d40-111">В команде не указан параметр *SKU* .</span><span class="sxs-lookup"><span data-stu-id="36d40-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="36d40-112">Таким образом, командлет использует значение по умолчанию для разработчика.</span><span class="sxs-lookup"><span data-stu-id="36d40-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="36d40-113">Пример 2: создание стандартной службы уровня с тремя единицами</span><span class="sxs-lookup"><span data-stu-id="36d40-113">Example 2: Create a Standard tier service that has three units</span></span>
```powershell
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="36d40-114">Эта команда создает стандартную службу управления многоуровневой ИНТЕРФЕЙСом с тремя единицами.</span><span class="sxs-lookup"><span data-stu-id="36d40-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="36d40-115">Пример 3: создание службы управления API для внешней виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="36d40-115">Example 3: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="36d40-116">Эта команда создает службу управления API высшего уровня в подсети виртуальной сети Azure, имеющей внешнюю доступную конечную точку шлюза с главным регионом в регионе "Западная часть США".</span><span class="sxs-lookup"><span data-stu-id="36d40-116">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="36d40-117">Пример 4: создание службы управления API для внутренней виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="36d40-117">Example 4: Create an API Management service for an internal virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="36d40-118">Эта команда создает службу управления API высшего уровня в подсети виртуальной сети Azure, которая имеет внутреннюю доступную конечную точку шлюза с главным регионом в регионе "Западная часть США".</span><span class="sxs-lookup"><span data-stu-id="36d40-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

## <span data-ttu-id="36d40-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="36d40-119">PARAMETERS</span></span>

### <span data-ttu-id="36d40-120">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="36d40-120">-AdditionalRegions</span></span>
<span data-ttu-id="36d40-121">Дополнительные области развертывания управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="36d40-121">Additional deployment regions of Azure API Management.</span></span>

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

### <span data-ttu-id="36d40-122">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="36d40-122">-AdminEmail</span></span>
<span data-ttu-id="36d40-123">Указывает исходный адрес электронной почты для всех уведомлений, которые отправляет система управления API.</span><span class="sxs-lookup"><span data-stu-id="36d40-123">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="36d40-124">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="36d40-124">-AssignIdentity</span></span>
<span data-ttu-id="36d40-125">Создавайте и назначайте удостоверение Azure Active Directory для этого сервера для использования со службами управления ключами, такими как Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="36d40-125">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36d40-126">-Capacity</span><span class="sxs-lookup"><span data-stu-id="36d40-126">-Capacity</span></span>
<span data-ttu-id="36d40-127">Указывает емкость SKU службы управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="36d40-127">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="36d40-128">Значение по умолчанию — One (1).</span><span class="sxs-lookup"><span data-stu-id="36d40-128">The default is one (1).</span></span>

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

### <span data-ttu-id="36d40-129">-CustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="36d40-129">-CustomHostnameConfiguration</span></span>
<span data-ttu-id="36d40-130">Пользовательские конфигурации hostname.</span><span class="sxs-lookup"><span data-stu-id="36d40-130">Custom hostname configurations.</span></span> <span data-ttu-id="36d40-131">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="36d40-131">Default value is $null.</span></span> <span data-ttu-id="36d40-132">Передача $null задаст имя HostName по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="36d40-132">Passing $null will set the default hostname.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36d40-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36d40-133">-DefaultProfile</span></span>
<span data-ttu-id="36d40-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="36d40-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36d40-135">-Location</span><span class="sxs-lookup"><span data-stu-id="36d40-135">-Location</span></span>
<span data-ttu-id="36d40-136">Указывает расположение для создания службы управления API.</span><span class="sxs-lookup"><span data-stu-id="36d40-136">Specifies the location to create the Api Management service.</span></span>
<span data-ttu-id="36d40-137">Для получения допустимых местоположений используйте командлет Get-AzureRmResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | where {$ _. ResourceTypes [0]. ResourceTypeName-EQ "Service"} | Расположение Select-Object</span><span class="sxs-lookup"><span data-stu-id="36d40-137">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="36d40-138">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="36d40-138">-Name</span></span>
<span data-ttu-id="36d40-139">Указывает имя для развертывания управления API.</span><span class="sxs-lookup"><span data-stu-id="36d40-139">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="36d40-140">-Организация</span><span class="sxs-lookup"><span data-stu-id="36d40-140">-Organization</span></span>
<span data-ttu-id="36d40-141">Указывает название организации.</span><span class="sxs-lookup"><span data-stu-id="36d40-141">Specifies the name of an organization.</span></span>
<span data-ttu-id="36d40-142">Управление API использует этот адрес на портале разработчика в уведомлениях по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="36d40-142">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="36d40-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36d40-143">-ResourceGroupName</span></span>
<span data-ttu-id="36d40-144">Указывает имя группы ресурсов, в которой этот командлет создает развертывание для управления API.</span><span class="sxs-lookup"><span data-stu-id="36d40-144">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="36d40-145">-SKU</span><span class="sxs-lookup"><span data-stu-id="36d40-145">-Sku</span></span>
<span data-ttu-id="36d40-146">Указывает уровень службы управления API.</span><span class="sxs-lookup"><span data-stu-id="36d40-146">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="36d40-147">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="36d40-147">Valid values are:</span></span> 
- <span data-ttu-id="36d40-148">Программист</span><span class="sxs-lookup"><span data-stu-id="36d40-148">Developer</span></span> 
- <span data-ttu-id="36d40-149">Стандартная</span><span class="sxs-lookup"><span data-stu-id="36d40-149">Standard</span></span> 
- <span data-ttu-id="36d40-150">Premium значение по умолчанию — разработчик.</span><span class="sxs-lookup"><span data-stu-id="36d40-150">Premium The default is Developer.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36d40-151">-SystemCertificateConfiguration</span><span class="sxs-lookup"><span data-stu-id="36d40-151">-SystemCertificateConfiguration</span></span>
<span data-ttu-id="36d40-152">Сертификаты, выданные внутренним центром сертификации для установки в службе.</span><span class="sxs-lookup"><span data-stu-id="36d40-152">Certificates issued by Internal CA to be installed on the service.</span></span> <span data-ttu-id="36d40-153">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="36d40-153">Default value is $null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36d40-154">-Тег</span><span class="sxs-lookup"><span data-stu-id="36d40-154">-Tag</span></span>
<span data-ttu-id="36d40-155">Словарь тегов.</span><span class="sxs-lookup"><span data-stu-id="36d40-155">Tags dictionary.</span></span>

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

### <span data-ttu-id="36d40-156">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="36d40-156">-VirtualNetwork</span></span>
<span data-ttu-id="36d40-157">Конфигурация виртуальной сети для главного региона развертывания управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="36d40-157">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

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

### <span data-ttu-id="36d40-158">-VpnType</span><span class="sxs-lookup"><span data-stu-id="36d40-158">-VpnType</span></span>
<span data-ttu-id="36d40-159">Тип виртуальной сети для развертывания ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="36d40-159">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="36d40-160">Допустимые значения</span><span class="sxs-lookup"><span data-stu-id="36d40-160">Valid Values are</span></span> 
- <span data-ttu-id="36d40-161">"Нет" (значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="36d40-161">"None" (Default Value.</span></span> <span data-ttu-id="36d40-162">ApiManagement не является частью какой-либо виртуальной сети.)</span><span class="sxs-lookup"><span data-stu-id="36d40-162">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="36d40-163">"External" (развертывание ApiManagement выполняется в виртуальной сети, у которой есть конечная точка, подключенная к Интернету)</span><span class="sxs-lookup"><span data-stu-id="36d40-163">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="36d40-164">"Internal" (развертывание ApiManagement в виртуальной сети, где есть конечная точка, подключенная к интрасети)</span><span class="sxs-lookup"><span data-stu-id="36d40-164">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

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

### <span data-ttu-id="36d40-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36d40-165">CommonParameters</span></span>
<span data-ttu-id="36d40-166">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="36d40-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36d40-167">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36d40-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36d40-168">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="36d40-168">INPUTS</span></span>

### <span data-ttu-id="36d40-169">System. String</span><span class="sxs-lookup"><span data-stu-id="36d40-169">System.String</span></span>

### <span data-ttu-id="36d40-170">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSku, Microsoft. Azure. Commands. ApiManagement, Version = 6.1.2.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="36d40-170">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.Commands.ApiManagement, Version=6.1.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="36d40-171">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="36d40-171">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="36d40-172">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="36d40-172">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="36d40-173">System. Collections. Generic. Dictionary "2 [[System. String, mscorlib, Version = 4.0.0.0, культура = нейтраль, PublicKeyToken = b77a5c561934e089], [System. String, mscorlib, Version = 4.0.0.0, культура = нейтральная, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="36d40-173">System.Collections.Generic.Dictionary\`2[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089],[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="36d40-174">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion []</span><span class="sxs-lookup"><span data-stu-id="36d40-174">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span></span>

### <span data-ttu-id="36d40-175">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementCustomHostNameConfiguration []</span><span class="sxs-lookup"><span data-stu-id="36d40-175">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span></span>

### <span data-ttu-id="36d40-176">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSystemCertificate []</span><span class="sxs-lookup"><span data-stu-id="36d40-176">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span></span>

## <span data-ttu-id="36d40-177">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="36d40-177">OUTPUTS</span></span>

### <span data-ttu-id="36d40-178">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="36d40-178">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="36d40-179">Пуск</span><span class="sxs-lookup"><span data-stu-id="36d40-179">NOTES</span></span>

## <span data-ttu-id="36d40-180">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36d40-180">RELATED LINKS</span></span>

[<span data-ttu-id="36d40-181">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="36d40-181">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="36d40-182">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="36d40-182">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="36d40-183">Set-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="36d40-183">Set-AzureRmApiManagement</span></span>](./Set-AzureRmApiManagement.md)

[<span data-ttu-id="36d40-184">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="36d40-184">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="36d40-185">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="36d40-185">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


