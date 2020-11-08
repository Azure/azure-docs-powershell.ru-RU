---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagement.md
ms.openlocfilehash: 901022972e6069d616e066a07dd8bedc536fafb2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073874"
---
# <span data-ttu-id="61166-101">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="61166-101">Set-AzApiManagement</span></span>

## <span data-ttu-id="61166-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="61166-102">SYNOPSIS</span></span>
<span data-ttu-id="61166-103">Обновляет службу управления API Azure</span><span class="sxs-lookup"><span data-stu-id="61166-103">Updates an Azure Api Management service</span></span>

## <span data-ttu-id="61166-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="61166-104">SYNTAX</span></span>

```
Set-AzApiManagement -InputObject <PsApiManagement> [-AssignIdentity] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61166-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61166-105">DESCRIPTION</span></span>

<span data-ttu-id="61166-106">Командлет **Set-AzApiManagement** обновляет службу управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="61166-106">The **Set-AzApiManagement** cmdlet updates an Azure API Management service.</span></span>

## <span data-ttu-id="61166-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="61166-107">EXAMPLES</span></span>

### <span data-ttu-id="61166-108">Пример 1. получите службу управления API и масштабируйте ее на Premium и добавьте регион.</span><span class="sxs-lookup"><span data-stu-id="61166-108">Example 1 Get an API Management service and scale it to Premium and Add a region</span></span>
```powershell
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.Sku = "Premium"
PS C:\> $apim.Capacity = 5
PS C:\> $apim.AddRegion("Central US", "Premium", 3)
PS C:\>Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="61166-109">В этом примере выполняется получение экземпляра управления API, масштабируется до пяти единиц измерения Premium, а затем в привилегированную область добавляются дополнительные три устройства.</span><span class="sxs-lookup"><span data-stu-id="61166-109">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="61166-110">Пример 2: развертывание обновления (внешняя виртуальная сеть)</span><span class="sxs-lookup"><span data-stu-id="61166-110">Example 2: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="61166-111">Эта команда обновляет существующее развертывание управления API и присоединяется к внешнему *VpnType*.</span><span class="sxs-lookup"><span data-stu-id="61166-111">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="61166-112">Пример 3: создание и инициализация экземпляра PsApiManagementCustomHostNameConfiguration с использованием секретного ключа из KeyVault ресурсов</span><span class="sxs-lookup"><span data-stu-id="61166-112">Example 3: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"
PS C:\>$proxy1 = New-AzApiManagementCustomHostnameConfiguration -Hostname "gatewayl.contoso.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/contoso-proxy-custom-ssl.pfx"
PS C:\>$proxy2 = New-AzApiManagementCustomHostnameConfiguration -Hostname "gatewayl.foobar.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/foobar-proxy-custom-ssl.pfx"
PS C:\>$proxyCustomConfig = @($proxy1,$proxy2)
PS C:\>$apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\>$apim.PortalCustomHostnameConfiguration = $portal
PS C:\>$apim.ProxyCustomHostnameConfiguration = $proxyCustomConfig 
PS C:\>Set-AzApiManagement -InputObject $apim -AssignIdentity
```

### <span data-ttu-id="61166-113">Пример 4: обновление электронной почты издателя, NotificationSender электронной почты и названия организации</span><span class="sxs-lookup"><span data-stu-id="61166-113">Example 4: Update Publisher Email, NotificationSender Email and Organization Name</span></span>
```powershell
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "api-Default-West-US" -Name "Contoso"
PS C:\> $apim.PublisherEmail = "foobar@contoso.com"
PS C:\> $apim.NotificationSenderEmail = "notification@contoso.com"
PS C:\> $apim.OrganizationName = "Contoso"
PS C:\> Set-AzApiManagement -InputObject $apim -PassThru
```

## <span data-ttu-id="61166-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="61166-114">PARAMETERS</span></span>

### <span data-ttu-id="61166-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61166-115">-AsJob</span></span>
<span data-ttu-id="61166-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="61166-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="61166-117">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="61166-117">-AssignIdentity</span></span>
<span data-ttu-id="61166-118">Создавайте и назначайте удостоверение Azure Active Directory для этого сервера для использования со службами управления ключами, такими как Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="61166-118">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="61166-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61166-119">-DefaultProfile</span></span>
<span data-ttu-id="61166-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="61166-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61166-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61166-121">-InputObject</span></span>
<span data-ttu-id="61166-122">Экземпляр ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="61166-122">The ApiManagement instance.</span></span>

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

### <span data-ttu-id="61166-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61166-123">-PassThru</span></span>
<span data-ttu-id="61166-124">Отправляет обновленный PsApiManagement в конвейер, если операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="61166-124">Sends updated PsApiManagement to pipeline if operation succeeds.</span></span>

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

### <span data-ttu-id="61166-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61166-125">-Confirm</span></span>
<span data-ttu-id="61166-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="61166-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61166-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61166-127">-WhatIf</span></span>
<span data-ttu-id="61166-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="61166-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="61166-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="61166-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61166-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61166-130">CommonParameters</span></span>
<span data-ttu-id="61166-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="61166-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61166-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="61166-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61166-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="61166-133">INPUTS</span></span>

### <span data-ttu-id="61166-134">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="61166-134">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="61166-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="61166-135">OUTPUTS</span></span>

### <span data-ttu-id="61166-136">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="61166-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="61166-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="61166-137">NOTES</span></span>

## <span data-ttu-id="61166-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61166-138">RELATED LINKS</span></span>

[<span data-ttu-id="61166-139">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="61166-139">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="61166-140">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="61166-140">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="61166-141">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="61166-141">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)
