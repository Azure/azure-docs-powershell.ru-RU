---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: E2A45461-6B41-42FF-A874-A4CEFC867A33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultsecretattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecretAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecretAttribute.md
ms.openlocfilehash: edb4c166fbacbf0ee394b10ff475fe90dc00a67d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734705"
---
# <span data-ttu-id="26662-101">Set-AzureKeyVaultSecretAttribute</span><span class="sxs-lookup"><span data-stu-id="26662-101">Set-AzureKeyVaultSecretAttribute</span></span>

## <span data-ttu-id="26662-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="26662-102">SYNOPSIS</span></span>
<span data-ttu-id="26662-103">Обновляет атрибуты секрета в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="26662-103">Updates attributes of a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26662-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="26662-104">SYNTAX</span></span>

### <span data-ttu-id="26662-105">По умолчанию</span><span class="sxs-lookup"><span data-stu-id="26662-105">Default</span></span>
```
Set-AzureKeyVaultSecretAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26662-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="26662-106">InputObject</span></span>
```
Set-AzureKeyVaultSecretAttribute [-InputObject] <PSKeyVaultSecretIdentityItem> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26662-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26662-107">DESCRIPTION</span></span>
<span data-ttu-id="26662-108">Командлет **Set-AzureKeyVaultSecretAttribute** обновляет редактируемые атрибуты секрета в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="26662-108">The **Set-AzureKeyVaultSecretAttribute** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="26662-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="26662-109">EXAMPLES</span></span>

### <span data-ttu-id="26662-110">Пример 1: изменение атрибутов секрета</span><span class="sxs-lookup"><span data-stu-id="26662-110">Example 1: Modify the attributes of a secret</span></span>
```
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = null}
PS C:\> $ContentType= 'xml'
PS C:\> Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="26662-111">Первые четыре команды определяют атрибуты для даты окончания срока действия, даты NotBefore, тегов и типа контекста и хранят атрибуты в переменных.</span><span class="sxs-lookup"><span data-stu-id="26662-111">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="26662-112">Последняя команда изменяет атрибуты секрета с именем HR в хранилище ключей с именем ContosoVault, используя хранимые переменные.</span><span class="sxs-lookup"><span data-stu-id="26662-112">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="26662-113">Пример 2: Удаление тегов и типа контента для секрета</span><span class="sxs-lookup"><span data-stu-id="26662-113">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\>Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="26662-114">Эта команда удаляет Теги и тип контента для указанной версии секретного файла с именем HR в хранилище ключей contoso.</span><span class="sxs-lookup"><span data-stu-id="26662-114">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="26662-115">Пример 3: отключение текущей версии секретных данных, имя которой начинается с нее</span><span class="sxs-lookup"><span data-stu-id="26662-115">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzureKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Set-AzureKeyVaultSecretAttribute -Enable $False
```

<span data-ttu-id="26662-116">Первая команда сохраняет строковое значение Contoso в переменной $Vault.</span><span class="sxs-lookup"><span data-stu-id="26662-116">The first command stores the string value Contoso in the $Vault variable.</span></span>

<span data-ttu-id="26662-117">Вторая команда сохраняет строковое значение в переменной $Prefix.</span><span class="sxs-lookup"><span data-stu-id="26662-117">The second command stores the string value IT in the $Prefix variable.</span></span>

<span data-ttu-id="26662-118">Третья команда использует командлет Get-AzureKeyVaultSecret для получения секретных данных в указанном хранилище ключей, а затем передает эти секреты в командлет **Where-Object** .</span><span class="sxs-lookup"><span data-stu-id="26662-118">The third command uses the Get-AzureKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="26662-119">Командлет **Where-Object** фильтрует секреты для имен, начинающихся с этих знаков.</span><span class="sxs-lookup"><span data-stu-id="26662-119">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="26662-120">Команда найдет секреты, соответствующие фильтру, в командлет Set-AzureKeyVaultSecretAttribute, который отключается.</span><span class="sxs-lookup"><span data-stu-id="26662-120">The command pipes the secrets that match the filter to the Set-AzureKeyVaultSecretAttribute cmdlet, which disables them.</span></span>

### <span data-ttu-id="26662-121">Пример 4: Настройка ContentType для всех версий секрета</span><span class="sxs-lookup"><span data-stu-id="26662-121">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\>$VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzureKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Set-AzureKeyVaultSecretAttribute -ContentType $ContentType
```

<span data-ttu-id="26662-122">Первые три команды определяют переменные типа String, используемые для параметров *VaultName* , *Name* и *ContentType* .</span><span class="sxs-lookup"><span data-stu-id="26662-122">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="26662-123">Четвертая команда использует командлет Get-AzureKeyVaultKey, чтобы получить указанные ключи, и переводит ключи в командлет Set-AzureKeyVaultSecretAttribute, чтобы задать для их типа содержимого значение XML.</span><span class="sxs-lookup"><span data-stu-id="26662-123">The fourth command uses the Get-AzureKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Set-AzureKeyVaultSecretAttribute cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="26662-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="26662-124">PARAMETERS</span></span>

### <span data-ttu-id="26662-125">-ContentType</span><span class="sxs-lookup"><span data-stu-id="26662-125">-ContentType</span></span>
<span data-ttu-id="26662-126">Указывает тип содержимого секрета.</span><span class="sxs-lookup"><span data-stu-id="26662-126">Specifies the content type of a secret.</span></span> <span data-ttu-id="26662-127">Если этот параметр не указан, изменение типа содержимого текущего секрета не производится.</span><span class="sxs-lookup"><span data-stu-id="26662-127">If you do not specify this parameter, there is no change to the current secret's content type.</span></span> <span data-ttu-id="26662-128">Чтобы удалить существующий тип контента, укажите пустую строку.</span><span class="sxs-lookup"><span data-stu-id="26662-128">To remove the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="26662-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26662-129">-DefaultProfile</span></span>
<span data-ttu-id="26662-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="26662-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26662-131">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="26662-131">-Enable</span></span>
<span data-ttu-id="26662-132">Указывает, следует ли включить секрет.</span><span class="sxs-lookup"><span data-stu-id="26662-132">Indicates whether to enable a secret.</span></span> <span data-ttu-id="26662-133">Укажите $False, чтобы отключить секрет, или $True, чтобы включить секрет.</span><span class="sxs-lookup"><span data-stu-id="26662-133">Specify $False to disable a secret, or $True to enable a secret.</span></span> <span data-ttu-id="26662-134">Если вы не укажете этот параметр, это не изменит состояние разрешенных и отключенных для текущего секрета.</span><span class="sxs-lookup"><span data-stu-id="26662-134">If you do not specify this parameter, there is no change to the current secret's enabled or disabled state.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26662-135">-Истекает</span><span class="sxs-lookup"><span data-stu-id="26662-135">-Expires</span></span>
<span data-ttu-id="26662-136">Указывает дату и время окончания срока действия секрета.</span><span class="sxs-lookup"><span data-stu-id="26662-136">Specifies the date and time that a secret expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26662-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26662-137">-InputObject</span></span>
<span data-ttu-id="26662-138">Секретный объект</span><span class="sxs-lookup"><span data-stu-id="26662-138">Secret object</span></span>

```yaml
Type: PSKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="26662-139">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="26662-139">-Name</span></span>
<span data-ttu-id="26662-140">Указывает имя секрета.</span><span class="sxs-lookup"><span data-stu-id="26662-140">Specifies the name of a secret.</span></span> <span data-ttu-id="26662-141">Этот командлет создает полное доменное имя (FQDN) для секрета на основе имени, которое указывает этот параметр, имя хранилища ключей и текущую среду.</span><span class="sxs-lookup"><span data-stu-id="26662-141">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26662-142">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="26662-142">-NotBefore</span></span>
<span data-ttu-id="26662-143">Указывает координированное координированное время (UTC), перед использованием которого невозможно использовать секретный код.</span><span class="sxs-lookup"><span data-stu-id="26662-143">Specifies the Coordinated Universal Time (UTC) before which the secret can't be used.</span></span>
<span data-ttu-id="26662-144">Если этот параметр не указан, изменение атрибута NotBefore текущего секрета не происходит.</span><span class="sxs-lookup"><span data-stu-id="26662-144">If you do not specify this parameter, there is no change to the current secret's NotBefore attribute.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26662-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="26662-145">-PassThru</span></span>
<span data-ttu-id="26662-146">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="26662-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="26662-147">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="26662-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="26662-148">-Тег</span><span class="sxs-lookup"><span data-stu-id="26662-148">-Tag</span></span>
<span data-ttu-id="26662-149">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="26662-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="26662-150">Например:</span><span class="sxs-lookup"><span data-stu-id="26662-150">For example:</span></span>

<span data-ttu-id="26662-151">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="26662-151">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26662-152">-VaultName</span><span class="sxs-lookup"><span data-stu-id="26662-152">-VaultName</span></span>
<span data-ttu-id="26662-153">Указывает имя хранилища ключей, которое нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="26662-153">Specifies the name of the key vault to modify.</span></span>
<span data-ttu-id="26662-154">Этот командлет создает полное доменное имя хранилища ключей, основываясь на имени, указанном этим параметром, и текущей выбранной среде.</span><span class="sxs-lookup"><span data-stu-id="26662-154">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies, and your currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26662-155">-Version</span><span class="sxs-lookup"><span data-stu-id="26662-155">-Version</span></span>
<span data-ttu-id="26662-156">Указывает версию секрета.</span><span class="sxs-lookup"><span data-stu-id="26662-156">Specifies the version of a secret.</span></span>
<span data-ttu-id="26662-157">Этот командлет создает полное доменное имя секрета на основе имени хранилища ключей, текущей выбранной среды, имени секрета и секретной версии.</span><span class="sxs-lookup"><span data-stu-id="26662-157">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26662-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="26662-158">-Confirm</span></span>
<span data-ttu-id="26662-159">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="26662-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26662-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26662-160">-WhatIf</span></span>
<span data-ttu-id="26662-161">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="26662-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26662-162">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="26662-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26662-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26662-163">CommonParameters</span></span>
<span data-ttu-id="26662-164">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="26662-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26662-165">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26662-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26662-166">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="26662-166">INPUTS</span></span>

### <span data-ttu-id="26662-167">Ничего</span><span class="sxs-lookup"><span data-stu-id="26662-167">None</span></span>
<span data-ttu-id="26662-168">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="26662-168">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="26662-169">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="26662-169">OUTPUTS</span></span>

### <span data-ttu-id="26662-170">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="26662-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>
<span data-ttu-id="26662-171">Возвращает объект Microsoft. Azure. Commands. KeyVault. Models. Secret, если указана функция PassThru.</span><span class="sxs-lookup"><span data-stu-id="26662-171">Returns Microsoft.Azure.Commands.KeyVault.Models.Secret object if PassThru is specified.</span></span> <span data-ttu-id="26662-172">В противном случае возвращает значение Nothing.</span><span class="sxs-lookup"><span data-stu-id="26662-172">Otherwise, returns nothing.</span></span>

## <span data-ttu-id="26662-173">Пуск</span><span class="sxs-lookup"><span data-stu-id="26662-173">NOTES</span></span>

## <span data-ttu-id="26662-174">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26662-174">RELATED LINKS</span></span>

[<span data-ttu-id="26662-175">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="26662-175">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="26662-176">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="26662-176">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="26662-177">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="26662-177">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
