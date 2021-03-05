---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
ms.openlocfilehash: f093a9f3a30ce1e46c08790d355689fdd9399c79
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984355"
---
# <span data-ttu-id="c6bd4-101">New-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6bd4-101">New-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="c6bd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6bd4-102">SYNOPSIS</span></span>
<span data-ttu-id="c6bd4-103">Создайте новую технологию VpnServerConfiguration, указываю на подключение к сайту.</span><span class="sxs-lookup"><span data-stu-id="c6bd4-103">Create a new VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="c6bd4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c6bd4-104">SYNTAX</span></span>

```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-AadTenant <String>] [-AadAudience <String>] [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c6bd4-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c6bd4-105">DESCRIPTION</span></span>
<span data-ttu-id="c6bd4-106">С помощью cmdlet **new-AzVpnServerConfiguration** можно создать новую проверку VPNServerConfiguration с разными средствами VpnProtocols, VpnAuthenticationTypes, IpsecPolicies и настроить параметры для выбранного типа проверки подлинности VPN в связи с требованиями клиента для подключения к сайту.</span><span class="sxs-lookup"><span data-stu-id="c6bd4-106">The **New-AzVpnServerConfiguration** cmdlet enables you to create a new VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="c6bd4-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c6bd4-107">EXAMPLES</span></span>

### <span data-ttu-id="c6bd4-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c6bd4-108">Example 1</span></span>
```powershell
PS C:\> $VpnServerConfigCertFilePath = Join-Path -Path $basedir -ChildPath "\ScenarioTests\Data\ApplicationGatewayAuthCert.cer"
PS C:\> $listOfCerts = New-Object "System.Collections.Generic.List[String]"
PS C:\> $listOfCerts.Add($VpnServerConfigCertFilePath)
PS C:\> New-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -VpnProtocol IkeV2 -VpnAuthenticationType Certificate -VpnClientRootCertificateFilesList $listOfCerts -VpnClientRevokedCertificateFilesList $listOfCerts -Location "westus"
ResourceGroupName            : P2SCortexGATesting
Name                         : test1config
Id                           : /subscriptions/b1f1deed-af60-4bab-9223-65d340462e24/resourceGroups/P2SCortexGATesting/providers/Microsoft.Network/vpnServerConfigurations/test1config
Location                     : westus
VpnProtocols                 : {IkeV2, OpenVPN}
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

<span data-ttu-id="c6bd4-109">С помощью этой команды создается новая команда VpnServerConfiguration с VPNAuthenticationType в качестве сертификата.</span><span class="sxs-lookup"><span data-stu-id="c6bd4-109">The above command will create a new VpnServerConfiguration with VpnAuthenticationType as Certificate.</span></span>

### <span data-ttu-id="c6bd4-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c6bd4-110">Example 2</span></span>

<span data-ttu-id="c6bd4-111">Создайте новую технологию VpnServerConfiguration, указываю на подключение к сайту.</span><span class="sxs-lookup"><span data-stu-id="c6bd4-111">Create a new VpnServerConfiguration for point to site connectivity.</span></span> <span data-ttu-id="c6bd4-112">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="c6bd4-112">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzVpnServerConfiguration -AadAudience <String> -AadIssuer <String> -AadTenant <String> -Location 'westus' -Name 'test1config' -ResourceGroupName 'P2SCortexGATesting' -VpnAuthenticationType Certificate -VpnProtocol IkeV2
```

## <span data-ttu-id="c6bd4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6bd4-113">PARAMETERS</span></span>

### <span data-ttu-id="c6bd4-114">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="c6bd4-114">-AadAudience</span></span>
<span data-ttu-id="c6bd4-115">Аудитория AAD для проверки подлинности P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="c6bd4-115">AAD audience for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="c6bd4-116">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="c6bd4-116">-AadIssuer</span></span>
<span data-ttu-id="c6bd4-117">AAD issuer for P2S AAD authentication.</span><span class="sxs-lookup"><span data-stu-id="c6bd4-117">AAD issuer for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="c6bd4-118">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="c6bd4-118">-AadTenant</span></span>
<span data-ttu-id="c6bd4-119">Клиент AAD для проверки подлинности AAD P2S.</span><span class="sxs-lookup"><span data-stu-id="c6bd4-119">AAD tenant for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="c6bd4-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6bd4-120">-AsJob</span></span>
<span data-ttu-id="c6bd4-121">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c6bd4-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c6bd4-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6bd4-122">-DefaultProfile</span></span>
<span data-ttu-id="c6bd4-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c6bd4-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6bd4-124">-Location</span><span class="sxs-lookup"><span data-stu-id="c6bd4-124">-Location</span></span>
<span data-ttu-id="c6bd4-125">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="c6bd4-125">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6bd4-126">-Name</span><span class="sxs-lookup"><span data-stu-id="c6bd4-126">-Name</span></span>
<span data-ttu-id="c6bd4-127">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="c6bd4-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6bd4-128">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="c6bd4-128">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="c6bd4-129">Список путей к файлам RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c6bd4-129">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="c6bd4-130">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="c6bd4-130">-RadiusServerAddress</span></span>
<span data-ttu-id="c6bd4-131">Адрес сервера внешнего радиуса P2S.</span><span class="sxs-lookup"><span data-stu-id="c6bd4-131">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="c6bd4-132">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="c6bd4-132">-RadiusServerList</span></span>
<span data-ttu-id="c6bd4-133">Внешние серверы с несколькими радиусами.</span><span class="sxs-lookup"><span data-stu-id="c6bd4-133">P2S External multiple radius servers.</span></span>

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

### <span data-ttu-id="c6bd4-134">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="c6bd4-134">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="c6bd4-135">Список путей к файлам RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="c6bd4-135">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="c6bd4-136">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="c6bd4-136">-RadiusServerSecret</span></span>
<span data-ttu-id="c6bd4-137">Секрет внешнего радиуса P2S.</span><span class="sxs-lookup"><span data-stu-id="c6bd4-137">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="c6bd4-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6bd4-138">-ResourceGroupName</span></span>
<span data-ttu-id="c6bd4-139">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c6bd4-139">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6bd4-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="c6bd4-140">-Tag</span></span>
<span data-ttu-id="c6bd4-141">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="c6bd4-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="c6bd4-142">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="c6bd4-142">-VpnAuthenticationType</span></span>
<span data-ttu-id="c6bd4-143">Список протоколов туннелинга VPN-клиентов P2S.</span><span class="sxs-lookup"><span data-stu-id="c6bd4-143">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="c6bd4-144">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="c6bd4-144">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="c6bd4-145">Список политик IPSec для VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c6bd4-145">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6bd4-146">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="c6bd4-146">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="c6bd4-147">A list of VpnClientCertificates to be revoked files' paths</span><span class="sxs-lookup"><span data-stu-id="c6bd4-147">A list of VpnClientCertificates to be revoked files' paths</span></span>

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

### <span data-ttu-id="c6bd4-148">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="c6bd4-148">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="c6bd4-149">A list of VpnClientRootCertificates to be added files' paths</span><span class="sxs-lookup"><span data-stu-id="c6bd4-149">A list of VpnClientRootCertificates to be added files' paths</span></span>

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

### <span data-ttu-id="c6bd4-150">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="c6bd4-150">-VpnProtocol</span></span>
<span data-ttu-id="c6bd4-151">Список протоколов туннелинга VPN-клиентов P2S.</span><span class="sxs-lookup"><span data-stu-id="c6bd4-151">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="c6bd4-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6bd4-152">-Confirm</span></span>
<span data-ttu-id="c6bd4-153">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6bd4-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6bd4-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6bd4-154">-WhatIf</span></span>
<span data-ttu-id="c6bd4-155">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6bd4-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6bd4-156">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c6bd4-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6bd4-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6bd4-157">CommonParameters</span></span>
<span data-ttu-id="c6bd4-158">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6bd4-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6bd4-159">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6bd4-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6bd4-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c6bd4-160">INPUTS</span></span>

### <span data-ttu-id="c6bd4-161">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="c6bd4-161">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="c6bd4-162">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c6bd4-162">OUTPUTS</span></span>

### <span data-ttu-id="c6bd4-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="c6bd4-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="c6bd4-164">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c6bd4-164">NOTES</span></span>

## <span data-ttu-id="c6bd4-165">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c6bd4-165">RELATED LINKS</span></span>
