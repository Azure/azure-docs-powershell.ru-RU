---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
ms.openlocfilehash: 8897b2e1175c82f3dcc25642dec920a4b6d7343c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244769"
---
# <span data-ttu-id="a95ea-101">Update-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a95ea-101">Update-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="a95ea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a95ea-102">SYNOPSIS</span></span>
<span data-ttu-id="a95ea-103">Обновление существующего VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a95ea-103">Updates an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="a95ea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a95ea-104">SYNTAX</span></span>

### <span data-ttu-id="a95ea-105">ByVpnServerConfigurationNameByCertificateAuthentication (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a95ea-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a95ea-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="a95ea-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a95ea-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="a95ea-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a95ea-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="a95ea-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a95ea-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="a95ea-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a95ea-110">ByVpnServerConfigurationObjectByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="a95ea-110">ByVpnServerConfigurationObjectByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a95ea-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="a95ea-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a95ea-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="a95ea-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a95ea-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="a95ea-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a95ea-114">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a95ea-114">DESCRIPTION</span></span>
<span data-ttu-id="a95ea-115">С помощью командлета **Update-AzVpnServerConfiguration** можно обновить существующий VpnServerConfiguration с разными VpnProtocols, VpnAuthenticationTypes, IpsecPolicies и настроить выбранные параметры проверки подлинности VPN в соответствии с требованием клиента для указания на подключение к сайту.</span><span class="sxs-lookup"><span data-stu-id="a95ea-115">The **Update-AzVpnServerConfiguration** cmdlet enables you to update the existing VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="a95ea-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a95ea-116">EXAMPLES</span></span>

### <span data-ttu-id="a95ea-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a95ea-117">Example 1</span></span>
```powershell
PS C:\> Update-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -VpnProtocol IkeV2

PS C:\> New-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -VpnProtocol IkeV2 -VpnAuthenticationType Certificate -VpnClientRootCertificateFilesList $listOfCerts -VpnClientRevokedCertificateFilesList $listOfCerts -Location "westus"
ResourceGroupName            : P2SCortexGATesting
Name                         : test1config
Id                           : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/test1config
Location                     : westus
VpnProtocols                 : {IkeV2}
VpnAuthenticationTypes       : {Certificate}
VpnClientRootCertificates    :
VpnClientRevokedCertificates : [
                                 {
                                   "Name": "cert2",
                                   "Thumbprint": "83FFBFC8848B5A5836C94D0112367E16148A286F"
                                 }
                               ]
RadiusServerAddress          :
RadiusServerRootCertificates : []
RadiusClientRootCertificates : []
VpnClientIpsecPolicies       : []
AadAuthenticationParameters  : null
P2sVpnGateways               : []
Type                         : Microsoft.Network/vpnServerConfigurations
ProvisioningState            : Succeeded
```

<span data-ttu-id="a95ea-118">Команда, описанная выше, будет обновлять существующий VpnServerConfiguration с VpnProtocol в качестве IkeV2.</span><span class="sxs-lookup"><span data-stu-id="a95ea-118">The above command will update an existing VpnServerConfiguration with VpnProtocol as IkeV2.</span></span>

## <span data-ttu-id="a95ea-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a95ea-119">PARAMETERS</span></span>

### <span data-ttu-id="a95ea-120">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="a95ea-120">-AadAudience</span></span>
<span data-ttu-id="a95ea-121">Аудитория AAD для проверки подлинности в P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="a95ea-121">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95ea-122">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="a95ea-122">-AadIssuer</span></span>
<span data-ttu-id="a95ea-123">Поставщик AAD для проверки подлинности в P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="a95ea-123">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95ea-124">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="a95ea-124">-AadTenant</span></span>
<span data-ttu-id="a95ea-125">Клиент AAD для проверки подлинности в P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="a95ea-125">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication, ByVpnServerConfigurationObjectByAadAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95ea-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a95ea-126">-AsJob</span></span>
<span data-ttu-id="a95ea-127">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a95ea-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a95ea-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a95ea-128">-DefaultProfile</span></span>
<span data-ttu-id="a95ea-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a95ea-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a95ea-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a95ea-130">-InputObject</span></span>
<span data-ttu-id="a95ea-131">Изменяемый объект конфигурации VPN-сервера</span><span class="sxs-lookup"><span data-stu-id="a95ea-131">The vpn server configuration object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationObjectByAadAuthentication
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a95ea-132">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a95ea-132">-Name</span></span>
<span data-ttu-id="a95ea-133">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="a95ea-133">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationNameByAadAuthentication
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95ea-134">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="a95ea-134">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="a95ea-135">Список путей к файлам RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a95ea-135">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95ea-136">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="a95ea-136">-RadiusServerAddress</span></span>
<span data-ttu-id="a95ea-137">Адрес внешнего RADIUS-сервера P2S.</span><span class="sxs-lookup"><span data-stu-id="a95ea-137">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95ea-138">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="a95ea-138">-RadiusServerList</span></span>
<span data-ttu-id="a95ea-139">P2S внешние множественные RADIUS-серверы.</span><span class="sxs-lookup"><span data-stu-id="a95ea-139">P2S External multiple radius servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95ea-140">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="a95ea-140">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="a95ea-141">Список путей к файлам RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="a95ea-141">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95ea-142">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="a95ea-142">-RadiusServerSecret</span></span>
<span data-ttu-id="a95ea-143">Секретный P2S внешнего RADIUS-сервера.</span><span class="sxs-lookup"><span data-stu-id="a95ea-143">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationObjectByRadiusAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95ea-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a95ea-144">-ResourceGroupName</span></span>
<span data-ttu-id="a95ea-145">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a95ea-145">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationNameByRadiusAuthentication, ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95ea-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a95ea-146">-ResourceId</span></span>
<span data-ttu-id="a95ea-147">Идентификатор ресурса Azure для конфигурации VPN-сервера.</span><span class="sxs-lookup"><span data-stu-id="a95ea-147">The Azure resource ID for the vpn server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationResourceIdByCertificateAuthentication, ByVpnServerConfigurationResourceIdByRadiusAuthentication, ByVpnServerConfigurationResourceIdByAadAuthentication
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a95ea-148">-Тег</span><span class="sxs-lookup"><span data-stu-id="a95ea-148">-Tag</span></span>
<span data-ttu-id="a95ea-149">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a95ea-149">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95ea-150">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="a95ea-150">-VpnAuthenticationType</span></span>
<span data-ttu-id="a95ea-151">Список туннельных протоколов клиента VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="a95ea-151">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Certificate, Radius, AAD

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95ea-152">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="a95ea-152">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="a95ea-153">Список политик IPSec для VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="a95ea-153">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a95ea-154">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="a95ea-154">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="a95ea-155">Список VpnClientCertificates, по которым будут отменяться пути к файлам</span><span class="sxs-lookup"><span data-stu-id="a95ea-155">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationResourceIdByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95ea-156">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="a95ea-156">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="a95ea-157">Список VpnClientRootCertificates, в который нужно добавить пути к файлам</span><span class="sxs-lookup"><span data-stu-id="a95ea-157">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication, ByVpnServerConfigurationObjectByCertificateAuthentication, ByVpnServerConfigurationResourceIdByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95ea-158">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="a95ea-158">-VpnProtocol</span></span>
<span data-ttu-id="a95ea-159">Список туннельных протоколов клиента VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="a95ea-159">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a95ea-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a95ea-160">-Confirm</span></span>
<span data-ttu-id="a95ea-161">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a95ea-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a95ea-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a95ea-162">-WhatIf</span></span>
<span data-ttu-id="a95ea-163">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a95ea-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a95ea-164">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a95ea-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a95ea-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a95ea-165">CommonParameters</span></span>
<span data-ttu-id="a95ea-166">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a95ea-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a95ea-167">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a95ea-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a95ea-168">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a95ea-168">INPUTS</span></span>

### <span data-ttu-id="a95ea-169">Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a95ea-169">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="a95ea-170">System. String Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="a95ea-170">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="a95ea-171">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a95ea-171">OUTPUTS</span></span>

### <span data-ttu-id="a95ea-172">Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="a95ea-172">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="a95ea-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="a95ea-173">NOTES</span></span>

## <span data-ttu-id="a95ea-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a95ea-174">RELATED LINKS</span></span>
