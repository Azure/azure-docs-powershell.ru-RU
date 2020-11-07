---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: E2A45461-6B41-42FF-A874-A4CEFC867A33
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultsecretattribute
schema: 2.0.0
ms.openlocfilehash: f8463533f8a153b74df1863ba251950f16f9e19a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913316"
---
# <span data-ttu-id="2e519-101">Set-AzureKeyVaultSecretAttribute</span><span class="sxs-lookup"><span data-stu-id="2e519-101">Set-AzureKeyVaultSecretAttribute</span></span>

## <span data-ttu-id="2e519-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2e519-102">SYNOPSIS</span></span>
<span data-ttu-id="2e519-103">Обновляет атрибуты секрета в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="2e519-103">Updates attributes of a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e519-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2e519-104">SYNTAX</span></span>

```
Set-AzureKeyVaultSecretAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e519-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e519-105">DESCRIPTION</span></span>
<span data-ttu-id="2e519-106">Командлет **Set-AzureKeyVaultSecretAttribute** обновляет редактируемые атрибуты секрета в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="2e519-106">The **Set-AzureKeyVaultSecretAttribute** cmdlet updates editable attributes of a secret in a key vault.</span></span>

## <span data-ttu-id="2e519-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2e519-107">EXAMPLES</span></span>

### <span data-ttu-id="2e519-108">Пример 1: изменение атрибутов секрета</span><span class="sxs-lookup"><span data-stu-id="2e519-108">Example 1: Modify the attributes of a secret</span></span>
```
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Nbf = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'HR' = null}
PS C:\> $ContentType= 'xml'
PS C:\> Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Expires $Expires -NotBefore $Nbf -ContentType $ContentType -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="2e519-109">Первые четыре команды определяют атрибуты для даты окончания срока действия, даты NotBefore, тегов и типа контекста и хранят атрибуты в переменных.</span><span class="sxs-lookup"><span data-stu-id="2e519-109">The first four commands define attributes for the expiry date, the NotBefore date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="2e519-110">Последняя команда изменяет атрибуты секрета с именем HR в хранилище ключей с именем ContosoVault, используя хранимые переменные.</span><span class="sxs-lookup"><span data-stu-id="2e519-110">The final command modifies the attributes for the secret named HR in the key vault named ContosoVault, using the stored variables.</span></span>

### <span data-ttu-id="2e519-111">Пример 2: Удаление тегов и типа контента для секрета</span><span class="sxs-lookup"><span data-stu-id="2e519-111">Example 2: Delete the tags and content type for a secret</span></span>
```
PS C:\>Set-AzureKeyVaultSecretAttribute -VaultName 'ContosoVault' -Name 'HR' -Version '9EEA45C6EE50490B9C3176A80AC1A0DF' -ContentType '' -Tag -@{}
```

<span data-ttu-id="2e519-112">Эта команда удаляет Теги и тип контента для указанной версии секретного файла с именем HR в хранилище ключей contoso.</span><span class="sxs-lookup"><span data-stu-id="2e519-112">This command deletes the tags and the content type for the specified version of the secret named HR in the key vault named Contoso.</span></span>

### <span data-ttu-id="2e519-113">Пример 3: отключение текущей версии секретных данных, имя которой начинается с нее</span><span class="sxs-lookup"><span data-stu-id="2e519-113">Example 3: Disable the current version of secrets whose name begins with IT</span></span>
```
PS C:\> $Vault = 'ContosoVault'
PS C:\> $Prefix = 'IT'
PS C:\> Get-AzureKeyVaultSecret $Vault | Where-Object {$_.Name -like $Prefix + '*'} | Set-AzureKeyVaultSecretAttribute -Enable $False
```

<span data-ttu-id="2e519-114">Первая команда сохраняет строковое значение Contoso в переменной $Vault.</span><span class="sxs-lookup"><span data-stu-id="2e519-114">The first command stores the string value Contoso in the $Vault variable.</span></span>

<span data-ttu-id="2e519-115">Вторая команда сохраняет строковое значение в переменной $Prefix.</span><span class="sxs-lookup"><span data-stu-id="2e519-115">The second command stores the string value IT in the $Prefix variable.</span></span>

<span data-ttu-id="2e519-116">Третья команда использует командлет Get-AzureKeyVaultSecret для получения секретных данных в указанном хранилище ключей, а затем передает эти секреты в командлет **Where-Object** .</span><span class="sxs-lookup"><span data-stu-id="2e519-116">The third command uses the Get-AzureKeyVaultSecret cmdlet to get the secrets in the specified key vault, and then passes those secrets to the **Where-Object** cmdlet.</span></span> <span data-ttu-id="2e519-117">Командлет **Where-Object** фильтрует секреты для имен, начинающихся с этих знаков.</span><span class="sxs-lookup"><span data-stu-id="2e519-117">The **Where-Object** cmdlet filters the secrets for names that begin with the characters IT.</span></span> <span data-ttu-id="2e519-118">Команда найдет секреты, соответствующие фильтру, в командлет Set-AzureKeyVaultSecretAttribute, который отключается.</span><span class="sxs-lookup"><span data-stu-id="2e519-118">The command pipes the secrets that match the filter to the Set-AzureKeyVaultSecretAttribute cmdlet, which disables them.</span></span>

### <span data-ttu-id="2e519-119">Пример 4: Настройка ContentType для всех версий секрета</span><span class="sxs-lookup"><span data-stu-id="2e519-119">Example 4: Set the ContentType for all versions of a secret</span></span>
```
PS C:\>$VaultName = 'ContosoVault'
PS C:\> $Name = 'HR'
PS C:\> $ContentType = 'xml'
PS C:\> Get-AzureKeyVaultKey -VaultName $VaultName -Name $Name -IncludeVersions | Set-AzureKeyVaultSecretAttribute -ContentType $ContentType
```

<span data-ttu-id="2e519-120">Первые три команды определяют переменные типа String, используемые для параметров *VaultName* , *Name* и *ContentType* .</span><span class="sxs-lookup"><span data-stu-id="2e519-120">The first three commands define string variables to use for the *VaultName* , *Name* , and *ContentType* parameters.</span></span> <span data-ttu-id="2e519-121">Четвертая команда использует командлет Get-AzureKeyVaultKey, чтобы получить указанные ключи, и переводит ключи в командлет Set-AzureKeyVaultSecretAttribute, чтобы задать для их типа содержимого значение XML.</span><span class="sxs-lookup"><span data-stu-id="2e519-121">The fourth command uses the Get-AzureKeyVaultKey cmdlet to get the specified keys, and pipes the keys to the Set-AzureKeyVaultSecretAttribute cmdlet to set their content type to XML.</span></span>

## <span data-ttu-id="2e519-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2e519-122">PARAMETERS</span></span>

### <span data-ttu-id="2e519-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="2e519-123">-ContentType</span></span>
<span data-ttu-id="2e519-124">Указывает тип содержимого секрета.</span><span class="sxs-lookup"><span data-stu-id="2e519-124">Specifies the content type of a secret.</span></span> <span data-ttu-id="2e519-125">Если этот параметр не указан, изменение типа содержимого текущего секрета не производится.</span><span class="sxs-lookup"><span data-stu-id="2e519-125">If you do not specify this parameter, there is no change to the current secret's content type.</span></span> <span data-ttu-id="2e519-126">Чтобы удалить существующий тип контента, укажите пустую строку.</span><span class="sxs-lookup"><span data-stu-id="2e519-126">To remove the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="2e519-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e519-127">-DefaultProfile</span></span>
<span data-ttu-id="2e519-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2e519-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2e519-129">-Enable (включить)</span><span class="sxs-lookup"><span data-stu-id="2e519-129">-Enable</span></span>
<span data-ttu-id="2e519-130">Указывает, следует ли включить секрет.</span><span class="sxs-lookup"><span data-stu-id="2e519-130">Indicates whether to enable a secret.</span></span> <span data-ttu-id="2e519-131">Укажите $False, чтобы отключить секрет, или $True, чтобы включить секрет.</span><span class="sxs-lookup"><span data-stu-id="2e519-131">Specify $False to disable a secret, or $True to enable a secret.</span></span> <span data-ttu-id="2e519-132">Если вы не укажете этот параметр, это не изменит состояние разрешенных и отключенных для текущего секрета.</span><span class="sxs-lookup"><span data-stu-id="2e519-132">If you do not specify this parameter, there is no change to the current secret's enabled or disabled state.</span></span>

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

### <span data-ttu-id="2e519-133">-Истекает</span><span class="sxs-lookup"><span data-stu-id="2e519-133">-Expires</span></span>
<span data-ttu-id="2e519-134">Указывает дату и время окончания срока действия секрета.</span><span class="sxs-lookup"><span data-stu-id="2e519-134">Specifies the date and time that a secret expires.</span></span>

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

### <span data-ttu-id="2e519-135">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2e519-135">-Name</span></span>
<span data-ttu-id="2e519-136">Указывает имя секрета.</span><span class="sxs-lookup"><span data-stu-id="2e519-136">Specifies the name of a secret.</span></span> <span data-ttu-id="2e519-137">Этот командлет создает полное доменное имя (FQDN) для секрета на основе имени, которое указывает этот параметр, имя хранилища ключей и текущую среду.</span><span class="sxs-lookup"><span data-stu-id="2e519-137">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="2e519-138">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="2e519-138">-NotBefore</span></span>
<span data-ttu-id="2e519-139">Указывает координированное координированное время (UTC), перед использованием которого невозможно использовать секретный код.</span><span class="sxs-lookup"><span data-stu-id="2e519-139">Specifies the Coordinated Universal Time (UTC) before which the secret can't be used.</span></span>
<span data-ttu-id="2e519-140">Если этот параметр не указан, изменение атрибута NotBefore текущего секрета не происходит.</span><span class="sxs-lookup"><span data-stu-id="2e519-140">If you do not specify this parameter, there is no change to the current secret's NotBefore attribute.</span></span>

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

### <span data-ttu-id="2e519-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e519-141">-PassThru</span></span>
<span data-ttu-id="2e519-142">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="2e519-142">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2e519-143">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="2e519-143">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2e519-144">-Тег</span><span class="sxs-lookup"><span data-stu-id="2e519-144">-Tag</span></span>
<span data-ttu-id="2e519-145">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="2e519-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="2e519-146">Например:</span><span class="sxs-lookup"><span data-stu-id="2e519-146">For example:</span></span>

<span data-ttu-id="2e519-147">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="2e519-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="2e519-148">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2e519-148">-VaultName</span></span>
<span data-ttu-id="2e519-149">Указывает имя хранилища ключей, которое нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="2e519-149">Specifies the name of the key vault to modify.</span></span>
<span data-ttu-id="2e519-150">Этот командлет создает полное доменное имя хранилища ключей, основываясь на имени, указанном этим параметром, и текущей выбранной среде.</span><span class="sxs-lookup"><span data-stu-id="2e519-150">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies, and your currently selected environment.</span></span>

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

### <span data-ttu-id="2e519-151">-Version</span><span class="sxs-lookup"><span data-stu-id="2e519-151">-Version</span></span>
<span data-ttu-id="2e519-152">Указывает версию секрета.</span><span class="sxs-lookup"><span data-stu-id="2e519-152">Specifies the version of a secret.</span></span>
<span data-ttu-id="2e519-153">Этот командлет создает полное доменное имя секрета на основе имени хранилища ключей, текущей выбранной среды, имени секрета и секретной версии.</span><span class="sxs-lookup"><span data-stu-id="2e519-153">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

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

### <span data-ttu-id="2e519-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e519-154">-Confirm</span></span>
<span data-ttu-id="2e519-155">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2e519-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e519-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e519-156">-WhatIf</span></span>
<span data-ttu-id="2e519-157">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2e519-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e519-158">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2e519-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e519-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e519-159">CommonParameters</span></span>
<span data-ttu-id="2e519-160">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2e519-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e519-161">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e519-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e519-162">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2e519-162">INPUTS</span></span>

## <span data-ttu-id="2e519-163">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2e519-163">OUTPUTS</span></span>

### <span data-ttu-id="2e519-164">Microsoft. Azure. Commands. KeyVault. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="2e519-164">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>
<span data-ttu-id="2e519-165">Возвращает объект Microsoft. Azure. Commands. KeyVault. Models. Secret, если указана функция PassThru.</span><span class="sxs-lookup"><span data-stu-id="2e519-165">Returns Microsoft.Azure.Commands.KeyVault.Models.Secret object if PassThru is specified.</span></span> <span data-ttu-id="2e519-166">В противном случае возвращает значение Nothing.</span><span class="sxs-lookup"><span data-stu-id="2e519-166">Otherwise, returns nothing.</span></span>

## <span data-ttu-id="2e519-167">Пуск</span><span class="sxs-lookup"><span data-stu-id="2e519-167">NOTES</span></span>

## <span data-ttu-id="2e519-168">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2e519-168">RELATED LINKS</span></span>

[<span data-ttu-id="2e519-169">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2e519-169">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="2e519-170">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2e519-170">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="2e519-171">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="2e519-171">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
