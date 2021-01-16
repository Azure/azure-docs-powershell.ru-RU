---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagement.md
ms.openlocfilehash: c00e8e8d33ef0f7b7b2591287e9bda9bc876e3c0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98423279"
---
# <span data-ttu-id="ce906-101">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ce906-101">Set-AzApiManagement</span></span>

## <span data-ttu-id="ce906-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce906-102">SYNOPSIS</span></span>
<span data-ttu-id="ce906-103">Обновление службы управления Azure Api</span><span class="sxs-lookup"><span data-stu-id="ce906-103">Updates an Azure Api Management service</span></span>

## <span data-ttu-id="ce906-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ce906-104">SYNTAX</span></span>

```
Set-AzApiManagement -InputObject <PsApiManagement> [-SystemAssignedIdentity] [-UserAssignedIdentity <String[]>]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce906-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce906-105">DESCRIPTION</span></span>

<span data-ttu-id="ce906-106">**Cmdlet Set-AzApiManagement** обновляет службу управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="ce906-106">The **Set-AzApiManagement** cmdlet updates an Azure API Management service.</span></span>

## <span data-ttu-id="ce906-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ce906-107">EXAMPLES</span></span>

### <span data-ttu-id="ce906-108">Пример 1. Получите службу управления API и в масштабе до уровня "Премиум" и добавьте регион</span><span class="sxs-lookup"><span data-stu-id="ce906-108">Example 1: Get an API Management service and scale it to Premium and Add a region</span></span>
```powershell
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.Sku = "Premium"
PS C:\> $apim.Capacity = 5
PS C:\> $apim.AddRegion("Central US", "Premium", 3)
PS C:\>Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="ce906-109">В этом примере мы наберем экземпляр управления Api, который масштабировать до пяти единиц премиум-класса, а затем добавляет дополнительные три единицы в этот регион.</span><span class="sxs-lookup"><span data-stu-id="ce906-109">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="ce906-110">Пример 2. Развертывание обновления (внешняя VNET)</span><span class="sxs-lookup"><span data-stu-id="ce906-110">Example 2: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="ce906-111">Эта команда обновляет существующее развертывание управления API и присоединяется к *внешнему VPNType.*</span><span class="sxs-lookup"><span data-stu-id="ce906-111">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="ce906-112">Пример 3. Создание и инициализация экземпляра PsApiManagementCustomHostNameConfiguration с помощью секретного ресурса KeyVault</span><span class="sxs-lookup"><span data-stu-id="ce906-112">Example 3: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"
PS C:\>$proxy1 = New-AzApiManagementCustomHostnameConfiguration -Hostname "gatewayl.contoso.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/contoso-proxy-custom-ssl.pfx"
PS C:\>$proxy2 = New-AzApiManagementCustomHostnameConfiguration -Hostname "gatewayl.foobar.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/foobar-proxy-custom-ssl.pfx"
PS C:\>$proxyCustomConfig = @($proxy1,$proxy2)
PS C:\>$apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\>$apim.PortalCustomHostnameConfiguration = $portal
PS C:\>$apim.ProxyCustomHostnameConfiguration = $proxyCustomConfig 
PS C:\>Set-AzApiManagement -InputObject $apim -SystemAssignedIdentity
```

### <span data-ttu-id="ce906-113">Пример 4. Обновление электронной почты Publisher, адреса электронной почты с уведомлением и названия организации</span><span class="sxs-lookup"><span data-stu-id="ce906-113">Example 4: Update Publisher Email, NotificationSender Email and Organization Name</span></span>
```powershell
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "api-Default-West-US" -Name "Contoso"
PS C:\> $apim.PublisherEmail = "foobar@contoso.com"
PS C:\> $apim.NotificationSenderEmail = "notification@contoso.com"
PS C:\> $apim.OrganizationName = "Contoso"
PS C:\> Set-AzApiManagement -InputObject $apim -PassThru
```

## <span data-ttu-id="ce906-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce906-114">PARAMETERS</span></span>

### <span data-ttu-id="ce906-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce906-115">-AsJob</span></span>
<span data-ttu-id="ce906-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ce906-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ce906-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce906-117">-DefaultProfile</span></span>
<span data-ttu-id="ce906-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ce906-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce906-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce906-119">-InputObject</span></span>
<span data-ttu-id="ce906-120">Экземпляр ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="ce906-120">The ApiManagement instance.</span></span>

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

### <span data-ttu-id="ce906-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce906-121">-PassThru</span></span>
<span data-ttu-id="ce906-122">Отправляет обновленную службу PsApiManagement для конвейера в случае успешного выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="ce906-122">Sends updated PsApiManagement to pipeline if operation succeeds.</span></span>

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

### <span data-ttu-id="ce906-123">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ce906-123">-SystemAssignedIdentity</span></span>
<span data-ttu-id="ce906-124">Создание и назначение удостоверения Azure Active Directory для этого сервера для использования с ключевыми службами управления, например Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="ce906-124">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="ce906-125">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ce906-125">-UserAssignedIdentity</span></span>
<span data-ttu-id="ce906-126">Назначьте этим серверам удостоверения пользователей для использования с ключевыми службами управления, например Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="ce906-126">Assign User Identities to this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="ce906-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce906-127">-Confirm</span></span>
<span data-ttu-id="ce906-128">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce906-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce906-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce906-129">-WhatIf</span></span>
<span data-ttu-id="ce906-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce906-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ce906-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ce906-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce906-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce906-132">CommonParameters</span></span>
<span data-ttu-id="ce906-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce906-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce906-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ce906-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce906-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ce906-135">INPUTS</span></span>

### <span data-ttu-id="ce906-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="ce906-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="ce906-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ce906-137">OUTPUTS</span></span>

### <span data-ttu-id="ce906-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="ce906-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="ce906-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ce906-139">NOTES</span></span>

## <span data-ttu-id="ce906-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ce906-140">RELATED LINKS</span></span>

[<span data-ttu-id="ce906-141">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ce906-141">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="ce906-142">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ce906-142">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="ce906-143">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ce906-143">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)
