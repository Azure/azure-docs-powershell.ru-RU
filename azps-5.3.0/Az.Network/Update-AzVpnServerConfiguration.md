---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
ms.openlocfilehash: 8897b2e1175c82f3dcc25642dec920a4b6d7343c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519862"
---
# <span data-ttu-id="505cb-101">Update-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="505cb-101">Update-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="505cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="505cb-102">SYNOPSIS</span></span>
<span data-ttu-id="505cb-103">Обновляет существующую структуру VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="505cb-103">Updates an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="505cb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="505cb-104">SYNTAX</span></span>

### <span data-ttu-id="505cb-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span><span class="sxs-lookup"><span data-stu-id="505cb-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="505cb-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="505cb-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="505cb-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="505cb-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="505cb-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="505cb-108">ByVpnServerConfigurationObjectByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="505cb-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="505cb-109">ByVpnServerConfigurationObjectByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="505cb-110">ByVpnServerConfigurationObjectByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="505cb-110">ByVpnServerConfigurationObjectByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="505cb-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span><span class="sxs-lookup"><span data-stu-id="505cb-111">ByVpnServerConfigurationResourceIdByCertificateAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="505cb-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="505cb-112">ByVpnServerConfigurationResourceIdByRadiusAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>] [-RadiusServerSecret <SecureString>]
 [-RadiusServerList <PSRadiusServer[]>] [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="505cb-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="505cb-113">ByVpnServerConfigurationResourceIdByAadAuthentication</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="505cb-114">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="505cb-114">DESCRIPTION</span></span>
<span data-ttu-id="505cb-115">С помощью cmdlet **Update-AzVpnServerConfiguration** можно обновить существующую проверку VpnServerConfiguration с использованием различных параметров VpnProtocols, VpnAuthenticationTypes, IpsecPolicies и настроить параметры для выбранного типа проверки подлинности VPN в рамках требований клиента к подключению к сайту Point.</span><span class="sxs-lookup"><span data-stu-id="505cb-115">The **Update-AzVpnServerConfiguration** cmdlet enables you to update the existing VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="505cb-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="505cb-116">EXAMPLES</span></span>

### <span data-ttu-id="505cb-117">Пример 1</span><span class="sxs-lookup"><span data-stu-id="505cb-117">Example 1</span></span>
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

<span data-ttu-id="505cb-118">При нажатии этой команды будет обновлена существующая команда VpnServerConfiguration с использованием VpnProtocol в качестве IkeV2.</span><span class="sxs-lookup"><span data-stu-id="505cb-118">The above command will update an existing VpnServerConfiguration with VpnProtocol as IkeV2.</span></span>

## <span data-ttu-id="505cb-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="505cb-119">PARAMETERS</span></span>

### <span data-ttu-id="505cb-120">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="505cb-120">-AadAudience</span></span>
<span data-ttu-id="505cb-121">Аудитория AAD для проверки подлинности P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="505cb-121">AAD audience for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="505cb-122">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="505cb-122">-AadIssuer</span></span>
<span data-ttu-id="505cb-123">AAD issuer for P2S AAD authentication.</span><span class="sxs-lookup"><span data-stu-id="505cb-123">AAD issuer for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="505cb-124">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="505cb-124">-AadTenant</span></span>
<span data-ttu-id="505cb-125">Клиент AAD для проверки подлинности AAD P2S.</span><span class="sxs-lookup"><span data-stu-id="505cb-125">AAD tenant for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="505cb-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="505cb-126">-AsJob</span></span>
<span data-ttu-id="505cb-127">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="505cb-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="505cb-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="505cb-128">-DefaultProfile</span></span>
<span data-ttu-id="505cb-129">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="505cb-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="505cb-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="505cb-130">-InputObject</span></span>
<span data-ttu-id="505cb-131">Объект конфигурации VPN-сервера, который нужно изменить</span><span class="sxs-lookup"><span data-stu-id="505cb-131">The vpn server configuration object to be modified</span></span>

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

### <span data-ttu-id="505cb-132">-Name</span><span class="sxs-lookup"><span data-stu-id="505cb-132">-Name</span></span>
<span data-ttu-id="505cb-133">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="505cb-133">The resource name.</span></span>

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

### <span data-ttu-id="505cb-134">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="505cb-134">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="505cb-135">Список путей к файлам RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="505cb-135">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="505cb-136">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="505cb-136">-RadiusServerAddress</span></span>
<span data-ttu-id="505cb-137">Адрес сервера внешнего радиуса P2S.</span><span class="sxs-lookup"><span data-stu-id="505cb-137">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="505cb-138">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="505cb-138">-RadiusServerList</span></span>
<span data-ttu-id="505cb-139">Внешние серверы с несколькими радиусами.</span><span class="sxs-lookup"><span data-stu-id="505cb-139">P2S External multiple radius servers.</span></span>

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

### <span data-ttu-id="505cb-140">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="505cb-140">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="505cb-141">Список путей к файлам RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="505cb-141">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="505cb-142">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="505cb-142">-RadiusServerSecret</span></span>
<span data-ttu-id="505cb-143">Секрет внешнего радиуса P2S.</span><span class="sxs-lookup"><span data-stu-id="505cb-143">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="505cb-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="505cb-144">-ResourceGroupName</span></span>
<span data-ttu-id="505cb-145">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="505cb-145">The resource group name.</span></span>

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

### <span data-ttu-id="505cb-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="505cb-146">-ResourceId</span></span>
<span data-ttu-id="505cb-147">ИД ресурсов Azure для конфигурации vpn-сервера.</span><span class="sxs-lookup"><span data-stu-id="505cb-147">The Azure resource ID for the vpn server configuration.</span></span>

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

### <span data-ttu-id="505cb-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="505cb-148">-Tag</span></span>
<span data-ttu-id="505cb-149">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="505cb-149">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="505cb-150">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="505cb-150">-VpnAuthenticationType</span></span>
<span data-ttu-id="505cb-151">Список протоколов туннелинга VPN-клиентов P2S.</span><span class="sxs-lookup"><span data-stu-id="505cb-151">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="505cb-152">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="505cb-152">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="505cb-153">Список политик IPSec для VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="505cb-153">A list of IPSec policies for VpnServerConfiguration.</span></span>

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

### <span data-ttu-id="505cb-154">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="505cb-154">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="505cb-155">A list of VpnClientCertificates to be revoked files' paths</span><span class="sxs-lookup"><span data-stu-id="505cb-155">A list of VpnClientCertificates to be revoked files' paths</span></span>

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

### <span data-ttu-id="505cb-156">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="505cb-156">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="505cb-157">A list of VpnClientRootCertificates to be added files' paths</span><span class="sxs-lookup"><span data-stu-id="505cb-157">A list of VpnClientRootCertificates to be added files' paths</span></span>

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

### <span data-ttu-id="505cb-158">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="505cb-158">-VpnProtocol</span></span>
<span data-ttu-id="505cb-159">Список протоколов туннелинга VPN-клиентов P2S.</span><span class="sxs-lookup"><span data-stu-id="505cb-159">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="505cb-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="505cb-160">-Confirm</span></span>
<span data-ttu-id="505cb-161">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="505cb-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="505cb-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="505cb-162">-WhatIf</span></span>
<span data-ttu-id="505cb-163">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="505cb-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="505cb-164">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="505cb-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="505cb-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="505cb-165">CommonParameters</span></span>
<span data-ttu-id="505cb-166">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="505cb-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="505cb-167">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="505cb-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="505cb-168">INPUTS</span><span class="sxs-lookup"><span data-stu-id="505cb-168">INPUTS</span></span>

### <span data-ttu-id="505cb-169">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="505cb-169">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="505cb-170">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="505cb-170">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="505cb-171">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="505cb-171">OUTPUTS</span></span>

### <span data-ttu-id="505cb-172">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="505cb-172">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="505cb-173">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="505cb-173">NOTES</span></span>

## <span data-ttu-id="505cb-174">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="505cb-174">RELATED LINKS</span></span>
