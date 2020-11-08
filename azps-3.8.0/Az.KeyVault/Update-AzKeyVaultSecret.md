---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultSecret.md
ms.openlocfilehash: 5efc920d4dd6e8e83c0a2ee5f61768ac7373f864
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065605"
---
# <span data-ttu-id="ce835-101">Update-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ce835-101">Update-AzKeyVaultSecret</span></span>

## <span data-ttu-id="ce835-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ce835-102">SYNOPSIS</span></span>
<span data-ttu-id="ce835-103">Обновляет атрибуты секрета в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="ce835-103">Updates attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="ce835-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ce835-104">SYNTAX</span></span>

### <span data-ttu-id="ce835-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ce835-105">Default (Default)</span></span>
```
Update-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce835-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ce835-106">InputObject</span></span>
```
Update-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce835-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce835-107">DESCRIPTION</span></span>
<span data-ttu-id="ce835-108">Командлет **Update-AzKeyVaultSecret** обновляет редактируемые атрибуты секрета в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="ce835-108">The **Update-AzKeyVaultSecret** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="ce835-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ce835-109">EXAMPLES</span></span>

### <span data-ttu-id="ce835-110">Пример 1: изменение атрибутов секрета</span><span class="sxs-lookup"><span data-stu-id="ce835-110">Example 1: Modify the attributes of a secret</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = 'true'}
PS C:\> $ContentType= 'xml'
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru

Vault Name   : ContosoVault
Name         : HR
Version      : d476edfcd3544017a03bc49c1f3abec0
Id           : https://ContosoVault.vault.azure.net:443/secrets/HR/d476edfcd3544017a03bc49c1f3abec0
Enabled      : True
Expires      : 5/25/2020 8:01:58 PM
Not Before   : 5/25/2018 8:02:02 PM
Created      : 4/11/2018 11:45:06 PM
Updated      : 5/25/2018 8:02:45 PM
Content Type : xml
Tags         : Name      Value
               Severity  medium
               HR        true
```

<span data-ttu-id="ce835-111">Первые четыре команды определяют атрибуты для даты окончания срока действия, даты NotBefore, тегов и типа контекста и хранят атрибуты в переменных.</span><span class="sxs-lookup"><span data-stu-id="ce835-111">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="ce835-112">Последняя команда изменяет атрибуты секрета с именем HR в хранилище ключей с именем ContosoVault, используя хранимые переменные.</span><span class="sxs-lookup"><span data-stu-id="ce835-112">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="ce835-113">Пример 2: Удаление тегов и типа контента для секрета</span><span class="sxs-lookup"><span data-stu-id="ce835-113">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\> Update-AzKeyVaultSecret -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="ce835-114">Эта команда удаляет Теги и тип контента для указанной версии секретного файла с именем HR в хранилище ключей contoso.</span><span class="sxs-lookup"><span data-stu-id="ce835-114">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="ce835-115">Пример 3: отключение текущей версии секретных данных, имя которой начинается с нее</span><span class="sxs-lookup"><span data-stu-id="ce835-115">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Update-AzKeyVaultSecret -Enable $False
```

<span data-ttu-id="ce835-116">Первая команда сохраняет строковое значение Contoso в переменной $Vault.</span><span class="sxs-lookup"><span data-stu-id="ce835-116">The first command stores the string value Contoso in the $Vault variable.</span></span>
<span data-ttu-id="ce835-117">Вторая команда сохраняет строковое значение в переменной $Prefix.</span><span class="sxs-lookup"><span data-stu-id="ce835-117">The second command stores the string value IT in the $Prefix variable.</span></span>
<span data-ttu-id="ce835-118">Третья команда использует командлет Get-AzKeyVaultSecret для получения секретных данных в указанном хранилище ключей, а затем передает эти секреты в командлет **Where-Object** .</span><span class="sxs-lookup"><span data-stu-id="ce835-118">The third command uses the Get-AzKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="ce835-119">Командлет **Where-Object** фильтрует секреты для имен, начинающихся с этих знаков.</span><span class="sxs-lookup"><span data-stu-id="ce835-119">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="ce835-120">Команда найдет секреты, соответствующие фильтру, в командлет Update-AzKeyVaultSecret, который отключается.</span><span class="sxs-lookup"><span data-stu-id="ce835-120">The command pipes the secrets that match the filter to the Update-AzKeyVaultSecret cmdlet, which disables them.</span></span>

### <span data-ttu-id="ce835-121">Пример 4: Настройка ContentType для всех версий секрета</span><span class="sxs-lookup"><span data-stu-id="ce835-121">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\> $VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Update-AzKeyVaultSecret -ContentType $ContentType
```

<span data-ttu-id="ce835-122">Первые три команды определяют переменные типа String, используемые для параметров *VaultName* , *Name* и *ContentType* .</span><span class="sxs-lookup"><span data-stu-id="ce835-122">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="ce835-123">Четвертая команда использует командлет Get-AzKeyVaultKey, чтобы получить указанные ключи, и переводит ключи в командлет Update-AzKeyVaultSecret, чтобы задать для их типа содержимого значение XML.</span><span class="sxs-lookup"><span data-stu-id="ce835-123">The fourth command uses the Get-AzKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Update-AzKeyVaultSecret cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="ce835-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ce835-124">PARAMETERS</span></span>

### <span data-ttu-id="ce835-125">-ContentType</span><span class="sxs-lookup"><span data-stu-id="ce835-125">-ContentType</span></span>
<span data-ttu-id="ce835-126">Тип контента "секрет".</span><span class="sxs-lookup"><span data-stu-id="ce835-126">Secret's content type.</span></span>
<span data-ttu-id="ce835-127">Если не указано, существующее значение типа содержимого секрета остается неизменным.</span><span class="sxs-lookup"><span data-stu-id="ce835-127">If not specified, the existing value of the secret's content type remains unchanged.</span></span>
<span data-ttu-id="ce835-128">Удалите существующее значение типа контента, указав пустую строку.</span><span class="sxs-lookup"><span data-stu-id="ce835-128">Remove the existing content type value by specifying an empty string.</span></span>

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

### <span data-ttu-id="ce835-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce835-129">-DefaultProfile</span></span>
<span data-ttu-id="ce835-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ce835-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce835-131">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="ce835-131">-Enable</span></span>
<span data-ttu-id="ce835-132">Если есть, включите секрет, если значение равно true.</span><span class="sxs-lookup"><span data-stu-id="ce835-132">If present, enable a secret if value is true.</span></span>
<span data-ttu-id="ce835-133">Отключение секрета, если значение равно false.</span><span class="sxs-lookup"><span data-stu-id="ce835-133">Disable a secret if value is false.</span></span>
<span data-ttu-id="ce835-134">Если этот параметр не указан, существующее значение состояния Enabled и Disabled для секрета не меняется.</span><span class="sxs-lookup"><span data-stu-id="ce835-134">If not specified, the existing value of the secret's enabled/disabled state remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce835-135">-Истекает</span><span class="sxs-lookup"><span data-stu-id="ce835-135">-Expires</span></span>
<span data-ttu-id="ce835-136">Время истечения срока действия секретного времени в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="ce835-136">The expiration time of a secret in UTC time.</span></span>
<span data-ttu-id="ce835-137">Если не указано, существующее значение срока действия секрета останется неизменным.</span><span class="sxs-lookup"><span data-stu-id="ce835-137">If not specified, the existing value of the secret's expiration time remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce835-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce835-138">-InputObject</span></span>
<span data-ttu-id="ce835-139">Секретный объект</span><span class="sxs-lookup"><span data-stu-id="ce835-139">Secret object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce835-140">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ce835-140">-Name</span></span>
<span data-ttu-id="ce835-141">Имя секрета.</span><span class="sxs-lookup"><span data-stu-id="ce835-141">Secret name.</span></span>
<span data-ttu-id="ce835-142">Командлет создает полное доменное имя секрета из имени хранилища, выбранного в настоящее время среды и имени секрета.</span><span class="sxs-lookup"><span data-stu-id="ce835-142">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce835-143">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="ce835-143">-NotBefore</span></span>
<span data-ttu-id="ce835-144">Время в формате UTC, после которого невозможно использовать секретный код.</span><span class="sxs-lookup"><span data-stu-id="ce835-144">The UTC time before which secret can't be used.</span></span>
<span data-ttu-id="ce835-145">Если он не указан, существующее значение атрибута NotBefore секрета остается неизменным.</span><span class="sxs-lookup"><span data-stu-id="ce835-145">If not specified, the existing value of the secret's NotBefore attribute remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce835-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce835-146">-PassThru</span></span>
<span data-ttu-id="ce835-147">По умолчанию командлет не возвращает объект.</span><span class="sxs-lookup"><span data-stu-id="ce835-147">Cmdlet does not return object by default.</span></span>
<span data-ttu-id="ce835-148">Если этот параметр указан, возвращают секретный объект.</span><span class="sxs-lookup"><span data-stu-id="ce835-148">If this switch is specified, return Secret object.</span></span>

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

### <span data-ttu-id="ce835-149">-Тег</span><span class="sxs-lookup"><span data-stu-id="ce835-149">-Tag</span></span>
<span data-ttu-id="ce835-150">Хэш-таблица, представляющая секретные Теги.</span><span class="sxs-lookup"><span data-stu-id="ce835-150">A hashtable representing secret tags.</span></span>
<span data-ttu-id="ce835-151">Если не указано, существующие теги секрета остаются без изменений.</span><span class="sxs-lookup"><span data-stu-id="ce835-151">If not specified, the existing tags of the secret remain unchanged.</span></span>
<span data-ttu-id="ce835-152">Удалите тег, указав пустую хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="ce835-152">Remove a tag by specifying an empty Hashtable.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce835-153">-VaultName</span><span class="sxs-lookup"><span data-stu-id="ce835-153">-VaultName</span></span>
<span data-ttu-id="ce835-154">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="ce835-154">Vault name.</span></span>
<span data-ttu-id="ce835-155">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="ce835-155">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce835-156">-Version</span><span class="sxs-lookup"><span data-stu-id="ce835-156">-Version</span></span>
<span data-ttu-id="ce835-157">Секретная версия.</span><span class="sxs-lookup"><span data-stu-id="ce835-157">Secret version.</span></span>
<span data-ttu-id="ce835-158">Командлет создает полное доменное имя секрета из имени хранилища, выбранной в данный момент среды, секретного имени и секретной версии.</span><span class="sxs-lookup"><span data-stu-id="ce835-158">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment, secret name and secret version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce835-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce835-159">-Confirm</span></span>
<span data-ttu-id="ce835-160">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ce835-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce835-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce835-161">-WhatIf</span></span>
<span data-ttu-id="ce835-162">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ce835-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce835-163">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ce835-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce835-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce835-164">CommonParameters</span></span>
<span data-ttu-id="ce835-165">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ce835-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce835-166">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce835-166">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce835-167">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ce835-167">INPUTS</span></span>

### <span data-ttu-id="ce835-168">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ce835-168">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="ce835-169">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ce835-169">OUTPUTS</span></span>

### <span data-ttu-id="ce835-170">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="ce835-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="ce835-171">Пуск</span><span class="sxs-lookup"><span data-stu-id="ce835-171">NOTES</span></span>

## <span data-ttu-id="ce835-172">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ce835-172">RELATED LINKS</span></span>
