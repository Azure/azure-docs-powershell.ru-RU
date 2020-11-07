---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultkey
schema: 2.0.0
ms.openlocfilehash: 7af5afeac742bf9d256ac16470af0169170eb1e9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913356"
---
# <span data-ttu-id="8cb3c-101">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8cb3c-101">Add-AzureKeyVaultKey</span></span>

## <span data-ttu-id="8cb3c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8cb3c-102">SYNOPSIS</span></span>
<span data-ttu-id="8cb3c-103">Создание ключа в хранилище ключей или импорт ключа в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cb3c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8cb3c-104">SYNTAX</span></span>

### <span data-ttu-id="8cb3c-105">Создать (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8cb3c-105">Create (Default)</span></span>
```
Add-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cb3c-106">Импортируем</span><span class="sxs-lookup"><span data-stu-id="8cb3c-106">Import</span></span>
```
Add-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cb3c-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8cb3c-107">DESCRIPTION</span></span>
<span data-ttu-id="8cb3c-108">Командлет **Add-AzureKeyVaultKey** создает ключ в хранилище ключей в хранилище ключей Azure или импортирует ключ в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-108">The **Add-AzureKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="8cb3c-109">Используйте этот командлет для добавления клавиш одним из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="8cb3c-109">Use this cmdlet to add keys by using any of the following methods:</span></span>

- <span data-ttu-id="8cb3c-110">Создание ключа в аппаратном модуле безопасности (HSM) в службе хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-110">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="8cb3c-111">Создание ключа в программном обеспечении в службе хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-111">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="8cb3c-112">Импортируйте ключ из собственного модуля безопасности оборудования (HSM) в HSMs в службе хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-112">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="8cb3c-113">Импорт ключа из PFX-файла на компьютере.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-113">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="8cb3c-114">Импорт ключа из PFX-файла на компьютере в модули безопасности оборудования (HSMs) в службе хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-114">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>

<span data-ttu-id="8cb3c-115">Для любой из этих операций можно задать ключевые атрибуты или оставить параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-115">For any of these operations, you can provide key attributes or accept default settings.</span></span>

<span data-ttu-id="8cb3c-116">Если вы создаете или импортируете ключ с тем же именем, что и у существующего ключа в вашем хранилище ключей, первоначальный ключ обновляется с учетом значений, которые вы указали для нового ключа.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-116">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="8cb3c-117">Вы можете получить доступ к предыдущим значениям, используя универсальный код ресурса (URI) для указанной версии ключа.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-117">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="8cb3c-118">Чтобы узнать о ключевых версиях и структуре URI, ознакомьтесь со статьей о ключах [andSecrets](https://go.microsoft.com/fwlink/?linkid=518560) в документации по API-интерфейсу для хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-118">To learn about key versions and the URI structure, see [About Keys andSecrets](https://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>

<span data-ttu-id="8cb3c-119">Примечание. чтобы импортировать ключ из собственного модуля безопасности оборудования, необходимо сначала создать пакет BYOK (файл с расширением BYOK Name) с помощью набора инструментов Azure Key Vault BYOK.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-119">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="8cb3c-120">Дополнительные сведения [можно найти в разделе Создание и перенос ключей HSM-Protected для Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="8cb3c-120">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

<span data-ttu-id="8cb3c-121">Рекомендуется создать резервную копию ключа после его создания или обновления с помощью командлета Backup-AzureKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-121">As a best practice, back up your key after it is created or updated, by using the Backup-AzureKeyVaultKey cmdlet.</span></span> <span data-ttu-id="8cb3c-122">Функция отмены удаления отсутствует, поэтому если вы случайно удалили ключ или удалите его, а затем передумали, ключ не подлежит восстановлению, только если у вас есть резервная копия, которую вы можете восстановить.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-122">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="8cb3c-123">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8cb3c-123">EXAMPLES</span></span>

### <span data-ttu-id="8cb3c-124">Пример 1: создание ключа</span><span class="sxs-lookup"><span data-stu-id="8cb3c-124">Example 1: Create a key</span></span>
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Destination 'Software'
```

<span data-ttu-id="8cb3c-125">Эта команда создает ключ с защитой программного обеспечения с именем ITSoftware в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-125">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="8cb3c-126">Пример 2: создание ключа, защищенного с помощью HSM</span><span class="sxs-lookup"><span data-stu-id="8cb3c-126">Example 2: Create an HSM-protected key</span></span>
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITHsm' -Destination 'HSM'
```

<span data-ttu-id="8cb3c-127">Эта команда создает ключ, защищенный HSM, в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-127">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="8cb3c-128">Пример 3: создание ключа с использованием значений, не заданных по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8cb3c-128">Example 3: Create a key with non-default values</span></span>
```
PS C:\>$KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags
```

<span data-ttu-id="8cb3c-129">Первая команда сохраняет значения для расшифровки и проверки в переменной $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-129">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>

<span data-ttu-id="8cb3c-130">Вторая команда создает объект **DateTime** , определенный в формате UTC, с помощью командлета **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="8cb3c-130">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="8cb3c-131">Этот объект указывает на время в будущем на два года.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-131">That object specifies a time two years in the future.</span></span> <span data-ttu-id="8cb3c-132">Команда сохраняет эту дату в переменной $Expires.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-132">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="8cb3c-133">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="8cb3c-133">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="8cb3c-134">Третья команда создает объект **DateTime** с помощью командлета **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="8cb3c-134">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="8cb3c-135">Этот объект указывает текущее время в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-135">That object specifies current UTC time.</span></span> <span data-ttu-id="8cb3c-136">Команда сохраняет эту дату в переменной $NotBefore.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-136">The command stores that date in the $NotBefore variable.</span></span>

<span data-ttu-id="8cb3c-137">Последняя команда создает ключ с именем ITHsmNonDefault, который является ключом, защищенным с помощью HSM.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-137">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="8cb3c-138">Команда задает значения разрешенных операций с ключами, сохраненными $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-138">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="8cb3c-139">В команде указаны значения времени для параметров *Expires* и *NotBefore* , созданных в предыдущих командах, а также теги для высокого уровня важности и.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-139">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="8cb3c-140">Новый ключ отключен.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-140">The new key is disabled.</span></span> <span data-ttu-id="8cb3c-141">Это можно сделать с помощью командлета **Set-AzureKeyVaultKey** .</span><span class="sxs-lookup"><span data-stu-id="8cb3c-141">You can enable it by using the **Set-AzureKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="8cb3c-142">Пример 4: импорт ключа, защищенного с помощью HSM</span><span class="sxs-lookup"><span data-stu-id="8cb3c-142">Example 4: Import an HSM-protected key</span></span>
```
PS C:\>Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'
```

<span data-ttu-id="8cb3c-143">Эта команда импортирует ключ с именем ITByok из расположения, указанного параметром *KeyFilePath* .</span><span class="sxs-lookup"><span data-stu-id="8cb3c-143">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="8cb3c-144">Импортированный ключ является ключом, защищенным с помощью HSM.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-144">The imported key is an HSM-protected key.</span></span>

<span data-ttu-id="8cb3c-145">Чтобы импортировать ключ из собственного модуля безопасности оборудования, необходимо сначала создать пакет BYOK (файл с расширением BYOK Name) с помощью набора инструментов Azure Key Vault BYOK.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-145">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="8cb3c-146">Дополнительные сведения [можно найти в разделе Создание и перенос ключей HSM-Protected для Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="8cb3c-146">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="8cb3c-147">Пример 5: импорт ключа, защищенного с помощью программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="8cb3c-147">Example 5: Import a software-protected key</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password
```

<span data-ttu-id="8cb3c-148">Первая команда преобразует строку в защищенную строку с помощью командлета **ConvertTo-SecureString** , а затем сохраняет эту строку в переменной $Password.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-148">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="8cb3c-149">Для получения дополнительных сведений введите `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="8cb3c-149">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="8cb3c-150">Вторая команда создает пароль программного обеспечения в хранилище ключей contoso.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-150">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="8cb3c-151">Команда задает расположение ключа и пароль, хранящийся в $Password.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-151">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="8cb3c-152">Пример 6: импорт ключа и назначение атрибутов</span><span class="sxs-lookup"><span data-stu-id="8cb3c-152">Example 6: Import a key and assign attributes</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = null }
PS C:\> Add-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags
```

<span data-ttu-id="8cb3c-153">Первая команда преобразует строку в защищенную строку с помощью командлета **ConvertTo-SecureString** , а затем сохраняет эту строку в переменной $Password.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-153">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>

<span data-ttu-id="8cb3c-154">Вторая команда создает объект **DateTime** с помощью командлета **Get-Date** , а затем сохраняет этот объект в переменной $Expires.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-154">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>

<span data-ttu-id="8cb3c-155">Третья команда создает переменную $tags, чтобы установить теги для высокого уровня важности и.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-155">The third command creates the $tags variable to set tags for high severity and IT.</span></span>

<span data-ttu-id="8cb3c-156">Последняя команда импортирует ключ в качестве ключа HSM из указанного места.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-156">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="8cb3c-157">Команда задает срок действия, хранящийся в $Expires и пароль, которые хранятся в $Password, и применяет теги, хранящиеся в $tags.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-157">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

## <span data-ttu-id="8cb3c-158">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8cb3c-158">PARAMETERS</span></span>

### <span data-ttu-id="8cb3c-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cb3c-159">-DefaultProfile</span></span>
<span data-ttu-id="8cb3c-160">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8cb3c-160">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8cb3c-161">-Destination</span><span class="sxs-lookup"><span data-stu-id="8cb3c-161">-Destination</span></span>
<span data-ttu-id="8cb3c-162">Указывает, следует ли добавить ключ в качестве ключа с защитой программного обеспечения или ключа, защищенного с помощью HSM, в службе хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-162">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="8cb3c-163">Допустимые значения: HSM и программное обеспечение.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-163">Valid values are: HSM and Software.</span></span>

<span data-ttu-id="8cb3c-164">Примечание. чтобы использовать HSM в качестве места назначения, необходимо иметь ключевое хранилище, которое поддерживает HSMs.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-164">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="8cb3c-165">Дополнительные сведения о уровнях обслуживания и возможностях Azure Key Vault можно найти на [веб-сайте ценообразования для Azure Key Vault](https://go.microsoft.com/fwlink/?linkid=512521).</span><span class="sxs-lookup"><span data-stu-id="8cb3c-165">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

<span data-ttu-id="8cb3c-166">Этот параметр является обязательным при создании нового ключа.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-166">This parameter is required when you create a new key.</span></span> <span data-ttu-id="8cb3c-167">При импорте ключа с помощью параметра *KeyFilePath* этот параметр является необязательным:</span><span class="sxs-lookup"><span data-stu-id="8cb3c-167">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>

- <span data-ttu-id="8cb3c-168">Если этот параметр не указан, а этот командлет импортирует ключ с расширением byok, он импортирует этот ключ в качестве ключа, защищенного с помощью HSM-файлов.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-168">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="8cb3c-169">Командлет не может импортировать эту клавишу в качестве ключа, защищенного с помощью программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-169">The cmdlet cannot import that key as software-protected key.</span></span>

- <span data-ttu-id="8cb3c-170">Если этот параметр не указан, а этот командлет импортирует ключ с расширением имени PFX-файла, он импортирует ключ как ключ, защищенный программным обеспечением.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-170">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

```yaml
Type: String
Parameter Sets: Create
Aliases: 
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Import
Aliases: 
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cb3c-171">-Отключение</span><span class="sxs-lookup"><span data-stu-id="8cb3c-171">-Disable</span></span>
<span data-ttu-id="8cb3c-172">Указывает на то, что для добавляемого ключа задано начальное состояние "отключено".</span><span class="sxs-lookup"><span data-stu-id="8cb3c-172">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="8cb3c-173">Любая попытка использования ключа завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-173">Any attempt to use the key will fail.</span></span> <span data-ttu-id="8cb3c-174">Используйте этот параметр, если нужно предварительно загрузить ключи, которые нужно включить в дальнейшем.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-174">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="8cb3c-175">-Истекает</span><span class="sxs-lookup"><span data-stu-id="8cb3c-175">-Expires</span></span>
<span data-ttu-id="8cb3c-176">Задает время истечения срока действия в виде объекта **DateTime** для ключа, который добавляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-176">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="8cb3c-177">Этот параметр использует координированное координированное время (UTC).</span><span class="sxs-lookup"><span data-stu-id="8cb3c-177">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="8cb3c-178">Чтобы получить объект **DateTime** , используйте командлет **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="8cb3c-178">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="8cb3c-179">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="8cb3c-179">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="8cb3c-180">Если этот параметр не указан, срок действия ключа не истекает.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-180">If you do not specify this parameter, the key does not expire.</span></span>

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

### <span data-ttu-id="8cb3c-181">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="8cb3c-181">-KeyFilePassword</span></span>
<span data-ttu-id="8cb3c-182">Указывает пароль для импортированного файла как объект **SecureString** .</span><span class="sxs-lookup"><span data-stu-id="8cb3c-182">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="8cb3c-183">Чтобы получить объект **SecureString** , используйте командлет **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="8cb3c-183">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="8cb3c-184">Для получения дополнительных сведений введите `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="8cb3c-184">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="8cb3c-185">Вы должны указать этот пароль, чтобы импортировать файл с расширением имени PFX-файла.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-185">You must specify this password to import a file with a .pfx file name extension.</span></span>

```yaml
Type: SecureString
Parameter Sets: Import
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cb3c-186">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="8cb3c-186">-KeyFilePath</span></span>
<span data-ttu-id="8cb3c-187">Указывает путь к локальному файлу, содержащему ключевой материал, который этот командлет импортирует.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-187">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="8cb3c-188">Допустимые расширения имен файлов: byok и PFX.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-188">The valid file name extensions are .byok and .pfx.</span></span>

- <span data-ttu-id="8cb3c-189">Если файл является файлом byok, ключ автоматически защищается HSMs после импорта, и вы не сможете переопределить этот параметр по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-189">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>

- <span data-ttu-id="8cb3c-190">Если файл является PFX-файлом, ключ автоматически защищается программным путем после импорта.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-190">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="8cb3c-191">Чтобы переопределить это значение по умолчанию, установите для параметра *Destination* значение HSM, чтобы ключ был защищен с помощью HSM-аппаратных защит.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-191">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>

<span data-ttu-id="8cb3c-192">Если указать этот параметр, параметр *Destination* является необязательным.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-192">When you specify this parameter, the *Destination* parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: Import
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cb3c-193">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="8cb3c-193">-KeyOps</span></span>
<span data-ttu-id="8cb3c-194">Задает массив операций, которые можно выполнить с помощью ключа, который добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-194">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="8cb3c-195">Если этот параметр не указан, может выполняться выполнение всех операций.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-195">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="8cb3c-196">Допустимые значения этого параметра — это разделенный запятыми список ключевых операций, заданных [спецификацией JSON Web Key (JWK)](https://go.microsoft.com/fwlink/?LinkID=613300):</span><span class="sxs-lookup"><span data-stu-id="8cb3c-196">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](https://go.microsoft.com/fwlink/?LinkID=613300):</span></span>

- <span data-ttu-id="8cb3c-197">EFS</span><span class="sxs-lookup"><span data-stu-id="8cb3c-197">Encrypt</span></span>
- <span data-ttu-id="8cb3c-198">Расшифровки</span><span class="sxs-lookup"><span data-stu-id="8cb3c-198">Decrypt</span></span>
- <span data-ttu-id="8cb3c-199">Инкапсулирует</span><span class="sxs-lookup"><span data-stu-id="8cb3c-199">Wrap</span></span>
- <span data-ttu-id="8cb3c-200">Разтекание</span><span class="sxs-lookup"><span data-stu-id="8cb3c-200">Unwrap</span></span>
- <span data-ttu-id="8cb3c-201">Рядом</span><span class="sxs-lookup"><span data-stu-id="8cb3c-201">Sign</span></span>
- <span data-ttu-id="8cb3c-202">Подтвержда</span><span class="sxs-lookup"><span data-stu-id="8cb3c-202">Verify</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cb3c-203">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8cb3c-203">-Name</span></span>
<span data-ttu-id="8cb3c-204">Задает имя ключа, который нужно добавить в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-204">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="8cb3c-205">Этот командлет создает полное доменное имя (FQDN) ключа на основе имени, которое указывает этот параметр, имя хранилища ключей и текущую среду.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-205">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="8cb3c-206">Имя должно быть строкой из 1 – 63 знаков длиной, содержащей только 0-9, a-z, A-Z и (дефис).</span><span class="sxs-lookup"><span data-stu-id="8cb3c-206">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cb3c-207">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="8cb3c-207">-NotBefore</span></span>
<span data-ttu-id="8cb3c-208">Указывает время в виде объекта **DateTime** , до которого невозможно использовать клавишу.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-208">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="8cb3c-209">Этот параметр использует время в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-209">This parameter uses UTC.</span></span> <span data-ttu-id="8cb3c-210">Чтобы получить объект **DateTime** , используйте командлет **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="8cb3c-210">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="8cb3c-211">Если этот параметр не указан, клавишу можно использовать сразу.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-211">If you do not specify this parameter, the key can be used immediately.</span></span>

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

### <span data-ttu-id="8cb3c-212">-Тег</span><span class="sxs-lookup"><span data-stu-id="8cb3c-212">-Tag</span></span>
<span data-ttu-id="8cb3c-213">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-213">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8cb3c-214">Например:</span><span class="sxs-lookup"><span data-stu-id="8cb3c-214">For example:</span></span>

<span data-ttu-id="8cb3c-215">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="8cb3c-215">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8cb3c-216">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8cb3c-216">-VaultName</span></span>
<span data-ttu-id="8cb3c-217">Указывает имя хранилища ключей, к которому этот командлет добавляет ключ.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-217">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="8cb3c-218">Этот командлет создает полное доменное имя хранилища ключей, основываясь на имени, указанном этим параметром, и текущей среде.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-218">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="8cb3c-219">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8cb3c-219">-Confirm</span></span>
<span data-ttu-id="8cb3c-220">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-220">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cb3c-221">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cb3c-221">-WhatIf</span></span>
<span data-ttu-id="8cb3c-222">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-222">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cb3c-223">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-223">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cb3c-224">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cb3c-224">CommonParameters</span></span>
<span data-ttu-id="8cb3c-225">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8cb3c-225">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cb3c-226">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cb3c-226">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cb3c-227">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8cb3c-227">INPUTS</span></span>

## <span data-ttu-id="8cb3c-228">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8cb3c-228">OUTPUTS</span></span>

### <span data-ttu-id="8cb3c-229">Microsoft. Azure. Commands. KeyVault. Models. KeyBundle</span><span class="sxs-lookup"><span data-stu-id="8cb3c-229">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="8cb3c-230">Пуск</span><span class="sxs-lookup"><span data-stu-id="8cb3c-230">NOTES</span></span>

## <span data-ttu-id="8cb3c-231">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8cb3c-231">RELATED LINKS</span></span>

[<span data-ttu-id="8cb3c-232">Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8cb3c-232">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="8cb3c-233">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8cb3c-233">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="8cb3c-234">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8cb3c-234">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="8cb3c-235">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="8cb3c-235">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)
