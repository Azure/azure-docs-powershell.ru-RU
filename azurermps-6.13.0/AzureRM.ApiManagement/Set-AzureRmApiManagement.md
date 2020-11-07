---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagement.md
ms.openlocfilehash: 3831be3072f6922ad986cbde5a0a800764d1656a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733499"
---
# <span data-ttu-id="9c4f8-101">Set-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="9c4f8-101">Set-AzureRmApiManagement</span></span>

## <span data-ttu-id="9c4f8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9c4f8-102">SYNOPSIS</span></span>
<span data-ttu-id="9c4f8-103">Обновляет службу управления API Azure</span><span class="sxs-lookup"><span data-stu-id="9c4f8-103">Updates an Azure Api Management service</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c4f8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9c4f8-104">SYNTAX</span></span>

```
Set-AzureRmApiManagement -InputObject <PsApiManagement> [-AssignIdentity] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c4f8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c4f8-105">DESCRIPTION</span></span>

<span data-ttu-id="9c4f8-106">Командлет **Set-AzureRmApiManagement** обновляет службу управления API Azure.</span><span class="sxs-lookup"><span data-stu-id="9c4f8-106">The **Set-AzureRmApiManagement** cmdlet updates an Azure API Management service.</span></span>

## <span data-ttu-id="9c4f8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9c4f8-107">EXAMPLES</span></span>

### <span data-ttu-id="9c4f8-108">Пример 1. получите службу управления API и масштабируйте ее на Premium и добавьте регион.</span><span class="sxs-lookup"><span data-stu-id="9c4f8-108">Example 1 Get an API Management service and scale it to Premium and Add a region</span></span>
```powershell
PS C:\> $apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.Sku = "Premium"
PS C:\> $apim.Capacity = 5
PS C:\> $apim.AddRegion("Central US", "Premium", 3)
PS C:\>Set-AzureRmApiManagement -ApiManagement $apim
```

<span data-ttu-id="9c4f8-109">В этом примере выполняется получение экземпляра управления API, масштабируется до пяти единиц измерения Premium, а затем в привилегированную область добавляются дополнительные три устройства.</span><span class="sxs-lookup"><span data-stu-id="9c4f8-109">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="9c4f8-110">Пример 2: развертывание обновления (внешняя виртуальная сеть)</span><span class="sxs-lookup"><span data-stu-id="9c4f8-110">Example 2: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzureRmApiManagement -ApiManagement $apim
```

<span data-ttu-id="9c4f8-111">Эта команда обновляет существующее развертывание управления API и присоединяется к внешнему *VpnType*.</span><span class="sxs-lookup"><span data-stu-id="9c4f8-111">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="9c4f8-112">Пример 3: создание и инициализация экземпляра PsApiManagementCustomHostNameConfiguration с использованием секретного ключа из KeyVault ресурсов</span><span class="sxs-lookup"><span data-stu-id="9c4f8-112">Example 3: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"
PS C:\>$proxy1 = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "gatewayl.contoso.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/contoso-proxy-custom-ssl.pfx"
PS C:\>$proxy2 = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "gatewayl.foobar.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/foobar-proxy-custom-ssl.pfx"
PS C:\>$proxyCustomConfig = @($proxy1,$proxy2)
PS C:\>$apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\>$apim.PortalCustomHostnameConfiguration = $portal
PS C:\>$apim.ProxyCustomHostnameConfiguration = $proxyCustomConfig 
PS C:\>Set-AzureRmApiManagement -InputObject $apim -AssignIdentity
```

## <span data-ttu-id="9c4f8-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9c4f8-113">PARAMETERS</span></span>

### <span data-ttu-id="9c4f8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c4f8-114">-AsJob</span></span>
<span data-ttu-id="9c4f8-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9c4f8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9c4f8-116">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="9c4f8-116">-AssignIdentity</span></span>
<span data-ttu-id="9c4f8-117">Создавайте и назначайте удостоверение Azure Active Directory для этого сервера для использования со службами управления ключами, такими как Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="9c4f8-117">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="9c4f8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c4f8-118">-DefaultProfile</span></span>
<span data-ttu-id="9c4f8-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9c4f8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c4f8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c4f8-120">-InputObject</span></span>
<span data-ttu-id="9c4f8-121">Экземпляр ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="9c4f8-121">The ApiManagement instance.</span></span>

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

### <span data-ttu-id="9c4f8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c4f8-122">-PassThru</span></span>
<span data-ttu-id="9c4f8-123">Отправляет обновленный PsApiManagement в конвейер, если операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="9c4f8-123">Sends updated PsApiManagement to pipeline if operation succeeds.</span></span>

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

### <span data-ttu-id="9c4f8-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c4f8-124">-Confirm</span></span>
<span data-ttu-id="9c4f8-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9c4f8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c4f8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c4f8-126">-WhatIf</span></span>
<span data-ttu-id="9c4f8-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9c4f8-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c4f8-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9c4f8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c4f8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c4f8-129">CommonParameters</span></span>
<span data-ttu-id="9c4f8-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9c4f8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c4f8-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c4f8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c4f8-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9c4f8-132">INPUTS</span></span>

### <span data-ttu-id="9c4f8-133">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="9c4f8-133">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="9c4f8-134">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9c4f8-134">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="9c4f8-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c4f8-135">OUTPUTS</span></span>

### <span data-ttu-id="9c4f8-136">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="9c4f8-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="9c4f8-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="9c4f8-137">NOTES</span></span>

## <span data-ttu-id="9c4f8-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c4f8-138">RELATED LINKS</span></span>

[<span data-ttu-id="9c4f8-139">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="9c4f8-139">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="9c4f8-140">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="9c4f8-140">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="9c4f8-141">Remove-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="9c4f8-141">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)
