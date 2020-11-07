---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
ms.openlocfilehash: 56a3fb2d31e4f80b15c027945437ffdc78aa131a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911148"
---
# <span data-ttu-id="5b4cc-101">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5b4cc-101">Set-AzKeyVaultSecret</span></span>

## <span data-ttu-id="5b4cc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5b4cc-102">SYNOPSIS</span></span>
<span data-ttu-id="5b4cc-103">Создание или обновление секрета в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-103">Creates or updates a secret in a key vault.</span></span>

## <span data-ttu-id="5b4cc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5b4cc-104">SYNTAX</span></span>

```
Set-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b4cc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b4cc-105">DESCRIPTION</span></span>
<span data-ttu-id="5b4cc-106">Командлет **Set-AzKeyVaultSecret** создает или обновляет секретный ключ в хранилище ключей Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-106">The **Set-AzKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="5b4cc-107">Если секрет не существует, этот командлет создаст его.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-107">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="5b4cc-108">Если секрет уже существует, этот командлет создает новую версию этого секрета.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-108">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="5b4cc-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5b4cc-109">EXAMPLES</span></span>

### <span data-ttu-id="5b4cc-110">Пример 1: изменение значения секрета с помощью атрибутов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="5b4cc-110">Example 1: Modify the value of a secret using default attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret
```

<span data-ttu-id="5b4cc-111">Первая команда преобразует строку в защищенную строку с помощью командлета **ConvertTo-SecureString** , а затем сохраняет эту строку в переменной $Secret.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-111">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="5b4cc-112">Для получения дополнительных сведений введите `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="5b4cc-112">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="5b4cc-113">Вторая команда изменяет значение секрета с именем ITSecret в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-113">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="5b4cc-114">Секретное значение становится значением, хранящимся в $Secret.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-114">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="5b4cc-115">Пример 2: изменение значения секрета с помощью настраиваемых атрибутов</span><span class="sxs-lookup"><span data-stu-id="5b4cc-115">Example 2: Modify the value of a secret using custom attributes</span></span>
```
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = null }
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable $False -Tags $Tags
```

<span data-ttu-id="5b4cc-116">Первая команда преобразует строку в защищенную строку с помощью командлета **ConvertTo-SecureString** , а затем сохраняет эту строку в переменной $Secret.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-116">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="5b4cc-117">Для получения дополнительных сведений введите `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="5b4cc-117">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="5b4cc-118">Следующие команды определяют пользовательские атрибуты для даты окончания срока действия, тегов и типа контекста и хранят атрибуты в переменных.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-118">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>

<span data-ttu-id="5b4cc-119">Последняя команда изменяет значения секрета ITSecret в хранилище ключей, именуемом Contoso, используя значения, указанные ранее в качестве переменных.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-119">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="5b4cc-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5b4cc-120">PARAMETERS</span></span>

### <span data-ttu-id="5b4cc-121">-ContentType</span><span class="sxs-lookup"><span data-stu-id="5b4cc-121">-ContentType</span></span>
<span data-ttu-id="5b4cc-122">Указывает тип содержимого секрета.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-122">Specifies the content type of a secret.</span></span>
<span data-ttu-id="5b4cc-123">Чтобы удалить существующий тип контента, укажите пустую строку.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-123">To delete the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="5b4cc-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b4cc-124">-DefaultProfile</span></span>
<span data-ttu-id="5b4cc-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5b4cc-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b4cc-126">-Отключение</span><span class="sxs-lookup"><span data-stu-id="5b4cc-126">-Disable</span></span>
<span data-ttu-id="5b4cc-127">Указывает на то, что этот командлет отключает секрет.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-127">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="5b4cc-128">-Истекает</span><span class="sxs-lookup"><span data-stu-id="5b4cc-128">-Expires</span></span>
<span data-ttu-id="5b4cc-129">Задает время истечения срока действия, как объект **DateTime** , для секрета, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-129">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="5b4cc-130">Этот параметр использует координированное координированное время (UTC).</span><span class="sxs-lookup"><span data-stu-id="5b4cc-130">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="5b4cc-131">Чтобы получить объект **DateTime** , используйте командлет **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="5b4cc-131">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="5b4cc-132">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="5b4cc-132">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="5b4cc-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5b4cc-133">-Name</span></span>
<span data-ttu-id="5b4cc-134">Указывает имя секрета, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-134">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="5b4cc-135">Этот командлет создает полное доменное имя (FQDN) для секрета на основе имени, которое указывает этот параметр, имя хранилища ключей и текущую среду.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-135">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="5b4cc-136">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="5b4cc-136">-NotBefore</span></span>
<span data-ttu-id="5b4cc-137">Указывает время в виде объекта **DateTime** , перед которым нельзя использовать секрет.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-137">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="5b4cc-138">Этот параметр использует время в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-138">This parameter uses UTC.</span></span> <span data-ttu-id="5b4cc-139">Чтобы получить объект **DateTime** , используйте командлет **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="5b4cc-139">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="5b4cc-140">-SecretValue</span><span class="sxs-lookup"><span data-stu-id="5b4cc-140">-SecretValue</span></span>
<span data-ttu-id="5b4cc-141">Задает значение для секрета как объект **SecureString** .</span><span class="sxs-lookup"><span data-stu-id="5b4cc-141">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="5b4cc-142">Чтобы получить объект **SecureString** , используйте командлет **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="5b4cc-142">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="5b4cc-143">Для получения дополнительных сведений введите `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="5b4cc-143">For more information, type `Get-Help
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

### <span data-ttu-id="5b4cc-144">-Тег</span><span class="sxs-lookup"><span data-stu-id="5b4cc-144">-Tag</span></span>
<span data-ttu-id="5b4cc-145">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-145">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5b4cc-146">Например:</span><span class="sxs-lookup"><span data-stu-id="5b4cc-146">For example:</span></span>

<span data-ttu-id="5b4cc-147">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="5b4cc-147">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5b4cc-148">-VaultName</span><span class="sxs-lookup"><span data-stu-id="5b4cc-148">-VaultName</span></span>
<span data-ttu-id="5b4cc-149">Указывает имя хранилища ключей, к которому относится этот секрет.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-149">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="5b4cc-150">Этот командлет создает полное доменное имя хранилища ключей, основываясь на имени, указанном этим параметром, и текущей среде.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-150">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="5b4cc-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b4cc-151">-Confirm</span></span>
<span data-ttu-id="5b4cc-152">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b4cc-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b4cc-153">-WhatIf</span></span>
<span data-ttu-id="5b4cc-154">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b4cc-155">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b4cc-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b4cc-156">CommonParameters</span></span>
<span data-ttu-id="5b4cc-157">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b4cc-158">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b4cc-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b4cc-159">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5b4cc-159">INPUTS</span></span>

### <span data-ttu-id="5b4cc-160">Ничего</span><span class="sxs-lookup"><span data-stu-id="5b4cc-160">None</span></span>
<span data-ttu-id="5b4cc-161">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="5b4cc-161">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5b4cc-162">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b4cc-162">OUTPUTS</span></span>

### <span data-ttu-id="5b4cc-163">Microsoft. Azure. Commands. KeyVault. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="5b4cc-163">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="5b4cc-164">Пуск</span><span class="sxs-lookup"><span data-stu-id="5b4cc-164">NOTES</span></span>

## <span data-ttu-id="5b4cc-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b4cc-165">RELATED LINKS</span></span>

[<span data-ttu-id="5b4cc-166">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5b4cc-166">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="5b4cc-167">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="5b4cc-167">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)
