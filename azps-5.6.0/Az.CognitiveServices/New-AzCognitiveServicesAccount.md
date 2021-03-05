---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: e6ed6669c98a54a037bcbdc579e08459cdff568e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981203"
---
# <span data-ttu-id="aa708-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="aa708-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="aa708-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa708-102">SYNOPSIS</span></span>
<span data-ttu-id="aa708-103">Создает учетную запись когнитивных служб.</span><span class="sxs-lookup"><span data-stu-id="aa708-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="aa708-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="aa708-104">SYNTAX</span></span>

### <span data-ttu-id="aa708-105">CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="aa708-105">CognitiveServicesEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-CognitiveServicesEncryption]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa708-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="aa708-106">KeyVaultEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa708-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa708-107">DESCRIPTION</span></span>
<span data-ttu-id="aa708-108">С **помощью cmdlet New-AzCognitiveServicesAccount** создается учетная запись Службы восприятия с указанным типом и номером SKU.</span><span class="sxs-lookup"><span data-stu-id="aa708-108">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="aa708-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="aa708-109">EXAMPLES</span></span>

### <span data-ttu-id="aa708-110">1:</span><span class="sxs-lookup"><span data-stu-id="aa708-110">1:</span></span>
```
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locatio
n 'WestUS'


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WestUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="aa708-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa708-111">PARAMETERS</span></span>

### <span data-ttu-id="aa708-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="aa708-112">-ApiProperty</span></span>
<span data-ttu-id="aa708-113">APIProperties учетной записи когнитивных служб.</span><span class="sxs-lookup"><span data-stu-id="aa708-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="aa708-114">Требуется для определенных типов учетных записей.</span><span class="sxs-lookup"><span data-stu-id="aa708-114">Required by specific account types.</span></span>

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

### <span data-ttu-id="aa708-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="aa708-115">-AssignIdentity</span></span>
<span data-ttu-id="aa708-116">Создание и назначение нового удостоверения учетной записи службы когнитивных услуг для этой учетной записи хранения для использования с ключевыми службами управления, например Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="aa708-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="aa708-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="aa708-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="aa708-118">Следует ли установить для ключа шифрования учетной записи службы когнитивных функций значение Microsoft.CognitiveServices или нет.</span><span class="sxs-lookup"><span data-stu-id="aa708-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="aa708-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="aa708-119">-CustomSubdomainName</span></span>
<span data-ttu-id="aa708-120">Имя поддомена учетной записи учетной записи Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="aa708-120">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="aa708-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa708-121">-DefaultProfile</span></span>
<span data-ttu-id="aa708-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="aa708-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa708-123">-Force</span><span class="sxs-lookup"><span data-stu-id="aa708-123">-Force</span></span>
<span data-ttu-id="aa708-124">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="aa708-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aa708-125">-KeyName</span><span class="sxs-lookup"><span data-stu-id="aa708-125">-KeyName</span></span>
<span data-ttu-id="aa708-126">Cognitive Services Account encryption keySource KeyVault KeyName</span><span class="sxs-lookup"><span data-stu-id="aa708-126">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="aa708-127">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="aa708-127">-KeyVaultEncryption</span></span>
<span data-ttu-id="aa708-128">Следует ли установить ключ шифрования учетной записи службы в Microsoft.KeyVault или нет.</span><span class="sxs-lookup"><span data-stu-id="aa708-128">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="aa708-129">Если указать KeyName, KeyVersion и KeyVaultUri, то для параметра Encryption KeySource учетной записи учетной записи Службы распознавания данных будет также задан параметр Microsoft.KeyVault, задан или нет.</span><span class="sxs-lookup"><span data-stu-id="aa708-129">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="aa708-130">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="aa708-130">-KeyVaultUri</span></span>
<span data-ttu-id="aa708-131">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="aa708-131">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="aa708-132">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="aa708-132">-KeyVersion</span></span>
<span data-ttu-id="aa708-133">Клавиша шифрования KeyVault KeyVault keyVersion учетной записи службы</span><span class="sxs-lookup"><span data-stu-id="aa708-133">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="aa708-134">-Location</span><span class="sxs-lookup"><span data-stu-id="aa708-134">-Location</span></span>
<span data-ttu-id="aa708-135">Определяет расположение, в котором нужно создать учетную запись.</span><span class="sxs-lookup"><span data-stu-id="aa708-135">Specifies the location in which to create the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa708-136">-Name</span><span class="sxs-lookup"><span data-stu-id="aa708-136">-Name</span></span>
<span data-ttu-id="aa708-137">Указывает имя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="aa708-137">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="aa708-138">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="aa708-138">-NetworkRuleSet</span></span>
<span data-ttu-id="aa708-139">NetworkRuleSet используется для определения набора правил конфигурации для брандмауэров и виртуальных сетей, а также для настройки значений для свойств сети, таких как обработка запросов, несо совпадений с определенными правилами</span><span class="sxs-lookup"><span data-stu-id="aa708-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="aa708-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="aa708-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="aa708-141">Тип доступа к сети для учетной записи службы восприятия.</span><span class="sxs-lookup"><span data-stu-id="aa708-141">The network access type for Cognitive Services Account.</span></span>

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

### <span data-ttu-id="aa708-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa708-142">-ResourceGroupName</span></span>
<span data-ttu-id="aa708-143">Задает имя группы ресурсов, которой нужно назначить учетную запись.</span><span class="sxs-lookup"><span data-stu-id="aa708-143">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="aa708-144">Группа ресурсов уже должна существовать.</span><span class="sxs-lookup"><span data-stu-id="aa708-144">The resource group must already exist.</span></span>

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

### <span data-ttu-id="aa708-145">-SkuName</span><span class="sxs-lookup"><span data-stu-id="aa708-145">-SkuName</span></span>
<span data-ttu-id="aa708-146">Определяет SKU учетной записи.</span><span class="sxs-lookup"><span data-stu-id="aa708-146">Specifies the SKU for the account.</span></span>
<span data-ttu-id="aa708-147">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="aa708-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="aa708-148">F0 (бесплатный уровень)</span><span class="sxs-lookup"><span data-stu-id="aa708-148">F0 (free tier)</span></span>
- <span data-ttu-id="aa708-149">S0</span><span class="sxs-lookup"><span data-stu-id="aa708-149">S0</span></span>
- <span data-ttu-id="aa708-150">S1</span><span class="sxs-lookup"><span data-stu-id="aa708-150">S1</span></span>
- <span data-ttu-id="aa708-151">S2</span><span class="sxs-lookup"><span data-stu-id="aa708-151">S2</span></span>
- <span data-ttu-id="aa708-152">S3</span><span class="sxs-lookup"><span data-stu-id="aa708-152">S3</span></span>
- <span data-ttu-id="aa708-153">S4 Для получения дополнительных сведений см. [API когнитивных служб.](https://www.microsoft.com/cognitive-services/en-us/apis)</span><span class="sxs-lookup"><span data-stu-id="aa708-153">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa708-154">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="aa708-154">-StorageAccountId</span></span>
<span data-ttu-id="aa708-155">Список учетных записей хранения, владельцем каждого пользователя.</span><span class="sxs-lookup"><span data-stu-id="aa708-155">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="aa708-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="aa708-156">-Tag</span></span>
<span data-ttu-id="aa708-157">Указывает тег как пару "имя/значение".</span><span class="sxs-lookup"><span data-stu-id="aa708-157">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aa708-158">-Type</span><span class="sxs-lookup"><span data-stu-id="aa708-158">-Type</span></span>
<span data-ttu-id="aa708-159">Определяет тип учетной записи, которая будет создаваться.</span><span class="sxs-lookup"><span data-stu-id="aa708-159">Specifies the type of account to create.</span></span> <span data-ttu-id="aa708-160">Для `Get-AzCognitiveServicesAccountType` получения текущих допустимых значений используйте cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa708-160">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aa708-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa708-161">-Confirm</span></span>
<span data-ttu-id="aa708-162">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="aa708-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa708-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa708-163">-WhatIf</span></span>
<span data-ttu-id="aa708-164">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa708-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa708-165">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="aa708-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa708-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa708-166">CommonParameters</span></span>
<span data-ttu-id="aa708-167">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa708-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa708-168">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa708-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa708-169">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aa708-169">INPUTS</span></span>

### <span data-ttu-id="aa708-170">System.String</span><span class="sxs-lookup"><span data-stu-id="aa708-170">System.String</span></span>

## <span data-ttu-id="aa708-171">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="aa708-171">OUTPUTS</span></span>

### <span data-ttu-id="aa708-172">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="aa708-172">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="aa708-173">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="aa708-173">NOTES</span></span>

## <span data-ttu-id="aa708-174">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa708-174">RELATED LINKS</span></span>

[<span data-ttu-id="aa708-175">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="aa708-175">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="aa708-176">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="aa708-176">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="aa708-177">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="aa708-177">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
