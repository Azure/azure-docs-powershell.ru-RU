---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
ms.openlocfilehash: 10feda31a97582ef56300b570ce2768c3ea0e277
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401212"
---
# <span data-ttu-id="34786-101">New-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="34786-101">New-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="34786-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34786-102">SYNOPSIS</span></span>
<span data-ttu-id="34786-103">Создайте новую технологию VpnServerConfiguration, указываю на подключение к сайту.</span><span class="sxs-lookup"><span data-stu-id="34786-103">Create a new VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="34786-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="34786-104">SYNTAX</span></span>

### <span data-ttu-id="34786-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span><span class="sxs-lookup"><span data-stu-id="34786-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="34786-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="34786-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34786-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="34786-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>]
 [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34786-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34786-108">DESCRIPTION</span></span>
<span data-ttu-id="34786-109">С помощью cmdlet **new-AzVpnServerConfiguration** можно создать новую проверку VPNServerConfiguration с разными средствами VpnProtocols, VpnAuthenticationTypes, IpsecPolicies и настроить параметры для выбранного типа проверки подлинности VPN в связи с требованиями клиента для подключения к сайту Point.</span><span class="sxs-lookup"><span data-stu-id="34786-109">The **New-AzVpnServerConfiguration** cmdlet enables you to create a new VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="34786-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="34786-110">EXAMPLES</span></span>

### <span data-ttu-id="34786-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="34786-111">Example 1</span></span>
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

<span data-ttu-id="34786-112">С помощью этой команды создается новая команда VpnServerConfiguration с VPNAuthenticationType в качестве сертификата.</span><span class="sxs-lookup"><span data-stu-id="34786-112">The above command will create a new VpnServerConfiguration with VpnAuthenticationType as Certificate.</span></span>

### <span data-ttu-id="34786-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="34786-113">Example 2</span></span>

<span data-ttu-id="34786-114">Создайте новую технологию VpnServerConfiguration, указываю на подключение к сайту.</span><span class="sxs-lookup"><span data-stu-id="34786-114">Create a new VpnServerConfiguration for point to site connectivity.</span></span> <span data-ttu-id="34786-115">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="34786-115">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVpnServerConfiguration -AadAudience <String> -AadIssuer <String> -AadTenant <String> -Location 'westus' -Name 'test1config' -ResourceGroupName 'P2SCortexGATesting' -VpnAuthenticationType Certificate -VpnProtocol IkeV2
```

## <span data-ttu-id="34786-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34786-116">PARAMETERS</span></span>

### <span data-ttu-id="34786-117">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="34786-117">-AadAudience</span></span>
<span data-ttu-id="34786-118">Аудитория AAD для проверки подлинности P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="34786-118">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34786-119">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="34786-119">-AadIssuer</span></span>
<span data-ttu-id="34786-120">AAD issuer for P2S AAD authentication.</span><span class="sxs-lookup"><span data-stu-id="34786-120">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34786-121">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="34786-121">-AadTenant</span></span>
<span data-ttu-id="34786-122">Клиент AAD для проверки подлинности AAD P2S.</span><span class="sxs-lookup"><span data-stu-id="34786-122">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34786-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="34786-123">-AsJob</span></span>
<span data-ttu-id="34786-124">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="34786-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="34786-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34786-125">-DefaultProfile</span></span>
<span data-ttu-id="34786-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="34786-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34786-127">-Location</span><span class="sxs-lookup"><span data-stu-id="34786-127">-Location</span></span>
<span data-ttu-id="34786-128">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="34786-128">The resource location.</span></span>

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

### <span data-ttu-id="34786-129">-Name</span><span class="sxs-lookup"><span data-stu-id="34786-129">-Name</span></span>
<span data-ttu-id="34786-130">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="34786-130">The resource name.</span></span>

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

### <span data-ttu-id="34786-131">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="34786-131">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="34786-132">Список путей к файлам RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="34786-132">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34786-133">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="34786-133">-RadiusServerAddress</span></span>
<span data-ttu-id="34786-134">Адрес сервера внешнего радиуса P2S.</span><span class="sxs-lookup"><span data-stu-id="34786-134">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34786-135">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="34786-135">-RadiusServerList</span></span>
<span data-ttu-id="34786-136">Внешние серверы с несколькими радиусами.</span><span class="sxs-lookup"><span data-stu-id="34786-136">P2S External multiple radius servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRadiusServer[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34786-137">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="34786-137">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="34786-138">Список путей к файлам RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="34786-138">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34786-139">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="34786-139">-RadiusServerSecret</span></span>
<span data-ttu-id="34786-140">Секрет внешнего радиуса P2S.</span><span class="sxs-lookup"><span data-stu-id="34786-140">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34786-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34786-141">-ResourceGroupName</span></span>
<span data-ttu-id="34786-142">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="34786-142">The resource group name.</span></span>

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

### <span data-ttu-id="34786-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="34786-143">-Tag</span></span>
<span data-ttu-id="34786-144">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="34786-144">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="34786-145">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="34786-145">-VpnAuthenticationType</span></span>
<span data-ttu-id="34786-146">Список протоколов туннелинга VPN-клиентов P2S.</span><span class="sxs-lookup"><span data-stu-id="34786-146">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="34786-147">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="34786-147">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="34786-148">Список политик IPSec для VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="34786-148">A list of IPSec policies for VpnServerConfiguration.</span></span>

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

### <span data-ttu-id="34786-149">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="34786-149">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="34786-150">A list of VpnClientCertificates to be revoked files' paths</span><span class="sxs-lookup"><span data-stu-id="34786-150">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34786-151">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="34786-151">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="34786-152">A list of VpnClientRootCertificates to be added files' paths</span><span class="sxs-lookup"><span data-stu-id="34786-152">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34786-153">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="34786-153">-VpnProtocol</span></span>
<span data-ttu-id="34786-154">Список протоколов туннелинга VPN-клиентов P2S.</span><span class="sxs-lookup"><span data-stu-id="34786-154">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="34786-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34786-155">-Confirm</span></span>
<span data-ttu-id="34786-156">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="34786-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34786-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34786-157">-WhatIf</span></span>
<span data-ttu-id="34786-158">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34786-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34786-159">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="34786-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34786-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34786-160">CommonParameters</span></span>
<span data-ttu-id="34786-161">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34786-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34786-162">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34786-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34786-163">INPUTS</span><span class="sxs-lookup"><span data-stu-id="34786-163">INPUTS</span></span>

### <span data-ttu-id="34786-164">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="34786-164">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="34786-165">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="34786-165">OUTPUTS</span></span>

### <span data-ttu-id="34786-166">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="34786-166">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="34786-167">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="34786-167">NOTES</span></span>

## <span data-ttu-id="34786-168">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34786-168">RELATED LINKS</span></span>
