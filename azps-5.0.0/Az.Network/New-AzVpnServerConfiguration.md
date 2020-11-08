---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
ms.openlocfilehash: 10feda31a97582ef56300b570ce2768c3ea0e277
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249645"
---
# <span data-ttu-id="6aec0-101">New-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="6aec0-101">New-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="6aec0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6aec0-102">SYNOPSIS</span></span>
<span data-ttu-id="6aec0-103">Создайте новый VpnServerConfiguration для подключения к сайту.</span><span class="sxs-lookup"><span data-stu-id="6aec0-103">Create a new VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="6aec0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6aec0-104">SYNTAX</span></span>

### <span data-ttu-id="6aec0-105">ByVpnServerConfigurationNameByCertificateAuthentication (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6aec0-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6aec0-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="6aec0-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-RadiusServerAddress <String>]
 [-RadiusServerSecret <SecureString>] [-RadiusServerList <PSRadiusServer[]>]
 [-RadiusServerRootCertificateFilesList <String[]>] [-RadiusClientRootCertificateFilesList <String[]>]
 [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6aec0-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="6aec0-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>]
 [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6aec0-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6aec0-108">DESCRIPTION</span></span>
<span data-ttu-id="6aec0-109">С помощью командлета **New-AzVpnServerConfiguration** можно создавать новые VpnServerConfiguration с разными VpnProtocols, VpnAuthenticationTypes, IpsecPolicies и настраивать выбранные параметры проверки подлинности VPN в соответствии с требованием клиента для указания на подключение к сайту.</span><span class="sxs-lookup"><span data-stu-id="6aec0-109">The **New-AzVpnServerConfiguration** cmdlet enables you to create a new VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="6aec0-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6aec0-110">EXAMPLES</span></span>

### <span data-ttu-id="6aec0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6aec0-111">Example 1</span></span>
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

<span data-ttu-id="6aec0-112">Вышеприведенная команда создаст новый VpnServerConfiguration с VpnAuthenticationType в качестве сертификата.</span><span class="sxs-lookup"><span data-stu-id="6aec0-112">The above command will create a new VpnServerConfiguration with VpnAuthenticationType as Certificate.</span></span>

### <span data-ttu-id="6aec0-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6aec0-113">Example 2</span></span>

<span data-ttu-id="6aec0-114">Создайте новый VpnServerConfiguration для подключения к сайту.</span><span class="sxs-lookup"><span data-stu-id="6aec0-114">Create a new VpnServerConfiguration for point to site connectivity.</span></span> <span data-ttu-id="6aec0-115">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="6aec0-115">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
New-AzVpnServerConfiguration -AadAudience <String> -AadIssuer <String> -AadTenant <String> -Location 'westus' -Name 'test1config' -ResourceGroupName 'P2SCortexGATesting' -VpnAuthenticationType Certificate -VpnProtocol IkeV2
```

## <span data-ttu-id="6aec0-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6aec0-116">PARAMETERS</span></span>

### <span data-ttu-id="6aec0-117">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="6aec0-117">-AadAudience</span></span>
<span data-ttu-id="6aec0-118">Аудитория AAD для проверки подлинности в P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="6aec0-118">AAD audience for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="6aec0-119">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="6aec0-119">-AadIssuer</span></span>
<span data-ttu-id="6aec0-120">Поставщик AAD для проверки подлинности в P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="6aec0-120">AAD issuer for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="6aec0-121">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="6aec0-121">-AadTenant</span></span>
<span data-ttu-id="6aec0-122">Клиент AAD для проверки подлинности в P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="6aec0-122">AAD tenant for P2S AAD authentication.</span></span>

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

### <span data-ttu-id="6aec0-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6aec0-123">-AsJob</span></span>
<span data-ttu-id="6aec0-124">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6aec0-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6aec0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aec0-125">-DefaultProfile</span></span>
<span data-ttu-id="6aec0-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6aec0-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6aec0-127">-Location</span><span class="sxs-lookup"><span data-stu-id="6aec0-127">-Location</span></span>
<span data-ttu-id="6aec0-128">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="6aec0-128">The resource location.</span></span>

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

### <span data-ttu-id="6aec0-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6aec0-129">-Name</span></span>
<span data-ttu-id="6aec0-130">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="6aec0-130">The resource name.</span></span>

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

### <span data-ttu-id="6aec0-131">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="6aec0-131">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="6aec0-132">Список путей к файлам RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6aec0-132">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="6aec0-133">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="6aec0-133">-RadiusServerAddress</span></span>
<span data-ttu-id="6aec0-134">Адрес внешнего RADIUS-сервера P2S.</span><span class="sxs-lookup"><span data-stu-id="6aec0-134">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="6aec0-135">-RadiusServerList</span><span class="sxs-lookup"><span data-stu-id="6aec0-135">-RadiusServerList</span></span>
<span data-ttu-id="6aec0-136">P2S внешние множественные RADIUS-серверы.</span><span class="sxs-lookup"><span data-stu-id="6aec0-136">P2S External multiple radius servers.</span></span>

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

### <span data-ttu-id="6aec0-137">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="6aec0-137">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="6aec0-138">Список путей к файлам RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="6aec0-138">A list of RadiusClientRootCertificate files' paths</span></span>

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

### <span data-ttu-id="6aec0-139">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="6aec0-139">-RadiusServerSecret</span></span>
<span data-ttu-id="6aec0-140">Секретный P2S внешнего RADIUS-сервера.</span><span class="sxs-lookup"><span data-stu-id="6aec0-140">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="6aec0-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6aec0-141">-ResourceGroupName</span></span>
<span data-ttu-id="6aec0-142">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6aec0-142">The resource group name.</span></span>

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

### <span data-ttu-id="6aec0-143">-Тег</span><span class="sxs-lookup"><span data-stu-id="6aec0-143">-Tag</span></span>
<span data-ttu-id="6aec0-144">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6aec0-144">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="6aec0-145">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="6aec0-145">-VpnAuthenticationType</span></span>
<span data-ttu-id="6aec0-146">Список туннельных протоколов клиента VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="6aec0-146">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="6aec0-147">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="6aec0-147">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="6aec0-148">Список политик IPSec для VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="6aec0-148">A list of IPSec policies for VpnServerConfiguration.</span></span>

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

### <span data-ttu-id="6aec0-149">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="6aec0-149">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="6aec0-150">Список VpnClientCertificates, по которым будут отменяться пути к файлам</span><span class="sxs-lookup"><span data-stu-id="6aec0-150">A list of VpnClientCertificates to be revoked files' paths</span></span>

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

### <span data-ttu-id="6aec0-151">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="6aec0-151">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="6aec0-152">Список VpnClientRootCertificates, в который нужно добавить пути к файлам</span><span class="sxs-lookup"><span data-stu-id="6aec0-152">A list of VpnClientRootCertificates to be added files' paths</span></span>

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

### <span data-ttu-id="6aec0-153">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="6aec0-153">-VpnProtocol</span></span>
<span data-ttu-id="6aec0-154">Список туннельных протоколов клиента VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="6aec0-154">The list of P2S VPN client tunneling protocols.</span></span>

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

### <span data-ttu-id="6aec0-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6aec0-155">-Confirm</span></span>
<span data-ttu-id="6aec0-156">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6aec0-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6aec0-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6aec0-157">-WhatIf</span></span>
<span data-ttu-id="6aec0-158">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6aec0-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6aec0-159">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6aec0-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6aec0-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aec0-160">CommonParameters</span></span>
<span data-ttu-id="6aec0-161">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6aec0-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aec0-162">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6aec0-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aec0-163">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6aec0-163">INPUTS</span></span>

### <span data-ttu-id="6aec0-164">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="6aec0-164">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="6aec0-165">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6aec0-165">OUTPUTS</span></span>

### <span data-ttu-id="6aec0-166">Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="6aec0-166">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="6aec0-167">Пуск</span><span class="sxs-lookup"><span data-stu-id="6aec0-167">NOTES</span></span>

## <span data-ttu-id="6aec0-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6aec0-168">RELATED LINKS</span></span>
