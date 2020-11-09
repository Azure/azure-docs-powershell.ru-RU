---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: 0c7e22174b0306a3b9b5a37bd99edeb06f124334
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315170"
---
# <span data-ttu-id="227d5-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="227d5-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="227d5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="227d5-102">SYNOPSIS</span></span>
<span data-ttu-id="227d5-103">Создание учетной записи службы для восприятия.</span><span class="sxs-lookup"><span data-stu-id="227d5-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="227d5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="227d5-104">SYNTAX</span></span>

### <span data-ttu-id="227d5-105">CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="227d5-105">CognitiveServicesEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-CognitiveServicesEncryption]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="227d5-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="227d5-106">KeyVaultEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="227d5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="227d5-107">DESCRIPTION</span></span>
<span data-ttu-id="227d5-108">Командлет **New-AzCognitiveServicesAccount** создает учетную запись службы с указанным типом и SKU.</span><span class="sxs-lookup"><span data-stu-id="227d5-108">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="227d5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="227d5-109">EXAMPLES</span></span>

### <span data-ttu-id="227d5-110">1:</span><span class="sxs-lookup"><span data-stu-id="227d5-110">1:</span></span>
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

## <span data-ttu-id="227d5-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="227d5-111">PARAMETERS</span></span>

### <span data-ttu-id="227d5-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="227d5-112">-ApiProperty</span></span>
<span data-ttu-id="227d5-113">ApiProperties учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="227d5-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="227d5-114">Требуется для определенных типов учетных записей.</span><span class="sxs-lookup"><span data-stu-id="227d5-114">Required by specific account types.</span></span>

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

### <span data-ttu-id="227d5-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="227d5-115">-AssignIdentity</span></span>
<span data-ttu-id="227d5-116">Создайте и назначьте для этой учетной записи новую учетную запись для службы управления ключами, например Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="227d5-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="227d5-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="227d5-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="227d5-118">Следует ли настраивать шифрование учетной записи KeySource в Microsoft. CognitiveServices или нет.</span><span class="sxs-lookup"><span data-stu-id="227d5-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="227d5-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="227d5-119">-CustomSubdomainName</span></span>
<span data-ttu-id="227d5-120">Имя поддомена учетной записи самообслуживания служб.</span><span class="sxs-lookup"><span data-stu-id="227d5-120">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="227d5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="227d5-121">-DefaultProfile</span></span>
<span data-ttu-id="227d5-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="227d5-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="227d5-123">-Force</span><span class="sxs-lookup"><span data-stu-id="227d5-123">-Force</span></span>
<span data-ttu-id="227d5-124">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="227d5-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="227d5-125">-KeyName</span><span class="sxs-lookup"><span data-stu-id="227d5-125">-KeyName</span></span>
<span data-ttu-id="227d5-126">Шифрование учетной записи службы для keySource KeyVault KeyName</span><span class="sxs-lookup"><span data-stu-id="227d5-126">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="227d5-127">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="227d5-127">-KeyVaultEncryption</span></span>
<span data-ttu-id="227d5-128">Следует ли настраивать шифрование учетной записи keySource в Microsoft. KeyVault или нет.</span><span class="sxs-lookup"><span data-stu-id="227d5-128">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="227d5-129">Если вы указали параметр KeyName, KeyVersion и KeyVaultUri, то при шифровании учетных записей служб KeySource также будет задано значение Microsoft. KeyVault weather. Этот параметр установлен или нет.</span><span class="sxs-lookup"><span data-stu-id="227d5-129">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="227d5-130">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="227d5-130">-KeyVaultUri</span></span>
<span data-ttu-id="227d5-131">Шифрование учетной записи службы для keySource KeyVault KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="227d5-131">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="227d5-132">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="227d5-132">-KeyVersion</span></span>
<span data-ttu-id="227d5-133">Шифрование учетной записи службы для keySource KeyVault KeyVersion</span><span class="sxs-lookup"><span data-stu-id="227d5-133">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="227d5-134">-Location</span><span class="sxs-lookup"><span data-stu-id="227d5-134">-Location</span></span>
<span data-ttu-id="227d5-135">Указывает место для создания учетной записи.</span><span class="sxs-lookup"><span data-stu-id="227d5-135">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="227d5-136">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="227d5-136">-Name</span></span>
<span data-ttu-id="227d5-137">Задает имя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="227d5-137">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="227d5-138">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="227d5-138">-NetworkRuleSet</span></span>
<span data-ttu-id="227d5-139">NetworkRuleSet используется для определения набора правил конфигурации для брандмауэров и виртуальных сетей, а также для задания значений свойств сети, например, как обрабатывать запросы, не соответствующие ни одному из заданных правил.</span><span class="sxs-lookup"><span data-stu-id="227d5-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="227d5-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="227d5-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="227d5-141">Тип сетевого доступа для учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="227d5-141">The network access type for Cognitive Services Account.</span></span>

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

### <span data-ttu-id="227d5-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="227d5-142">-ResourceGroupName</span></span>
<span data-ttu-id="227d5-143">Указывает имя группы ресурсов, для которой необходимо назначить учетную запись.</span><span class="sxs-lookup"><span data-stu-id="227d5-143">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="227d5-144">Группа ресурсов должна быть уже создана.</span><span class="sxs-lookup"><span data-stu-id="227d5-144">The resource group must already exist.</span></span>

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

### <span data-ttu-id="227d5-145">-SkuName</span><span class="sxs-lookup"><span data-stu-id="227d5-145">-SkuName</span></span>
<span data-ttu-id="227d5-146">Указывает SKU для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="227d5-146">Specifies the SKU for the account.</span></span>
<span data-ttu-id="227d5-147">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="227d5-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="227d5-148">F0 (бесплатный уровень)</span><span class="sxs-lookup"><span data-stu-id="227d5-148">F0 (free tier)</span></span>
- <span data-ttu-id="227d5-149">S0</span><span class="sxs-lookup"><span data-stu-id="227d5-149">S0</span></span>
- <span data-ttu-id="227d5-150">Состояний</span><span class="sxs-lookup"><span data-stu-id="227d5-150">S1</span></span>
- <span data-ttu-id="227d5-151">S2</span><span class="sxs-lookup"><span data-stu-id="227d5-151">S2</span></span>
- <span data-ttu-id="227d5-152">Режима</span><span class="sxs-lookup"><span data-stu-id="227d5-152">S3</span></span>
- <span data-ttu-id="227d5-153">Дополнительные сведения можно найти в разделе [API службы](https://www.microsoft.com/cognitive-services/en-us/apis)для наприведения.</span><span class="sxs-lookup"><span data-stu-id="227d5-153">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="227d5-154">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="227d5-154">-StorageAccountId</span></span>
<span data-ttu-id="227d5-155">Список учетных записей хранения, принадлежащих пользователю.</span><span class="sxs-lookup"><span data-stu-id="227d5-155">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="227d5-156">-Тег</span><span class="sxs-lookup"><span data-stu-id="227d5-156">-Tag</span></span>
<span data-ttu-id="227d5-157">Указывает тег как пару имя/значение.</span><span class="sxs-lookup"><span data-stu-id="227d5-157">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="227d5-158">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="227d5-158">-Type</span></span>
<span data-ttu-id="227d5-159">Указывает тип создаваемой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="227d5-159">Specifies the type of account to create.</span></span> <span data-ttu-id="227d5-160">Используйте `Get-AzCognitiveServicesAccountType` командлет для получения текущих приемлемых значений.</span><span class="sxs-lookup"><span data-stu-id="227d5-160">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="227d5-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="227d5-161">-Confirm</span></span>
<span data-ttu-id="227d5-162">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="227d5-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="227d5-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="227d5-163">-WhatIf</span></span>
<span data-ttu-id="227d5-164">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="227d5-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="227d5-165">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="227d5-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="227d5-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="227d5-166">CommonParameters</span></span>
<span data-ttu-id="227d5-167">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="227d5-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="227d5-168">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="227d5-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="227d5-169">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="227d5-169">INPUTS</span></span>

### <span data-ttu-id="227d5-170">System. String</span><span class="sxs-lookup"><span data-stu-id="227d5-170">System.String</span></span>

## <span data-ttu-id="227d5-171">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="227d5-171">OUTPUTS</span></span>

### <span data-ttu-id="227d5-172">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="227d5-172">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="227d5-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="227d5-173">NOTES</span></span>

## <span data-ttu-id="227d5-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="227d5-174">RELATED LINKS</span></span>

[<span data-ttu-id="227d5-175">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="227d5-175">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="227d5-176">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="227d5-176">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="227d5-177">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="227d5-177">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
