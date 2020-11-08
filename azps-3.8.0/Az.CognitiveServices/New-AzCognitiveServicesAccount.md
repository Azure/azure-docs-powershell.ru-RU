---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: 713c5cb34133a233bace576ea80035b8e004eb7f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94064783"
---
# <span data-ttu-id="f7b44-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f7b44-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="f7b44-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7b44-102">SYNOPSIS</span></span>
<span data-ttu-id="f7b44-103">Создание учетной записи службы для восприятия.</span><span class="sxs-lookup"><span data-stu-id="f7b44-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="f7b44-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7b44-104">SYNTAX</span></span>

### <span data-ttu-id="f7b44-105">CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="f7b44-105">CognitiveServicesEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-CognitiveServicesEncryption]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f7b44-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="f7b44-106">KeyVaultEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7b44-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7b44-107">DESCRIPTION</span></span>
<span data-ttu-id="f7b44-108">Командлет **New-AzCognitiveServicesAccount** создает учетную запись службы с указанным типом и SKU.</span><span class="sxs-lookup"><span data-stu-id="f7b44-108">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="f7b44-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7b44-109">EXAMPLES</span></span>

### <span data-ttu-id="f7b44-110">1:</span><span class="sxs-lookup"><span data-stu-id="f7b44-110">1:</span></span>
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

## <span data-ttu-id="f7b44-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7b44-111">PARAMETERS</span></span>

### <span data-ttu-id="f7b44-112">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="f7b44-112">-AssignIdentity</span></span>
<span data-ttu-id="f7b44-113">Создайте и назначьте для этой учетной записи новую учетную запись для службы управления ключами, например Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="f7b44-113">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="f7b44-114">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="f7b44-114">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="f7b44-115">Следует ли настраивать шифрование учетной записи KeySource в Microsoft. CognitiveServices или нет.</span><span class="sxs-lookup"><span data-stu-id="f7b44-115">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="f7b44-116">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="f7b44-116">-CustomSubdomainName</span></span>
<span data-ttu-id="f7b44-117">Имя поддомена учетной записи самообслуживания служб.</span><span class="sxs-lookup"><span data-stu-id="f7b44-117">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="f7b44-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7b44-118">-DefaultProfile</span></span>
<span data-ttu-id="f7b44-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f7b44-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7b44-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f7b44-120">-Force</span></span>
<span data-ttu-id="f7b44-121">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="f7b44-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f7b44-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="f7b44-122">-KeyName</span></span>
<span data-ttu-id="f7b44-123">Шифрование учетной записи службы для keySource KeyVault KeyName</span><span class="sxs-lookup"><span data-stu-id="f7b44-123">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="f7b44-124">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="f7b44-124">-KeyVaultEncryption</span></span>
<span data-ttu-id="f7b44-125">Следует ли настраивать шифрование учетной записи keySource в Microsoft. KeyVault или нет.</span><span class="sxs-lookup"><span data-stu-id="f7b44-125">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="f7b44-126">Если вы указали параметр KeyName, KeyVersion и KeyVaultUri, то при шифровании учетных записей служб KeySource также будет задано значение Microsoft. KeyVault weather. Этот параметр установлен или нет.</span><span class="sxs-lookup"><span data-stu-id="f7b44-126">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="f7b44-127">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="f7b44-127">-KeyVaultUri</span></span>
<span data-ttu-id="f7b44-128">Шифрование учетной записи службы для keySource KeyVault KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="f7b44-128">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="f7b44-129">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="f7b44-129">-KeyVersion</span></span>
<span data-ttu-id="f7b44-130">Шифрование учетной записи службы для keySource KeyVault KeyVersion</span><span class="sxs-lookup"><span data-stu-id="f7b44-130">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="f7b44-131">-Location</span><span class="sxs-lookup"><span data-stu-id="f7b44-131">-Location</span></span>
<span data-ttu-id="f7b44-132">Указывает место для создания учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f7b44-132">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="f7b44-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f7b44-133">-Name</span></span>
<span data-ttu-id="f7b44-134">Задает имя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f7b44-134">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="f7b44-135">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f7b44-135">-NetworkRuleSet</span></span>
<span data-ttu-id="f7b44-136">NetworkRuleSet используется для определения набора правил конфигурации для брандмауэров и виртуальных сетей, а также для задания значений свойств сети, например, как обрабатывать запросы, не соответствующие ни одному из заданных правил.</span><span class="sxs-lookup"><span data-stu-id="f7b44-136">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="f7b44-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7b44-137">-ResourceGroupName</span></span>
<span data-ttu-id="f7b44-138">Указывает имя группы ресурсов, для которой необходимо назначить учетную запись.</span><span class="sxs-lookup"><span data-stu-id="f7b44-138">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="f7b44-139">Группа ресурсов должна быть уже создана.</span><span class="sxs-lookup"><span data-stu-id="f7b44-139">The resource group must already exist.</span></span>

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

### <span data-ttu-id="f7b44-140">-SkuName</span><span class="sxs-lookup"><span data-stu-id="f7b44-140">-SkuName</span></span>
<span data-ttu-id="f7b44-141">Указывает SKU для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f7b44-141">Specifies the SKU for the account.</span></span>
<span data-ttu-id="f7b44-142">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="f7b44-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f7b44-143">F0 (бесплатный уровень)</span><span class="sxs-lookup"><span data-stu-id="f7b44-143">F0 (free tier)</span></span>
- <span data-ttu-id="f7b44-144">S0</span><span class="sxs-lookup"><span data-stu-id="f7b44-144">S0</span></span>
- <span data-ttu-id="f7b44-145">Состояний</span><span class="sxs-lookup"><span data-stu-id="f7b44-145">S1</span></span>
- <span data-ttu-id="f7b44-146">S2</span><span class="sxs-lookup"><span data-stu-id="f7b44-146">S2</span></span>
- <span data-ttu-id="f7b44-147">Режима</span><span class="sxs-lookup"><span data-stu-id="f7b44-147">S3</span></span>
- <span data-ttu-id="f7b44-148">Дополнительные сведения можно найти в разделе [API службы](https://www.microsoft.com/cognitive-services/en-us/apis)для наприведения.</span><span class="sxs-lookup"><span data-stu-id="f7b44-148">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="f7b44-149">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f7b44-149">-StorageAccountId</span></span>
<span data-ttu-id="f7b44-150">Список учетных записей хранения, принадлежащих пользователю.</span><span class="sxs-lookup"><span data-stu-id="f7b44-150">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="f7b44-151">-Тег</span><span class="sxs-lookup"><span data-stu-id="f7b44-151">-Tag</span></span>
<span data-ttu-id="f7b44-152">Указывает тег как пару имя/значение.</span><span class="sxs-lookup"><span data-stu-id="f7b44-152">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="f7b44-153">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="f7b44-153">-Type</span></span>
<span data-ttu-id="f7b44-154">Указывает тип создаваемой учетной записи.</span><span class="sxs-lookup"><span data-stu-id="f7b44-154">Specifies the type of account to create.</span></span> <span data-ttu-id="f7b44-155">Используйте `Get-AzCognitiveServicesAccountType` командлет для получения текущих приемлемых значений.</span><span class="sxs-lookup"><span data-stu-id="f7b44-155">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="f7b44-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7b44-156">-Confirm</span></span>
<span data-ttu-id="f7b44-157">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f7b44-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7b44-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7b44-158">-WhatIf</span></span>
<span data-ttu-id="f7b44-159">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f7b44-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7b44-160">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f7b44-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7b44-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7b44-161">CommonParameters</span></span>
<span data-ttu-id="f7b44-162">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7b44-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7b44-163">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7b44-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7b44-164">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7b44-164">INPUTS</span></span>

### <span data-ttu-id="f7b44-165">System. String</span><span class="sxs-lookup"><span data-stu-id="f7b44-165">System.String</span></span>

## <span data-ttu-id="f7b44-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7b44-166">OUTPUTS</span></span>

### <span data-ttu-id="f7b44-167">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f7b44-167">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="f7b44-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7b44-168">NOTES</span></span>

## <span data-ttu-id="f7b44-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7b44-169">RELATED LINKS</span></span>

[<span data-ttu-id="f7b44-170">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f7b44-170">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="f7b44-171">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f7b44-171">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="f7b44-172">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="f7b44-172">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
