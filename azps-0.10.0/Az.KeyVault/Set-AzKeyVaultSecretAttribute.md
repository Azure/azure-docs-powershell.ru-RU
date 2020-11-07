---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: E2A45461-6B41-42FF-A874-A4CEFC867A33
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultsecretattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecretAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecretAttribute.md
ms.openlocfilehash: 719f0676b87cf785785b0adfbfde71ad2a6b965b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910272"
---
# <span data-ttu-id="f7dec-101">Set-AzKeyVaultSecretAttribute</span><span class="sxs-lookup"><span data-stu-id="f7dec-101">Set-AzKeyVaultSecretAttribute</span></span>

## <span data-ttu-id="f7dec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7dec-102">SYNOPSIS</span></span>
<span data-ttu-id="f7dec-103">Обновляет атрибуты секрета в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="f7dec-103">Updates attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="f7dec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7dec-104">SYNTAX</span></span>

```
Set-AzKeyVaultSecretAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7dec-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7dec-105">DESCRIPTION</span></span>
<span data-ttu-id="f7dec-106">Командлет **Set-AzKeyVaultSecretAttribute** обновляет редактируемые атрибуты секрета в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="f7dec-106">The **Set-AzKeyVaultSecretAttribute** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="f7dec-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7dec-107">EXAMPLES</span></span>

### <span data-ttu-id="f7dec-108">Пример 1: изменение атрибутов секрета</span><span class="sxs-lookup"><span data-stu-id="f7dec-108">Example 1: Modify the attributes of a secret</span></span>
```
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = null}
PS C:\> $ContentType= 'xml'
PS C:\> Set-AzKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="f7dec-109">Первые четыре команды определяют атрибуты для даты окончания срока действия, даты NotBefore, тегов и типа контекста и хранят атрибуты в переменных.</span><span class="sxs-lookup"><span data-stu-id="f7dec-109">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="f7dec-110">Последняя команда изменяет атрибуты секрета с именем HR в хранилище ключей с именем ContosoVault, используя хранимые переменные.</span><span class="sxs-lookup"><span data-stu-id="f7dec-110">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="f7dec-111">Пример 2: Удаление тегов и типа контента для секрета</span><span class="sxs-lookup"><span data-stu-id="f7dec-111">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\>Set-AzKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="f7dec-112">Эта команда удаляет Теги и тип контента для указанной версии секретного файла с именем HR в хранилище ключей contoso.</span><span class="sxs-lookup"><span data-stu-id="f7dec-112">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="f7dec-113">Пример 3: отключение текущей версии секретных данных, имя которой начинается с нее</span><span class="sxs-lookup"><span data-stu-id="f7dec-113">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Set-AzKeyVaultSecretAttribute -Enable $False
```

<span data-ttu-id="f7dec-114">Первая команда сохраняет строковое значение Contoso в переменной $Vault.</span><span class="sxs-lookup"><span data-stu-id="f7dec-114">The first command stores the string value Contoso in the $Vault variable.</span></span>

<span data-ttu-id="f7dec-115">Вторая команда сохраняет строковое значение в переменной $Prefix.</span><span class="sxs-lookup"><span data-stu-id="f7dec-115">The second command stores the string value IT in the $Prefix variable.</span></span>

<span data-ttu-id="f7dec-116">Третья команда использует командлет Get-AzKeyVaultSecret для получения секретных данных в указанном хранилище ключей, а затем передает эти секреты в командлет **Where-Object** .</span><span class="sxs-lookup"><span data-stu-id="f7dec-116">The third command uses the Get-AzKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="f7dec-117">Командлет **Where-Object** фильтрует секреты для имен, начинающихся с этих знаков.</span><span class="sxs-lookup"><span data-stu-id="f7dec-117">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="f7dec-118">Команда найдет секреты, соответствующие фильтру, в командлет Set-AzKeyVaultSecretAttribute, который отключается.</span><span class="sxs-lookup"><span data-stu-id="f7dec-118">The command pipes the secrets that match the filter to the Set-AzKeyVaultSecretAttribute cmdlet, which disables them.</span></span>

### <span data-ttu-id="f7dec-119">Пример 4: Настройка ContentType для всех версий секрета</span><span class="sxs-lookup"><span data-stu-id="f7dec-119">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\>$VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Set-AzKeyVaultSecretAttribute -ContentType $ContentType
```

<span data-ttu-id="f7dec-120">Первые три команды определяют переменные типа String, используемые для параметров *VaultName* , *Name* и *ContentType* .</span><span class="sxs-lookup"><span data-stu-id="f7dec-120">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="f7dec-121">Четвертая команда использует командлет Get-AzKeyVaultKey, чтобы получить указанные ключи, и переводит ключи в командлет Set-AzKeyVaultSecretAttribute, чтобы задать для их типа содержимого значение XML.</span><span class="sxs-lookup"><span data-stu-id="f7dec-121">The fourth command uses the Get-AzKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Set-AzKeyVaultSecretAttribute cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="f7dec-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7dec-122">PARAMETERS</span></span>

### <span data-ttu-id="f7dec-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="f7dec-123">-ContentType</span></span>
<span data-ttu-id="f7dec-124">Указывает тип содержимого секрета.</span><span class="sxs-lookup"><span data-stu-id="f7dec-124">Specifies the content type of a secret.</span></span> <span data-ttu-id="f7dec-125">Если этот параметр не указан, изменение типа содержимого текущего секрета не производится.</span><span class="sxs-lookup"><span data-stu-id="f7dec-125">If you do not specify this parameter, there is no change to the current secret's content type.</span></span> <span data-ttu-id="f7dec-126">Чтобы удалить существующий тип контента, укажите пустую строку.</span><span class="sxs-lookup"><span data-stu-id="f7dec-126">To remove the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="f7dec-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7dec-127">-DefaultProfile</span></span>
<span data-ttu-id="f7dec-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f7dec-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7dec-129">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="f7dec-129">-Enable</span></span>
<span data-ttu-id="f7dec-130">Указывает, следует ли включить секрет.</span><span class="sxs-lookup"><span data-stu-id="f7dec-130">Indicates whether to enable a secret.</span></span> <span data-ttu-id="f7dec-131">Укажите $False, чтобы отключить секрет, или $True, чтобы включить секрет.</span><span class="sxs-lookup"><span data-stu-id="f7dec-131">Specify $False to disable a secret, or $True to enable a secret.</span></span> <span data-ttu-id="f7dec-132">Если вы не укажете этот параметр, это не изменит состояние разрешенных и отключенных для текущего секрета.</span><span class="sxs-lookup"><span data-stu-id="f7dec-132">If you do not specify this parameter, there is no change to the current secret's enabled or disabled state.</span></span>

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

### <span data-ttu-id="f7dec-133">-Истекает</span><span class="sxs-lookup"><span data-stu-id="f7dec-133">-Expires</span></span>
<span data-ttu-id="f7dec-134">Указывает дату и время окончания срока действия секрета.</span><span class="sxs-lookup"><span data-stu-id="f7dec-134">Specifies the date and time that a secret expires.</span></span>

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

### <span data-ttu-id="f7dec-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f7dec-135">-Name</span></span>
<span data-ttu-id="f7dec-136">Указывает имя секрета.</span><span class="sxs-lookup"><span data-stu-id="f7dec-136">Specifies the name of a secret.</span></span> <span data-ttu-id="f7dec-137">Этот командлет создает полное доменное имя (FQDN) для секрета на основе имени, которое указывает этот параметр, имя хранилища ключей и текущую среду.</span><span class="sxs-lookup"><span data-stu-id="f7dec-137">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7dec-138">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="f7dec-138">-NotBefore</span></span>
<span data-ttu-id="f7dec-139">Указывает координированное координированное время (UTC), перед использованием которого невозможно использовать секретный код.</span><span class="sxs-lookup"><span data-stu-id="f7dec-139">Specifies the Coordinated Universal Time (UTC) before which the secret can't be used.</span></span>
<span data-ttu-id="f7dec-140">Если этот параметр не указан, изменение атрибута NotBefore текущего секрета не происходит.</span><span class="sxs-lookup"><span data-stu-id="f7dec-140">If you do not specify this parameter, there is no change to the current secret's NotBefore attribute.</span></span>

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

### <span data-ttu-id="f7dec-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7dec-141">-PassThru</span></span>
<span data-ttu-id="f7dec-142">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="f7dec-142">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f7dec-143">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f7dec-143">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f7dec-144">-Тег</span><span class="sxs-lookup"><span data-stu-id="f7dec-144">-Tag</span></span>
<span data-ttu-id="f7dec-145">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="f7dec-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f7dec-146">Например:</span><span class="sxs-lookup"><span data-stu-id="f7dec-146">For example:</span></span>

<span data-ttu-id="f7dec-147">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="f7dec-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f7dec-148">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f7dec-148">-VaultName</span></span>
<span data-ttu-id="f7dec-149">Указывает имя хранилища ключей, которое нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="f7dec-149">Specifies the name of the key vault to modify.</span></span>
<span data-ttu-id="f7dec-150">Этот командлет создает полное доменное имя хранилища ключей, основываясь на имени, указанном этим параметром, и текущей выбранной среде.</span><span class="sxs-lookup"><span data-stu-id="f7dec-150">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies, and your currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7dec-151">-Version</span><span class="sxs-lookup"><span data-stu-id="f7dec-151">-Version</span></span>
<span data-ttu-id="f7dec-152">Указывает версию секрета.</span><span class="sxs-lookup"><span data-stu-id="f7dec-152">Specifies the version of a secret.</span></span>
<span data-ttu-id="f7dec-153">Этот командлет создает полное доменное имя секрета на основе имени хранилища ключей, текущей выбранной среды, имени секрета и секретной версии.</span><span class="sxs-lookup"><span data-stu-id="f7dec-153">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

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

### <span data-ttu-id="f7dec-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7dec-154">-Confirm</span></span>
<span data-ttu-id="f7dec-155">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f7dec-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7dec-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7dec-156">-WhatIf</span></span>
<span data-ttu-id="f7dec-157">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f7dec-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7dec-158">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f7dec-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7dec-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7dec-159">CommonParameters</span></span>
<span data-ttu-id="f7dec-160">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7dec-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7dec-161">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7dec-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7dec-162">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7dec-162">INPUTS</span></span>

### <span data-ttu-id="f7dec-163">Ничего</span><span class="sxs-lookup"><span data-stu-id="f7dec-163">None</span></span>
<span data-ttu-id="f7dec-164">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f7dec-164">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f7dec-165">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7dec-165">OUTPUTS</span></span>

### <span data-ttu-id="f7dec-166">Microsoft. Azure. Commands. KeyVault. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="f7dec-166">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>
<span data-ttu-id="f7dec-167">Возвращает объект Microsoft. Azure. Commands. KeyVault. Models. Secret, если указана функция PassThru.</span><span class="sxs-lookup"><span data-stu-id="f7dec-167">Returns Microsoft.Azure.Commands.KeyVault.Models.Secret object if PassThru is specified.</span></span> <span data-ttu-id="f7dec-168">В противном случае возвращает значение Nothing.</span><span class="sxs-lookup"><span data-stu-id="f7dec-168">Otherwise, returns nothing.</span></span>

## <span data-ttu-id="f7dec-169">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7dec-169">NOTES</span></span>

## <span data-ttu-id="f7dec-170">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7dec-170">RELATED LINKS</span></span>

[<span data-ttu-id="f7dec-171">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f7dec-171">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="f7dec-172">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f7dec-172">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="f7dec-173">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f7dec-173">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)
