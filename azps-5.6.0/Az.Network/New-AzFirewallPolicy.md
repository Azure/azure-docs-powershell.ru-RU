---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicy.md
ms.openlocfilehash: 3e60546992957a027dd5bbb94281e19e74e42274
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976691"
---
# <span data-ttu-id="9b1e3-101">New-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="9b1e3-101">New-AzFirewallPolicy</span></span>

## <span data-ttu-id="9b1e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b1e3-102">SYNOPSIS</span></span>
<span data-ttu-id="9b1e3-103">Создание политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="9b1e3-103">Creates a new Azure Firewall Policy</span></span>

## <span data-ttu-id="9b1e3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9b1e3-104">SYNTAX</span></span>

```
New-AzFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String> [-ThreatIntelMode <String>]
 [-ThreatIntelWhitelist <PSAzureFirewallPolicyThreatIntelWhitelist>] [-BasePolicy <String>]
 [-DnsSetting <PSAzureFirewallPolicyDnsSettings>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-IntrusionDetection <PSAzureFirewallPolicyIntrusionDetection>] [-TransportSecurityName <String>]
 [-TransportSecurityKeyVaultSecretId <String>] [-SkuTier <String>] [-UserAssignedIdentityId <String>]
 [-Identity <PSManagedServiceIdentity>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b1e3-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9b1e3-105">DESCRIPTION</span></span>
<span data-ttu-id="9b1e3-106">С **помощью cmdlet New-AzFirewallPolicy** создается политика брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="9b1e3-106">The **New-AzFirewallPolicy** cmdlet creates an Azure Firewall Policy.</span></span>

## <span data-ttu-id="9b1e3-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9b1e3-107">EXAMPLES</span></span>

### <span data-ttu-id="9b1e3-108">Пример 1: 1.</span><span class="sxs-lookup"><span data-stu-id="9b1e3-108">Example 1: 1.</span></span> <span data-ttu-id="9b1e3-109">Создание пустой политики</span><span class="sxs-lookup"><span data-stu-id="9b1e3-109">Create an empty policy</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg
```

<span data-ttu-id="9b1e3-110">В этом примере создается политика брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="9b1e3-110">This example creates an azure firewall policy</span></span>

### <span data-ttu-id="9b1e3-111">Пример 2: 2.</span><span class="sxs-lookup"><span data-stu-id="9b1e3-111">Example 2: 2.</span></span> <span data-ttu-id="9b1e3-112">Создание пустой политики в режиме ThreatIntel</span><span class="sxs-lookup"><span data-stu-id="9b1e3-112">Create an empty policy with ThreatIntel Mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelMode "Deny"
```

<span data-ttu-id="9b1e3-113">В этом примере создается политика брандмауэра Azure с режимом intel-угрозы</span><span class="sxs-lookup"><span data-stu-id="9b1e3-113">This example creates an azure firewall policy with a threat intel mode</span></span>

### <span data-ttu-id="9b1e3-114">Пример 3: 3.</span><span class="sxs-lookup"><span data-stu-id="9b1e3-114">Example 3: 3.</span></span> <span data-ttu-id="9b1e3-115">Создание пустой политики с белым списком ThreatIntel</span><span class="sxs-lookup"><span data-stu-id="9b1e3-115">Create an empty policy with ThreatIntel Whitelist</span></span>
```powershell
PS C:\> $threatIntelWhitelist = New-AzFirewallPolicyThreatIntelWhitelist -IpAddress 23.46.72.91,192.79.236.79 -FQDN microsoft.com
PS C:\> New-AzFirewallPolicy -Name fp1 -ResourceGroupName TestRg -ThreatIntelWhitelist $threatIntelWhitelist
```

<span data-ttu-id="9b1e3-116">В этом примере создается политика брандмауэра Azure с белым списком угроз Intel</span><span class="sxs-lookup"><span data-stu-id="9b1e3-116">This example creates an azure firewall policy with a threat intel whitelist</span></span>

### <span data-ttu-id="9b1e3-117">Пример 4: 4.</span><span class="sxs-lookup"><span data-stu-id="9b1e3-117">Example 4: 4.</span></span> <span data-ttu-id="9b1e3-118">Создание политики с обнаружением назойки, удостоверениями и безопасностью транспорта</span><span class="sxs-lookup"><span data-stu-id="9b1e3-118">Create policy with intrusion detection, identity and transport security</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> $intrusionDetection = New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride -BypassTraffic $bypass
PS C:\> $userAssignedIdentity = '/subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourcegroups/TestRg/providers/Microsoft.ManagedIdentity/userAssignedIdentities/user-assign-identity'
PS C:\> New-AzFirewallPolicy -Name fp1 -Location "westus2" -ResourceGroup TestRg -SkuTier "Premium" -IntrusionDetection $intrusionDetection -TransportSecurityName tsName -TransportSecurityKeyVaultSecretId "https://<keyvaultname>.vault.azure.net/secrets/cacert"  -UserAssignedIdentityId $userAssignedIdentity
```

<span data-ttu-id="9b1e3-119">В этом примере создается политика брандмауэра Azure с обнаружением назойки в режиме оповещения, удостоверением пользователя и безопасностью транспорта.</span><span class="sxs-lookup"><span data-stu-id="9b1e3-119">This example creates an azure firewall policy with a intrusion detection in mode alert, user assigned identity and transport security</span></span>

## <span data-ttu-id="9b1e3-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b1e3-120">PARAMETERS</span></span>

### <span data-ttu-id="9b1e3-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b1e3-121">-AsJob</span></span>
<span data-ttu-id="9b1e3-122">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9b1e3-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b1e3-123">-BasePolicy</span><span class="sxs-lookup"><span data-stu-id="9b1e3-123">-BasePolicy</span></span>
<span data-ttu-id="9b1e3-124">Базовая политика, наследуемая от</span><span class="sxs-lookup"><span data-stu-id="9b1e3-124">The base policy to inherit from</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b1e3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b1e3-125">-DefaultProfile</span></span>
<span data-ttu-id="9b1e3-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9b1e3-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b1e3-127">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="9b1e3-127">-DnsSetting</span></span>
<span data-ttu-id="9b1e3-128">Параметр DNS</span><span class="sxs-lookup"><span data-stu-id="9b1e3-128">The DNS Setting</span></span>

```yaml
Type: PSAzureFirewallPolicyDnsSettings
Parameter Sets: (All)
Aliases:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b1e3-129">-Force</span><span class="sxs-lookup"><span data-stu-id="9b1e3-129">-Force</span></span>
<span data-ttu-id="9b1e3-130">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="9b1e3-130">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="9b1e3-131">-Identity</span><span class="sxs-lookup"><span data-stu-id="9b1e3-131">-Identity</span></span>
<span data-ttu-id="9b1e3-132">Удостоверение политики брандмауэра, назначенное политике брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="9b1e3-132">Firewall Policy Identity to be assigned to Firewall Policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b1e3-133">-IntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="9b1e3-133">-IntrusionDetection</span></span>
<span data-ttu-id="9b1e3-134">Параметр обнаружения intrusion</span><span class="sxs-lookup"><span data-stu-id="9b1e3-134">The Intrusion Detection Setting</span></span>

```yaml
Type: PSAzureFirewallPolicyIntrusionDetection
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b1e3-135">-Location</span><span class="sxs-lookup"><span data-stu-id="9b1e3-135">-Location</span></span>
<span data-ttu-id="9b1e3-136">расположение.</span><span class="sxs-lookup"><span data-stu-id="9b1e3-136">location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b1e3-137">-Name</span><span class="sxs-lookup"><span data-stu-id="9b1e3-137">-Name</span></span>
<span data-ttu-id="9b1e3-138">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="9b1e3-138">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b1e3-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b1e3-139">-ResourceGroupName</span></span>
<span data-ttu-id="9b1e3-140">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9b1e3-140">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b1e3-141">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="9b1e3-141">-SkuTier</span></span>
<span data-ttu-id="9b1e3-142">Уровень SKU политики брандмауэра</span><span class="sxs-lookup"><span data-stu-id="9b1e3-142">Firewall policy sku tier</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b1e3-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="9b1e3-143">-Tag</span></span>
<span data-ttu-id="9b1e3-144">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="9b1e3-144">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b1e3-145">-ThreatIntelMode</span><span class="sxs-lookup"><span data-stu-id="9b1e3-145">-ThreatIntelMode</span></span>
<span data-ttu-id="9b1e3-146">Режим операции для Threat Intelligence.</span><span class="sxs-lookup"><span data-stu-id="9b1e3-146">The operation mode for Threat Intelligence.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Alert, Deny, Off

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9b1e3-147">-ThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="9b1e3-147">-ThreatIntelWhitelist</span></span>
<span data-ttu-id="9b1e3-148">Белый список для Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="9b1e3-148">The whitelist for Threat Intelligence</span></span>

```yaml
Type: PSAzureFirewallPolicyThreatIntelWhitelist
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b1e3-149">-TransportSecurityKeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="9b1e3-149">-TransportSecurityKeyVaultSecretId</span></span>
<span data-ttu-id="9b1e3-150">Секретный код (зашифрованный незашифрованный объект pfx с кодом base-64) "Секрет" или "Сертификат", который хранится в KeyVault</span><span class="sxs-lookup"><span data-stu-id="9b1e3-150">Secret Id of (base-64 encoded unencrypted pfx) 'Secret' or 'Certificate' object stored in KeyVault</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b1e3-151">-TransportSecurityName</span><span class="sxs-lookup"><span data-stu-id="9b1e3-151">-TransportSecurityName</span></span>
<span data-ttu-id="9b1e3-152">Имя безопасности транспорта</span><span class="sxs-lookup"><span data-stu-id="9b1e3-152">Transport security name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b1e3-153">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="9b1e3-153">-UserAssignedIdentityId</span></span>
<span data-ttu-id="9b1e3-154">ResourceId идентификатора пользователя, назначенного политике брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="9b1e3-154">ResourceId of the user assigned identity to be assigned to Firewall Policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: UserAssignedIdentity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b1e3-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9b1e3-155">-Confirm</span></span>
<span data-ttu-id="9b1e3-156">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b1e3-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b1e3-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b1e3-157">-WhatIf</span></span>
<span data-ttu-id="9b1e3-158">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b1e3-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b1e3-159">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9b1e3-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b1e3-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b1e3-160">CommonParameters</span></span>
<span data-ttu-id="9b1e3-161">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b1e3-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b1e3-162">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b1e3-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b1e3-163">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9b1e3-163">INPUTS</span></span>

### <span data-ttu-id="9b1e3-164">System.String</span><span class="sxs-lookup"><span data-stu-id="9b1e3-164">System.String</span></span>

### <span data-ttu-id="9b1e3-165">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="9b1e3-165">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9b1e3-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9b1e3-166">OUTPUTS</span></span>

### <span data-ttu-id="9b1e3-167">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="9b1e3-167">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="9b1e3-168">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9b1e3-168">NOTES</span></span>

## <span data-ttu-id="9b1e3-169">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9b1e3-169">RELATED LINKS</span></span>
