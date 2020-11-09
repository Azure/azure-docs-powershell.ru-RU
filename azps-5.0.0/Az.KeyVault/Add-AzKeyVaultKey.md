---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: 8583a078e12be5da3a6bcbbe16bc3349f51b9bdb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312392"
---
# <span data-ttu-id="1e36f-101">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e36f-101">Add-AzKeyVaultKey</span></span>

## <span data-ttu-id="1e36f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1e36f-102">SYNOPSIS</span></span>
<span data-ttu-id="1e36f-103">Создание ключа в хранилище ключей или импорт ключа в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="1e36f-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

## <span data-ttu-id="1e36f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1e36f-104">SYNTAX</span></span>

### <span data-ttu-id="1e36f-105">InteractiveCreate (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1e36f-105">InteractiveCreate (Default)</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e36f-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="1e36f-106">InteractiveImport</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e36f-107">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="1e36f-107">InputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e36f-108">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="1e36f-108">InputObjectImport</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e36f-109">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="1e36f-109">ResourceIdCreate</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e36f-110">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="1e36f-110">ResourceIdImport</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e36f-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e36f-111">DESCRIPTION</span></span>
<span data-ttu-id="1e36f-112">Командлет **Add-AzKeyVaultKey** создает ключ в хранилище ключей в хранилище ключей Azure или импортирует ключ в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="1e36f-112">The **Add-AzKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="1e36f-113">Используйте этот командлет для добавления клавиш одним из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="1e36f-113">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="1e36f-114">Создание ключа в аппаратном модуле безопасности (HSM) в службе хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="1e36f-114">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="1e36f-115">Создание ключа в программном обеспечении в службе хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="1e36f-115">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="1e36f-116">Импортируйте ключ из собственного модуля безопасности оборудования (HSM) в HSMs в службе хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="1e36f-116">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="1e36f-117">Импорт ключа из PFX-файла на компьютере.</span><span class="sxs-lookup"><span data-stu-id="1e36f-117">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="1e36f-118">Импорт ключа из PFX-файла на компьютере в модули безопасности оборудования (HSMs) в службе хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="1e36f-118">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>
<span data-ttu-id="1e36f-119">Для любой из этих операций можно задать ключевые атрибуты или оставить параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1e36f-119">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="1e36f-120">Если вы создаете или импортируете ключ с тем же именем, что и у существующего ключа в вашем хранилище ключей, первоначальный ключ обновляется с учетом значений, которые вы указали для нового ключа.</span><span class="sxs-lookup"><span data-stu-id="1e36f-120">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="1e36f-121">Вы можете получить доступ к предыдущим значениям, используя универсальный код ресурса (URI) для указанной версии ключа.</span><span class="sxs-lookup"><span data-stu-id="1e36f-121">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="1e36f-122">Чтобы узнать о ключевых версиях и структуре URI, ознакомьтесь с [разделами о ключах и секретах](http://go.microsoft.com/fwlink/?linkid=518560) в документации API для оставшейся части хранилища.</span><span class="sxs-lookup"><span data-stu-id="1e36f-122">To learn about key versions and the URI structure, see [About Keys and Secrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>
<span data-ttu-id="1e36f-123">Примечание. чтобы импортировать ключ из собственного модуля безопасности оборудования, необходимо сначала создать пакет BYOK (файл с расширением BYOK Name) с помощью набора инструментов Azure Key Vault BYOK.</span><span class="sxs-lookup"><span data-stu-id="1e36f-123">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="1e36f-124">Дополнительные сведения [можно найти в разделе Создание и перенос ключей HSM-Protected для Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="1e36f-124">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>
<span data-ttu-id="1e36f-125">Рекомендуется создать резервную копию ключа после его создания или обновления с помощью командлета Backup-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="1e36f-125">As a best practice, back up your key after it is created or updated, by using the Backup-AzKeyVaultKey cmdlet.</span></span> <span data-ttu-id="1e36f-126">Функция отмены удаления отсутствует, поэтому если вы случайно удалили ключ или удалите его, а затем передумали, ключ не подлежит восстановлению, только если у вас есть резервная копия, которую вы можете восстановить.</span><span class="sxs-lookup"><span data-stu-id="1e36f-126">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="1e36f-127">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1e36f-127">EXAMPLES</span></span>

### <span data-ttu-id="1e36f-128">Пример 1: создание ключа</span><span class="sxs-lookup"><span data-stu-id="1e36f-128">Example 1: Create a key</span></span>
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

<span data-ttu-id="1e36f-129">Эта команда создает ключ с защитой программного обеспечения с именем ITSoftware в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="1e36f-129">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="1e36f-130">Пример 2: создание ключа, защищенного с помощью HSM</span><span class="sxs-lookup"><span data-stu-id="1e36f-130">Example 2: Create an HSM-protected key</span></span>
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

<span data-ttu-id="1e36f-131">Эта команда создает ключ, защищенный HSM, в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="1e36f-131">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="1e36f-132">Пример 3: создание ключа с использованием значений, не заданных по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1e36f-132">Example 3: Create a key with non-default values</span></span>
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

<span data-ttu-id="1e36f-133">Первая команда сохраняет значения для расшифровки и проверки в переменной $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="1e36f-133">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="1e36f-134">Вторая команда создает объект **DateTime** , определенный в формате UTC, с помощью командлета **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="1e36f-134">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="1e36f-135">Этот объект указывает на время в будущем на два года.</span><span class="sxs-lookup"><span data-stu-id="1e36f-135">That object specifies a time two years in the future.</span></span> <span data-ttu-id="1e36f-136">Команда сохраняет эту дату в переменной $Expires.</span><span class="sxs-lookup"><span data-stu-id="1e36f-136">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="1e36f-137">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="1e36f-137">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="1e36f-138">Третья команда создает объект **DateTime** с помощью командлета **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="1e36f-138">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="1e36f-139">Этот объект указывает текущее время в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="1e36f-139">That object specifies current UTC time.</span></span> <span data-ttu-id="1e36f-140">Команда сохраняет эту дату в переменной $NotBefore.</span><span class="sxs-lookup"><span data-stu-id="1e36f-140">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="1e36f-141">Последняя команда создает ключ с именем ITHsmNonDefault, который является ключом, защищенным с помощью HSM.</span><span class="sxs-lookup"><span data-stu-id="1e36f-141">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="1e36f-142">Команда задает значения разрешенных операций с ключами, сохраненными $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="1e36f-142">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="1e36f-143">В команде указаны значения времени для параметров *Expires* и *NotBefore* , созданных в предыдущих командах, а также теги для высокого уровня важности и.</span><span class="sxs-lookup"><span data-stu-id="1e36f-143">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="1e36f-144">Новый ключ отключен.</span><span class="sxs-lookup"><span data-stu-id="1e36f-144">The new key is disabled.</span></span> <span data-ttu-id="1e36f-145">Это можно сделать с помощью командлета **Set-AzKeyVaultKey** .</span><span class="sxs-lookup"><span data-stu-id="1e36f-145">You can enable it by using the **Set-AzKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="1e36f-146">Пример 4: импорт ключа, защищенного с помощью HSM</span><span class="sxs-lookup"><span data-stu-id="1e36f-146">Example 4: Import an HSM-protected key</span></span>
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

<span data-ttu-id="1e36f-147">Эта команда импортирует ключ с именем ITByok из расположения, указанного параметром *KeyFilePath* .</span><span class="sxs-lookup"><span data-stu-id="1e36f-147">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="1e36f-148">Импортированный ключ является ключом, защищенным с помощью HSM.</span><span class="sxs-lookup"><span data-stu-id="1e36f-148">The imported key is an HSM-protected key.</span></span>
<span data-ttu-id="1e36f-149">Чтобы импортировать ключ из собственного модуля безопасности оборудования, необходимо сначала создать пакет BYOK (файл с расширением BYOK Name) с помощью набора инструментов Azure Key Vault BYOK.</span><span class="sxs-lookup"><span data-stu-id="1e36f-149">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="1e36f-150">Дополнительные сведения [можно найти в разделе Создание и перенос ключей HSM-Protected для Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="1e36f-150">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="1e36f-151">Пример 5: импорт ключа, защищенного с помощью программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="1e36f-151">Example 5: Import a software-protected key</span></span>
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

<span data-ttu-id="1e36f-152">Первая команда преобразует строку в защищенную строку с помощью командлета **ConvertTo-SecureString** , а затем сохраняет эту строку в переменной $Password.</span><span class="sxs-lookup"><span data-stu-id="1e36f-152">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="1e36f-153">Для получения дополнительных сведений введите `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="1e36f-153">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="1e36f-154">Вторая команда создает пароль программного обеспечения в хранилище ключей contoso.</span><span class="sxs-lookup"><span data-stu-id="1e36f-154">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="1e36f-155">Команда задает расположение ключа и пароль, хранящийся в $Password.</span><span class="sxs-lookup"><span data-stu-id="1e36f-155">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="1e36f-156">Пример 6: импорт ключа и назначение атрибутов</span><span class="sxs-lookup"><span data-stu-id="1e36f-156">Example 6: Import a key and assign attributes</span></span>
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

<span data-ttu-id="1e36f-157">Первая команда преобразует строку в защищенную строку с помощью командлета **ConvertTo-SecureString** , а затем сохраняет эту строку в переменной $Password.</span><span class="sxs-lookup"><span data-stu-id="1e36f-157">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>
<span data-ttu-id="1e36f-158">Вторая команда создает объект **DateTime** с помощью командлета **Get-Date** , а затем сохраняет этот объект в переменной $Expires.</span><span class="sxs-lookup"><span data-stu-id="1e36f-158">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>
<span data-ttu-id="1e36f-159">Третья команда создает переменную $tags, чтобы установить теги для высокого уровня важности и.</span><span class="sxs-lookup"><span data-stu-id="1e36f-159">The third command creates the $tags variable to set tags for high severity and IT.</span></span>
<span data-ttu-id="1e36f-160">Последняя команда импортирует ключ в качестве ключа HSM из указанного места.</span><span class="sxs-lookup"><span data-stu-id="1e36f-160">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="1e36f-161">Команда задает срок действия, хранящийся в $Expires и пароль, которые хранятся в $Password, и применяет теги, хранящиеся в $tags.</span><span class="sxs-lookup"><span data-stu-id="1e36f-161">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

### <span data-ttu-id="1e36f-162">Пример 7: создание ключа обмена ключами (Кек) для функции "создать собственный ключ" (BYOK)</span><span class="sxs-lookup"><span data-stu-id="1e36f-162">Example 7: Generate a Key Exchange Key (KEK) for "bring your own key" (BYOK) feature</span></span>

```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName $vaultName -Name $keyName -Destination HSM -Size 2048 -KeyOps "import"
```

<span data-ttu-id="1e36f-163">Создание ключа (который называется ключом обмена ключами (Кек)).</span><span class="sxs-lookup"><span data-stu-id="1e36f-163">Generates a key (referred to as a Key Exchange Key (KEK)).</span></span> <span data-ttu-id="1e36f-164">Кек должен быть ключом RSA-HSM, который имеет только операцию импорта ключа.</span><span class="sxs-lookup"><span data-stu-id="1e36f-164">The KEK must be an RSA-HSM key that has only the import key operation.</span></span> <span data-ttu-id="1e36f-165">Ключи RSA-HSM поддерживаются только в конфигурации Key Vault Premium.</span><span class="sxs-lookup"><span data-stu-id="1e36f-165">Only Key Vault Premium SKU supports RSA-HSM keys.</span></span>
<span data-ttu-id="1e36f-166">Подробнее читайте в статье https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="1e36f-166">For more details please refer to https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="1e36f-167">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1e36f-167">PARAMETERS</span></span>

### <span data-ttu-id="1e36f-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e36f-168">-DefaultProfile</span></span>
<span data-ttu-id="1e36f-169">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1e36f-169">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e36f-170">-Destination</span><span class="sxs-lookup"><span data-stu-id="1e36f-170">-Destination</span></span>
<span data-ttu-id="1e36f-171">Указывает, следует ли добавить ключ в качестве ключа с защитой программного обеспечения или ключа, защищенного с помощью HSM, в службе хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="1e36f-171">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="1e36f-172">Допустимые значения: HSM и программное обеспечение.</span><span class="sxs-lookup"><span data-stu-id="1e36f-172">Valid values are: HSM and Software.</span></span>
<span data-ttu-id="1e36f-173">Примечание. чтобы использовать HSM в качестве места назначения, необходимо иметь ключевое хранилище, которое поддерживает HSMs.</span><span class="sxs-lookup"><span data-stu-id="1e36f-173">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="1e36f-174">Дополнительные сведения о уровнях обслуживания и возможностях Azure Key Vault можно найти на [веб-сайте ценообразования для Azure Key Vault](http://go.microsoft.com/fwlink/?linkid=512521).</span><span class="sxs-lookup"><span data-stu-id="1e36f-174">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](http://go.microsoft.com/fwlink/?linkid=512521).</span></span>
<span data-ttu-id="1e36f-175">Этот параметр является обязательным при создании нового ключа.</span><span class="sxs-lookup"><span data-stu-id="1e36f-175">This parameter is required when you create a new key.</span></span> <span data-ttu-id="1e36f-176">При импорте ключа с помощью параметра *KeyFilePath* этот параметр является необязательным:</span><span class="sxs-lookup"><span data-stu-id="1e36f-176">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>
- <span data-ttu-id="1e36f-177">Если этот параметр не указан, а этот командлет импортирует ключ с расширением byok, он импортирует этот ключ в качестве ключа, защищенного с помощью HSM-файлов.</span><span class="sxs-lookup"><span data-stu-id="1e36f-177">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="1e36f-178">Командлет не может импортировать эту клавишу в качестве ключа, защищенного с помощью программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="1e36f-178">The cmdlet cannot import that key as software-protected key.</span></span>
- <span data-ttu-id="1e36f-179">Если этот параметр не указан, а этот командлет импортирует ключ с расширением имени PFX-файла, он импортирует ключ как ключ, защищенный программным обеспечением.</span><span class="sxs-lookup"><span data-stu-id="1e36f-179">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

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

### <span data-ttu-id="1e36f-180">-Отключение</span><span class="sxs-lookup"><span data-stu-id="1e36f-180">-Disable</span></span>
<span data-ttu-id="1e36f-181">Указывает на то, что для добавляемого ключа задано начальное состояние "отключено".</span><span class="sxs-lookup"><span data-stu-id="1e36f-181">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="1e36f-182">Любая попытка использования ключа завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="1e36f-182">Any attempt to use the key will fail.</span></span> <span data-ttu-id="1e36f-183">Используйте этот параметр, если нужно предварительно загрузить ключи, которые нужно включить в дальнейшем.</span><span class="sxs-lookup"><span data-stu-id="1e36f-183">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="1e36f-184">-Истекает</span><span class="sxs-lookup"><span data-stu-id="1e36f-184">-Expires</span></span>
<span data-ttu-id="1e36f-185">Задает время истечения срока действия в виде объекта **DateTime** для ключа, который добавляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="1e36f-185">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="1e36f-186">Этот параметр использует координированное координированное время (UTC).</span><span class="sxs-lookup"><span data-stu-id="1e36f-186">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="1e36f-187">Чтобы получить объект **DateTime** , используйте командлет **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="1e36f-187">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="1e36f-188">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="1e36f-188">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="1e36f-189">Если этот параметр не указан, срок действия ключа не истекает.</span><span class="sxs-lookup"><span data-stu-id="1e36f-189">If you do not specify this parameter, the key does not expire.</span></span>

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

### <span data-ttu-id="1e36f-190">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e36f-190">-InputObject</span></span>
<span data-ttu-id="1e36f-191">Объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="1e36f-191">Vault object.</span></span>

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

### <span data-ttu-id="1e36f-192">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="1e36f-192">-KeyFilePassword</span></span>
<span data-ttu-id="1e36f-193">Указывает пароль для импортированного файла как объект **SecureString** .</span><span class="sxs-lookup"><span data-stu-id="1e36f-193">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="1e36f-194">Чтобы получить объект **SecureString** , используйте командлет **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="1e36f-194">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="1e36f-195">Для получения дополнительных сведений введите `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="1e36f-195">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="1e36f-196">Вы должны указать этот пароль, чтобы импортировать файл с расширением имени PFX-файла.</span><span class="sxs-lookup"><span data-stu-id="1e36f-196">You must specify this password to import a file with a .pfx file name extension.</span></span>

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

### <span data-ttu-id="1e36f-197">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="1e36f-197">-KeyFilePath</span></span>
<span data-ttu-id="1e36f-198">Указывает путь к локальному файлу, содержащему ключевой материал, который этот командлет импортирует.</span><span class="sxs-lookup"><span data-stu-id="1e36f-198">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="1e36f-199">Допустимые расширения имен файлов: byok и PFX.</span><span class="sxs-lookup"><span data-stu-id="1e36f-199">The valid file name extensions are .byok and .pfx.</span></span>
- <span data-ttu-id="1e36f-200">Если файл является файлом byok, ключ автоматически защищается HSMs после импорта, и вы не сможете переопределить этот параметр по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1e36f-200">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>
- <span data-ttu-id="1e36f-201">Если файл является PFX-файлом, ключ автоматически защищается программным путем после импорта.</span><span class="sxs-lookup"><span data-stu-id="1e36f-201">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="1e36f-202">Чтобы переопределить это значение по умолчанию, установите для параметра *Destination* значение HSM, чтобы ключ был защищен с помощью HSM-аппаратных защит.</span><span class="sxs-lookup"><span data-stu-id="1e36f-202">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>
<span data-ttu-id="1e36f-203">Если указать этот параметр, параметр *Destination* является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1e36f-203">When you specify this parameter, the *Destination* parameter is optional.</span></span>

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

### <span data-ttu-id="1e36f-204">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="1e36f-204">-KeyOps</span></span>
<span data-ttu-id="1e36f-205">Задает массив операций, которые можно выполнить с помощью ключа, который добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1e36f-205">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="1e36f-206">Если этот параметр не указан, может выполняться выполнение всех операций.</span><span class="sxs-lookup"><span data-stu-id="1e36f-206">If you do not specify this parameter, all operations can be performed.</span></span>
<span data-ttu-id="1e36f-207">Допустимые значения этого параметра — это разделенный запятыми список ключевых операций, заданных [спецификацией JSON Web Key (JWK)](http://go.microsoft.com/fwlink/?LinkID=613300):</span><span class="sxs-lookup"><span data-stu-id="1e36f-207">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](http://go.microsoft.com/fwlink/?LinkID=613300):</span></span>
- <span data-ttu-id="1e36f-208">EFS</span><span class="sxs-lookup"><span data-stu-id="1e36f-208">encrypt</span></span>
- <span data-ttu-id="1e36f-209">расшифровки</span><span class="sxs-lookup"><span data-stu-id="1e36f-209">decrypt</span></span>
- <span data-ttu-id="1e36f-210">wrapKey</span><span class="sxs-lookup"><span data-stu-id="1e36f-210">wrapKey</span></span>
- <span data-ttu-id="1e36f-211">unwrapKey</span><span class="sxs-lookup"><span data-stu-id="1e36f-211">unwrapKey</span></span>
- <span data-ttu-id="1e36f-212">рядом</span><span class="sxs-lookup"><span data-stu-id="1e36f-212">sign</span></span>
- <span data-ttu-id="1e36f-213">подтвержда</span><span class="sxs-lookup"><span data-stu-id="1e36f-213">verify</span></span>
- <span data-ttu-id="1e36f-214">Import (только для Кек см. Пример 7)</span><span class="sxs-lookup"><span data-stu-id="1e36f-214">import (for KEK only, see example 7)</span></span>

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

### <span data-ttu-id="1e36f-215">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1e36f-215">-Name</span></span>
<span data-ttu-id="1e36f-216">Задает имя ключа, который нужно добавить в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="1e36f-216">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="1e36f-217">Этот командлет создает полное доменное имя (FQDN) ключа на основе имени, которое указывает этот параметр, имя хранилища ключей и текущую среду.</span><span class="sxs-lookup"><span data-stu-id="1e36f-217">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="1e36f-218">Имя должно быть строкой из 1 – 63 знаков длиной, содержащей только 0-9, a-z, A-Z и (дефис).</span><span class="sxs-lookup"><span data-stu-id="1e36f-218">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

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

### <span data-ttu-id="1e36f-219">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="1e36f-219">-NotBefore</span></span>
<span data-ttu-id="1e36f-220">Указывает время в виде объекта **DateTime** , до которого невозможно использовать клавишу.</span><span class="sxs-lookup"><span data-stu-id="1e36f-220">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="1e36f-221">Этот параметр использует время в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="1e36f-221">This parameter uses UTC.</span></span> <span data-ttu-id="1e36f-222">Чтобы получить объект **DateTime** , используйте командлет **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="1e36f-222">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="1e36f-223">Если этот параметр не указан, клавишу можно использовать сразу.</span><span class="sxs-lookup"><span data-stu-id="1e36f-223">If you do not specify this parameter, the key can be used immediately.</span></span>

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

### <span data-ttu-id="1e36f-224">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e36f-224">-ResourceId</span></span>
<span data-ttu-id="1e36f-225">Идентификатор ресурса хранилища.</span><span class="sxs-lookup"><span data-stu-id="1e36f-225">Vault Resource Id.</span></span>

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

### <span data-ttu-id="1e36f-226">-Size</span><span class="sxs-lookup"><span data-stu-id="1e36f-226">-Size</span></span>
<span data-ttu-id="1e36f-227">Размер ключа RSA в битах.</span><span class="sxs-lookup"><span data-stu-id="1e36f-227">RSA key size, in bits.</span></span> <span data-ttu-id="1e36f-228">Если он не указан, служба обеспечивает безопасность по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1e36f-228">If not specified, the service will provide a safe default.</span></span>

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

### <span data-ttu-id="1e36f-229">-Тег</span><span class="sxs-lookup"><span data-stu-id="1e36f-229">-Tag</span></span>
<span data-ttu-id="1e36f-230">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="1e36f-230">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1e36f-231">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="1e36f-231">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1e36f-232">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1e36f-232">-VaultName</span></span>
<span data-ttu-id="1e36f-233">Указывает имя хранилища ключей, к которому этот командлет добавляет ключ.</span><span class="sxs-lookup"><span data-stu-id="1e36f-233">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="1e36f-234">Этот командлет создает полное доменное имя хранилища ключей, основываясь на имени, указанном этим параметром, и текущей среде.</span><span class="sxs-lookup"><span data-stu-id="1e36f-234">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="1e36f-235">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e36f-235">-Confirm</span></span>
<span data-ttu-id="1e36f-236">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1e36f-236">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e36f-237">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e36f-237">-WhatIf</span></span>
<span data-ttu-id="1e36f-238">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1e36f-238">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e36f-239">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1e36f-239">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e36f-240">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e36f-240">CommonParameters</span></span>
<span data-ttu-id="1e36f-241">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1e36f-241">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e36f-242">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1e36f-242">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e36f-243">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1e36f-243">INPUTS</span></span>

### <span data-ttu-id="1e36f-244">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="1e36f-244">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="1e36f-245">System. String</span><span class="sxs-lookup"><span data-stu-id="1e36f-245">System.String</span></span>

## <span data-ttu-id="1e36f-246">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1e36f-246">OUTPUTS</span></span>

### <span data-ttu-id="1e36f-247">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e36f-247">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="1e36f-248">Пуск</span><span class="sxs-lookup"><span data-stu-id="1e36f-248">NOTES</span></span>

## <span data-ttu-id="1e36f-249">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1e36f-249">RELATED LINKS</span></span>

[<span data-ttu-id="1e36f-250">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e36f-250">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="1e36f-251">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e36f-251">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="1e36f-252">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e36f-252">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="1e36f-253">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="1e36f-253">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)
