---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 5cfbfa0452fba4d01d2af5aa8e6acc3a141a4426
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509285"
---
# <span data-ttu-id="22de4-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="22de4-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="22de4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22de4-102">SYNOPSIS</span></span>
<span data-ttu-id="22de4-103">Изменяет учетную запись.</span><span class="sxs-lookup"><span data-stu-id="22de4-103">Modifies an account.</span></span>

## <span data-ttu-id="22de4-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="22de4-104">SYNTAX</span></span>

### <span data-ttu-id="22de4-105">CognitiveServicesEncryption (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="22de4-105">CognitiveServicesEncryption (Default)</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-CognitiveServicesEncryption] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-PublicNetworkAccess <String>] [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22de4-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="22de4-106">KeyVaultEncryption</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22de4-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="22de4-107">DESCRIPTION</span></span>
<span data-ttu-id="22de4-108">Командлет **Set-AzCognitiveServicesAccount** изменяет SKU или теги указанной учетной записи Службы восприятия.</span><span class="sxs-lookup"><span data-stu-id="22de4-108">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="22de4-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="22de4-109">EXAMPLES</span></span>

### <span data-ttu-id="22de4-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="22de4-110">Example 1</span></span>
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

## <span data-ttu-id="22de4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22de4-111">PARAMETERS</span></span>

### <span data-ttu-id="22de4-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="22de4-112">-ApiProperty</span></span>
<span data-ttu-id="22de4-113">APIProperties учетной записи когнитивных служб.</span><span class="sxs-lookup"><span data-stu-id="22de4-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="22de4-114">Требуется для определенных типов учетных записей.</span><span class="sxs-lookup"><span data-stu-id="22de4-114">Required by specific account types.</span></span>

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

### <span data-ttu-id="22de4-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="22de4-115">-AssignIdentity</span></span>
<span data-ttu-id="22de4-116">Создание и назначение нового удостоверения учетной записи службы когнитивных услуг для этой учетной записи хранения для использования с ключевыми службами управления, например Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="22de4-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="22de4-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="22de4-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="22de4-118">Следует ли установить для ключа шифрования учетной записи службы когнитивных функций значение Microsoft.CognitiveServices или нет.</span><span class="sxs-lookup"><span data-stu-id="22de4-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="22de4-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="22de4-119">-CustomSubdomainName</span></span>
<span data-ttu-id="22de4-120">Имя поддомена учетной записи учетной записи Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="22de4-120">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="22de4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22de4-121">-DefaultProfile</span></span>
<span data-ttu-id="22de4-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="22de4-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22de4-123">-Force</span><span class="sxs-lookup"><span data-stu-id="22de4-123">-Force</span></span>
<span data-ttu-id="22de4-124">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="22de4-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="22de4-125">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="22de4-125">-IdentityType</span></span>
<span data-ttu-id="22de4-126">Тип управляемого удостоверения службы.</span><span class="sxs-lookup"><span data-stu-id="22de4-126">Type of managed service identity.</span></span>

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

### <span data-ttu-id="22de4-127">-KeyName</span><span class="sxs-lookup"><span data-stu-id="22de4-127">-KeyName</span></span>
<span data-ttu-id="22de4-128">Cognitive Services Account encryption keySource KeyVault KeyName</span><span class="sxs-lookup"><span data-stu-id="22de4-128">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="22de4-129">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="22de4-129">-KeyVaultEncryption</span></span>
<span data-ttu-id="22de4-130">Следует ли установить ключ шифрования учетной записи службы в Microsoft.KeyVault или нет.</span><span class="sxs-lookup"><span data-stu-id="22de4-130">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="22de4-131">Если указать KeyName, KeyVersion и KeyVaultUri, то для параметра Encryption KeySource учетной записи учетной записи Службы распознавания данных будет также задан параметр Microsoft.KeyVault, заданный или нет.</span><span class="sxs-lookup"><span data-stu-id="22de4-131">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="22de4-132">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="22de4-132">-KeyVaultUri</span></span>
<span data-ttu-id="22de4-133">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="22de4-133">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="22de4-134">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="22de4-134">-KeyVersion</span></span>
<span data-ttu-id="22de4-135">Клавиша шифрования KeyVault KeyVault keyVersion учетной записи службы</span><span class="sxs-lookup"><span data-stu-id="22de4-135">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="22de4-136">-Name</span><span class="sxs-lookup"><span data-stu-id="22de4-136">-Name</span></span>
<span data-ttu-id="22de4-137">Указывает имя изменяемой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="22de4-137">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="22de4-138">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="22de4-138">-NetworkRuleSet</span></span>
<span data-ttu-id="22de4-139">NetworkRuleSet используется для определения набора правил конфигурации для брандмауэров и виртуальных сетей, а также для настройки значений для свойств сети, таких как обработка запросов, несо совпадений с определенными правилами</span><span class="sxs-lookup"><span data-stu-id="22de4-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="22de4-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="22de4-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="22de4-141">Тип доступа к сети для учетной записи службы восприятия.</span><span class="sxs-lookup"><span data-stu-id="22de4-141">The network access type for Cognitive Services Account.</span></span>

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

### <span data-ttu-id="22de4-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22de4-142">-ResourceGroupName</span></span>
<span data-ttu-id="22de4-143">Имя группы ресурсов, назначенной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="22de4-143">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="22de4-144">-SkuName</span><span class="sxs-lookup"><span data-stu-id="22de4-144">-SkuName</span></span>
<span data-ttu-id="22de4-145">Указывает SKU учетной записи.</span><span class="sxs-lookup"><span data-stu-id="22de4-145">Specifies the SKU for the account.</span></span>
<span data-ttu-id="22de4-146">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="22de4-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="22de4-147">F0 (бесплатный уровень)</span><span class="sxs-lookup"><span data-stu-id="22de4-147">F0 (free tier)</span></span>
- <span data-ttu-id="22de4-148">S0</span><span class="sxs-lookup"><span data-stu-id="22de4-148">S0</span></span>
- <span data-ttu-id="22de4-149">S1</span><span class="sxs-lookup"><span data-stu-id="22de4-149">S1</span></span>
- <span data-ttu-id="22de4-150">S2</span><span class="sxs-lookup"><span data-stu-id="22de4-150">S2</span></span>
- <span data-ttu-id="22de4-151">S3</span><span class="sxs-lookup"><span data-stu-id="22de4-151">S3</span></span>
- <span data-ttu-id="22de4-152">S4</span><span class="sxs-lookup"><span data-stu-id="22de4-152">S4</span></span>

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

### <span data-ttu-id="22de4-153">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="22de4-153">-StorageAccountId</span></span>
<span data-ttu-id="22de4-154">Список пользовательских учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="22de4-154">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="22de4-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="22de4-155">-Tag</span></span>
<span data-ttu-id="22de4-156">Указывает тег как пару "имя и значение".</span><span class="sxs-lookup"><span data-stu-id="22de4-156">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="22de4-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="22de4-157">-Confirm</span></span>
<span data-ttu-id="22de4-158">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22de4-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22de4-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22de4-159">-WhatIf</span></span>
<span data-ttu-id="22de4-160">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22de4-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22de4-161">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="22de4-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22de4-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22de4-162">CommonParameters</span></span>
<span data-ttu-id="22de4-163">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22de4-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22de4-164">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22de4-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22de4-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="22de4-165">INPUTS</span></span>

### <span data-ttu-id="22de4-166">System.String</span><span class="sxs-lookup"><span data-stu-id="22de4-166">System.String</span></span>

### <span data-ttu-id="22de4-167">System.Collections.Hashtable[]</span><span class="sxs-lookup"><span data-stu-id="22de4-167">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="22de4-168">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="22de4-168">OUTPUTS</span></span>

### <span data-ttu-id="22de4-169">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="22de4-169">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="22de4-170">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="22de4-170">NOTES</span></span>

## <span data-ttu-id="22de4-171">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="22de4-171">RELATED LINKS</span></span>

[<span data-ttu-id="22de4-172">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="22de4-172">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="22de4-173">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="22de4-173">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="22de4-174">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="22de4-174">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
