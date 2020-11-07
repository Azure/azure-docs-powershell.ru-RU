---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
ms.openlocfilehash: 489df2abd46f3ec198422991c2627804f6dc140b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728080"
---
# <span data-ttu-id="535dc-101">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="535dc-101">New-AzApiManagement</span></span>

## <span data-ttu-id="535dc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="535dc-102">SYNOPSIS</span></span>
<span data-ttu-id="535dc-103">Создает развертывание управления API.</span><span class="sxs-lookup"><span data-stu-id="535dc-103">Creates an API Management deployment.</span></span>

## <span data-ttu-id="535dc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="535dc-104">SYNTAX</span></span>

```
New-AzApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>]
 [-CustomHostnameConfiguration <PsApiManagementCustomHostNameConfiguration[]>]
 [-SystemCertificateConfiguration <PsApiManagementSystemCertificate[]>]
 [-SslSetting <PsApiManagementSslSetting>] [-AssignIdentity] [-EnableClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="535dc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="535dc-105">DESCRIPTION</span></span>
<span data-ttu-id="535dc-106">Командлет **New-AzApiManagement** создает развертывание управления API в Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="535dc-106">The **New-AzApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="535dc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="535dc-107">EXAMPLES</span></span>

### <span data-ttu-id="535dc-108">Пример 1: создание службы управления API уровня разработчика</span><span class="sxs-lookup"><span data-stu-id="535dc-108">Example 1: Create a Developer tier API Management service</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="535dc-109">Эта команда создает службу управления API уровня разработчика.</span><span class="sxs-lookup"><span data-stu-id="535dc-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="535dc-110">Команда определяет организацию и адрес администратора.</span><span class="sxs-lookup"><span data-stu-id="535dc-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="535dc-111">В команде не указан параметр *SKU* .</span><span class="sxs-lookup"><span data-stu-id="535dc-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="535dc-112">Таким образом, командлет использует значение по умолчанию для разработчика.</span><span class="sxs-lookup"><span data-stu-id="535dc-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="535dc-113">Пример 2: создание стандартной службы уровня с тремя единицами</span><span class="sxs-lookup"><span data-stu-id="535dc-113">Example 2: Create a Standard tier service that has three units</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="535dc-114">Эта команда создает стандартную службу управления многоуровневой ИНТЕРФЕЙСом с тремя единицами.</span><span class="sxs-lookup"><span data-stu-id="535dc-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="535dc-115">Пример 3: создание услуги уровня потребления</span><span class="sxs-lookup"><span data-stu-id="535dc-115">Example 3: Create a Consumption tier service</span></span>
```powershell
PS D:\github\azure-powershell> New-AzApiManagement -ResourceGroupName Api-Default-North-Europe -Name consumptionskuservice -Location 'West Europe' -Sku Consumption -Organization microsoft -AdminEmail contoso@contoso.com -AssignIdentity -EnableClientCertificate

PublicIPAddresses                     :
PrivateIPAddresses                    :
Id                                    : /subscriptions/subid/resourceGroups/Api-Default-North-Europe/providers/Microsoft.ApiManagement/service/consumptionskuservice
Name                                  : consumptionskuservice
Location                              : West Europe
Sku                                   : Consumption
Capacity                              : 0
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://consumptionskuservice.azure-api.net
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {consumptionskuservice.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity
EnableClientCertificate               : True
ResourceGroupName                     : Api-Default-North-Europe
```

<span data-ttu-id="535dc-116">Эта команда создает службу управления API уровня потребления с сертификатом клиента, который включен в Западная Европа.</span><span class="sxs-lookup"><span data-stu-id="535dc-116">This command creates a consumption tier API Management service with Client Certificate enabled in west Europe.</span></span>

### <span data-ttu-id="535dc-117">Пример 4: создание службы управления API для внешней виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="535dc-117">Example 4: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="535dc-118">Эта команда создает службу управления API высшего уровня в подсети виртуальной сети Azure, имеющей внешнюю доступную конечную точку шлюза с главным регионом в регионе "Западная часть США".</span><span class="sxs-lookup"><span data-stu-id="535dc-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="535dc-119">Пример 5: создание службы управления API для внутренней виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="535dc-119">Example 5: Create an API Management service for an internal virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="535dc-120">Эта команда создает службу управления API высшего уровня в подсети виртуальной сети Azure, которая имеет внутреннюю доступную конечную точку шлюза с главным регионом в регионе "Западная часть США".</span><span class="sxs-lookup"><span data-stu-id="535dc-120">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="535dc-121">Пример 6: создание службы управления API и включение протокола TLS 1,0</span><span class="sxs-lookup"><span data-stu-id="535dc-121">Example 6: Create an API Management service and Enable TLS 1.0 protocol</span></span>
```powershell
PS C:\> $enableTls=@{"Tls10" = "True"}
PS C:\> $sslSetting = New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls
PS C:\> New-AzApiManagement -ResourceGroupName Api-Default-CentralUS -Name "testtlspowershell" -Sku Standard -Location "CentralUS" -Organization "Microsoft" -AdminEmail "bar@contoso.com" -SslSetting $sslSetting

PublicIPAddresses                     : {23.99.140.18}
PrivateIPAddresses                    :
Id                                    : /subscriptions/subid/resourceGroups/Api-Default-CentralUS/providers/Microsoft.ApiManagement/service/testtlspowershell
Name                                  : testtlspowershell
Location                              : Central US
Sku                                   : Standard
Capacity                              : 1
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://testtlspowershell.azure-api.net
RuntimeRegionalUrl                    : https://testtlspowershell-centralus-01.regional.azure-api.net
PortalUrl                             : https://testtlspowershell.portal.azure-api.net
ManagementApiUrl                      : https://testtlspowershell.management.azure-api.net
ScmUrl                                : https://testtlspowershell.scm.azure-api.net
PublisherEmail                        : bar@contoso.com
OrganizationName                      : Microsoft
NotificationSenderEmail               : apimgmt-noreply@mail.windowsazure.com
VirtualNetwork                        :
VpnType                               : None
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {testtlspowershell.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              :
EnableClientCertificate               :
ResourceGroupName                     : Api-Default-CentralUS
```

<span data-ttu-id="535dc-122">Эта команда создает стандартную службу управления КОНФИГУРАЦИей API и включает TLS 1,0 на стороне клиента для ApiManagement шлюза и внутреннего клиента между ApiManagement шлюзом и внутренним сервером.</span><span class="sxs-lookup"><span data-stu-id="535dc-122">This command creates a Standard SKU Api Management service and Enable TLS 1.0 on Frontend client to ApiManagement Gateway and Backend client between ApiManagement Gateway and Backend.</span></span>

## <span data-ttu-id="535dc-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="535dc-123">PARAMETERS</span></span>

### <span data-ttu-id="535dc-124">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="535dc-124">-AdditionalRegions</span></span>
<span data-ttu-id="535dc-125">Дополнительные области развертывания управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="535dc-125">Additional deployment regions of Azure API Management.</span></span>

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

### <span data-ttu-id="535dc-126">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="535dc-126">-AdminEmail</span></span>
<span data-ttu-id="535dc-127">Указывает исходный адрес электронной почты для всех уведомлений, которые отправляет система управления API.</span><span class="sxs-lookup"><span data-stu-id="535dc-127">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="535dc-128">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="535dc-128">-AssignIdentity</span></span>
<span data-ttu-id="535dc-129">Создавайте и назначайте удостоверение Azure Active Directory для этого сервера для использования со службами управления ключами, такими как Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="535dc-129">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="535dc-130">-Capacity</span><span class="sxs-lookup"><span data-stu-id="535dc-130">-Capacity</span></span>
<span data-ttu-id="535dc-131">Указывает емкость SKU службы управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="535dc-131">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="535dc-132">Значение по умолчанию — One (1).</span><span class="sxs-lookup"><span data-stu-id="535dc-132">The default is one (1).</span></span>

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

### <span data-ttu-id="535dc-133">-CustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="535dc-133">-CustomHostnameConfiguration</span></span>
<span data-ttu-id="535dc-134">Пользовательские конфигурации hostname.</span><span class="sxs-lookup"><span data-stu-id="535dc-134">Custom hostname configurations.</span></span> <span data-ttu-id="535dc-135">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="535dc-135">Default value is $null.</span></span> <span data-ttu-id="535dc-136">Передача $null задаст имя HostName по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="535dc-136">Passing $null will set the default hostname.</span></span>

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

### <span data-ttu-id="535dc-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="535dc-137">-DefaultProfile</span></span>
<span data-ttu-id="535dc-138">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="535dc-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="535dc-139">-EnableClientCertificate</span><span class="sxs-lookup"><span data-stu-id="535dc-139">-EnableClientCertificate</span></span>
<span data-ttu-id="535dc-140">Пометка, предназначенная только для использования в качестве услуги ApiManagement SKU за потребление.</span><span class="sxs-lookup"><span data-stu-id="535dc-140">Flag only meant to be used for Consumption SKU ApiManagement Service.</span></span> <span data-ttu-id="535dc-141">Это обеспечивает получение сертификата клиента при каждом запросе на доступ к шлюзу.</span><span class="sxs-lookup"><span data-stu-id="535dc-141">This enforces a client certificate to be presented on each request to the gateway.</span></span> <span data-ttu-id="535dc-142">Это также позволяет проверять подлинность сертификата в политике на шлюзе.</span><span class="sxs-lookup"><span data-stu-id="535dc-142">This also enables the ability to authenticate the certificate in the policy on the gateway.</span></span>

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

### <span data-ttu-id="535dc-143">-Location</span><span class="sxs-lookup"><span data-stu-id="535dc-143">-Location</span></span>
<span data-ttu-id="535dc-144">Указывает расположение для создания службы управления API.</span><span class="sxs-lookup"><span data-stu-id="535dc-144">Specifies the location to create the Api Management service.</span></span>
<span data-ttu-id="535dc-145">Для получения допустимых местоположений используйте командлет Get-AzResourceProvider-ProviderNamespace "Microsoft. ApiManagement" | where {$ _. ResourceTypes [0]. ResourceTypeName-EQ "Service"} | Расположение Select-Object</span><span class="sxs-lookup"><span data-stu-id="535dc-145">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="535dc-146">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="535dc-146">-Name</span></span>
<span data-ttu-id="535dc-147">Указывает имя для развертывания управления API.</span><span class="sxs-lookup"><span data-stu-id="535dc-147">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="535dc-148">-Организация</span><span class="sxs-lookup"><span data-stu-id="535dc-148">-Organization</span></span>
<span data-ttu-id="535dc-149">Указывает название организации.</span><span class="sxs-lookup"><span data-stu-id="535dc-149">Specifies the name of an organization.</span></span>
<span data-ttu-id="535dc-150">Управление API использует этот адрес на портале разработчика в уведомлениях по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="535dc-150">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="535dc-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="535dc-151">-ResourceGroupName</span></span>
<span data-ttu-id="535dc-152">Указывает имя группы ресурсов, в которой этот командлет создает развертывание для управления API.</span><span class="sxs-lookup"><span data-stu-id="535dc-152">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="535dc-153">-SKU</span><span class="sxs-lookup"><span data-stu-id="535dc-153">-Sku</span></span>
<span data-ttu-id="535dc-154">Указывает уровень службы управления API.</span><span class="sxs-lookup"><span data-stu-id="535dc-154">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="535dc-155">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="535dc-155">Valid values are:</span></span> 
- <span data-ttu-id="535dc-156">Программист</span><span class="sxs-lookup"><span data-stu-id="535dc-156">Developer</span></span> 
- <span data-ttu-id="535dc-157">Стандартная</span><span class="sxs-lookup"><span data-stu-id="535dc-157">Standard</span></span> 
- <span data-ttu-id="535dc-158">Premium значение по умолчанию — разработчик.</span><span class="sxs-lookup"><span data-stu-id="535dc-158">Premium The default is Developer.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Basic, Standard, Premium, Consumption

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="535dc-159">-SslSetting</span><span class="sxs-lookup"><span data-stu-id="535dc-159">-SslSetting</span></span>
<span data-ttu-id="535dc-160">Параметр SSL службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="535dc-160">The Ssl Setting of the ApiManagement Service.</span></span> <span data-ttu-id="535dc-161">Значение по умолчанию — $null</span><span class="sxs-lookup"><span data-stu-id="535dc-161">Default value is $null</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="535dc-162">-SystemCertificateConfiguration</span><span class="sxs-lookup"><span data-stu-id="535dc-162">-SystemCertificateConfiguration</span></span>
<span data-ttu-id="535dc-163">Сертификаты, выданные внутренним центром сертификации для установки в службе.</span><span class="sxs-lookup"><span data-stu-id="535dc-163">Certificates issued by Internal CA to be installed on the service.</span></span> <span data-ttu-id="535dc-164">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="535dc-164">Default value is $null.</span></span>

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

### <span data-ttu-id="535dc-165">-Тег</span><span class="sxs-lookup"><span data-stu-id="535dc-165">-Tag</span></span>
<span data-ttu-id="535dc-166">Словарь тегов.</span><span class="sxs-lookup"><span data-stu-id="535dc-166">Tags dictionary.</span></span>

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

### <span data-ttu-id="535dc-167">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="535dc-167">-VirtualNetwork</span></span>
<span data-ttu-id="535dc-168">Конфигурация виртуальной сети для главного региона развертывания управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="535dc-168">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

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

### <span data-ttu-id="535dc-169">-VpnType</span><span class="sxs-lookup"><span data-stu-id="535dc-169">-VpnType</span></span>
<span data-ttu-id="535dc-170">Тип виртуальной сети для развертывания ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="535dc-170">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="535dc-171">Допустимые значения</span><span class="sxs-lookup"><span data-stu-id="535dc-171">Valid Values are</span></span> 
- <span data-ttu-id="535dc-172">"Нет" (значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="535dc-172">"None" (Default Value.</span></span> <span data-ttu-id="535dc-173">ApiManagement не является частью какой-либо виртуальной сети.)</span><span class="sxs-lookup"><span data-stu-id="535dc-173">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="535dc-174">"External" (развертывание ApiManagement выполняется в виртуальной сети, у которой есть конечная точка, подключенная к Интернету)</span><span class="sxs-lookup"><span data-stu-id="535dc-174">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="535dc-175">"Internal" (развертывание ApiManagement в виртуальной сети, где есть конечная точка, подключенная к интрасети)</span><span class="sxs-lookup"><span data-stu-id="535dc-175">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

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

### <span data-ttu-id="535dc-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="535dc-176">CommonParameters</span></span>
<span data-ttu-id="535dc-177">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="535dc-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="535dc-178">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="535dc-178">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="535dc-179">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="535dc-179">INPUTS</span></span>

### <span data-ttu-id="535dc-180">System. String</span><span class="sxs-lookup"><span data-stu-id="535dc-180">System.String</span></span>

### <span data-ttu-id="535dc-181">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSku, Microsoft. Azure. PowerShell. командлеты. ApiManagement, Version = 1.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="535dc-181">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="535dc-182">System. Nullable "1 [[System. Int32, System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="535dc-182">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="535dc-183">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="535dc-183">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="535dc-184">System. Collections. Generic. Dictionary "2 [[System. String, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]; [System. String; System. Private. CoreLib, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="535dc-184">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="535dc-185">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementRegion []</span><span class="sxs-lookup"><span data-stu-id="535dc-185">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span></span>

### <span data-ttu-id="535dc-186">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementCustomHostNameConfiguration []</span><span class="sxs-lookup"><span data-stu-id="535dc-186">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span></span>

### <span data-ttu-id="535dc-187">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementSystemCertificate []</span><span class="sxs-lookup"><span data-stu-id="535dc-187">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span></span>

## <span data-ttu-id="535dc-188">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="535dc-188">OUTPUTS</span></span>

### <span data-ttu-id="535dc-189">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="535dc-189">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="535dc-190">Пуск</span><span class="sxs-lookup"><span data-stu-id="535dc-190">NOTES</span></span>

## <span data-ttu-id="535dc-191">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="535dc-191">RELATED LINKS</span></span>

[<span data-ttu-id="535dc-192">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="535dc-192">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="535dc-193">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="535dc-193">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="535dc-194">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="535dc-194">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)

[<span data-ttu-id="535dc-195">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="535dc-195">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="535dc-196">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="535dc-196">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


