---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultSecret.md
ms.openlocfilehash: c7968d915ab28dca6bf595e5339d2681962ecdea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734706"
---
# <span data-ttu-id="7d6be-101">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7d6be-101">Set-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="7d6be-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7d6be-102">SYNOPSIS</span></span>
<span data-ttu-id="7d6be-103">Создание или обновление секрета в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="7d6be-103">Creates or updates a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d6be-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7d6be-104">SYNTAX</span></span>

### <span data-ttu-id="7d6be-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7d6be-105">Default (Default)</span></span>
```
Set-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d6be-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="7d6be-106">InputObject</span></span>
```
Set-AzureKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d6be-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d6be-107">DESCRIPTION</span></span>
<span data-ttu-id="7d6be-108">Командлет **Set-AzureKeyVaultSecret** создает или обновляет секретный ключ в хранилище ключей Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="7d6be-108">The **Set-AzureKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="7d6be-109">Если секрет не существует, этот командлет создаст его.</span><span class="sxs-lookup"><span data-stu-id="7d6be-109">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="7d6be-110">Если секрет уже существует, этот командлет создает новую версию этого секрета.</span><span class="sxs-lookup"><span data-stu-id="7d6be-110">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="7d6be-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7d6be-111">EXAMPLES</span></span>

### <span data-ttu-id="7d6be-112">Пример 1: изменение значения секрета с помощью атрибутов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="7d6be-112">Example 1: Modify the value of a secret using default attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret
```

<span data-ttu-id="7d6be-113">Первая команда преобразует строку в защищенную строку с помощью командлета **ConvertTo-SecureString** , а затем сохраняет эту строку в переменной $Secret.</span><span class="sxs-lookup"><span data-stu-id="7d6be-113">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="7d6be-114">Для получения дополнительных сведений введите `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="7d6be-114">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="7d6be-115">Вторая команда изменяет значение секрета с именем ITSecret в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="7d6be-115">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="7d6be-116">Секретное значение становится значением, хранящимся в $Secret.</span><span class="sxs-lookup"><span data-stu-id="7d6be-116">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="7d6be-117">Пример 2: изменение значения секрета с помощью настраиваемых атрибутов</span><span class="sxs-lookup"><span data-stu-id="7d6be-117">Example 2: Modify the value of a secret using custom attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = null }
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable $False -Tags $Tags
```

<span data-ttu-id="7d6be-118">Первая команда преобразует строку в защищенную строку с помощью командлета **ConvertTo-SecureString** , а затем сохраняет эту строку в переменной $Secret.</span><span class="sxs-lookup"><span data-stu-id="7d6be-118">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="7d6be-119">Для получения дополнительных сведений введите `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="7d6be-119">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="7d6be-120">Следующие команды определяют пользовательские атрибуты для даты окончания срока действия, тегов и типа контекста и хранят атрибуты в переменных.</span><span class="sxs-lookup"><span data-stu-id="7d6be-120">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="7d6be-121">Последняя команда изменяет значения секрета ITSecret в хранилище ключей, именуемом Contoso, используя значения, указанные ранее в качестве переменных.</span><span class="sxs-lookup"><span data-stu-id="7d6be-121">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="7d6be-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7d6be-122">PARAMETERS</span></span>

### <span data-ttu-id="7d6be-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="7d6be-123">-ContentType</span></span>
<span data-ttu-id="7d6be-124">Указывает тип содержимого секрета.</span><span class="sxs-lookup"><span data-stu-id="7d6be-124">Specifies the content type of a secret.</span></span>
<span data-ttu-id="7d6be-125">Чтобы удалить существующий тип контента, укажите пустую строку.</span><span class="sxs-lookup"><span data-stu-id="7d6be-125">To delete the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="7d6be-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d6be-126">-DefaultProfile</span></span>
<span data-ttu-id="7d6be-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7d6be-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d6be-128">-Отключение</span><span class="sxs-lookup"><span data-stu-id="7d6be-128">-Disable</span></span>
<span data-ttu-id="7d6be-129">Указывает на то, что этот командлет отключает секрет.</span><span class="sxs-lookup"><span data-stu-id="7d6be-129">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="7d6be-130">-Истекает</span><span class="sxs-lookup"><span data-stu-id="7d6be-130">-Expires</span></span>
<span data-ttu-id="7d6be-131">Задает время истечения срока действия, как объект **DateTime** , для секрета, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="7d6be-131">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="7d6be-132">Этот параметр использует координированное координированное время (UTC).</span><span class="sxs-lookup"><span data-stu-id="7d6be-132">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="7d6be-133">Чтобы получить объект **DateTime** , используйте командлет **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="7d6be-133">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="7d6be-134">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="7d6be-134">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="7d6be-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d6be-135">-InputObject</span></span>
<span data-ttu-id="7d6be-136">Секретный объект</span><span class="sxs-lookup"><span data-stu-id="7d6be-136">Secret object</span></span>

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

### <span data-ttu-id="7d6be-137">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7d6be-137">-Name</span></span>
<span data-ttu-id="7d6be-138">Указывает имя секрета, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="7d6be-138">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="7d6be-139">Этот командлет создает полное доменное имя (FQDN) для секрета на основе имени, которое указывает этот параметр, имя хранилища ключей и текущую среду.</span><span class="sxs-lookup"><span data-stu-id="7d6be-139">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="7d6be-140">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="7d6be-140">-NotBefore</span></span>
<span data-ttu-id="7d6be-141">Указывает время в виде объекта **DateTime** , перед которым нельзя использовать секрет.</span><span class="sxs-lookup"><span data-stu-id="7d6be-141">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="7d6be-142">Этот параметр использует время в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="7d6be-142">This parameter uses UTC.</span></span> <span data-ttu-id="7d6be-143">Чтобы получить объект **DateTime** , используйте командлет **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="7d6be-143">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="7d6be-144">-SecretValue</span><span class="sxs-lookup"><span data-stu-id="7d6be-144">-SecretValue</span></span>
<span data-ttu-id="7d6be-145">Задает значение для секрета как объект **SecureString** .</span><span class="sxs-lookup"><span data-stu-id="7d6be-145">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="7d6be-146">Чтобы получить объект **SecureString** , используйте командлет **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="7d6be-146">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="7d6be-147">Для получения дополнительных сведений введите `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="7d6be-147">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6be-148">-Тег</span><span class="sxs-lookup"><span data-stu-id="7d6be-148">-Tag</span></span>
<span data-ttu-id="7d6be-149">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="7d6be-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="7d6be-150">Например:</span><span class="sxs-lookup"><span data-stu-id="7d6be-150">For example:</span></span>

<span data-ttu-id="7d6be-151">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="7d6be-151">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7d6be-152">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7d6be-152">-VaultName</span></span>
<span data-ttu-id="7d6be-153">Указывает имя хранилища ключей, к которому относится этот секрет.</span><span class="sxs-lookup"><span data-stu-id="7d6be-153">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="7d6be-154">Этот командлет создает полное доменное имя хранилища ключей, основываясь на имени, указанном этим параметром, и текущей среде.</span><span class="sxs-lookup"><span data-stu-id="7d6be-154">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="7d6be-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7d6be-155">-Confirm</span></span>
<span data-ttu-id="7d6be-156">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7d6be-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d6be-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d6be-157">-WhatIf</span></span>
<span data-ttu-id="7d6be-158">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7d6be-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d6be-159">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7d6be-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d6be-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d6be-160">CommonParameters</span></span>
<span data-ttu-id="7d6be-161">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7d6be-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d6be-162">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d6be-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d6be-163">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7d6be-163">INPUTS</span></span>

### <span data-ttu-id="7d6be-164">Ничего</span><span class="sxs-lookup"><span data-stu-id="7d6be-164">None</span></span>
<span data-ttu-id="7d6be-165">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="7d6be-165">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7d6be-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7d6be-166">OUTPUTS</span></span>

### <span data-ttu-id="7d6be-167">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7d6be-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="7d6be-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="7d6be-168">NOTES</span></span>

## <span data-ttu-id="7d6be-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7d6be-169">RELATED LINKS</span></span>

[<span data-ttu-id="7d6be-170">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7d6be-170">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="7d6be-171">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7d6be-171">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)
