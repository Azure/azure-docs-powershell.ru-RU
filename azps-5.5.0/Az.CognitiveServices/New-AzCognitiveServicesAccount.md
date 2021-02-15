---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: 0c7e22174b0306a3b9b5a37bd99edeb06f124334
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244224"
---
# <span data-ttu-id="c90aa-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c90aa-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="c90aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c90aa-102">SYNOPSIS</span></span>
<span data-ttu-id="c90aa-103">Создает учетную запись когнитивных служб.</span><span class="sxs-lookup"><span data-stu-id="c90aa-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="c90aa-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c90aa-104">SYNTAX</span></span>

### <span data-ttu-id="c90aa-105">CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="c90aa-105">CognitiveServicesEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-CognitiveServicesEncryption]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c90aa-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="c90aa-106">KeyVaultEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c90aa-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c90aa-107">DESCRIPTION</span></span>
<span data-ttu-id="c90aa-108">С **помощью cmdlet New-AzCognitiveServicesAccount** создается учетная запись Службы восприятия с указанным типом и номером SKU.</span><span class="sxs-lookup"><span data-stu-id="c90aa-108">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="c90aa-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c90aa-109">EXAMPLES</span></span>

### <span data-ttu-id="c90aa-110">1:</span><span class="sxs-lookup"><span data-stu-id="c90aa-110">1:</span></span>
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

## <span data-ttu-id="c90aa-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c90aa-111">PARAMETERS</span></span>

### <span data-ttu-id="c90aa-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="c90aa-112">-ApiProperty</span></span>
<span data-ttu-id="c90aa-113">APIProperties учетной записи когнитивных служб.</span><span class="sxs-lookup"><span data-stu-id="c90aa-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="c90aa-114">Требуется для определенных типов учетных записей.</span><span class="sxs-lookup"><span data-stu-id="c90aa-114">Required by specific account types.</span></span>

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

### <span data-ttu-id="c90aa-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c90aa-115">-AssignIdentity</span></span>
<span data-ttu-id="c90aa-116">Создание и назначение нового удостоверения учетной записи службы когнитивных услуг для этой учетной записи хранения для использования с ключевыми службами управления, например Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="c90aa-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="c90aa-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="c90aa-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="c90aa-118">Следует ли установить для ключа шифрования учетной записи службы когнитивных функций значение Microsoft.CognitiveServices или нет.</span><span class="sxs-lookup"><span data-stu-id="c90aa-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="c90aa-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="c90aa-119">-CustomSubdomainName</span></span>
<span data-ttu-id="c90aa-120">Имя поддомена учетной записи учетной записи Cognitive Services.</span><span class="sxs-lookup"><span data-stu-id="c90aa-120">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="c90aa-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c90aa-121">-DefaultProfile</span></span>
<span data-ttu-id="c90aa-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c90aa-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c90aa-123">-Force</span><span class="sxs-lookup"><span data-stu-id="c90aa-123">-Force</span></span>
<span data-ttu-id="c90aa-124">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="c90aa-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c90aa-125">-KeyName</span><span class="sxs-lookup"><span data-stu-id="c90aa-125">-KeyName</span></span>
<span data-ttu-id="c90aa-126">Cognitive Services Account encryption keySource KeyVault KeyName</span><span class="sxs-lookup"><span data-stu-id="c90aa-126">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="c90aa-127">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="c90aa-127">-KeyVaultEncryption</span></span>
<span data-ttu-id="c90aa-128">Следует ли установить ключ шифрования учетной записи службы в Microsoft.KeyVault или нет.</span><span class="sxs-lookup"><span data-stu-id="c90aa-128">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="c90aa-129">Если указать KeyName, KeyVersion и KeyVaultUri, то для параметра Encryption KeySource учетной записи учетной записи Службы распознавания данных будет также задан параметр Microsoft.KeyVault, заданный или нет.</span><span class="sxs-lookup"><span data-stu-id="c90aa-129">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="c90aa-130">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="c90aa-130">-KeyVaultUri</span></span>
<span data-ttu-id="c90aa-131">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="c90aa-131">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="c90aa-132">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="c90aa-132">-KeyVersion</span></span>
<span data-ttu-id="c90aa-133">Клавиша шифрования KeyVault KeyVault keyVersion учетной записи службы</span><span class="sxs-lookup"><span data-stu-id="c90aa-133">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="c90aa-134">-Location</span><span class="sxs-lookup"><span data-stu-id="c90aa-134">-Location</span></span>
<span data-ttu-id="c90aa-135">Определяет расположение, в котором нужно создать учетную запись.</span><span class="sxs-lookup"><span data-stu-id="c90aa-135">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="c90aa-136">-Name</span><span class="sxs-lookup"><span data-stu-id="c90aa-136">-Name</span></span>
<span data-ttu-id="c90aa-137">Указывает имя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="c90aa-137">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="c90aa-138">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="c90aa-138">-NetworkRuleSet</span></span>
<span data-ttu-id="c90aa-139">NetworkRuleSet используется для определения набора правил конфигурации для брандмауэров и виртуальных сетей, а также для настройки значений для свойств сети, таких как обработка запросов, несо совпадений с определенными правилами</span><span class="sxs-lookup"><span data-stu-id="c90aa-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="c90aa-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="c90aa-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="c90aa-141">Тип доступа к сети для учетной записи службы восприятия.</span><span class="sxs-lookup"><span data-stu-id="c90aa-141">The network access type for Cognitive Services Account.</span></span>

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

### <span data-ttu-id="c90aa-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c90aa-142">-ResourceGroupName</span></span>
<span data-ttu-id="c90aa-143">Задает имя группы ресурсов, которой нужно назначить учетную запись.</span><span class="sxs-lookup"><span data-stu-id="c90aa-143">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="c90aa-144">Группа ресурсов уже должна существовать.</span><span class="sxs-lookup"><span data-stu-id="c90aa-144">The resource group must already exist.</span></span>

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

### <span data-ttu-id="c90aa-145">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c90aa-145">-SkuName</span></span>
<span data-ttu-id="c90aa-146">Определяет SKU учетной записи.</span><span class="sxs-lookup"><span data-stu-id="c90aa-146">Specifies the SKU for the account.</span></span>
<span data-ttu-id="c90aa-147">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="c90aa-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c90aa-148">F0 (бесплатный уровень)</span><span class="sxs-lookup"><span data-stu-id="c90aa-148">F0 (free tier)</span></span>
- <span data-ttu-id="c90aa-149">S0</span><span class="sxs-lookup"><span data-stu-id="c90aa-149">S0</span></span>
- <span data-ttu-id="c90aa-150">S1</span><span class="sxs-lookup"><span data-stu-id="c90aa-150">S1</span></span>
- <span data-ttu-id="c90aa-151">S2</span><span class="sxs-lookup"><span data-stu-id="c90aa-151">S2</span></span>
- <span data-ttu-id="c90aa-152">S3</span><span class="sxs-lookup"><span data-stu-id="c90aa-152">S3</span></span>
- <span data-ttu-id="c90aa-153">S4 Дополнительные сведения см. в [API когнитивных служб.](https://www.microsoft.com/cognitive-services/en-us/apis)</span><span class="sxs-lookup"><span data-stu-id="c90aa-153">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="c90aa-154">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="c90aa-154">-StorageAccountId</span></span>
<span data-ttu-id="c90aa-155">Список пользовательских учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="c90aa-155">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="c90aa-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="c90aa-156">-Tag</span></span>
<span data-ttu-id="c90aa-157">Указывает тег как пару "имя и значение".</span><span class="sxs-lookup"><span data-stu-id="c90aa-157">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="c90aa-158">-Type</span><span class="sxs-lookup"><span data-stu-id="c90aa-158">-Type</span></span>
<span data-ttu-id="c90aa-159">Определяет тип учетной записи, которая будет создаваться.</span><span class="sxs-lookup"><span data-stu-id="c90aa-159">Specifies the type of account to create.</span></span> <span data-ttu-id="c90aa-160">Для `Get-AzCognitiveServicesAccountType` получения текущих допустимых значений используйте cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c90aa-160">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="c90aa-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c90aa-161">-Confirm</span></span>
<span data-ttu-id="c90aa-162">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c90aa-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c90aa-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c90aa-163">-WhatIf</span></span>
<span data-ttu-id="c90aa-164">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c90aa-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c90aa-165">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c90aa-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c90aa-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c90aa-166">CommonParameters</span></span>
<span data-ttu-id="c90aa-167">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c90aa-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c90aa-168">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c90aa-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c90aa-169">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c90aa-169">INPUTS</span></span>

### <span data-ttu-id="c90aa-170">System.String</span><span class="sxs-lookup"><span data-stu-id="c90aa-170">System.String</span></span>

## <span data-ttu-id="c90aa-171">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c90aa-171">OUTPUTS</span></span>

### <span data-ttu-id="c90aa-172">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c90aa-172">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="c90aa-173">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c90aa-173">NOTES</span></span>

## <span data-ttu-id="c90aa-174">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c90aa-174">RELATED LINKS</span></span>

[<span data-ttu-id="c90aa-175">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c90aa-175">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="c90aa-176">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c90aa-176">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="c90aa-177">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c90aa-177">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
