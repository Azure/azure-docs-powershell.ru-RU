---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: fc510ebede11168dd8d8b090cd2069ce3e6de52c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94064770"
---
# <span data-ttu-id="7ec95-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7ec95-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="7ec95-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7ec95-102">SYNOPSIS</span></span>
<span data-ttu-id="7ec95-103">Изменение учетной записи.</span><span class="sxs-lookup"><span data-stu-id="7ec95-103">Modifies an account.</span></span>

## <span data-ttu-id="7ec95-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7ec95-104">SYNTAX</span></span>

### <span data-ttu-id="7ec95-105">CognitiveServicesEncryption (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7ec95-105">CognitiveServicesEncryption (Default)</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-CognitiveServicesEncryption] [-NetworkRuleSet <PSNetworkRuleSet>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ec95-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="7ec95-106">KeyVaultEncryption</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ec95-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ec95-107">DESCRIPTION</span></span>
<span data-ttu-id="7ec95-108">Командлет **Set-AzCognitiveServicesAccount** изменяет SKU или теги указанной учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="7ec95-108">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="7ec95-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7ec95-109">EXAMPLES</span></span>

### <span data-ttu-id="7ec95-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="7ec95-110">Example 1</span></span>
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

## <span data-ttu-id="7ec95-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7ec95-111">PARAMETERS</span></span>

### <span data-ttu-id="7ec95-112">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="7ec95-112">-AssignIdentity</span></span>
<span data-ttu-id="7ec95-113">Создайте и назначьте для этой учетной записи новую учетную запись для службы управления ключами, например Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="7ec95-113">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="7ec95-114">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="7ec95-114">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="7ec95-115">Следует ли настраивать шифрование учетной записи KeySource в Microsoft. CognitiveServices или нет.</span><span class="sxs-lookup"><span data-stu-id="7ec95-115">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="7ec95-116">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="7ec95-116">-CustomSubdomainName</span></span>
<span data-ttu-id="7ec95-117">Имя поддомена учетной записи самообслуживания служб.</span><span class="sxs-lookup"><span data-stu-id="7ec95-117">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="7ec95-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ec95-118">-DefaultProfile</span></span>
<span data-ttu-id="7ec95-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7ec95-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ec95-120">-Force</span><span class="sxs-lookup"><span data-stu-id="7ec95-120">-Force</span></span>
<span data-ttu-id="7ec95-121">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="7ec95-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7ec95-122">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="7ec95-122">-IdentityType</span></span>
<span data-ttu-id="7ec95-123">Тип идентификатора управляемой службы.</span><span class="sxs-lookup"><span data-stu-id="7ec95-123">Type of managed service identity.</span></span>

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

### <span data-ttu-id="7ec95-124">-KeyName</span><span class="sxs-lookup"><span data-stu-id="7ec95-124">-KeyName</span></span>
<span data-ttu-id="7ec95-125">Шифрование учетной записи службы для keySource KeyVault KeyName</span><span class="sxs-lookup"><span data-stu-id="7ec95-125">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="7ec95-126">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="7ec95-126">-KeyVaultEncryption</span></span>
<span data-ttu-id="7ec95-127">Следует ли настраивать шифрование учетной записи keySource в Microsoft. KeyVault или нет.</span><span class="sxs-lookup"><span data-stu-id="7ec95-127">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="7ec95-128">Если вы указали параметр KeyName, KeyVersion и KeyVaultUri, то при шифровании учетных записей служб KeySource также будет задано значение Microsoft. KeyVault weather. Этот параметр установлен или нет.</span><span class="sxs-lookup"><span data-stu-id="7ec95-128">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="7ec95-129">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="7ec95-129">-KeyVaultUri</span></span>
<span data-ttu-id="7ec95-130">Шифрование учетной записи службы для keySource KeyVault KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="7ec95-130">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="7ec95-131">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="7ec95-131">-KeyVersion</span></span>
<span data-ttu-id="7ec95-132">Шифрование учетной записи службы для keySource KeyVault KeyVersion</span><span class="sxs-lookup"><span data-stu-id="7ec95-132">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="7ec95-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7ec95-133">-Name</span></span>
<span data-ttu-id="7ec95-134">Указывает имя учетной записи, которую нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="7ec95-134">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="7ec95-135">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="7ec95-135">-NetworkRuleSet</span></span>
<span data-ttu-id="7ec95-136">NetworkRuleSet используется для определения набора правил конфигурации для брандмауэров и виртуальных сетей, а также для задания значений свойств сети, например, как обрабатывать запросы, не соответствующие ни одному из заданных правил.</span><span class="sxs-lookup"><span data-stu-id="7ec95-136">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="7ec95-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ec95-137">-ResourceGroupName</span></span>
<span data-ttu-id="7ec95-138">Указывает имя группы ресурсов, которой назначена эта учетная запись.</span><span class="sxs-lookup"><span data-stu-id="7ec95-138">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="7ec95-139">-SkuName</span><span class="sxs-lookup"><span data-stu-id="7ec95-139">-SkuName</span></span>
<span data-ttu-id="7ec95-140">Указывает SKU для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="7ec95-140">Specifies the SKU for the account.</span></span>
<span data-ttu-id="7ec95-141">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="7ec95-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7ec95-142">F0 (бесплатный уровень)</span><span class="sxs-lookup"><span data-stu-id="7ec95-142">F0 (free tier)</span></span>
- <span data-ttu-id="7ec95-143">S0</span><span class="sxs-lookup"><span data-stu-id="7ec95-143">S0</span></span>
- <span data-ttu-id="7ec95-144">Состояний</span><span class="sxs-lookup"><span data-stu-id="7ec95-144">S1</span></span>
- <span data-ttu-id="7ec95-145">S2</span><span class="sxs-lookup"><span data-stu-id="7ec95-145">S2</span></span>
- <span data-ttu-id="7ec95-146">Режима</span><span class="sxs-lookup"><span data-stu-id="7ec95-146">S3</span></span>
- <span data-ttu-id="7ec95-147">Режим</span><span class="sxs-lookup"><span data-stu-id="7ec95-147">S4</span></span>

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

### <span data-ttu-id="7ec95-148">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="7ec95-148">-StorageAccountId</span></span>
<span data-ttu-id="7ec95-149">Список учетных записей хранения, принадлежащих пользователю.</span><span class="sxs-lookup"><span data-stu-id="7ec95-149">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="7ec95-150">-Тег</span><span class="sxs-lookup"><span data-stu-id="7ec95-150">-Tag</span></span>
<span data-ttu-id="7ec95-151">Указывает тег как пару имя/значение.</span><span class="sxs-lookup"><span data-stu-id="7ec95-151">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="7ec95-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7ec95-152">-Confirm</span></span>
<span data-ttu-id="7ec95-153">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7ec95-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ec95-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ec95-154">-WhatIf</span></span>
<span data-ttu-id="7ec95-155">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7ec95-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ec95-156">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7ec95-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ec95-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ec95-157">CommonParameters</span></span>
<span data-ttu-id="7ec95-158">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7ec95-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ec95-159">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7ec95-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ec95-160">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7ec95-160">INPUTS</span></span>

### <span data-ttu-id="7ec95-161">System. String</span><span class="sxs-lookup"><span data-stu-id="7ec95-161">System.String</span></span>

### <span data-ttu-id="7ec95-162">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="7ec95-162">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="7ec95-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7ec95-163">OUTPUTS</span></span>

### <span data-ttu-id="7ec95-164">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7ec95-164">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="7ec95-165">Пуск</span><span class="sxs-lookup"><span data-stu-id="7ec95-165">NOTES</span></span>

## <span data-ttu-id="7ec95-166">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7ec95-166">RELATED LINKS</span></span>

[<span data-ttu-id="7ec95-167">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7ec95-167">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="7ec95-168">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7ec95-168">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="7ec95-169">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="7ec95-169">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
