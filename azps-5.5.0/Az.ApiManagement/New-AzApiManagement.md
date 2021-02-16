---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
ms.openlocfilehash: 32e3bc6419ef94b177a06735654844d09ea04f3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226564"
---
# <span data-ttu-id="0882d-101">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="0882d-101">New-AzApiManagement</span></span>

## <span data-ttu-id="0882d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0882d-102">SYNOPSIS</span></span>
<span data-ttu-id="0882d-103">Создает развертывание управления API.</span><span class="sxs-lookup"><span data-stu-id="0882d-103">Creates an API Management deployment.</span></span>

## <span data-ttu-id="0882d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0882d-104">SYNTAX</span></span>

```
New-AzApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>]
 [-CustomHostnameConfiguration <PsApiManagementCustomHostNameConfiguration[]>]
 [-SystemCertificateConfiguration <PsApiManagementSystemCertificate[]>]
 [-SslSetting <PsApiManagementSslSetting>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String[]>]
 [-EnableClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0882d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0882d-105">DESCRIPTION</span></span>
<span data-ttu-id="0882d-106">С **его использованием** создается развертывание управления API в службе управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="0882d-106">The **New-AzApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="0882d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0882d-107">EXAMPLES</span></span>

### <span data-ttu-id="0882d-108">Пример 1. Создание службы управления API уровня разработчика</span><span class="sxs-lookup"><span data-stu-id="0882d-108">Example 1: Create a Developer tier API Management service</span></span>
```powershell
PS D:\> New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi2" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"


PublicIPAddresses                     : {104.43.240.65}
PrivateIPAddresses                    :
Id                                    : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/ContosoGroup02/providers/Microsoft.ApiManagement/service/ContosoApi2
Name                                  : ContosoApi2
Location                              : Central US
Sku                                   : Developer
Capacity                              : 1
CreatedTimeUtc                        : 2/24/2020 10:34:12 PM
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://contosoapi2.azure-api.net
RuntimeRegionalUrl                    : https://contosoapi2-centralus-01.regional.azure-api.net
PortalUrl                             : https://contosoapi2.portal.azure-api.net
DeveloperPortalUrl                    : https://contosoapi2.developer.azure-api.net
ManagementApiUrl                      : https://contosoapi2.management.azure-api.net
ScmUrl                                : https://contosoapi2.scm.azure-api.net
PublisherEmail                        : admin@contoso.com
OrganizationName                      : Contoso
NotificationSenderEmail               : apimgmt-noreply@mail.windowsazure.com
VirtualNetwork                        :
VpnType                               : None
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {contosoapi2.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              :
EnableClientCertificate               :
ResourceGroupName                     : ContosoGroup02
```

<span data-ttu-id="0882d-109">Эта команда создает службу управления API уровня разработчика.</span><span class="sxs-lookup"><span data-stu-id="0882d-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="0882d-110">Эта команда определяет адрес администратора и организации.</span><span class="sxs-lookup"><span data-stu-id="0882d-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="0882d-111">Эта команда не указывает параметр *SKU.*</span><span class="sxs-lookup"><span data-stu-id="0882d-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="0882d-112">Таким образом, для этого используется стандартное значение Developer.</span><span class="sxs-lookup"><span data-stu-id="0882d-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="0882d-113">Пример 2. Создание стандартной службы уровня с тремя единицами</span><span class="sxs-lookup"><span data-stu-id="0882d-113">Example 2: Create a Standard tier service that has three units</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="0882d-114">Эта команда создает службу управления API стандартного уровня, которая имеет три единицы.</span><span class="sxs-lookup"><span data-stu-id="0882d-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="0882d-115">Пример 3. Создание службы уровня потребления</span><span class="sxs-lookup"><span data-stu-id="0882d-115">Example 3: Create a Consumption tier service</span></span>
```powershell
PS D:\github\azure-powershell> New-AzApiManagement -ResourceGroupName Api-Default-North-Europe -Name consumptionskuservice -Location 'West Europe' -Sku Consumption -Organization microsoft -AdminEmail contoso@contoso.com -SystemAssignedIdentity -EnableClientCertificate

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

<span data-ttu-id="0882d-116">Эта команда создает службу управления API уровня потребления с включенным сертификатом клиента в Западной Европе.</span><span class="sxs-lookup"><span data-stu-id="0882d-116">This command creates a consumption tier API Management service with Client Certificate enabled in west Europe.</span></span>

### <span data-ttu-id="0882d-117">Пример 4. Создание службы управления API для внешней виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="0882d-117">Example 4: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="0882d-118">Эта команда создает службу управления API премиум-уровня в виртуальной сетевой подсети Azure, в которой есть конечная точка внешнего шлюза с эталонным регионом в западной части США.</span><span class="sxs-lookup"><span data-stu-id="0882d-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="0882d-119">Пример 5. Создание службы управления API для внутренней виртуальной сети</span><span class="sxs-lookup"><span data-stu-id="0882d-119">Example 5: Create an API Management service for an internal virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="0882d-120">Эта команда создает службу управления API премиум-уровня в виртуальной подсети Azure, в которой есть конечная точка внутреннего шлюза с эталонным регионом в западной части США.</span><span class="sxs-lookup"><span data-stu-id="0882d-120">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="0882d-121">Пример 6. Создание службы управления API и включить протокол TLS 1.0</span><span class="sxs-lookup"><span data-stu-id="0882d-121">Example 6: Create an API Management service and Enable TLS 1.0 protocol</span></span>
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

<span data-ttu-id="0882d-122">Эта команда создает стандартную службу управления API SKU и включает TLS 1.0 в клиенте Frontend для шлюза ApiManagement и обратного клиента между ApiManagement Gateway и Backend.</span><span class="sxs-lookup"><span data-stu-id="0882d-122">This command creates a Standard SKU Api Management service and Enable TLS 1.0 on Frontend client to ApiManagement Gateway and Backend client between ApiManagement Gateway and Backend.</span></span>

## <span data-ttu-id="0882d-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0882d-123">PARAMETERS</span></span>

### <span data-ttu-id="0882d-124">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="0882d-124">-AdditionalRegions</span></span>
<span data-ttu-id="0882d-125">Дополнительные регионы развертывания управления Azure API.</span><span class="sxs-lookup"><span data-stu-id="0882d-125">Additional deployment regions of Azure API Management.</span></span>

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

### <span data-ttu-id="0882d-126">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="0882d-126">-AdminEmail</span></span>
<span data-ttu-id="0882d-127">Указывает почтовый адрес всех уведомлений, отправляемых системой управления API.</span><span class="sxs-lookup"><span data-stu-id="0882d-127">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="0882d-128">-Capacity</span><span class="sxs-lookup"><span data-stu-id="0882d-128">-Capacity</span></span>
<span data-ttu-id="0882d-129">Определяет емкость SKU службы управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="0882d-129">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="0882d-130">Значение по умолчанию — 1(1).</span><span class="sxs-lookup"><span data-stu-id="0882d-130">The default is one (1).</span></span>

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

### <span data-ttu-id="0882d-131">-CustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="0882d-131">-CustomHostnameConfiguration</span></span>
<span data-ttu-id="0882d-132">Настраиваемые конфигурации имен хостов.</span><span class="sxs-lookup"><span data-stu-id="0882d-132">Custom hostname configurations.</span></span> <span data-ttu-id="0882d-133">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="0882d-133">Default value is $null.</span></span> <span data-ttu-id="0882d-134">При $null будет установлено имя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0882d-134">Passing $null will set the default hostname.</span></span>

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

### <span data-ttu-id="0882d-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0882d-135">-DefaultProfile</span></span>
<span data-ttu-id="0882d-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0882d-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0882d-137">-EnableClientCertificate</span><span class="sxs-lookup"><span data-stu-id="0882d-137">-EnableClientCertificate</span></span>
<span data-ttu-id="0882d-138">Флаг предназначен только для службы ApiManagement Service для потребления.</span><span class="sxs-lookup"><span data-stu-id="0882d-138">Flag only meant to be used for Consumption SKU ApiManagement Service.</span></span> <span data-ttu-id="0882d-139">При этом для каждого запроса шлюзу будет выдан сертификат клиента.</span><span class="sxs-lookup"><span data-stu-id="0882d-139">This enforces a client certificate to be presented on each request to the gateway.</span></span> <span data-ttu-id="0882d-140">Это также позволяет проверить подлинность сертификата в политике на шлюзе.</span><span class="sxs-lookup"><span data-stu-id="0882d-140">This also enables the ability to authenticate the certificate in the policy on the gateway.</span></span>

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

### <span data-ttu-id="0882d-141">-Location</span><span class="sxs-lookup"><span data-stu-id="0882d-141">-Location</span></span>
<span data-ttu-id="0882d-142">Указывает расположение для создания службы управления API.</span><span class="sxs-lookup"><span data-stu-id="0882d-142">Specifies the location to create the Api Management service.</span></span>
<span data-ttu-id="0882d-143">Чтобы получить допустимые расположения, используйте Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | где {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object Расположения</span><span class="sxs-lookup"><span data-stu-id="0882d-143">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="0882d-144">-Name</span><span class="sxs-lookup"><span data-stu-id="0882d-144">-Name</span></span>
<span data-ttu-id="0882d-145">Указывает имя развертывания управления API.</span><span class="sxs-lookup"><span data-stu-id="0882d-145">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="0882d-146">-Организация</span><span class="sxs-lookup"><span data-stu-id="0882d-146">-Organization</span></span>
<span data-ttu-id="0882d-147">Указывает имя организации.</span><span class="sxs-lookup"><span data-stu-id="0882d-147">Specifies the name of an organization.</span></span>
<span data-ttu-id="0882d-148">Для управления API этот адрес используется на портале разработчика в уведомлениях по электронной почте.</span><span class="sxs-lookup"><span data-stu-id="0882d-148">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="0882d-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0882d-149">-ResourceGroupName</span></span>
<span data-ttu-id="0882d-150">Имя группы ресурсов, для которой этот cmdlet создает развертывание управления API.</span><span class="sxs-lookup"><span data-stu-id="0882d-150">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="0882d-151">-SKU</span><span class="sxs-lookup"><span data-stu-id="0882d-151">-Sku</span></span>
<span data-ttu-id="0882d-152">Определяет уровень службы управления API.</span><span class="sxs-lookup"><span data-stu-id="0882d-152">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="0882d-153">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="0882d-153">Valid values are:</span></span> 
- <span data-ttu-id="0882d-154">Разработчик</span><span class="sxs-lookup"><span data-stu-id="0882d-154">Developer</span></span> 
- <span data-ttu-id="0882d-155">Стандартный</span><span class="sxs-lookup"><span data-stu-id="0882d-155">Standard</span></span> 
- <span data-ttu-id="0882d-156">Premium по умолчанию — "Разработчик".</span><span class="sxs-lookup"><span data-stu-id="0882d-156">Premium The default is Developer.</span></span>

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

### <span data-ttu-id="0882d-157">-SslSetting</span><span class="sxs-lookup"><span data-stu-id="0882d-157">-SslSetting</span></span>
<span data-ttu-id="0882d-158">Параметр SSL службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="0882d-158">The Ssl Setting of the ApiManagement Service.</span></span> <span data-ttu-id="0882d-159">Значение по умолчанию — $null</span><span class="sxs-lookup"><span data-stu-id="0882d-159">Default value is $null</span></span>

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

### <span data-ttu-id="0882d-160">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="0882d-160">-SystemAssignedIdentity</span></span>
<span data-ttu-id="0882d-161">Создание и назначение удостоверения Azure Active Directory для этого сервера для использования с ключевыми службами управления, например Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="0882d-161">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="0882d-162">-SystemCertificateConfiguration</span><span class="sxs-lookup"><span data-stu-id="0882d-162">-SystemCertificateConfiguration</span></span>
<span data-ttu-id="0882d-163">Сертификаты, выданные внутренним ЦС, для установки в службе.</span><span class="sxs-lookup"><span data-stu-id="0882d-163">Certificates issued by Internal CA to be installed on the service.</span></span> <span data-ttu-id="0882d-164">Значение по умолчанию — $null.</span><span class="sxs-lookup"><span data-stu-id="0882d-164">Default value is $null.</span></span>

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

### <span data-ttu-id="0882d-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="0882d-165">-Tag</span></span>
<span data-ttu-id="0882d-166">Словарь тегов.</span><span class="sxs-lookup"><span data-stu-id="0882d-166">Tags dictionary.</span></span>

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

### <span data-ttu-id="0882d-167">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="0882d-167">-UserAssignedIdentity</span></span>
<span data-ttu-id="0882d-168">Назначьте этим серверам удостоверения пользователей для использования с ключевыми службами управления, например Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="0882d-168">Assign User Identities to this server for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0882d-169">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0882d-169">-VirtualNetwork</span></span>
<span data-ttu-id="0882d-170">Виртуальная конфигурация сети для master Azure API Management deployment region.</span><span class="sxs-lookup"><span data-stu-id="0882d-170">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

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

### <span data-ttu-id="0882d-171">-VpnType</span><span class="sxs-lookup"><span data-stu-id="0882d-171">-VpnType</span></span>
<span data-ttu-id="0882d-172">Виртуальный тип сети развертывания ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="0882d-172">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="0882d-173">Допустимые значения</span><span class="sxs-lookup"><span data-stu-id="0882d-173">Valid Values are</span></span> 
- <span data-ttu-id="0882d-174">"Нет" (значение по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="0882d-174">"None" (Default Value.</span></span> <span data-ttu-id="0882d-175">ApiManagement не является частью любой виртуальной сети")</span><span class="sxs-lookup"><span data-stu-id="0882d-175">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="0882d-176">"Внешняя" (развертывание ApiManagement настроено в виртуальной сети с конечной точкой для подключения к Интернету)</span><span class="sxs-lookup"><span data-stu-id="0882d-176">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="0882d-177">"Внутренняя" (развертывание ApiManagement настроено в виртуальной сети, в которой есть конечная точка интрасети)</span><span class="sxs-lookup"><span data-stu-id="0882d-177">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

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

### <span data-ttu-id="0882d-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0882d-178">CommonParameters</span></span>
<span data-ttu-id="0882d-179">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0882d-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0882d-180">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0882d-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0882d-181">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0882d-181">INPUTS</span></span>

### <span data-ttu-id="0882d-182">System.String</span><span class="sxs-lookup"><span data-stu-id="0882d-182">System.String</span></span>

### <span data-ttu-id="0882d-183">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="0882d-183">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="0882d-184">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0882d-184">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0882d-185">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0882d-185">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="0882d-186">System.Collections.Generic.Dictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0882d-186">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0882d-187">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span><span class="sxs-lookup"><span data-stu-id="0882d-187">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span></span>

### <span data-ttu-id="0882d-188">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="0882d-188">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span></span>

### <span data-ttu-id="0882d-189">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span><span class="sxs-lookup"><span data-stu-id="0882d-189">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span></span>

## <span data-ttu-id="0882d-190">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0882d-190">OUTPUTS</span></span>

### <span data-ttu-id="0882d-191">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="0882d-191">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="0882d-192">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0882d-192">NOTES</span></span>

## <span data-ttu-id="0882d-193">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0882d-193">RELATED LINKS</span></span>

[<span data-ttu-id="0882d-194">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="0882d-194">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="0882d-195">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="0882d-195">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="0882d-196">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="0882d-196">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)

[<span data-ttu-id="0882d-197">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="0882d-197">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="0882d-198">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="0882d-198">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


