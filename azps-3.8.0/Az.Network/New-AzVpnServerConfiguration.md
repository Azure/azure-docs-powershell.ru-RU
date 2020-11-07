---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVpnServerConfiguration.md
ms.openlocfilehash: de0806585cee16eed19291766ab29696a9a1b960
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912576"
---
# <span data-ttu-id="4fc32-101">New-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fc32-101">New-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="4fc32-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4fc32-102">SYNOPSIS</span></span>
<span data-ttu-id="4fc32-103">Создайте новый VpnServerConfiguration для подключения к сайту.</span><span class="sxs-lookup"><span data-stu-id="4fc32-103">Create a new VpnServerConfiguration for point to site connectivity.</span></span>

## <span data-ttu-id="4fc32-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4fc32-104">SYNTAX</span></span>

### <span data-ttu-id="4fc32-105">ByVpnServerConfigurationNameByCertificateAuthentication (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4fc32-105">ByVpnServerConfigurationNameByCertificateAuthentication (Default)</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-VpnClientRootCertificateFilesList <String[]>]
 [-VpnClientRevokedCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4fc32-106">ByVpnServerConfigurationNameByRadiusAuthentication</span><span class="sxs-lookup"><span data-stu-id="4fc32-106">ByVpnServerConfigurationNameByRadiusAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-RadiusServerRootCertificateFilesList <String[]>]
 [-RadiusClientRootCertificateFilesList <String[]>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4fc32-107">ByVpnServerConfigurationNameByAadAuthentication</span><span class="sxs-lookup"><span data-stu-id="4fc32-107">ByVpnServerConfigurationNameByAadAuthentication</span></span>
```
New-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> -Location <String>
 [-VpnProtocol <String[]>] [-VpnAuthenticationType <String[]>] [-AadTenant <String>] [-AadAudience <String>]
 [-AadIssuer <String>] [-VpnClientIpsecPolicy <PSIpsecPolicy[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fc32-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4fc32-108">DESCRIPTION</span></span>
<span data-ttu-id="4fc32-109">С помощью командлета **New-AzVpnServerConfiguration** можно создавать новые VpnServerConfiguration с разными VpnProtocols, VpnAuthenticationTypes, IpsecPolicies и настраивать выбранные параметры проверки подлинности VPN в соответствии с требованием клиента для указания на подключение к сайту.</span><span class="sxs-lookup"><span data-stu-id="4fc32-109">The **New-AzVpnServerConfiguration** cmdlet enables you to create a new VpnServerConfiguration with different VpnProtocols, VpnAuthenticationTypes, IpsecPolicies and to set selected vpn authentication type related parameters as  per the customer's requirement for Point to site connectivity.</span></span>

## <span data-ttu-id="4fc32-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4fc32-110">EXAMPLES</span></span>

### <span data-ttu-id="4fc32-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4fc32-111">Example 1</span></span>
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

<span data-ttu-id="4fc32-112">Вышеприведенная команда создаст новый VpnServerConfiguration с VpnAuthenticationType в качестве сертификата.</span><span class="sxs-lookup"><span data-stu-id="4fc32-112">The above command will create a new VpnServerConfiguration with VpnAuthenticationType as Certificate.</span></span>

## <span data-ttu-id="4fc32-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4fc32-113">PARAMETERS</span></span>

### <span data-ttu-id="4fc32-114">-AadAudience</span><span class="sxs-lookup"><span data-stu-id="4fc32-114">-AadAudience</span></span>
<span data-ttu-id="4fc32-115">Аудитория AAD для проверки подлинности в P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="4fc32-115">AAD audience for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc32-116">-AadIssuer</span><span class="sxs-lookup"><span data-stu-id="4fc32-116">-AadIssuer</span></span>
<span data-ttu-id="4fc32-117">Поставщик AAD для проверки подлинности в P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="4fc32-117">AAD issuer for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc32-118">-AadTenant</span><span class="sxs-lookup"><span data-stu-id="4fc32-118">-AadTenant</span></span>
<span data-ttu-id="4fc32-119">Клиент AAD для проверки подлинности в P2S AAD.</span><span class="sxs-lookup"><span data-stu-id="4fc32-119">AAD tenant for P2S AAD authentication.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByAadAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc32-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4fc32-120">-AsJob</span></span>
<span data-ttu-id="4fc32-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4fc32-121">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc32-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fc32-122">-DefaultProfile</span></span>
<span data-ttu-id="4fc32-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4fc32-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc32-124">-Location</span><span class="sxs-lookup"><span data-stu-id="4fc32-124">-Location</span></span>
<span data-ttu-id="4fc32-125">Расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="4fc32-125">The resource location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc32-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4fc32-126">-Name</span></span>
<span data-ttu-id="4fc32-127">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="4fc32-127">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc32-128">-RadiusClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="4fc32-128">-RadiusClientRootCertificateFilesList</span></span>
<span data-ttu-id="4fc32-129">Список путей к файлам RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4fc32-129">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc32-130">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="4fc32-130">-RadiusServerAddress</span></span>
<span data-ttu-id="4fc32-131">Адрес внешнего RADIUS-сервера P2S.</span><span class="sxs-lookup"><span data-stu-id="4fc32-131">P2S External Radius server address.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc32-132">-RadiusServerRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="4fc32-132">-RadiusServerRootCertificateFilesList</span></span>
<span data-ttu-id="4fc32-133">Список путей к файлам RadiusClientRootCertificate</span><span class="sxs-lookup"><span data-stu-id="4fc32-133">A list of RadiusClientRootCertificate files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc32-134">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="4fc32-134">-RadiusServerSecret</span></span>
<span data-ttu-id="4fc32-135">Секретный P2S внешнего RADIUS-сервера.</span><span class="sxs-lookup"><span data-stu-id="4fc32-135">P2S External Radius server secret.</span></span>

```yaml
Type: SecureString
Parameter Sets: ByVpnServerConfigurationNameByRadiusAuthentication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc32-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fc32-136">-ResourceGroupName</span></span>
<span data-ttu-id="4fc32-137">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4fc32-137">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc32-138">-Тег</span><span class="sxs-lookup"><span data-stu-id="4fc32-138">-Tag</span></span>
<span data-ttu-id="4fc32-139">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4fc32-139">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc32-140">-VpnAuthenticationType</span><span class="sxs-lookup"><span data-stu-id="4fc32-140">-VpnAuthenticationType</span></span>
<span data-ttu-id="4fc32-141">Список туннельных протоколов клиента VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="4fc32-141">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: Certificate, Radius, AAD

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc32-142">-VpnClientIpsecPolicy</span><span class="sxs-lookup"><span data-stu-id="4fc32-142">-VpnClientIpsecPolicy</span></span>
<span data-ttu-id="4fc32-143">Список политик IPSec для VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="4fc32-143">A list of IPSec policies for VpnServerConfiguration.</span></span>

```yaml
Type: PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fc32-144">-VpnClientRevokedCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="4fc32-144">-VpnClientRevokedCertificateFilesList</span></span>
<span data-ttu-id="4fc32-145">Список VpnClientCertificates, по которым будут отменяться пути к файлам</span><span class="sxs-lookup"><span data-stu-id="4fc32-145">A list of VpnClientCertificates to be revoked files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc32-146">-VpnClientRootCertificateFilesList</span><span class="sxs-lookup"><span data-stu-id="4fc32-146">-VpnClientRootCertificateFilesList</span></span>
<span data-ttu-id="4fc32-147">Список VpnClientRootCertificates, в который нужно добавить пути к файлам</span><span class="sxs-lookup"><span data-stu-id="4fc32-147">A list of VpnClientRootCertificates to be added files' paths</span></span>

```yaml
Type: String[]
Parameter Sets: ByVpnServerConfigurationNameByCertificateAuthentication
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc32-148">-VpnProtocol</span><span class="sxs-lookup"><span data-stu-id="4fc32-148">-VpnProtocol</span></span>
<span data-ttu-id="4fc32-149">Список туннельных протоколов клиента VPN P2S.</span><span class="sxs-lookup"><span data-stu-id="4fc32-149">The list of P2S VPN client tunneling protocols.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: IkeV2, OpenVPN

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc32-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4fc32-150">-Confirm</span></span>
<span data-ttu-id="4fc32-151">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4fc32-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc32-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fc32-152">-WhatIf</span></span>
<span data-ttu-id="4fc32-153">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4fc32-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fc32-154">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4fc32-154">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc32-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fc32-155">CommonParameters</span></span>
<span data-ttu-id="4fc32-156">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4fc32-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fc32-157">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fc32-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fc32-158">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4fc32-158">INPUTS</span></span>

### <span data-ttu-id="4fc32-159">Microsoft. Azure. Commands. Network. Models. PSIpsecPolicy []</span><span class="sxs-lookup"><span data-stu-id="4fc32-159">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

## <span data-ttu-id="4fc32-160">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4fc32-160">OUTPUTS</span></span>

### <span data-ttu-id="4fc32-161">Microsoft. Azure. Commands. Network. Models. PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="4fc32-161">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>

## <span data-ttu-id="4fc32-162">Пуск</span><span class="sxs-lookup"><span data-stu-id="4fc32-162">NOTES</span></span>

## <span data-ttu-id="4fc32-163">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4fc32-163">RELATED LINKS</span></span>
