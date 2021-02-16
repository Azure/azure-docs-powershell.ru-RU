---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
ms.openlocfilehash: b46f346c1aa58b8c6f155ad9a742271fa121f630
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236665"
---
# <span data-ttu-id="d4339-101">New-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4339-101">New-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="d4339-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4339-102">SYNOPSIS</span></span>
<span data-ttu-id="d4339-103">Создайте новую технологию VpnServerConfiguration, указываю на подключение к сайту.</span><span class="sxs-lookup"><span data-stu-id="d4339-103">Create a new VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="d4339-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d4339-104">SYNTAX</span></span>

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

## <span data-ttu-id="d4339-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4339-105">DESCRIPTION</span></span>
<span data-ttu-id="d4339-106">С помощью cmdlet **new-AzVpnServerConfiguration** можно создать новую проверку VPNServerConfiguration с разными средствами VpnProtocols, VpnAuthenticationTypes, IpsecPolicies и настроить параметры для выбранного типа проверки подлинности VPN в связи с требованиями клиента для подключения к сайту.</span><span class="sxs-lookup"><span data-stu-id="d4339-106">The **New-AzVpnServerConfiguration** cmdlet enables you to create a new VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="d4339-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d4339-107">EXAMPLES</span></span>

### <span data-ttu-id="d4339-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d4339-108">Example 1</span></span>
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

<span data-ttu-id="d4339-109">С помощью этой команды создается новая команда VpnServerConfiguration с VPNAuthenticationType в качестве сертификата.</span><span class="sxs-lookup"><span data-stu-id="d4339-109">The above command will create a new VpnServerConfiguration with VpnAuthenticationType as Certificate.</span></span>

### <span data-ttu-id="d4339-110">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d4339-110">Example 2</span></span>

<span data-ttu-id="d4339-111">Создайте новую технологию VpnServerConfiguration, указываю на подключение к сайту.</span><span class="sxs-lookup"><span data-stu-id="d4339-111">Create a new VpnServerConfiguration for point to site connectivity.</span></span> <span data-ttu-id="d4339-112">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="d4339-112">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->


```powershell
New-AzVpnServerConfiguration -AadAudience <String> -AadIssuer <String> -AadTenant <String> -Location 'westus' -Name 'test1config' -ResourceGroupName 'P2SCortexGATesting' -VpnAuthenticationType Certificate -VpnProtocol IkeV2
```

## <span data-ttu-id="d4339-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4339-113">PARAMETERS</span></span>

### <span data-ttu-id="d4339-114">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="d4339-114">-AadAudience</span></span>
<span data-ttu-id="d4339-115">Аудитория AAD для проверки подлинности P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="d4339-115">AAD audience for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="d4339-116">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="d4339-116">-AadIssuer</span></span>
<span data-ttu-id="d4339-117">AAD issuer for P2S AAD authentication.</span><span class="sxs-lookup"><span data-stu-id="d4339-117">AAD issuer for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="d4339-118">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="d4339-118">-AadTenant</span></span>
<span data-ttu-id="d4339-119">Клиент AAD для проверки подлинности AAD P2S.</span><span class="sxs-lookup"><span data-stu-id="d4339-119">AAD tenant for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="d4339-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4339-120">-AsJob</span></span>
<span data-ttu-id="d4339-121">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d4339-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d4339-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4339-122">-DefaultProfile</span></span>
<span data-ttu-id="d4339-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d4339-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4339-124">-Location</span><span class="sxs-lookup"><span data-stu-id="d4339-124">-Location</span></span>
<span data-ttu-id="d4339-125">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="d4339-125">The resource location.</span></span>

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

### <span data-ttu-id="d4339-126">-Name</span><span class="sxs-lookup"><span data-stu-id="d4339-126">-Name</span></span>
<span data-ttu-id="d4339-127">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="d4339-127">The resource name.</span></span>

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

### <span data-ttu-id="d4339-128">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="d4339-128">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="d4339-129">Список путей к файлам RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d4339-129">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="d4339-130">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="d4339-130">-RadiusServerAddress</span></span>
<span data-ttu-id="d4339-131">Адрес сервера внешнего радиуса P2S.</span><span class="sxs-lookup"><span data-stu-id="d4339-131">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="d4339-132">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="d4339-132">-RadiusServerList</span></span>
<span data-ttu-id="d4339-133">Внешние серверы с несколькими радиусами.</span><span class="sxs-lookup"><span data-stu-id="d4339-133">P2S External multiple radius servers.</span></span>

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

### <span data-ttu-id="d4339-134">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="d4339-134">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="d4339-135">Список путей к файлам RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="d4339-135">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="d4339-136">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="d4339-136">-RadiusServerSecret</span></span>
<span data-ttu-id="d4339-137">Секрет внешнего радиуса P2S.</span><span class="sxs-lookup"><span data-stu-id="d4339-137">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="d4339-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4339-138">-ResourceGroupName</span></span>
<span data-ttu-id="d4339-139">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d4339-139">The resource group name.</span></span>

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

### <span data-ttu-id="d4339-140">-Tag</span><span class="sxs-lookup"><span data-stu-id="d4339-140">-Tag</span></span>
<span data-ttu-id="d4339-141">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="d4339-141">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="d4339-142">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="d4339-142">-VpnAuthenticationType</span></span>
<span data-ttu-id="d4339-143">Список протоколов туннелинга VPN-клиентов P2S.</span><span class="sxs-lookup"><span data-stu-id="d4339-143">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="d4339-144">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="d4339-144">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="d4339-145">Список политик IPSec для VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d4339-145">A list of IPSec policies for VpnServerConfiguration.</span></span>

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

### <span data-ttu-id="d4339-146">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="d4339-146">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="d4339-147">A list of VpnClientCertificates to be revoked files' paths</span><span class="sxs-lookup"><span data-stu-id="d4339-147">A list of VpnClientCertificates to be revoked files' paths</span></span>

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

### <span data-ttu-id="d4339-148">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="d4339-148">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="d4339-149">Список путей к файлам vpnClientRootCertificates</span><span class="sxs-lookup"><span data-stu-id="d4339-149">A list of VpnClientRootCertificates to be added files' paths</span></span>

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

### <span data-ttu-id="d4339-150">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="d4339-150">-VpnProtocol</span></span>
<span data-ttu-id="d4339-151">Список протоколов туннелинга VPN-клиентов P2S.</span><span class="sxs-lookup"><span data-stu-id="d4339-151">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="d4339-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4339-152">-Confirm</span></span>
<span data-ttu-id="d4339-153">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4339-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4339-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4339-154">-WhatIf</span></span>
<span data-ttu-id="d4339-155">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4339-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4339-156">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d4339-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4339-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4339-157">CommonParameters</span></span>
<span data-ttu-id="d4339-158">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4339-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4339-159">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4339-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4339-160">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4339-160">INPUTS</span></span>

### <span data-ttu-id="d4339-161">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span><span class="sxs-lookup"><span data-stu-id="d4339-161">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="d4339-162">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d4339-162">OUTPUTS</span></span>

### <span data-ttu-id="d4339-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="d4339-163">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="d4339-164">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d4339-164">NOTES</span></span>

## <span data-ttu-id="d4339-165">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4339-165">RELATED LINKS</span></span>
