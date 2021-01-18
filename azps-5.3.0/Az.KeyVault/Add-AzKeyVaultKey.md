---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: 6cea7f2584de3a27be2cee36c3f32fd792564160
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518386"
---
# <span data-ttu-id="f5dee-101">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f5dee-101">Add-AzKeyVaultKey</span></span>

## <span data-ttu-id="f5dee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5dee-102">SYNOPSIS</span></span>
<span data-ttu-id="f5dee-103">Создает ключ в хранилище ключей или импортирует его в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="f5dee-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

## <span data-ttu-id="f5dee-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f5dee-104">SYNTAX</span></span>

### <span data-ttu-id="f5dee-105">InteractiveCreate (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f5dee-105">InteractiveCreate (Default)</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5dee-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="f5dee-106">InteractiveImport</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5dee-107">HsmInteractiveCreate</span><span class="sxs-lookup"><span data-stu-id="f5dee-107">HsmInteractiveCreate</span></span>
```
Add-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String> [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5dee-108">HsmInteractiveImport</span><span class="sxs-lookup"><span data-stu-id="f5dee-108">HsmInteractiveImport</span></span>
```
Add-AzKeyVaultKey -HsmName <String> [-Name] <String> -KeyFilePath <String> [-KeyFilePassword <SecureString>]
 [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5dee-109">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="f5dee-109">InputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5dee-110">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="f5dee-110">InputObjectImport</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5dee-111">HsmInputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="f5dee-111">HsmInputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String>
 [-CurveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5dee-112">HsmInputObjectImport</span><span class="sxs-lookup"><span data-stu-id="f5dee-112">HsmInputObjectImport</span></span>
```
Add-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f5dee-113">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="f5dee-113">ResourceIdCreate</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5dee-114">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="f5dee-114">ResourceIdImport</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5dee-115">HsmResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="f5dee-115">HsmResourceIdCreate</span></span>
```
Add-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String>
 [-CurveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5dee-116">HsmResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="f5dee-116">HsmResourceIdImport</span></span>
```
Add-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5dee-117">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f5dee-117">DESCRIPTION</span></span>
<span data-ttu-id="f5dee-118">С **его** использованием можно создать ключ в хранилище ключей Azure или импортировать его в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="f5dee-118">The **Add-AzKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="f5dee-119">Используйте этот cmdlet для добавления клавиш, используя один из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="f5dee-119">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="f5dee-120">Создайте ключ в модуле безопасности оборудования (HSM) в службе key Vault.</span><span class="sxs-lookup"><span data-stu-id="f5dee-120">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="f5dee-121">Создайте ключ в программном обеспечении в службе key Vault.</span><span class="sxs-lookup"><span data-stu-id="f5dee-121">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="f5dee-122">Импорт ключа из собственного модуля безопасности оборудования (HSM) в HSMs в службе key Vault.</span><span class="sxs-lookup"><span data-stu-id="f5dee-122">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="f5dee-123">Импортировать ключ из PFX-файла на компьютере.</span><span class="sxs-lookup"><span data-stu-id="f5dee-123">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="f5dee-124">Импортировать ключ из PFX-файла на компьютере в аппаратные модули безопасности (HSMs) в службе key Vault.</span><span class="sxs-lookup"><span data-stu-id="f5dee-124">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>
<span data-ttu-id="f5dee-125">Для любой из этих операций можно уписать ключевые атрибуты или принять параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f5dee-125">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="f5dee-126">При создании или импорте ключа с тем же именем, что и у существующего ключа в хранилище ключей, исходный ключ обновляется с помощью значений, которые вы указываете для нового ключа.</span><span class="sxs-lookup"><span data-stu-id="f5dee-126">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="f5dee-127">Вы можете получить доступ к предыдущим значениям, используя URI для конкретной версии ключа.</span><span class="sxs-lookup"><span data-stu-id="f5dee-127">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="f5dee-128">Чтобы узнать о ключевых версиях и [](http://go.microsoft.com/fwlink/?linkid=518560) структуре URI, см. информацию о ключах и секретах в документации KEY Vault REST API.</span><span class="sxs-lookup"><span data-stu-id="f5dee-128">To learn about key versions and the URI structure, see [About Keys and Secrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>
<span data-ttu-id="f5dee-129">Примечание. Чтобы импортировать ключ из собственного модуля безопасности оборудования, необходимо сначала создать пакет BYOK (файл с расширением "BYOK"), используя инструменты BYOK key Vault Azure.</span><span class="sxs-lookup"><span data-stu-id="f5dee-129">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="f5dee-130">Дополнительные сведения см. в сведениях о том, как создавать и [HSM-Protected клавиш для хранилища ключей Azure.](http://go.microsoft.com/fwlink/?LinkId=522252)</span><span class="sxs-lookup"><span data-stu-id="f5dee-130">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>
<span data-ttu-id="f5dee-131">Лучше всего создать или обновить ключ с помощью Backup-AzKeyVaultKey управления.</span><span class="sxs-lookup"><span data-stu-id="f5dee-131">As a best practice, back up your key after it is created or updated, by using the Backup-AzKeyVaultKey cmdlet.</span></span> <span data-ttu-id="f5dee-132">Функции отменить невозможно, поэтому если вы случайно удалили или удалили ключ, а затем передумали, его невозможно восстановить, если у вас нет резервной копии, которую вы сможете восстановить.</span><span class="sxs-lookup"><span data-stu-id="f5dee-132">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="f5dee-133">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f5dee-133">EXAMPLES</span></span>

### <span data-ttu-id="f5dee-134">Пример 1. Создание ключа</span><span class="sxs-lookup"><span data-stu-id="f5dee-134">Example 1: Create a key</span></span>
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

<span data-ttu-id="f5dee-135">Эта команда создает защищенный программным обеспечением ключ ITSoftware в хранилище с именем Contoso.</span><span class="sxs-lookup"><span data-stu-id="f5dee-135">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="f5dee-136">Пример 2. Создание защищенного HSM ключа</span><span class="sxs-lookup"><span data-stu-id="f5dee-136">Example 2: Create an HSM-protected key</span></span>
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

<span data-ttu-id="f5dee-137">Эта команда создает ключ, защищенный HSM, в хранилище с именем Contoso.</span><span class="sxs-lookup"><span data-stu-id="f5dee-137">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="f5dee-138">Пример 3. Создание ключа со значениями, которые не являются значениями по умолчанию</span><span class="sxs-lookup"><span data-stu-id="f5dee-138">Example 3: Create a key with non-default values</span></span>
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

<span data-ttu-id="f5dee-139">Первая команда сохраняет значения в переменной "$KeyOperations".</span><span class="sxs-lookup"><span data-stu-id="f5dee-139">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="f5dee-140">Вторая команда создает объект **даты** и времени, определенный в UTC, с помощью командлета **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="f5dee-140">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="f5dee-141">Этот объект определяет время на два года в будущем.</span><span class="sxs-lookup"><span data-stu-id="f5dee-141">That object specifies a time two years in the future.</span></span> <span data-ttu-id="f5dee-142">Эта команда сохраняет эту дату в переменной $Expires.</span><span class="sxs-lookup"><span data-stu-id="f5dee-142">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="f5dee-143">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="f5dee-143">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="f5dee-144">Третья команда создает объект **даты и времени** с помощью командлета **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="f5dee-144">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="f5dee-145">Этот объект указывает текущее время в UTC.</span><span class="sxs-lookup"><span data-stu-id="f5dee-145">That object specifies current UTC time.</span></span> <span data-ttu-id="f5dee-146">Эта команда сохраняет эту дату в переменной $NotBefore.</span><span class="sxs-lookup"><span data-stu-id="f5dee-146">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="f5dee-147">Конечная команда создает ключ с именем ITHsmNonDefault, защищенный HSM.</span><span class="sxs-lookup"><span data-stu-id="f5dee-147">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="f5dee-148">Команда определяет значения для разрешенных операций ключа, хранимых $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="f5dee-148">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="f5dee-149">Команда определяет время параметров *Expires* (Срок действия) и *NotBefore,* созданных в предыдущих командах, и тегов для высокой важности и ИТ-параметров.</span><span class="sxs-lookup"><span data-stu-id="f5dee-149">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="f5dee-150">Новый ключ отключен.</span><span class="sxs-lookup"><span data-stu-id="f5dee-150">The new key is disabled.</span></span> <span data-ttu-id="f5dee-151">Вы можете включить его с помощью **cmdlet Set-AzKeyVaultKey.**</span><span class="sxs-lookup"><span data-stu-id="f5dee-151">You can enable it by using the **Set-AzKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="f5dee-152">Пример 4. Импорт ключа, защищенного HSM</span><span class="sxs-lookup"><span data-stu-id="f5dee-152">Example 4: Import an HSM-protected key</span></span>
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

<span data-ttu-id="f5dee-153">Эта команда импортирует ключ "ITByok" из расположения, заданного *параметром KeyFilePath.*</span><span class="sxs-lookup"><span data-stu-id="f5dee-153">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="f5dee-154">Импортируемый ключ является ключом, защищенным HSM.</span><span class="sxs-lookup"><span data-stu-id="f5dee-154">The imported key is an HSM-protected key.</span></span>
<span data-ttu-id="f5dee-155">Чтобы импортировать ключ из собственного модуля безопасности оборудования, необходимо сначала создать пакет BYOK (файл с расширением имени файла BYOK) с помощью средства BYOK key Vault Azure.</span><span class="sxs-lookup"><span data-stu-id="f5dee-155">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="f5dee-156">Дополнительные сведения см. в сведениях о том, как создавать и [HSM-Protected ключей для хранилища ключей Azure.](http://go.microsoft.com/fwlink/?LinkId=522252)</span><span class="sxs-lookup"><span data-stu-id="f5dee-156">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="f5dee-157">Пример 5. Импорт ключа, защищенного программным обеспечением</span><span class="sxs-lookup"><span data-stu-id="f5dee-157">Example 5: Import a software-protected key</span></span>
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

<span data-ttu-id="f5dee-158">Первая команда преобразует строку в безопасную строку с помощью командлета **ConvertTo-SecureString,** а затем сохраняет ее в $Password переменной.</span><span class="sxs-lookup"><span data-stu-id="f5dee-158">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="f5dee-159">Для получения дополнительных сведений введите `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="f5dee-159">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="f5dee-160">Вторая команда создает пароль программного обеспечения в хранилище ключей Contoso.</span><span class="sxs-lookup"><span data-stu-id="f5dee-160">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="f5dee-161">Команда определяет расположение ключа и пароля, которые хранятся в $Password.</span><span class="sxs-lookup"><span data-stu-id="f5dee-161">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="f5dee-162">Пример 6. Импорт ключа и назначение атрибутов</span><span class="sxs-lookup"><span data-stu-id="f5dee-162">Example 6: Import a key and assign attributes</span></span>
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

<span data-ttu-id="f5dee-163">Первая команда преобразует строку в безопасную строку с помощью командлета **ConvertTo-SecureString,** а затем сохраняет ее в $Password переменной.</span><span class="sxs-lookup"><span data-stu-id="f5dee-163">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>
<span data-ttu-id="f5dee-164">Вторая команда создает объект **даты** и времени с помощью командлета **Get-Date,** а затем сохраняет его в $Expires переменной.</span><span class="sxs-lookup"><span data-stu-id="f5dee-164">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>
<span data-ttu-id="f5dee-165">Третья команда создает переменную $tags для заметок высокой важности и ИТ-информации.</span><span class="sxs-lookup"><span data-stu-id="f5dee-165">The third command creates the $tags variable to set tags for high severity and IT.</span></span>
<span data-ttu-id="f5dee-166">Конечная команда импортирует ключ как клавишу HSM из указанного расположения.</span><span class="sxs-lookup"><span data-stu-id="f5dee-166">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="f5dee-167">Команда определяет срок действия, которые хранятся $Expires пароль, которые хранятся в $Password, и применяет теги, хранимые в $tags.</span><span class="sxs-lookup"><span data-stu-id="f5dee-167">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

### <span data-ttu-id="f5dee-168">Пример 7. Создание ключа Exchange (KEK) для функции "создать собственный ключ" (BYOK)</span><span class="sxs-lookup"><span data-stu-id="f5dee-168">Example 7: Generate a Key Exchange Key (KEK) for "bring your own key" (BYOK) feature</span></span>

```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName $vaultName -Name $keyName -Destination HSM -Size 2048 -KeyOps "import"
```

<span data-ttu-id="f5dee-169">Создает ключ (ключ, который называется ключом Exchange)</span><span class="sxs-lookup"><span data-stu-id="f5dee-169">Generates a key (referred to as a Key Exchange Key (KEK)).</span></span> <span data-ttu-id="f5dee-170">КЕК должен быть ключом RSA-HSM, который имеет только операцию импорта.</span><span class="sxs-lookup"><span data-stu-id="f5dee-170">The KEK must be an RSA-HSM key that has only the import key operation.</span></span> <span data-ttu-id="f5dee-171">Только key Vault Premium SKU поддерживает клавиши RSA-HSM.</span><span class="sxs-lookup"><span data-stu-id="f5dee-171">Only Key Vault Premium SKU supports RSA-HSM keys.</span></span>
<span data-ttu-id="f5dee-172">Дополнительные сведения https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="f5dee-172">For more details please refer to https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="f5dee-173">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5dee-173">PARAMETERS</span></span>

### <span data-ttu-id="f5dee-174">-CurveName</span><span class="sxs-lookup"><span data-stu-id="f5dee-174">-CurveName</span></span>
<span data-ttu-id="f5dee-175">Определяет имя кривой шифрования с многотипной кривой. Это значение допустимо, если KeyType — EC.</span><span class="sxs-lookup"><span data-stu-id="f5dee-175">Specifies the curve name of elliptic curve cryptography, this value is valid when KeyType is EC.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmInteractiveCreate, HsmInputObjectCreate, HsmResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5dee-176">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5dee-176">-DefaultProfile</span></span>
<span data-ttu-id="f5dee-177">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f5dee-177">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5dee-178">-Destination</span><span class="sxs-lookup"><span data-stu-id="f5dee-178">-Destination</span></span>
<span data-ttu-id="f5dee-179">Указывает, следует ли добавить ключ в качестве защищенного по программному обеспечению или защищенного HSM ключа в службе key Vault.</span><span class="sxs-lookup"><span data-stu-id="f5dee-179">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="f5dee-180">Допустимые значения: HSM и Программное обеспечение.</span><span class="sxs-lookup"><span data-stu-id="f5dee-180">Valid values are: HSM and Software.</span></span>
<span data-ttu-id="f5dee-181">Примечание. Чтобы использовать HSM в качестве назначения, необходимо иметь ключ сейф, который поддерживает HSMs.</span><span class="sxs-lookup"><span data-stu-id="f5dee-181">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="f5dee-182">Дополнительные сведения об уровнях обслуживания и возможностях хранилища ключей Azure см. на веб-сайте цены [на ключ хранилища Azure.](http://go.microsoft.com/fwlink/?linkid=512521)</span><span class="sxs-lookup"><span data-stu-id="f5dee-182">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](http://go.microsoft.com/fwlink/?linkid=512521).</span></span>
<span data-ttu-id="f5dee-183">Этот параметр требуется при создании нового ключа.</span><span class="sxs-lookup"><span data-stu-id="f5dee-183">This parameter is required when you create a new key.</span></span> <span data-ttu-id="f5dee-184">Если вы импортируете ключ с помощью *параметра KeyFilePath,* этот параметр является необязательным:</span><span class="sxs-lookup"><span data-stu-id="f5dee-184">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>
- <span data-ttu-id="f5dee-185">Если этот параметр не задан и этот cmdlet импортирует ключ с расширением byok, он будет импортироваться как ключ, защищенный HSM.</span><span class="sxs-lookup"><span data-stu-id="f5dee-185">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="f5dee-186">Этот ключ нельзя импортировать как защищенный программным обеспечением ключ.</span><span class="sxs-lookup"><span data-stu-id="f5dee-186">The cmdlet cannot import that key as software-protected key.</span></span>
- <span data-ttu-id="f5dee-187">Если этот параметр не указан, а этот cmdlet импортирует ключ с расширением имени файла PFX, ключ будет импортироваться как защищенный программным обеспечением ключ.</span><span class="sxs-lookup"><span data-stu-id="f5dee-187">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

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

### <span data-ttu-id="f5dee-188">-Disable</span><span class="sxs-lookup"><span data-stu-id="f5dee-188">-Disable</span></span>
<span data-ttu-id="f5dee-189">Указывает на то, что для добавляемого ключа за установлено начальное состояние отключения.</span><span class="sxs-lookup"><span data-stu-id="f5dee-189">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="f5dee-190">Любая попытка использовать ключ будет неудачной.</span><span class="sxs-lookup"><span data-stu-id="f5dee-190">Any attempt to use the key will fail.</span></span> <span data-ttu-id="f5dee-191">Используйте этот параметр, если вы предварительно добавили ключи, которые предполагается включить позже.</span><span class="sxs-lookup"><span data-stu-id="f5dee-191">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="f5dee-192">-Expires</span><span class="sxs-lookup"><span data-stu-id="f5dee-192">-Expires</span></span>
<span data-ttu-id="f5dee-193">Срок действия ключа, который добавляет этот **cmdlet,** определяет срок действия в качестве объекта даты и времени.</span><span class="sxs-lookup"><span data-stu-id="f5dee-193">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="f5dee-194">Этот параметр использует UTC.</span><span class="sxs-lookup"><span data-stu-id="f5dee-194">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="f5dee-195">Чтобы получить объект **даты и времени,** используйте cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="f5dee-195">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="f5dee-196">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="f5dee-196">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="f5dee-197">Если этот параметр не задан, срок действия ключа не истекает.</span><span class="sxs-lookup"><span data-stu-id="f5dee-197">If you do not specify this parameter, the key does not expire.</span></span>

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

### <span data-ttu-id="f5dee-198">-HsmName</span><span class="sxs-lookup"><span data-stu-id="f5dee-198">-HsmName</span></span>
<span data-ttu-id="f5dee-199">Имя HSM.</span><span class="sxs-lookup"><span data-stu-id="f5dee-199">HSM name.</span></span> <span data-ttu-id="f5dee-200">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span><span class="sxs-lookup"><span data-stu-id="f5dee-200">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmInteractiveCreate, HsmInteractiveImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5dee-201">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="f5dee-201">-HsmObject</span></span>
<span data-ttu-id="f5dee-202">Объект HSM.</span><span class="sxs-lookup"><span data-stu-id="f5dee-202">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: HsmInputObjectCreate, HsmInputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5dee-203">-HsmResourceId</span><span class="sxs-lookup"><span data-stu-id="f5dee-203">-HsmResourceId</span></span>
<span data-ttu-id="f5dee-204">ИД ресурса HSM.</span><span class="sxs-lookup"><span data-stu-id="f5dee-204">Resource ID of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmResourceIdCreate, HsmResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5dee-205">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5dee-205">-InputObject</span></span>
<span data-ttu-id="f5dee-206">Объект Vault.</span><span class="sxs-lookup"><span data-stu-id="f5dee-206">Vault object.</span></span>

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

### <span data-ttu-id="f5dee-207">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="f5dee-207">-KeyFilePassword</span></span>
<span data-ttu-id="f5dee-208">Пароль импортируемого файла в качестве объекта **SecureString.**</span><span class="sxs-lookup"><span data-stu-id="f5dee-208">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="f5dee-209">Чтобы получить объект **SecureString,** воспользуйтесь **cmdlet ConvertTo-SecureString.**</span><span class="sxs-lookup"><span data-stu-id="f5dee-209">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="f5dee-210">Для получения дополнительных сведений введите `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="f5dee-210">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="f5dee-211">Этот пароль необходимо указать для импорта файла с расширением PFX.</span><span class="sxs-lookup"><span data-stu-id="f5dee-211">You must specify this password to import a file with a .pfx file name extension.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, HsmInteractiveImport, InputObjectImport, HsmInputObjectImport, ResourceIdImport, HsmResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5dee-212">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="f5dee-212">-KeyFilePath</span></span>
<span data-ttu-id="f5dee-213">Путь к локальному файлу, который содержит ключевые материалы, импортируемые этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5dee-213">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="f5dee-214">Допустимые расширения имен файлов: BYOK и PFX.</span><span class="sxs-lookup"><span data-stu-id="f5dee-214">The valid file name extensions are .byok and .pfx.</span></span>
- <span data-ttu-id="f5dee-215">Если это BYOK-файл, он автоматически защищен HSMs после импорта, и этот элемент по умолчанию нельзя переопрестить.</span><span class="sxs-lookup"><span data-stu-id="f5dee-215">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>
- <span data-ttu-id="f5dee-216">Если файл является PFX-файлом, ключ автоматически защищен программным обеспечением после импорта.</span><span class="sxs-lookup"><span data-stu-id="f5dee-216">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="f5dee-217">Чтобы переопререгировать этот параметр по умолчанию, задате для параметра *Destination* параметр HSM так, чтобы ключ защищен HSM.</span><span class="sxs-lookup"><span data-stu-id="f5dee-217">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>
<span data-ttu-id="f5dee-218">Если этот параметр указан, параметр *Destination* является необязательным.</span><span class="sxs-lookup"><span data-stu-id="f5dee-218">When you specify this parameter, the *Destination* parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, HsmInteractiveImport, InputObjectImport, HsmInputObjectImport, ResourceIdImport, HsmResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5dee-219">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="f5dee-219">-KeyOps</span></span>
<span data-ttu-id="f5dee-220">Определяет массив операций, которые можно выполнять с помощью ключа, который добавляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5dee-220">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="f5dee-221">Если этот параметр не задан, можно выполнить все операции.</span><span class="sxs-lookup"><span data-stu-id="f5dee-221">If you do not specify this parameter, all operations can be performed.</span></span>
<span data-ttu-id="f5dee-222">Допустимыми значениями для этого параметра является список операций, разделенных запятыми, в соответствии со спецификацией [JSON Web Key (JWK):](http://go.microsoft.com/fwlink/?LinkID=613300)</span><span class="sxs-lookup"><span data-stu-id="f5dee-222">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](http://go.microsoft.com/fwlink/?LinkID=613300):</span></span>
- <span data-ttu-id="f5dee-223">шифровать</span><span class="sxs-lookup"><span data-stu-id="f5dee-223">encrypt</span></span>
- <span data-ttu-id="f5dee-224">расшифровать</span><span class="sxs-lookup"><span data-stu-id="f5dee-224">decrypt</span></span>
- <span data-ttu-id="f5dee-225">wrapKey</span><span class="sxs-lookup"><span data-stu-id="f5dee-225">wrapKey</span></span>
- <span data-ttu-id="f5dee-226">unw уберегатьKey</span><span class="sxs-lookup"><span data-stu-id="f5dee-226">unwrapKey</span></span>
- <span data-ttu-id="f5dee-227">подписать</span><span class="sxs-lookup"><span data-stu-id="f5dee-227">sign</span></span>
- <span data-ttu-id="f5dee-228">проверить</span><span class="sxs-lookup"><span data-stu-id="f5dee-228">verify</span></span>
- <span data-ttu-id="f5dee-229">импорт (только для KEK, см. пример 7)</span><span class="sxs-lookup"><span data-stu-id="f5dee-229">import (for KEK only, see example 7)</span></span>

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

### <span data-ttu-id="f5dee-230">-KeyType</span><span class="sxs-lookup"><span data-stu-id="f5dee-230">-KeyType</span></span>
<span data-ttu-id="f5dee-231">Определяет тип ключа этого ключа.</span><span class="sxs-lookup"><span data-stu-id="f5dee-231">Specifies the key type of this key.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmInteractiveCreate, HsmInputObjectCreate, HsmResourceIdCreate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5dee-232">-Name</span><span class="sxs-lookup"><span data-stu-id="f5dee-232">-Name</span></span>
<span data-ttu-id="f5dee-233">Указывает имя ключа, который нужно добавить в хранилище.</span><span class="sxs-lookup"><span data-stu-id="f5dee-233">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="f5dee-234">Этот cmdlet конструирует полное доменное имя (FQDN) ключа на основе имени, указанного этим параметром, имени хранилища ключа и текущей среды.</span><span class="sxs-lookup"><span data-stu-id="f5dee-234">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="f5dee-235">Имя должно быть строкой длиной от 1 до 63 символов, содержашей только 0–9, a–z, A-Z и - (символ тире).</span><span class="sxs-lookup"><span data-stu-id="f5dee-235">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

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

### <span data-ttu-id="f5dee-236">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="f5dee-236">-NotBefore</span></span>
<span data-ttu-id="f5dee-237">Время в качестве объекта **даты и времени,** перед которым нельзя использовать ключ.</span><span class="sxs-lookup"><span data-stu-id="f5dee-237">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="f5dee-238">Этот параметр использует UTC.</span><span class="sxs-lookup"><span data-stu-id="f5dee-238">This parameter uses UTC.</span></span> <span data-ttu-id="f5dee-239">Чтобы получить объект **даты и времени,** используйте cmdlet **Get-Date.**</span><span class="sxs-lookup"><span data-stu-id="f5dee-239">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="f5dee-240">Если этот параметр не задан, его можно использовать сразу же.</span><span class="sxs-lookup"><span data-stu-id="f5dee-240">If you do not specify this parameter, the key can be used immediately.</span></span>

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

### <span data-ttu-id="f5dee-241">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f5dee-241">-ResourceId</span></span>
<span data-ttu-id="f5dee-242">ИД ресурса хранилища.</span><span class="sxs-lookup"><span data-stu-id="f5dee-242">Vault Resource Id.</span></span>

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

### <span data-ttu-id="f5dee-243">-Size</span><span class="sxs-lookup"><span data-stu-id="f5dee-243">-Size</span></span>
<span data-ttu-id="f5dee-244">Размер ключа RSA в битах.</span><span class="sxs-lookup"><span data-stu-id="f5dee-244">RSA key size, in bits.</span></span> <span data-ttu-id="f5dee-245">Если не указано, служба предоставит безопасный стандартный стандарт.</span><span class="sxs-lookup"><span data-stu-id="f5dee-245">If not specified, the service will provide a safe default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, HsmInteractiveCreate, InputObjectCreate, HsmInputObjectCreate, ResourceIdCreate, HsmResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5dee-246">-Tag</span><span class="sxs-lookup"><span data-stu-id="f5dee-246">-Tag</span></span>
<span data-ttu-id="f5dee-247">Пары значений ключа в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="f5dee-247">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f5dee-248">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="f5dee-248">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f5dee-249">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f5dee-249">-VaultName</span></span>
<span data-ttu-id="f5dee-250">Указывает имя хранилища ключей, к которому этот cmdlet добавляет ключ.</span><span class="sxs-lookup"><span data-stu-id="f5dee-250">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="f5dee-251">Этот cmdlet конструирует FQDN ключа хранилища на основе имени, указанного этим параметром, и текущей среды.</span><span class="sxs-lookup"><span data-stu-id="f5dee-251">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="f5dee-252">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f5dee-252">-Confirm</span></span>
<span data-ttu-id="f5dee-253">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f5dee-253">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5dee-254">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5dee-254">-WhatIf</span></span>
<span data-ttu-id="f5dee-255">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5dee-255">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5dee-256">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f5dee-256">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5dee-257">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5dee-257">CommonParameters</span></span>
<span data-ttu-id="f5dee-258">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5dee-258">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5dee-259">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5dee-259">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5dee-260">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f5dee-260">INPUTS</span></span>

### <span data-ttu-id="f5dee-261">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="f5dee-261">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="f5dee-262">System.String</span><span class="sxs-lookup"><span data-stu-id="f5dee-262">System.String</span></span>

## <span data-ttu-id="f5dee-263">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f5dee-263">OUTPUTS</span></span>

### <span data-ttu-id="f5dee-264">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f5dee-264">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="f5dee-265">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f5dee-265">NOTES</span></span>

## <span data-ttu-id="f5dee-266">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f5dee-266">RELATED LINKS</span></span>

[<span data-ttu-id="f5dee-267">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f5dee-267">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="f5dee-268">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f5dee-268">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="f5dee-269">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f5dee-269">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="f5dee-270">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="f5dee-270">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)
