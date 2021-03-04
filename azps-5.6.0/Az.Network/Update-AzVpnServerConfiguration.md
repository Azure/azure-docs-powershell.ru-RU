---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVpnServerConfiguration.md
ms.openlocfilehash: e5bd6c612cb78d2c6d38a1484452c814ecdf714c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951443"
---
# <span data-ttu-id="d1f88-101">Update-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1f88-101">Update-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="d1f88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1f88-102">SYNOPSIS</span></span>
<span data-ttu-id="d1f88-103">Обновляет существующую структуру VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d1f88-103">Updates an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="d1f88-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d1f88-104">SYNTAX</span></span>

### <span data-ttu-id="d1f88-105">ByVpnServerConfigurationName (default)</span><span class="sxs-lookup"><span data-stu-id="d1f88-105">ByVpnServerConfigurationName (Default)</span></span>
```
Update-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d1f88-106">ByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="d1f88-106">ByVpnServerConfigurationObject</span></span>
```
Update-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d1f88-107">ByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="d1f88-107">ByVpnServerConfigurationResourceId</span></span>
```
Update-AzVpnServerConfiguration -ResourceId <String> [-VpnProtocol <String[]>]
 [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d1f88-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d1f88-108">DESCRIPTION</span></span>
<span data-ttu-id="d1f88-109">С помощью cmdlet **Update-AzVpnServerConfiguration** можно обновить существующую проверку VpnServerConfiguration с использованием различных параметров VpnProtocols, VpnAuthenticationTypes, IpsecPolicies и настроить параметры для выбранного типа vpn-проверки подлинности в рамках требований клиента к подключению к сайту Point.</span><span class="sxs-lookup"><span data-stu-id="d1f88-109">The **Update-AzVpnServerConfiguration** cmdlet enables you to update the existing VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="d1f88-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d1f88-110">EXAMPLES</span></span>

### <span data-ttu-id="d1f88-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d1f88-111">Example 1</span></span>
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

<span data-ttu-id="d1f88-112">При нажатии этой команды будет обновлена существующая команда VpnServerConfiguration с использованием VpnProtocol в качестве IkeV2.</span><span class="sxs-lookup"><span data-stu-id="d1f88-112">The above command will update an existing VpnServerConfiguration with VpnProtocol as IkeV2.</span></span>

## <span data-ttu-id="d1f88-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1f88-113">PARAMETERS</span></span>

### <span data-ttu-id="d1f88-114">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="d1f88-114">-AadAudience</span></span>
<span data-ttu-id="d1f88-115">Аудитория AAD для проверки подлинности P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="d1f88-115">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f88-116">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="d1f88-116">-AadIssuer</span></span>
<span data-ttu-id="d1f88-117">AAD issuer for P2S AAD authentication.</span><span class="sxs-lookup"><span data-stu-id="d1f88-117">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f88-118">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="d1f88-118">-AadTenant</span></span>
<span data-ttu-id="d1f88-119">Клиент AAD для проверки подлинности AAD P2S.</span><span class="sxs-lookup"><span data-stu-id="d1f88-119">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f88-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1f88-120">-AsJob</span></span>
<span data-ttu-id="d1f88-121">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d1f88-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d1f88-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1f88-122">-DefaultProfile</span></span>
<span data-ttu-id="d1f88-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d1f88-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1f88-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1f88-124">-InputObject</span></span>
<span data-ttu-id="d1f88-125">Объект конфигурации VPN-сервера, который нужно изменить</span><span class="sxs-lookup"><span data-stu-id="d1f88-125">The vpn server configuration object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObject
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1f88-126">-Name</span><span class="sxs-lookup"><span data-stu-id="d1f88-126">-Name</span></span>
<span data-ttu-id="d1f88-127">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="d1f88-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationName
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f88-128">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="d1f88-128">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="d1f88-129">Список путей к файлам RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d1f88-129">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f88-130">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="d1f88-130">-RadiusServerAddress</span></span>
<span data-ttu-id="d1f88-131">Адрес сервера внешнего радиуса P2S.</span><span class="sxs-lookup"><span data-stu-id="d1f88-131">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f88-132">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="d1f88-132">-RadiusServerList</span></span>
<span data-ttu-id="d1f88-133">Внешние серверы с несколькими радиусами.</span><span class="sxs-lookup"><span data-stu-id="d1f88-133">P2S External multiple radius servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f88-134">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="d1f88-134">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="d1f88-135">Список путей к файлам RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d1f88-135">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f88-136">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="d1f88-136">-RadiusServerSecret</span></span>
<span data-ttu-id="d1f88-137">Секрет внешнего радиуса P2S.</span><span class="sxs-lookup"><span data-stu-id="d1f88-137">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f88-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1f88-138">-ResourceGroupName</span></span>
<span data-ttu-id="d1f88-139">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d1f88-139">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f88-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1f88-140">-ResourceId</span></span>
<span data-ttu-id="d1f88-141">ИД ресурсов Azure для конфигурации vpn-сервера.</span><span class="sxs-lookup"><span data-stu-id="d1f88-141">The Azure resource ID for the vpn server configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationResourceId
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1f88-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="d1f88-142">-Tag</span></span>
<span data-ttu-id="d1f88-143">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="d1f88-143">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="d1f88-144">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="d1f88-144">-VpnAuthenticationType</span></span>
<span data-ttu-id="d1f88-145">Список протоколов туннелинга VPN-клиентов P2S.</span><span class="sxs-lookup"><span data-stu-id="d1f88-145">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="d1f88-146">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="d1f88-146">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="d1f88-147">Список политик IPSec для VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d1f88-147">A list of IPSec policies for VpnServerConfiguration.</span></span>

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

### <span data-ttu-id="d1f88-148">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="d1f88-148">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="d1f88-149">A list of VpnClientCertificates to be revoked files' paths</span><span class="sxs-lookup"><span data-stu-id="d1f88-149">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f88-150">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="d1f88-150">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="d1f88-151">A list of VpnClientRootCertificates to be added files' paths</span><span class="sxs-lookup"><span data-stu-id="d1f88-151">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1f88-152">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="d1f88-152">-VpnProtocol</span></span>
<span data-ttu-id="d1f88-153">Список протоколов туннелинга VPN-клиентов P2S.</span><span class="sxs-lookup"><span data-stu-id="d1f88-153">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="d1f88-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d1f88-154">-Confirm</span></span>
<span data-ttu-id="d1f88-155">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d1f88-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1f88-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1f88-156">-WhatIf</span></span>
<span data-ttu-id="d1f88-157">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1f88-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1f88-158">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d1f88-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1f88-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1f88-159">CommonParameters</span></span>
<span data-ttu-id="d1f88-160">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1f88-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1f88-161">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1f88-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1f88-162">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d1f88-162">INPUTS</span></span>

### <span data-ttu-id="d1f88-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1f88-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="d1f88-164">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="d1f88-164">System.String Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="d1f88-165">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d1f88-165">OUTPUTS</span></span>

### <span data-ttu-id="d1f88-166">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d1f88-166">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="d1f88-167">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d1f88-167">NOTES</span></span>

## <span data-ttu-id="d1f88-168">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d1f88-168">RELATED LINKS</span></span>
