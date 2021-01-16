---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 9FC72DE9-46BB-4CB5-9880-F53756DBE012
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultSecret.md
ms.openlocfilehash: 0733cf722e26cb52abdb84f7917a78d088f49fd4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402775"
---
# <span data-ttu-id="149eb-101">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="149eb-101">Set-AzKeyVaultSecret</span></span>

## <span data-ttu-id="149eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="149eb-102">SYNOPSIS</span></span>
<span data-ttu-id="149eb-103">Создает или обновляет секрет в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="149eb-103">Creates or updates a secret in a key vault.</span></span>

## <span data-ttu-id="149eb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="149eb-104">SYNTAX</span></span>

### <span data-ttu-id="149eb-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="149eb-105">Default (Default)</span></span>
```
Set-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="149eb-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="149eb-106">InputObject</span></span>
```
Set-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-SecretValue] <SecureString> [-Disable]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-ContentType <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="149eb-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="149eb-107">DESCRIPTION</span></span>
<span data-ttu-id="149eb-108">**Cmdlet Set-AzKeyVaultSecret** создает или обновляет секрет в хранилище ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="149eb-108">The **Set-AzKeyVaultSecret** cmdlet creates or updates a secret in a key vault in Azure Key Vault.</span></span> <span data-ttu-id="149eb-109">Если секрет не существует, он создается этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="149eb-109">If the secret does not exist, this cmdlet creates it.</span></span> <span data-ttu-id="149eb-110">Если секрет уже существует, этот cmdlet создает новую версию этого секрета.</span><span class="sxs-lookup"><span data-stu-id="149eb-110">If the secret already exists, this cmdlet creates a new version of that secret.</span></span>

## <span data-ttu-id="149eb-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="149eb-111">EXAMPLES</span></span>

### <span data-ttu-id="149eb-112">Пример 1. Изменение значения секретного с помощью атрибутов по умолчанию</span><span class="sxs-lookup"><span data-stu-id="149eb-112">Example 1: Modify the value of a secret using default attributes</span></span>
```powershell
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Set-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret

Vault Name   : Contoso
Name         : ITSecret
Version      : 8b5c0cb0326e4350bd78200fac932b51
Id           : https://contoso.vault.azure.net:443/secrets/ITSecret/8b5c0cb0326e4350bd78200fac932b51
Enabled      : True
Expires      :
Not Before   :
Created      : 5/25/2018 6:39:30 PM
Updated      : 5/25/2018 6:39:30 PM
Content Type :
Tags         :
```

<span data-ttu-id="149eb-113">Первая команда преобразует строку в безопасную строку с помощью командлета **ConvertTo-SecureString,** а затем сохраняет ее в $Secret строке.</span><span class="sxs-lookup"><span data-stu-id="149eb-113">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="149eb-114">Для получения дополнительных сведений введите `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="149eb-114">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="149eb-115">Вторая команда изменяет значение секретного имени ITSecret в хранилище ключей Contoso.</span><span class="sxs-lookup"><span data-stu-id="149eb-115">The second command modifies value of the secret named ITSecret in the key vault named Contoso.</span></span> <span data-ttu-id="149eb-116">Секретное значение становится значением, храняным в $Secret.</span><span class="sxs-lookup"><span data-stu-id="149eb-116">The secret value becomes the value stored in $Secret.</span></span>

### <span data-ttu-id="149eb-117">Пример 2. Изменение значения секретного с помощью настраиваемого атрибута</span><span class="sxs-lookup"><span data-stu-id="149eb-117">Example 2: Modify the value of a secret using custom attributes</span></span>
```powershell
PS C:\> $Secret = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NBF =(Get-Date).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'medium'; 'IT' = 'true'}
PS C:\> $ContentType = 'txt'
PS C:\> Set-AzKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -SecretValue $Secret -Expires $Expires -NotBefore $NBF -ContentType $ContentType -Disable -Tags $Tags

Vault Name   : Contoso
Name         : ITSecret
Version      : a2c150be3ea24dd6b8286986e6364851
Id           : https://contoso.vault.azure.net:443/secrets/ITSecret/a2c150be3ea24dd6b8286986e6364851
Enabled      : False
Expires      : 5/25/2020 6:40:00 PM
Not Before   : 5/25/2018 6:40:05 PM
Created      : 5/25/2018 6:41:22 PM
Updated      : 5/25/2018 6:41:22 PM
Content Type : txt
Tags         : Name      Value
               Severity  medium
               IT        true
```

<span data-ttu-id="149eb-118">Первая команда преобразует строку в безопасную строку с помощью командлета **ConvertTo-SecureString,** а затем сохраняет ее в $Secret строке.</span><span class="sxs-lookup"><span data-stu-id="149eb-118">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Secret variable.</span></span> <span data-ttu-id="149eb-119">Для получения дополнительных сведений введите `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="149eb-119">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="149eb-120">Следующая команда определяет настраиваемые атрибуты для даты окончания срока действия, тегов и типа контекста и сохраняет атрибуты в переменных.</span><span class="sxs-lookup"><span data-stu-id="149eb-120">The next commands define custom attributes for the expiry date, tags, and context type, and store the attributes in variables.</span></span>
<span data-ttu-id="149eb-121">Итоговая команда изменяет значения секретного ИТ-секрета в хранилище ключей Contoso, используя значения, указанные ранее в качестве переменных.</span><span class="sxs-lookup"><span data-stu-id="149eb-121">The final command modifies values of the secret named ITSecret in the key vault named Contoso, by using the values specified previously as variables.</span></span>

## <span data-ttu-id="149eb-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="149eb-122">PARAMETERS</span></span>

### <span data-ttu-id="149eb-123">-ContentType</span><span class="sxs-lookup"><span data-stu-id="149eb-123">-ContentType</span></span>
<span data-ttu-id="149eb-124">Тип содержимого секрета.</span><span class="sxs-lookup"><span data-stu-id="149eb-124">Specifies the content type of a secret.</span></span>
<span data-ttu-id="149eb-125">Чтобы удалить существующий тип контента, укажите пустую строку.</span><span class="sxs-lookup"><span data-stu-id="149eb-125">To delete the existing content type, specify an empty string.</span></span>

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

### <span data-ttu-id="149eb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="149eb-126">-DefaultProfile</span></span>
<span data-ttu-id="149eb-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="149eb-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="149eb-128">-Disable</span><span class="sxs-lookup"><span data-stu-id="149eb-128">-Disable</span></span>
<span data-ttu-id="149eb-129">Указывает на то, что этот cmdlet отключает секрет.</span><span class="sxs-lookup"><span data-stu-id="149eb-129">Indicates that this cmdlet disables a secret.</span></span>

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

### <span data-ttu-id="149eb-130">-Expires</span><span class="sxs-lookup"><span data-stu-id="149eb-130">-Expires</span></span>
<span data-ttu-id="149eb-131">Срок действия указывается в качестве объекта **даты и** времени для секретного объекта, который обновляется этим cmdletом.</span><span class="sxs-lookup"><span data-stu-id="149eb-131">Specifies the expiration time, as a **DateTime** object, for the secret that this cmdlet updates.</span></span>
<span data-ttu-id="149eb-132">Этот параметр использует UTC.</span><span class="sxs-lookup"><span data-stu-id="149eb-132">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="149eb-133">Чтобы получить объект **даты и времени,** используйте cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="149eb-133">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="149eb-134">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="149eb-134">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="149eb-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="149eb-135">-InputObject</span></span>
<span data-ttu-id="149eb-136">Секретный объект</span><span class="sxs-lookup"><span data-stu-id="149eb-136">Secret object</span></span>

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

### <span data-ttu-id="149eb-137">-Name</span><span class="sxs-lookup"><span data-stu-id="149eb-137">-Name</span></span>
<span data-ttu-id="149eb-138">Имя секретного человека, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="149eb-138">Specifies the name of a secret to modify.</span></span> <span data-ttu-id="149eb-139">Этот cmdlet конструирует полное доменное имя секретного домена на основе имени, указанного этим параметром, имени сейфа ключа и текущей среды.</span><span class="sxs-lookup"><span data-stu-id="149eb-139">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="149eb-140">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="149eb-140">-NotBefore</span></span>
<span data-ttu-id="149eb-141">Время в качестве объекта **даты и времени,** перед которым нельзя использовать секрет.</span><span class="sxs-lookup"><span data-stu-id="149eb-141">Specifies the time, as a **DateTime** object, before which the secret cannot be used.</span></span> <span data-ttu-id="149eb-142">Этот параметр использует UTC.</span><span class="sxs-lookup"><span data-stu-id="149eb-142">This parameter uses UTC.</span></span> <span data-ttu-id="149eb-143">Чтобы получить объект **даты и времени,** используйте cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="149eb-143">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

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

### <span data-ttu-id="149eb-144">-SecretValue</span><span class="sxs-lookup"><span data-stu-id="149eb-144">-SecretValue</span></span>
<span data-ttu-id="149eb-145">Указывает значение секрета как объекта **SecureString.**</span><span class="sxs-lookup"><span data-stu-id="149eb-145">Specifies the value for the secret as a **SecureString** object.</span></span> <span data-ttu-id="149eb-146">Чтобы получить объект **SecureString,** воспользуйтесь **cmdlet ConvertTo-SecureString.**</span><span class="sxs-lookup"><span data-stu-id="149eb-146">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="149eb-147">Для получения дополнительных сведений введите `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="149eb-147">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="149eb-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="149eb-148">-Tag</span></span>
<span data-ttu-id="149eb-149">Пары "ключевое значение" в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="149eb-149">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="149eb-150">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="149eb-150">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="149eb-151">-VaultName</span><span class="sxs-lookup"><span data-stu-id="149eb-151">-VaultName</span></span>
<span data-ttu-id="149eb-152">Указывает имя ключного сейфа, к которому относится эта секретная часть.</span><span class="sxs-lookup"><span data-stu-id="149eb-152">Specifies the name of the key vault to which this secret belongs.</span></span> <span data-ttu-id="149eb-153">Этот cmdlet конструирует FQDN ключа хранилища на основе имени, указанного этим параметром, и текущей среды.</span><span class="sxs-lookup"><span data-stu-id="149eb-153">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="149eb-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="149eb-154">-Confirm</span></span>
<span data-ttu-id="149eb-155">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="149eb-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="149eb-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="149eb-156">-WhatIf</span></span>
<span data-ttu-id="149eb-157">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="149eb-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="149eb-158">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="149eb-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="149eb-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="149eb-159">CommonParameters</span></span>
<span data-ttu-id="149eb-160">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="149eb-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="149eb-161">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="149eb-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="149eb-162">INPUTS</span><span class="sxs-lookup"><span data-stu-id="149eb-162">INPUTS</span></span>

### <span data-ttu-id="149eb-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="149eb-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="149eb-164">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="149eb-164">OUTPUTS</span></span>

### <span data-ttu-id="149eb-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="149eb-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="149eb-166">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="149eb-166">NOTES</span></span>

## <span data-ttu-id="149eb-167">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="149eb-167">RELATED LINKS</span></span>

[<span data-ttu-id="149eb-168">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="149eb-168">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="149eb-169">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="149eb-169">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)
