---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 2c995157b56bafb56df7b385c250b6f7c4fdd4e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991682"
---
# <span data-ttu-id="2d883-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="2d883-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="2d883-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d883-102">SYNOPSIS</span></span>
<span data-ttu-id="2d883-103">Изменяет учетную запись.</span><span class="sxs-lookup"><span data-stu-id="2d883-103">Modifies an account.</span></span>

## <span data-ttu-id="2d883-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2d883-104">SYNTAX</span></span>

### <span data-ttu-id="2d883-105">CognitiveServicesEncryption (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2d883-105">CognitiveServicesEncryption (Default)</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-CognitiveServicesEncryption] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-PublicNetworkAccess <String>] [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d883-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="2d883-106">KeyVaultEncryption</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d883-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d883-107">DESCRIPTION</span></span>
<span data-ttu-id="2d883-108">Командлет **Set-AzCognitiveServicesAccount** изменяет SKU или теги указанной учетной записи Службы восприятия.</span><span class="sxs-lookup"><span data-stu-id="2d883-108">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="2d883-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2d883-109">EXAMPLES</span></span>

### <span data-ttu-id="2d883-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2d883-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -SkuName S0


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WESTUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="2d883-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d883-111">PARAMETERS</span></span>

### <span data-ttu-id="2d883-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="2d883-112">-ApiProperty</span></span>
<span data-ttu-id="2d883-113">APIProperties учетной записи когнитивных служб.</span><span class="sxs-lookup"><span data-stu-id="2d883-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="2d883-114">Требуется для определенных типов учетных записей.</span><span class="sxs-lookup"><span data-stu-id="2d883-114">Required by specific account types.</span></span>

```yaml
Type: Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d883-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="2d883-115">-AssignIdentity</span></span>
<span data-ttu-id="2d883-116">Создание и назначение нового удостоверения учетной записи службы когнитивных услуг для этой учетной записи хранения для использования с ключевыми службами управления, например Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="2d883-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="2d883-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="2d883-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="2d883-118">Следует ли установить для ключа шифрования учетной записи службы когнитивных функций значение Microsoft.CognitiveServices или нет.</span><span class="sxs-lookup"><span data-stu-id="2d883-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CognitiveServicesEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d883-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="2d883-119">-CustomSubdomainName</span></span>
<span data-ttu-id="2d883-120">Имя поддомена учетной записи учетной записи Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="2d883-120">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="2d883-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d883-121">-DefaultProfile</span></span>
<span data-ttu-id="2d883-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2d883-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d883-123">-Force</span><span class="sxs-lookup"><span data-stu-id="2d883-123">-Force</span></span>
<span data-ttu-id="2d883-124">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="2d883-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2d883-125">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="2d883-125">-IdentityType</span></span>
<span data-ttu-id="2d883-126">Тип удостоверения управляемой службы.</span><span class="sxs-lookup"><span data-stu-id="2d883-126">Type of managed service identity.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.CognitiveServices.Models.IdentityType]
Parameter Sets: (All)
Aliases:
Accepted values: None, SystemAssigned, UserAssigned

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d883-127">-KeyName</span><span class="sxs-lookup"><span data-stu-id="2d883-127">-KeyName</span></span>
<span data-ttu-id="2d883-128">Cognitive Services Account encryption keySource KeyVault KeyName</span><span class="sxs-lookup"><span data-stu-id="2d883-128">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

```yaml
Type: System.String
Parameter Sets: KeyVaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d883-129">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="2d883-129">-KeyVaultEncryption</span></span>
<span data-ttu-id="2d883-130">Следует ли установить для ключа шифрования учетной записи службы восприятия значение Microsoft.KeyVault или нет.</span><span class="sxs-lookup"><span data-stu-id="2d883-130">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="2d883-131">Если указать KeyName, KeyVersion и KeyVaultUri, то для параметра Encryption KeySource учетной записи учетной записи Службы распознавания данных будет также задан параметр Microsoft.KeyVault, заданный или нет.</span><span class="sxs-lookup"><span data-stu-id="2d883-131">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: KeyVaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d883-132">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="2d883-132">-KeyVaultUri</span></span>
<span data-ttu-id="2d883-133">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="2d883-133">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

```yaml
Type: System.String
Parameter Sets: KeyVaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d883-134">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="2d883-134">-KeyVersion</span></span>
<span data-ttu-id="2d883-135">Клавиши шифрования keyVault KeyVault для учетной записи службы</span><span class="sxs-lookup"><span data-stu-id="2d883-135">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

```yaml
Type: System.String
Parameter Sets: KeyVaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d883-136">-Name</span><span class="sxs-lookup"><span data-stu-id="2d883-136">-Name</span></span>
<span data-ttu-id="2d883-137">Указывает имя изменяемой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="2d883-137">Specifies the name of the account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d883-138">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="2d883-138">-NetworkRuleSet</span></span>
<span data-ttu-id="2d883-139">NetworkRuleSet используется для определения набора правил конфигурации для брандмауэров и виртуальных сетей, а также для настройки значений для свойств сети, таких как обработка запросов, несо совпадений с определенными правилами</span><span class="sxs-lookup"><span data-stu-id="2d883-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d883-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="2d883-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="2d883-141">Тип доступа к сети для учетной записи службы восприятия.</span><span class="sxs-lookup"><span data-stu-id="2d883-141">The network access type for Cognitive Services Account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d883-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d883-142">-ResourceGroupName</span></span>
<span data-ttu-id="2d883-143">Имя группы ресурсов, назначенной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="2d883-143">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d883-144">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2d883-144">-SkuName</span></span>
<span data-ttu-id="2d883-145">Определяет SKU учетной записи.</span><span class="sxs-lookup"><span data-stu-id="2d883-145">Specifies the SKU for the account.</span></span>
<span data-ttu-id="2d883-146">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="2d883-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2d883-147">F0 (бесплатный уровень)</span><span class="sxs-lookup"><span data-stu-id="2d883-147">F0 (free tier)</span></span>
- <span data-ttu-id="2d883-148">S0</span><span class="sxs-lookup"><span data-stu-id="2d883-148">S0</span></span>
- <span data-ttu-id="2d883-149">S1</span><span class="sxs-lookup"><span data-stu-id="2d883-149">S1</span></span>
- <span data-ttu-id="2d883-150">S2</span><span class="sxs-lookup"><span data-stu-id="2d883-150">S2</span></span>
- <span data-ttu-id="2d883-151">S3</span><span class="sxs-lookup"><span data-stu-id="2d883-151">S3</span></span>
- <span data-ttu-id="2d883-152">S4</span><span class="sxs-lookup"><span data-stu-id="2d883-152">S4</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d883-153">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="2d883-153">-StorageAccountId</span></span>
<span data-ttu-id="2d883-154">Список пользовательских учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="2d883-154">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="2d883-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="2d883-155">-Tag</span></span>
<span data-ttu-id="2d883-156">Указывает тег как пару "имя/значение".</span><span class="sxs-lookup"><span data-stu-id="2d883-156">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d883-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d883-157">-Confirm</span></span>
<span data-ttu-id="2d883-158">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="2d883-158">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d883-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d883-159">-WhatIf</span></span>
<span data-ttu-id="2d883-160">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d883-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d883-161">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2d883-161">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d883-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d883-162">CommonParameters</span></span>
<span data-ttu-id="2d883-163">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d883-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d883-164">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d883-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d883-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2d883-165">INPUTS</span></span>

### <span data-ttu-id="2d883-166">System.String</span><span class="sxs-lookup"><span data-stu-id="2d883-166">System.String</span></span>

### <span data-ttu-id="2d883-167">System.Collections.Hashtable[]</span><span class="sxs-lookup"><span data-stu-id="2d883-167">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="2d883-168">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2d883-168">OUTPUTS</span></span>

### <span data-ttu-id="2d883-169">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="2d883-169">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="2d883-170">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2d883-170">NOTES</span></span>

## <span data-ttu-id="2d883-171">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d883-171">RELATED LINKS</span></span>

[<span data-ttu-id="2d883-172">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="2d883-172">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="2d883-173">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="2d883-173">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="2d883-174">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="2d883-174">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
