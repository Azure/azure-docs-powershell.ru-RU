---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
ms.openlocfilehash: 43393995fcc370e2b3ff2b20586ab696c39d059b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720126"
---
# <span data-ttu-id="132fa-101">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="132fa-101">New-AzApiManagement</span></span>

## <span data-ttu-id="132fa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="132fa-102">SYNOPSIS</span></span>
<span data-ttu-id="132fa-103">Создает развертывание управления API.</span><span class="sxs-lookup"><span data-stu-id="132fa-103">Creates an API Management deployment.</span></span>

## <span data-ttu-id="132fa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="132fa-104">SYNTAX</span></span>

```
New-AzApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>]
 [-CustomHostnameConfiguration <PsApiManagementCustomHostNameConfiguration[]>]
 [-SystemCertificateConfiguration <PsApiManagementSystemCertificate[]>] [-AssignIdentity]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="132fa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="132fa-105">DESCRIPTION</span></span>
<span data-ttu-id="132fa-106">Командлет **New-AzApiManagement** создает развертывание управления API в Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="132fa-106">The **New-AzApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="132fa-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="132fa-107">EXAMPLES</span></span>

### <span data-ttu-id="132fa-108">Пример 1: создание службы управления API уровня разработчика</span><span class="sxs-lookup"><span data-stu-id="132fa-108">Example 1: Create a Developer tier API Management service</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="132fa-109">Эта команда создает службу управления API уровня разработчика.</span><span class="sxs-lookup"><span data-stu-id="132fa-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="132fa-110">Команда определяет организацию и адрес администратора.</span><span class="sxs-lookup"><span data-stu-id="132fa-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="132fa-111">В команде не указан параметр *SKU* .</span><span class="sxs-lookup"><span data-stu-id="132fa-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="132fa-112">Таким образом, командлет использует значение по умолчанию для разработчика.</span><span class="sxs-lookup"><span data-stu-id="132fa-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="132fa-113">Пример 2: создание стандартной службы уровня с тремя единицами</span><span class="sxs-lookup"><span data-stu-id="132fa-113">Example 2: Create a Standard tier service that has three units</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="132fa-114">Эта команда создает стандартную службу управления многоуровневой ИНТЕРФЕЙСом с тремя единицами.</span><span class="sxs-lookup"><span data-stu-id="132fa-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="132fa-115">Пример 3: создание службы управления API для внешней виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="132fa-115">Example 3: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="132fa-116">Эта команда создает службу управления API высшего уровня в подсети виртуальной сети Azure, имеющей внешнюю доступную конечную точку шлюза с главным регионом в регионе "Западная часть США".</span><span class="sxs-lookup"><span data-stu-id="132fa-116">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="132fa-117">Пример 4: создание службы управления API для внутренней виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="132fa-117">Example 4: Create an API Management service for an internal virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="132fa-118">Эта команда создает службу управления API высшего уровня в подсети виртуальной сети Azure, которая имеет внутреннюю доступную конечную точку шлюза с главным регионом в регионе "Западная часть США".</span><span class="sxs-lookup"><span data-stu-id="132fa-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

## <span data-ttu-id="132fa-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="132fa-119">PARAMETERS</span></span>

### <span data-ttu-id="132fa-120">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="132fa-120">-AdditionalRegions</span></span>
<span data-ttu-id="132fa-121">Дополнительные области развертывания управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="132fa-121">Additional deployment regions of Azure API Management.</span></span>

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

### <span data-ttu-id="132fa-122">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="132fa-122">-AdminEmail</span></span>
<span data-ttu-id="132fa-123">Указывает исходный адрес электронной почты для всех уведомлений, которые отправляет система управления API.</span><span class="sxs-lookup"><span data-stu-id="132fa-123">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="132fa-124">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="132fa-124">-AssignIdentity</span></span>
<span data-ttu-id="132fa-125">Создавайте и назначайте удостоверение Azure Active Directory для этого сервера для использования со службами управления ключами, такими как Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="132fa-125">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="132fa-126">-Capacity</span><span class="sxs-lookup"><span data-stu-id="132fa-126">-Capacity</span></span>
<span data-ttu-id="132fa-127">Указывает емкость SKU службы управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="132fa-127">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="132fa-128">Значение по умолчанию — One (1).</span><span class="sxs-lookup"><span data-stu-id="132fa-128">The default is one (1).</span></span>

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

### <span data-ttu-id="132fa-129">-CustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="132fa-129">-CustomHostnameConfiguration</span></span>
<span data-ttu-id="132fa-130">Пользовательские конфигурации hostname.</span><span class="sxs-lookup"><span data-stu-id="132fa-130">Custom hostname configurations.</span></span> <span data-ttu-id="132fa-131">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="132fa-131">Default value is $null.</span></span> <span data-ttu-id="132fa-132">Передача $null задаст имя HostName по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="132fa-132">Passing $null will set the default hostname.</span></span>

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

### <span data-ttu-id="132fa-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="132fa-133">-DefaultProfile</span></span>
<span data-ttu-id="132fa-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="132fa-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="132fa-135">-Location</span><span class="sxs-lookup"><span data-stu-id="132fa-135">-Location</span></span>
<span data-ttu-id="132fa-136">Указывает расположение для создания службы управления API.</span><span class="sxs-lookup"><span data-stu-id="132fa-136">Specifies the location to create the Api Management service.</span></span>
<span data-ttu-id="132fa-137">Для получения допустимых местоположений используйте командлет Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | where {$ _. ResourceTypes [0]. ResourceTypeName-EQ "Service"} | Расположение Select-Object</span><span class="sxs-lookup"><span data-stu-id="132fa-137">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="132fa-138">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="132fa-138">-Name</span></span>
<span data-ttu-id="132fa-139">Указывает имя для развертывания управления API.</span><span class="sxs-lookup"><span data-stu-id="132fa-139">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="132fa-140">-Организация</span><span class="sxs-lookup"><span data-stu-id="132fa-140">-Organization</span></span>
<span data-ttu-id="132fa-141">Указывает название организации.</span><span class="sxs-lookup"><span data-stu-id="132fa-141">Specifies the name of an organization.</span></span>
<span data-ttu-id="132fa-142">Управление API использует этот адрес на портале разработчика в уведомлениях по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="132fa-142">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="132fa-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="132fa-143">-ResourceGroupName</span></span>
<span data-ttu-id="132fa-144">Указывает имя группы ресурсов, в которой этот командлет создает развертывание для управления API.</span><span class="sxs-lookup"><span data-stu-id="132fa-144">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="132fa-145">-SKU</span><span class="sxs-lookup"><span data-stu-id="132fa-145">-Sku</span></span>
<span data-ttu-id="132fa-146">Указывает уровень службы управления API.</span><span class="sxs-lookup"><span data-stu-id="132fa-146">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="132fa-147">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="132fa-147">Valid values are:</span></span> 
- <span data-ttu-id="132fa-148">Программист</span><span class="sxs-lookup"><span data-stu-id="132fa-148">Developer</span></span> 
- <span data-ttu-id="132fa-149">Стандартная</span><span class="sxs-lookup"><span data-stu-id="132fa-149">Standard</span></span> 
- <span data-ttu-id="132fa-150">Premium значение по умолчанию — разработчик.</span><span class="sxs-lookup"><span data-stu-id="132fa-150">Premium The default is Developer.</span></span>

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

### <span data-ttu-id="132fa-151">-SystemCertificateConfiguration</span><span class="sxs-lookup"><span data-stu-id="132fa-151">-SystemCertificateConfiguration</span></span>
<span data-ttu-id="132fa-152">Сертификаты, выданные внутренним центром сертификации для установки в службе.</span><span class="sxs-lookup"><span data-stu-id="132fa-152">Certificates issued by Internal CA to be installed on the service.</span></span> <span data-ttu-id="132fa-153">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="132fa-153">Default value is $null.</span></span>

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

### <span data-ttu-id="132fa-154">-Тег</span><span class="sxs-lookup"><span data-stu-id="132fa-154">-Tag</span></span>
<span data-ttu-id="132fa-155">Словарь тегов.</span><span class="sxs-lookup"><span data-stu-id="132fa-155">Tags dictionary.</span></span>

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

### <span data-ttu-id="132fa-156">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="132fa-156">-VirtualNetwork</span></span>
<span data-ttu-id="132fa-157">Конфигурация виртуальной сети для главного региона развертывания управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="132fa-157">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

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

### <span data-ttu-id="132fa-158">-VpnType</span><span class="sxs-lookup"><span data-stu-id="132fa-158">-VpnType</span></span>
<span data-ttu-id="132fa-159">Тип виртуальной сети для развертывания ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="132fa-159">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="132fa-160">Допустимые значения</span><span class="sxs-lookup"><span data-stu-id="132fa-160">Valid Values are</span></span> 
- <span data-ttu-id="132fa-161">"Нет" (значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="132fa-161">"None" (Default Value.</span></span> <span data-ttu-id="132fa-162">ApiManagement не является частью какой-либо виртуальной сети.)</span><span class="sxs-lookup"><span data-stu-id="132fa-162">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="132fa-163">"External" (развертывание ApiManagement выполняется в виртуальной сети, у которой есть конечная точка, подключенная к Интернету)</span><span class="sxs-lookup"><span data-stu-id="132fa-163">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="132fa-164">"Internal" (развертывание ApiManagement в виртуальной сети, где есть конечная точка, подключенная к интрасети)</span><span class="sxs-lookup"><span data-stu-id="132fa-164">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

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

### <span data-ttu-id="132fa-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="132fa-165">CommonParameters</span></span>
<span data-ttu-id="132fa-166">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="132fa-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="132fa-167">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="132fa-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="132fa-168">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="132fa-168">INPUTS</span></span>

### <span data-ttu-id="132fa-169">System. String</span><span class="sxs-lookup"><span data-stu-id="132fa-169">System.String</span></span>

### <span data-ttu-id="132fa-170">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSku, Microsoft. Azure. PowerShell. командлеты. ApiManagement, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="132fa-170">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="132fa-171">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="132fa-171">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="132fa-172">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="132fa-172">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="132fa-173">System. Collections. Generic. Dictionary "2 [[System. String, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]; [System. String; System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="132fa-173">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="132fa-174">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion []</span><span class="sxs-lookup"><span data-stu-id="132fa-174">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span></span>

### <span data-ttu-id="132fa-175">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementCustomHostNameConfiguration []</span><span class="sxs-lookup"><span data-stu-id="132fa-175">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span></span>

### <span data-ttu-id="132fa-176">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSystemCertificate []</span><span class="sxs-lookup"><span data-stu-id="132fa-176">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span></span>

## <span data-ttu-id="132fa-177">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="132fa-177">OUTPUTS</span></span>

### <span data-ttu-id="132fa-178">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="132fa-178">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="132fa-179">Пуск</span><span class="sxs-lookup"><span data-stu-id="132fa-179">NOTES</span></span>

## <span data-ttu-id="132fa-180">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="132fa-180">RELATED LINKS</span></span>

[<span data-ttu-id="132fa-181">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="132fa-181">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="132fa-182">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="132fa-182">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="132fa-183">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="132fa-183">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)

[<span data-ttu-id="132fa-184">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="132fa-184">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="132fa-185">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="132fa-185">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


