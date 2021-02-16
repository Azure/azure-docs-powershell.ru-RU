---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: d2c153cf0ae2f5cffbf47656d3ae64a531cb780b
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413801"
---
# <span data-ttu-id="8397c-101">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8397c-101">Add-AzKeyVaultKey</span></span>

## <span data-ttu-id="8397c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8397c-102">SYNOPSIS</span></span>
<span data-ttu-id="8397c-103">Создает ключ в хранилище ключей или импортирует его в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="8397c-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

## <span data-ttu-id="8397c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8397c-104">SYNTAX</span></span>

### <span data-ttu-id="8397c-105">InteractiveCreate (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8397c-105">InteractiveCreate (Default)</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8397c-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="8397c-106">InteractiveImport</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8397c-107">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="8397c-107">InputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8397c-108">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="8397c-108">InputObjectImport</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8397c-109">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="8397c-109">ResourceIdCreate</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8397c-110">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="8397c-110">ResourceIdImport</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8397c-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8397c-111">DESCRIPTION</span></span>
<span data-ttu-id="8397c-112">С **его** использованием можно создать ключ в хранилище ключей Azure или импортировать его в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="8397c-112">The **Add-AzKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="8397c-113">Используйте этот cmdlet для добавления клавиш, используя один из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="8397c-113">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="8397c-114">Создайте ключ в модуле безопасности оборудования (HSM) в службе key Vault.</span><span class="sxs-lookup"><span data-stu-id="8397c-114">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="8397c-115">Создайте ключ в программном обеспечении в службе key Vault.</span><span class="sxs-lookup"><span data-stu-id="8397c-115">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="8397c-116">Импортировать ключ из собственного модуля безопасности оборудования (HSM) в HSMs в службе key Vault.</span><span class="sxs-lookup"><span data-stu-id="8397c-116">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="8397c-117">Импортировать ключ из PFX-файла на компьютере.</span><span class="sxs-lookup"><span data-stu-id="8397c-117">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="8397c-118">Импортировать ключ из PFX-файла на компьютере в аппаратные модули безопасности (HSMs) в службе key Vault.</span><span class="sxs-lookup"><span data-stu-id="8397c-118">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>
<span data-ttu-id="8397c-119">Для любой из этих операций можно уписать ключевые атрибуты или принять параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8397c-119">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="8397c-120">При создании или импорте ключа, который имеет то же имя, что и у существующего ключа в хранилище ключей, исходный ключ обновляется с помощью значений, которые вы указываете для нового ключа.</span><span class="sxs-lookup"><span data-stu-id="8397c-120">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="8397c-121">Для доступа к предыдущим значениям можно использовать URI для конкретной версии ключа.</span><span class="sxs-lookup"><span data-stu-id="8397c-121">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="8397c-122">Чтобы узнать о ключевых версиях и [](http://go.microsoft.com/fwlink/?linkid=518560) структуре URI, см. документацию по ключевому сейфу REST API "Ключи и секрет".</span><span class="sxs-lookup"><span data-stu-id="8397c-122">To learn about key versions and the URI structure, see [About Keys and Secrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>
<span data-ttu-id="8397c-123">Примечание. Чтобы импортировать ключ из собственного модуля безопасности оборудования, необходимо сначала создать пакет BYOK (файл с расширением byok file name) с помощью инструмента "Хранилище ключей Azure BYOK".</span><span class="sxs-lookup"><span data-stu-id="8397c-123">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="8397c-124">Дополнительные сведения см. в сведениях о том, как создавать и [HSM-Protected ключей для хранилища ключей Azure.](http://go.microsoft.com/fwlink/?LinkId=522252)</span><span class="sxs-lookup"><span data-stu-id="8397c-124">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>
<span data-ttu-id="8397c-125">Лучше всего создать или обновить ключ с помощью Backup-AzKeyVaultKey управления.</span><span class="sxs-lookup"><span data-stu-id="8397c-125">As a best practice, back up your key after it is created or updated, by using the Backup-AzKeyVaultKey cmdlet.</span></span> <span data-ttu-id="8397c-126">Функции отменить невозможно, поэтому если вы случайно удалили или удалили ключ, а затем передумали, его невозможно восстановить, если у вас нет резервной копии, которую вы сможете восстановить.</span><span class="sxs-lookup"><span data-stu-id="8397c-126">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="8397c-127">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8397c-127">EXAMPLES</span></span>

### <span data-ttu-id="8397c-128">Пример 1. Создание ключа</span><span class="sxs-lookup"><span data-stu-id="8397c-128">Example 1: Create a key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITSoftware' -Destination 'Software'

Vault Name     : contoso
Name           : ITSoftware
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="8397c-129">Эта команда создает защищенный программным обеспечением ключ ITSoftware в хранилище с именем Contoso.</span><span class="sxs-lookup"><span data-stu-id="8397c-129">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="8397c-130">Пример 2. Создание защищенного HSM ключа</span><span class="sxs-lookup"><span data-stu-id="8397c-130">Example 2: Create an HSM-protected key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsm' -Destination 'HSM'

Vault Name     : contoso
Name           : ITHsm
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="8397c-131">Эта команда создает ключ, защищенный HSM, в хранилище с именем Contoso.</span><span class="sxs-lookup"><span data-stu-id="8397c-131">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="8397c-132">Пример 3. Создание ключа со значениями, которые не являются значениями по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8397c-132">Example 3: Create a key with non-default values</span></span>
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

Vault Name     : contoso
Name           : ITHsmNonDefault
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITHsmNonDefault/929bfc14db84439b823ffd1bedadaf5f
Enabled        : False
Expires        : 5/21/2020 11:12:43 PM
Not Before     : 5/21/2018 11:12:50 PM
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="8397c-133">Первая команда сохраняет значения в переменной "$KeyOperations".</span><span class="sxs-lookup"><span data-stu-id="8397c-133">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="8397c-134">Вторая команда создает объект **даты** и времени, определенный в UTC, с помощью командлета **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="8397c-134">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="8397c-135">Этот объект определяет время на два года в будущем.</span><span class="sxs-lookup"><span data-stu-id="8397c-135">That object specifies a time two years in the future.</span></span> <span data-ttu-id="8397c-136">Эта команда сохраняет эту дату в переменной $Expires.</span><span class="sxs-lookup"><span data-stu-id="8397c-136">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="8397c-137">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="8397c-137">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="8397c-138">Третья команда создает объект **даты и времени** с помощью командлета **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="8397c-138">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="8397c-139">Этот объект указывает текущее время в UTC.</span><span class="sxs-lookup"><span data-stu-id="8397c-139">That object specifies current UTC time.</span></span> <span data-ttu-id="8397c-140">Эта команда сохраняет эту дату в переменной $NotBefore.</span><span class="sxs-lookup"><span data-stu-id="8397c-140">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="8397c-141">Конечная команда создает ключ с именем ITHsmNonDefault, защищенный HSM.</span><span class="sxs-lookup"><span data-stu-id="8397c-141">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="8397c-142">Команда определяет значения для разрешенных операций ключа, хранимых $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="8397c-142">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="8397c-143">Команда определяет время параметров *Expires* (Срок действия) и *NotBefore,* созданных в предыдущих командах, и тегов для высокой важности и ИТ-параметров.</span><span class="sxs-lookup"><span data-stu-id="8397c-143">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="8397c-144">Новый ключ отключен.</span><span class="sxs-lookup"><span data-stu-id="8397c-144">The new key is disabled.</span></span> <span data-ttu-id="8397c-145">Вы можете включить его с помощью **cmdlet Set-AzKeyVaultKey.**</span><span class="sxs-lookup"><span data-stu-id="8397c-145">You can enable it by using the **Set-AzKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="8397c-146">Пример 4. Импорт ключа, защищенного HSM</span><span class="sxs-lookup"><span data-stu-id="8397c-146">Example 4: Import an HSM-protected key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'

Vault Name     : contoso
Name           : ITByok
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITByok/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="8397c-147">Эта команда импортирует ключ "ITByok" из расположения, заданного *параметром KeyFilePath.*</span><span class="sxs-lookup"><span data-stu-id="8397c-147">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="8397c-148">Импортируемый ключ является ключом, защищенным HSM.</span><span class="sxs-lookup"><span data-stu-id="8397c-148">The imported key is an HSM-protected key.</span></span>
<span data-ttu-id="8397c-149">Чтобы импортировать ключ из собственного модуля безопасности оборудования, необходимо сначала создать пакет BYOK (файл с расширением имени файла BYOK) с помощью средства BYOK key Vault Azure.</span><span class="sxs-lookup"><span data-stu-id="8397c-149">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="8397c-150">Дополнительные сведения см. в сведениях о том, как создавать и [HSM-Protected ключей для хранилища ключей Azure.](http://go.microsoft.com/fwlink/?LinkId=522252)</span><span class="sxs-lookup"><span data-stu-id="8397c-150">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="8397c-151">Пример 5. Импорт ключа, защищенного программным обеспечением</span><span class="sxs-lookup"><span data-stu-id="8397c-151">Example 5: Import a software-protected key</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password

Vault Name     : contoso
Name           : ITPfx
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITPfx/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="8397c-152">Первая команда преобразует строку в безопасную строку с помощью командлета **ConvertTo-SecureString,** а затем сохраняет ее в $Password строке.</span><span class="sxs-lookup"><span data-stu-id="8397c-152">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="8397c-153">Для получения дополнительных сведений введите `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="8397c-153">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="8397c-154">Вторая команда создает пароль программного обеспечения в хранилище ключей Contoso.</span><span class="sxs-lookup"><span data-stu-id="8397c-154">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="8397c-155">Команда определяет расположение ключа и пароля, которые хранятся в $Password.</span><span class="sxs-lookup"><span data-stu-id="8397c-155">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="8397c-156">Пример 6. Импорт ключа и назначение атрибутов</span><span class="sxs-lookup"><span data-stu-id="8397c-156">Example 6: Import a key and assign attributes</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = "true" }
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags

Vault Name     : contoso
Name           : ITPfxToHSM
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITPfxToHSM/929bfc14db84439b823ffd1bedadaf5f
Enabled        : True
Expires        : 5/21/2020 11:12:43 PM
Not Before     :
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="8397c-157">Первая команда преобразует строку в безопасную строку с помощью командлета **ConvertTo-SecureString,** а затем сохраняет ее в $Password строке.</span><span class="sxs-lookup"><span data-stu-id="8397c-157">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>
<span data-ttu-id="8397c-158">Вторая команда создает объект **даты** и времени с помощью командлета **Get-Date,** а затем сохраняет его в $Expires переменной.</span><span class="sxs-lookup"><span data-stu-id="8397c-158">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>
<span data-ttu-id="8397c-159">Третья команда создает переменную $tags, чтобы настроить теги для высокой важности и ИТ-информации.</span><span class="sxs-lookup"><span data-stu-id="8397c-159">The third command creates the $tags variable to set tags for high severity and IT.</span></span>
<span data-ttu-id="8397c-160">Конечная команда импортирует ключ как клавишу HSM из указанного расположения.</span><span class="sxs-lookup"><span data-stu-id="8397c-160">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="8397c-161">Команда определяет срок действия, которые хранятся $Expires пароль, которые хранятся в $Password, и применяет теги, хранимые в $tags.</span><span class="sxs-lookup"><span data-stu-id="8397c-161">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

### <span data-ttu-id="8397c-162">Пример 7. Создание ключа Exchange (KEK) для функции "создать собственный ключ" (BYOK)</span><span class="sxs-lookup"><span data-stu-id="8397c-162">Example 7: Generate a Key Exchange Key (KEK) for "bring your own key" (BYOK) feature</span></span>

```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName $vaultName -Name $keyName -Destination HSM -Size 2048 -KeyOps "import"
```

<span data-ttu-id="8397c-163">Создает ключ (ключ обмена ключом).</span><span class="sxs-lookup"><span data-stu-id="8397c-163">Generates a key (referred to as a Key Exchange Key (KEK)).</span></span> <span data-ttu-id="8397c-164">КЕК должен быть ключом RSA-HSM, который имеет только операцию импорта.</span><span class="sxs-lookup"><span data-stu-id="8397c-164">The KEK must be an RSA-HSM key that has only the import key operation.</span></span> <span data-ttu-id="8397c-165">Только ключ сейфа Premium SKU поддерживает ключи RSA-HSM.</span><span class="sxs-lookup"><span data-stu-id="8397c-165">Only Key Vault Premium SKU supports RSA-HSM keys.</span></span>
<span data-ttu-id="8397c-166">Дополнительные сведения https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="8397c-166">For more details please refer to https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="8397c-167">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8397c-167">PARAMETERS</span></span>

### <span data-ttu-id="8397c-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8397c-168">-DefaultProfile</span></span>
<span data-ttu-id="8397c-169">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8397c-169">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8397c-170">-Destination</span><span class="sxs-lookup"><span data-stu-id="8397c-170">-Destination</span></span>
<span data-ttu-id="8397c-171">Указывает, следует ли добавить ключ в качестве защищенного по программному обеспечению или защищенного HSM ключа в службе key Vault.</span><span class="sxs-lookup"><span data-stu-id="8397c-171">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="8397c-172">Допустимые значения: HSM и Программное обеспечение.</span><span class="sxs-lookup"><span data-stu-id="8397c-172">Valid values are: HSM and Software.</span></span>
<span data-ttu-id="8397c-173">Примечание. Чтобы использовать HSM в качестве назначения, у вас должен быть ключ сейф, который поддерживает HSMs.</span><span class="sxs-lookup"><span data-stu-id="8397c-173">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="8397c-174">Дополнительные сведения об уровнях обслуживания и возможностях хранилища ключей Azure см. на веб-сайте цены [на ключ хранилища Azure.](http://go.microsoft.com/fwlink/?linkid=512521)</span><span class="sxs-lookup"><span data-stu-id="8397c-174">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](http://go.microsoft.com/fwlink/?linkid=512521).</span></span>
<span data-ttu-id="8397c-175">Этот параметр требуется при создании нового ключа.</span><span class="sxs-lookup"><span data-stu-id="8397c-175">This parameter is required when you create a new key.</span></span> <span data-ttu-id="8397c-176">Если вы импортируете ключ с помощью *параметра KeyFilePath,* этот параметр является необязательным:</span><span class="sxs-lookup"><span data-stu-id="8397c-176">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>
- <span data-ttu-id="8397c-177">Если этот параметр не задан и этот cmdlet импортирует ключ с расширением byok, он будет импортироваться как ключ, защищенный HSM.</span><span class="sxs-lookup"><span data-stu-id="8397c-177">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="8397c-178">Этот ключ нельзя импортировать как защищенный программным обеспечением ключ.</span><span class="sxs-lookup"><span data-stu-id="8397c-178">The cmdlet cannot import that key as software-protected key.</span></span>
- <span data-ttu-id="8397c-179">Если этот параметр не указан, а этот cmdlet импортирует ключ с расширением имени файла PFX, ключ будет импортироваться как защищенный программным обеспечением ключ.</span><span class="sxs-lookup"><span data-stu-id="8397c-179">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8397c-180">-Disable</span><span class="sxs-lookup"><span data-stu-id="8397c-180">-Disable</span></span>
<span data-ttu-id="8397c-181">Указывает на то, что для добавляемого ключа за установлено начальное состояние отключения.</span><span class="sxs-lookup"><span data-stu-id="8397c-181">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="8397c-182">Любая попытка использовать ключ будет со сбой.</span><span class="sxs-lookup"><span data-stu-id="8397c-182">Any attempt to use the key will fail.</span></span> <span data-ttu-id="8397c-183">Используйте этот параметр, если вы предварительно добавили ключи, которые предполагается включить позже.</span><span class="sxs-lookup"><span data-stu-id="8397c-183">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="8397c-184">-Expires</span><span class="sxs-lookup"><span data-stu-id="8397c-184">-Expires</span></span>
<span data-ttu-id="8397c-185">Срок действия ключа, который добавляет этот **cmdlet,** определяет срок действия в качестве объекта даты и времени.</span><span class="sxs-lookup"><span data-stu-id="8397c-185">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="8397c-186">Этот параметр использует UTC.</span><span class="sxs-lookup"><span data-stu-id="8397c-186">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="8397c-187">Чтобы получить объект **даты и времени,** используйте cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="8397c-187">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="8397c-188">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="8397c-188">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="8397c-189">Если этот параметр не задан, срок действия ключа не истекает.</span><span class="sxs-lookup"><span data-stu-id="8397c-189">If you do not specify this parameter, the key does not expire.</span></span>

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

### <span data-ttu-id="8397c-190">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8397c-190">-InputObject</span></span>
<span data-ttu-id="8397c-191">Объект Vault.</span><span class="sxs-lookup"><span data-stu-id="8397c-191">Vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8397c-192">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="8397c-192">-KeyFilePassword</span></span>
<span data-ttu-id="8397c-193">Пароль импортируемого файла в качестве объекта **SecureString.**</span><span class="sxs-lookup"><span data-stu-id="8397c-193">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="8397c-194">Чтобы получить объект **SecureString,** используйте **cmdlet ConvertTo-SecureString.**</span><span class="sxs-lookup"><span data-stu-id="8397c-194">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="8397c-195">Для получения дополнительных сведений введите `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="8397c-195">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="8397c-196">Этот пароль необходимо указать для импорта файла с расширением PFX.</span><span class="sxs-lookup"><span data-stu-id="8397c-196">You must specify this password to import a file with a .pfx file name extension.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8397c-197">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="8397c-197">-KeyFilePath</span></span>
<span data-ttu-id="8397c-198">Путь к локальному файлу, который содержит ключевые материалы, импортируемые этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8397c-198">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="8397c-199">Допустимые расширения имен файлов: BYOK и PFX.</span><span class="sxs-lookup"><span data-stu-id="8397c-199">The valid file name extensions are .byok and .pfx.</span></span>
- <span data-ttu-id="8397c-200">Если это BYOK-файл, он автоматически защищен HSMs после импорта, и этот элемент по умолчанию нельзя переопрестить.</span><span class="sxs-lookup"><span data-stu-id="8397c-200">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>
- <span data-ttu-id="8397c-201">Если это PFX-файл, ключ автоматически защищен программным обеспечением после импорта.</span><span class="sxs-lookup"><span data-stu-id="8397c-201">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="8397c-202">Чтобы переопререгировать этот параметр по умолчанию, задате для параметра *Destination* параметр HSM так, чтобы ключ защищен HSM.</span><span class="sxs-lookup"><span data-stu-id="8397c-202">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>
<span data-ttu-id="8397c-203">Если этот параметр указан, параметр *Destination* является необязательным.</span><span class="sxs-lookup"><span data-stu-id="8397c-203">When you specify this parameter, the *Destination* parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8397c-204">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="8397c-204">-KeyOps</span></span>
<span data-ttu-id="8397c-205">Определяет массив операций, которые можно выполнять с помощью ключа, который добавляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8397c-205">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="8397c-206">Если этот параметр не задан, можно выполнить все операции.</span><span class="sxs-lookup"><span data-stu-id="8397c-206">If you do not specify this parameter, all operations can be performed.</span></span>
<span data-ttu-id="8397c-207">Допустимыми значениями для этого параметра является список операций, разделенных запятыми, в соответствии со спецификацией [JSON Web Key (JWK):](http://go.microsoft.com/fwlink/?LinkID=613300)</span><span class="sxs-lookup"><span data-stu-id="8397c-207">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](http://go.microsoft.com/fwlink/?LinkID=613300):</span></span>
- <span data-ttu-id="8397c-208">шифровать</span><span class="sxs-lookup"><span data-stu-id="8397c-208">encrypt</span></span>
- <span data-ttu-id="8397c-209">расшифровать</span><span class="sxs-lookup"><span data-stu-id="8397c-209">decrypt</span></span>
- <span data-ttu-id="8397c-210">wrapKey</span><span class="sxs-lookup"><span data-stu-id="8397c-210">wrapKey</span></span>
- <span data-ttu-id="8397c-211">unw уберегатьKey</span><span class="sxs-lookup"><span data-stu-id="8397c-211">unwrapKey</span></span>
- <span data-ttu-id="8397c-212">подписать</span><span class="sxs-lookup"><span data-stu-id="8397c-212">sign</span></span>
- <span data-ttu-id="8397c-213">проверить</span><span class="sxs-lookup"><span data-stu-id="8397c-213">verify</span></span>
- <span data-ttu-id="8397c-214">импорт (только для KEK, см. пример 7)</span><span class="sxs-lookup"><span data-stu-id="8397c-214">import (for KEK only, see example 7)</span></span>

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

### <span data-ttu-id="8397c-215">-Name</span><span class="sxs-lookup"><span data-stu-id="8397c-215">-Name</span></span>
<span data-ttu-id="8397c-216">Указывает имя ключа, который нужно добавить в хранилище.</span><span class="sxs-lookup"><span data-stu-id="8397c-216">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="8397c-217">Этот cmdlet конструирует полное доменное имя (FQDN) ключа на основе имени, указанного этим параметром, имени хранилища ключа и текущей среды.</span><span class="sxs-lookup"><span data-stu-id="8397c-217">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="8397c-218">Имя должно быть строкой от 1 до 63 символов длины, которая содержит только 0–9, a-z, A-Z и - (символ тире).</span><span class="sxs-lookup"><span data-stu-id="8397c-218">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8397c-219">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="8397c-219">-NotBefore</span></span>
<span data-ttu-id="8397c-220">Время в качестве объекта **даты и времени,** перед которым нельзя использовать ключ.</span><span class="sxs-lookup"><span data-stu-id="8397c-220">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="8397c-221">Этот параметр использует UTC.</span><span class="sxs-lookup"><span data-stu-id="8397c-221">This parameter uses UTC.</span></span> <span data-ttu-id="8397c-222">Чтобы получить объект **даты и времени,** используйте cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="8397c-222">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="8397c-223">Если этот параметр не задан, его можно использовать сразу же.</span><span class="sxs-lookup"><span data-stu-id="8397c-223">If you do not specify this parameter, the key can be used immediately.</span></span>

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

### <span data-ttu-id="8397c-224">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8397c-224">-ResourceId</span></span>
<span data-ttu-id="8397c-225">ИД ресурса хранилища.</span><span class="sxs-lookup"><span data-stu-id="8397c-225">Vault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdCreate, ResourceIdImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8397c-226">-Size</span><span class="sxs-lookup"><span data-stu-id="8397c-226">-Size</span></span>
<span data-ttu-id="8397c-227">Размер ключа RSA в битах.</span><span class="sxs-lookup"><span data-stu-id="8397c-227">RSA key size, in bits.</span></span> <span data-ttu-id="8397c-228">Если не указано, служба предоставит безопасный стандартный стандарт.</span><span class="sxs-lookup"><span data-stu-id="8397c-228">If not specified, the service will provide a safe default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8397c-229">-Tag</span><span class="sxs-lookup"><span data-stu-id="8397c-229">-Tag</span></span>
<span data-ttu-id="8397c-230">Пары значений ключа в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="8397c-230">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="8397c-231">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="8397c-231">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8397c-232">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8397c-232">-VaultName</span></span>
<span data-ttu-id="8397c-233">Указывает имя хранилища ключей, к которому этот cmdlet добавляет ключ.</span><span class="sxs-lookup"><span data-stu-id="8397c-233">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="8397c-234">Этот cmdlet конструирует FQDN ключа хранилища на основе имени, указанного этим параметром, и текущей среды.</span><span class="sxs-lookup"><span data-stu-id="8397c-234">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InteractiveImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8397c-235">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8397c-235">-Confirm</span></span>
<span data-ttu-id="8397c-236">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8397c-236">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8397c-237">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8397c-237">-WhatIf</span></span>
<span data-ttu-id="8397c-238">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8397c-238">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8397c-239">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8397c-239">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8397c-240">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8397c-240">CommonParameters</span></span>
<span data-ttu-id="8397c-241">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8397c-241">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8397c-242">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8397c-242">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8397c-243">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8397c-243">INPUTS</span></span>

### <span data-ttu-id="8397c-244">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="8397c-244">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="8397c-245">System.String</span><span class="sxs-lookup"><span data-stu-id="8397c-245">System.String</span></span>

## <span data-ttu-id="8397c-246">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8397c-246">OUTPUTS</span></span>

### <span data-ttu-id="8397c-247">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8397c-247">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="8397c-248">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8397c-248">NOTES</span></span>

## <span data-ttu-id="8397c-249">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8397c-249">RELATED LINKS</span></span>

[<span data-ttu-id="8397c-250">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8397c-250">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="8397c-251">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8397c-251">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="8397c-252">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8397c-252">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

