---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultKey.md
ms.openlocfilehash: c363f32b8c28b2e6f83f4e065c677926800d04b2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734653"
---
# <span data-ttu-id="71ef0-101">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="71ef0-101">Add-AzureKeyVaultKey</span></span>

## <span data-ttu-id="71ef0-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="71ef0-102">SYNOPSIS</span></span>
<span data-ttu-id="71ef0-103">Создание ключа в хранилище ключей или импорт ключа в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="71ef0-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71ef0-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="71ef0-104">SYNTAX</span></span>

### <span data-ttu-id="71ef0-105">InteractiveCreate (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="71ef0-105">InteractiveCreate (Default)</span></span>
```
Add-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71ef0-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="71ef0-106">InteractiveImport</span></span>
```
Add-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71ef0-107">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="71ef0-107">InputObjectCreate</span></span>
```
Add-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71ef0-108">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="71ef0-108">InputObjectImport</span></span>
```
Add-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71ef0-109">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="71ef0-109">ResourceIdCreate</span></span>
```
Add-AzureKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71ef0-110">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="71ef0-110">ResourceIdImport</span></span>
```
Add-AzureKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71ef0-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="71ef0-111">DESCRIPTION</span></span>
<span data-ttu-id="71ef0-112">Командлет **Add-AzureKeyVaultKey** создает ключ в хранилище ключей в хранилище ключей Azure или импортирует ключ в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="71ef0-112">The **Add-AzureKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="71ef0-113">Используйте этот командлет для добавления клавиш одним из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="71ef0-113">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="71ef0-114">Создание ключа в аппаратном модуле безопасности (HSM) в службе хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="71ef0-114">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="71ef0-115">Создание ключа в программном обеспечении в службе хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="71ef0-115">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="71ef0-116">Импортируйте ключ из собственного модуля безопасности оборудования (HSM) в HSMs в службе хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="71ef0-116">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="71ef0-117">Импорт ключа из PFX-файла на компьютере.</span><span class="sxs-lookup"><span data-stu-id="71ef0-117">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="71ef0-118">Импорт ключа из PFX-файла на компьютере в модули безопасности оборудования (HSMs) в службе хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="71ef0-118">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>
<span data-ttu-id="71ef0-119">Для любой из этих операций можно задать ключевые атрибуты или оставить параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="71ef0-119">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="71ef0-120">Если вы создаете или импортируете ключ с тем же именем, что и у существующего ключа в вашем хранилище ключей, первоначальный ключ обновляется с учетом значений, которые вы указали для нового ключа.</span><span class="sxs-lookup"><span data-stu-id="71ef0-120">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="71ef0-121">Вы можете получить доступ к предыдущим значениям, используя универсальный код ресурса (URI) для указанной версии ключа.</span><span class="sxs-lookup"><span data-stu-id="71ef0-121">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="71ef0-122">Чтобы узнать о ключевых версиях и структуре URI, ознакомьтесь с [разделами о ключах и секретах](https://go.microsoft.com/fwlink/?linkid=518560) в документации API для оставшейся части хранилища.</span><span class="sxs-lookup"><span data-stu-id="71ef0-122">To learn about key versions and the URI structure, see [About Keys and Secrets](https://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>
<span data-ttu-id="71ef0-123">Примечание. чтобы импортировать ключ из собственного модуля безопасности оборудования, необходимо сначала создать пакет BYOK (файл с расширением BYOK Name) с помощью набора инструментов Azure Key Vault BYOK.</span><span class="sxs-lookup"><span data-stu-id="71ef0-123">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="71ef0-124">Дополнительные сведения [можно найти в разделе Создание и перенос ключей HSM-Protected для Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="71ef0-124">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span></span>
<span data-ttu-id="71ef0-125">Рекомендуется создать резервную копию ключа после его создания или обновления с помощью командлета Backup-AzureKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="71ef0-125">As a best practice, back up your key after it is created or updated, by using the Backup-AzureKeyVaultKey cmdlet.</span></span> <span data-ttu-id="71ef0-126">Функция отмены удаления отсутствует, поэтому если вы случайно удалили ключ или удалите его, а затем передумали, ключ не подлежит восстановлению, только если у вас есть резервная копия, которую вы можете восстановить.</span><span class="sxs-lookup"><span data-stu-id="71ef0-126">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="71ef0-127">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="71ef0-127">EXAMPLES</span></span>

### <span data-ttu-id="71ef0-128">Пример 1: создание ключа</span><span class="sxs-lookup"><span data-stu-id="71ef0-128">Example 1: Create a key</span></span>
```powershell
PS C:\> Add-AzureKeyVaultKey -VaultName 'contoso' -Name 'ITSoftware' -Destination 'Software'

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

<span data-ttu-id="71ef0-129">Эта команда создает ключ с защитой программного обеспечения с именем ITSoftware в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="71ef0-129">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="71ef0-130">Пример 2: создание ключа, защищенного с помощью HSM</span><span class="sxs-lookup"><span data-stu-id="71ef0-130">Example 2: Create an HSM-protected key</span></span>
```powershell
PS C:\> Add-AzureKeyVaultKey -VaultName 'contoso' -Name 'ITHsm' -Destination 'HSM'

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

<span data-ttu-id="71ef0-131">Эта команда создает ключ, защищенный HSM, в хранилище ключей, именуемом contoso.</span><span class="sxs-lookup"><span data-stu-id="71ef0-131">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="71ef0-132">Пример 3: создание ключа с использованием значений, не заданных по умолчанию</span><span class="sxs-lookup"><span data-stu-id="71ef0-132">Example 3: Create a key with non-default values</span></span>
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzureKeyVaultKey -VaultName 'contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

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

<span data-ttu-id="71ef0-133">Первая команда сохраняет значения для расшифровки и проверки в переменной $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="71ef0-133">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="71ef0-134">Вторая команда создает объект **DateTime** , определенный в формате UTC, с помощью командлета **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="71ef0-134">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="71ef0-135">Этот объект указывает на время в будущем на два года.</span><span class="sxs-lookup"><span data-stu-id="71ef0-135">That object specifies a time two years in the future.</span></span> <span data-ttu-id="71ef0-136">Команда сохраняет эту дату в переменной $Expires.</span><span class="sxs-lookup"><span data-stu-id="71ef0-136">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="71ef0-137">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="71ef0-137">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="71ef0-138">Третья команда создает объект **DateTime** с помощью командлета **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="71ef0-138">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="71ef0-139">Этот объект указывает текущее время в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="71ef0-139">That object specifies current UTC time.</span></span> <span data-ttu-id="71ef0-140">Команда сохраняет эту дату в переменной $NotBefore.</span><span class="sxs-lookup"><span data-stu-id="71ef0-140">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="71ef0-141">Последняя команда создает ключ с именем ITHsmNonDefault, который является ключом, защищенным с помощью HSM.</span><span class="sxs-lookup"><span data-stu-id="71ef0-141">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="71ef0-142">Команда задает значения разрешенных операций с ключами, сохраненными $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="71ef0-142">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="71ef0-143">В команде указаны значения времени для параметров *Expires* и *NotBefore* , созданных в предыдущих командах, а также теги для высокого уровня важности и.</span><span class="sxs-lookup"><span data-stu-id="71ef0-143">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="71ef0-144">Новый ключ отключен.</span><span class="sxs-lookup"><span data-stu-id="71ef0-144">The new key is disabled.</span></span> <span data-ttu-id="71ef0-145">Это можно сделать с помощью командлета **Set-AzureKeyVaultKey** .</span><span class="sxs-lookup"><span data-stu-id="71ef0-145">You can enable it by using the **Set-AzureKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="71ef0-146">Пример 4: импорт ключа, защищенного с помощью HSM</span><span class="sxs-lookup"><span data-stu-id="71ef0-146">Example 4: Import an HSM-protected key</span></span>
```powershell
PS C:\> Add-AzureKeyVaultKey -VaultName 'contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'

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

<span data-ttu-id="71ef0-147">Эта команда импортирует ключ с именем ITByok из расположения, указанного параметром *KeyFilePath* .</span><span class="sxs-lookup"><span data-stu-id="71ef0-147">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="71ef0-148">Импортированный ключ является ключом, защищенным с помощью HSM.</span><span class="sxs-lookup"><span data-stu-id="71ef0-148">The imported key is an HSM-protected key.</span></span>
<span data-ttu-id="71ef0-149">Чтобы импортировать ключ из собственного модуля безопасности оборудования, необходимо сначала создать пакет BYOK (файл с расширением BYOK Name) с помощью набора инструментов Azure Key Vault BYOK.</span><span class="sxs-lookup"><span data-stu-id="71ef0-149">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="71ef0-150">Дополнительные сведения [можно найти в разделе Создание и перенос ключей HSM-Protected для Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="71ef0-150">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](https://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="71ef0-151">Пример 5: импорт ключа, защищенного с помощью программного обеспечения</span><span class="sxs-lookup"><span data-stu-id="71ef0-151">Example 5: Import a software-protected key</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzureKeyVaultKey -VaultName 'contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password

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

<span data-ttu-id="71ef0-152">Первая команда преобразует строку в защищенную строку с помощью командлета **ConvertTo-SecureString** , а затем сохраняет эту строку в переменной $Password.</span><span class="sxs-lookup"><span data-stu-id="71ef0-152">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="71ef0-153">Для получения дополнительных сведений введите `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="71ef0-153">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="71ef0-154">Вторая команда создает пароль программного обеспечения в хранилище ключей contoso.</span><span class="sxs-lookup"><span data-stu-id="71ef0-154">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="71ef0-155">Команда задает расположение ключа и пароль, хранящийся в $Password.</span><span class="sxs-lookup"><span data-stu-id="71ef0-155">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="71ef0-156">Пример 6: импорт ключа и назначение атрибутов</span><span class="sxs-lookup"><span data-stu-id="71ef0-156">Example 6: Import a key and assign attributes</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = "true" }
PS C:\> Add-AzureKeyVaultKey -VaultName 'contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags

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

<span data-ttu-id="71ef0-157">Первая команда преобразует строку в защищенную строку с помощью командлета **ConvertTo-SecureString** , а затем сохраняет эту строку в переменной $Password.</span><span class="sxs-lookup"><span data-stu-id="71ef0-157">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>
<span data-ttu-id="71ef0-158">Вторая команда создает объект **DateTime** с помощью командлета **Get-Date** , а затем сохраняет этот объект в переменной $Expires.</span><span class="sxs-lookup"><span data-stu-id="71ef0-158">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>
<span data-ttu-id="71ef0-159">Третья команда создает переменную $tags, чтобы установить теги для высокого уровня важности и.</span><span class="sxs-lookup"><span data-stu-id="71ef0-159">The third command creates the $tags variable to set tags for high severity and IT.</span></span>
<span data-ttu-id="71ef0-160">Последняя команда импортирует ключ в качестве ключа HSM из указанного места.</span><span class="sxs-lookup"><span data-stu-id="71ef0-160">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="71ef0-161">Команда задает срок действия, хранящийся в $Expires и пароль, которые хранятся в $Password, и применяет теги, хранящиеся в $tags.</span><span class="sxs-lookup"><span data-stu-id="71ef0-161">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

## <span data-ttu-id="71ef0-162">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="71ef0-162">PARAMETERS</span></span>

### <span data-ttu-id="71ef0-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71ef0-163">-DefaultProfile</span></span>
<span data-ttu-id="71ef0-164">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="71ef0-164">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71ef0-165">-Destination</span><span class="sxs-lookup"><span data-stu-id="71ef0-165">-Destination</span></span>
<span data-ttu-id="71ef0-166">Указывает, следует ли добавить ключ в качестве ключа с защитой программного обеспечения или ключа, защищенного с помощью HSM, в службе хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="71ef0-166">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="71ef0-167">Допустимые значения: HSM и программное обеспечение.</span><span class="sxs-lookup"><span data-stu-id="71ef0-167">Valid values are: HSM and Software.</span></span>
<span data-ttu-id="71ef0-168">Примечание. чтобы использовать HSM в качестве места назначения, необходимо иметь ключевое хранилище, которое поддерживает HSMs.</span><span class="sxs-lookup"><span data-stu-id="71ef0-168">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="71ef0-169">Дополнительные сведения о уровнях обслуживания и возможностях Azure Key Vault можно найти на [веб-сайте ценообразования для Azure Key Vault](https://go.microsoft.com/fwlink/?linkid=512521).</span><span class="sxs-lookup"><span data-stu-id="71ef0-169">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](https://go.microsoft.com/fwlink/?linkid=512521).</span></span>
<span data-ttu-id="71ef0-170">Этот параметр является обязательным при создании нового ключа.</span><span class="sxs-lookup"><span data-stu-id="71ef0-170">This parameter is required when you create a new key.</span></span> <span data-ttu-id="71ef0-171">При импорте ключа с помощью параметра *KeyFilePath* этот параметр является необязательным:</span><span class="sxs-lookup"><span data-stu-id="71ef0-171">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>
- <span data-ttu-id="71ef0-172">Если этот параметр не указан, а этот командлет импортирует ключ с расширением byok, он импортирует этот ключ в качестве ключа, защищенного с помощью HSM-файлов.</span><span class="sxs-lookup"><span data-stu-id="71ef0-172">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="71ef0-173">Командлет не может импортировать эту клавишу в качестве ключа, защищенного с помощью программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="71ef0-173">The cmdlet cannot import that key as software-protected key.</span></span>
- <span data-ttu-id="71ef0-174">Если этот параметр не указан, а этот командлет импортирует ключ с расширением имени PFX-файла, он импортирует ключ как ключ, защищенный программным обеспечением.</span><span class="sxs-lookup"><span data-stu-id="71ef0-174">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

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

### <span data-ttu-id="71ef0-175">-Отключение</span><span class="sxs-lookup"><span data-stu-id="71ef0-175">-Disable</span></span>
<span data-ttu-id="71ef0-176">Указывает на то, что для добавляемого ключа задано начальное состояние "отключено".</span><span class="sxs-lookup"><span data-stu-id="71ef0-176">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="71ef0-177">Любая попытка использования ключа завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="71ef0-177">Any attempt to use the key will fail.</span></span> <span data-ttu-id="71ef0-178">Используйте этот параметр, если нужно предварительно загрузить ключи, которые нужно включить в дальнейшем.</span><span class="sxs-lookup"><span data-stu-id="71ef0-178">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="71ef0-179">-Истекает</span><span class="sxs-lookup"><span data-stu-id="71ef0-179">-Expires</span></span>
<span data-ttu-id="71ef0-180">Задает время истечения срока действия в виде объекта **DateTime** для ключа, который добавляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="71ef0-180">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="71ef0-181">Этот параметр использует координированное координированное время (UTC).</span><span class="sxs-lookup"><span data-stu-id="71ef0-181">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="71ef0-182">Чтобы получить объект **DateTime** , используйте командлет **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="71ef0-182">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="71ef0-183">Для получения дополнительных сведений введите `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="71ef0-183">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="71ef0-184">Если этот параметр не указан, срок действия ключа не истекает.</span><span class="sxs-lookup"><span data-stu-id="71ef0-184">If you do not specify this parameter, the key does not expire.</span></span>

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

### <span data-ttu-id="71ef0-185">-InputObject</span><span class="sxs-lookup"><span data-stu-id="71ef0-185">-InputObject</span></span>
<span data-ttu-id="71ef0-186">Объект хранилища.</span><span class="sxs-lookup"><span data-stu-id="71ef0-186">Vault object.</span></span>

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

### <span data-ttu-id="71ef0-187">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="71ef0-187">-KeyFilePassword</span></span>
<span data-ttu-id="71ef0-188">Указывает пароль для импортированного файла как объект **SecureString** .</span><span class="sxs-lookup"><span data-stu-id="71ef0-188">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="71ef0-189">Чтобы получить объект **SecureString** , используйте командлет **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="71ef0-189">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="71ef0-190">Для получения дополнительных сведений введите `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="71ef0-190">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="71ef0-191">Вы должны указать этот пароль, чтобы импортировать файл с расширением имени PFX-файла.</span><span class="sxs-lookup"><span data-stu-id="71ef0-191">You must specify this password to import a file with a .pfx file name extension.</span></span>

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

### <span data-ttu-id="71ef0-192">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="71ef0-192">-KeyFilePath</span></span>
<span data-ttu-id="71ef0-193">Указывает путь к локальному файлу, содержащему ключевой материал, который этот командлет импортирует.</span><span class="sxs-lookup"><span data-stu-id="71ef0-193">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="71ef0-194">Допустимые расширения имен файлов: byok и PFX.</span><span class="sxs-lookup"><span data-stu-id="71ef0-194">The valid file name extensions are .byok and .pfx.</span></span>
- <span data-ttu-id="71ef0-195">Если файл является файлом byok, ключ автоматически защищается HSMs после импорта, и вы не сможете переопределить этот параметр по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="71ef0-195">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>
- <span data-ttu-id="71ef0-196">Если файл является PFX-файлом, ключ автоматически защищается программным путем после импорта.</span><span class="sxs-lookup"><span data-stu-id="71ef0-196">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="71ef0-197">Чтобы переопределить это значение по умолчанию, установите для параметра *Destination* значение HSM, чтобы ключ был защищен с помощью HSM-аппаратных защит.</span><span class="sxs-lookup"><span data-stu-id="71ef0-197">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>
<span data-ttu-id="71ef0-198">Если указать этот параметр, параметр *Destination* является необязательным.</span><span class="sxs-lookup"><span data-stu-id="71ef0-198">When you specify this parameter, the *Destination* parameter is optional.</span></span>

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

### <span data-ttu-id="71ef0-199">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="71ef0-199">-KeyOps</span></span>
<span data-ttu-id="71ef0-200">Задает массив операций, которые можно выполнить с помощью ключа, который добавляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="71ef0-200">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="71ef0-201">Если этот параметр не указан, может выполняться выполнение всех операций.</span><span class="sxs-lookup"><span data-stu-id="71ef0-201">If you do not specify this parameter, all operations can be performed.</span></span>
<span data-ttu-id="71ef0-202">Допустимые значения этого параметра — это разделенный запятыми список ключевых операций, заданных [спецификацией JSON Web Key (JWK)](https://go.microsoft.com/fwlink/?LinkID=613300):</span><span class="sxs-lookup"><span data-stu-id="71ef0-202">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](https://go.microsoft.com/fwlink/?LinkID=613300):</span></span>
- <span data-ttu-id="71ef0-203">EFS</span><span class="sxs-lookup"><span data-stu-id="71ef0-203">Encrypt</span></span>
- <span data-ttu-id="71ef0-204">Расшифровки</span><span class="sxs-lookup"><span data-stu-id="71ef0-204">Decrypt</span></span>
- <span data-ttu-id="71ef0-205">Инкапсулирует</span><span class="sxs-lookup"><span data-stu-id="71ef0-205">Wrap</span></span>
- <span data-ttu-id="71ef0-206">Разтекание</span><span class="sxs-lookup"><span data-stu-id="71ef0-206">Unwrap</span></span>
- <span data-ttu-id="71ef0-207">Рядом</span><span class="sxs-lookup"><span data-stu-id="71ef0-207">Sign</span></span>
- <span data-ttu-id="71ef0-208">Подтвержда</span><span class="sxs-lookup"><span data-stu-id="71ef0-208">Verify</span></span>

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

### <span data-ttu-id="71ef0-209">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="71ef0-209">-Name</span></span>
<span data-ttu-id="71ef0-210">Задает имя ключа, который нужно добавить в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="71ef0-210">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="71ef0-211">Этот командлет создает полное доменное имя (FQDN) ключа на основе имени, которое указывает этот параметр, имя хранилища ключей и текущую среду.</span><span class="sxs-lookup"><span data-stu-id="71ef0-211">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="71ef0-212">Имя должно быть строкой из 1 – 63 знаков длиной, содержащей только 0-9, a-z, A-Z и (дефис).</span><span class="sxs-lookup"><span data-stu-id="71ef0-212">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

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

### <span data-ttu-id="71ef0-213">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="71ef0-213">-NotBefore</span></span>
<span data-ttu-id="71ef0-214">Указывает время в виде объекта **DateTime** , до которого невозможно использовать клавишу.</span><span class="sxs-lookup"><span data-stu-id="71ef0-214">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="71ef0-215">Этот параметр использует время в формате UTC.</span><span class="sxs-lookup"><span data-stu-id="71ef0-215">This parameter uses UTC.</span></span> <span data-ttu-id="71ef0-216">Чтобы получить объект **DateTime** , используйте командлет **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="71ef0-216">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="71ef0-217">Если этот параметр не указан, клавишу можно использовать сразу.</span><span class="sxs-lookup"><span data-stu-id="71ef0-217">If you do not specify this parameter, the key can be used immediately.</span></span>

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

### <span data-ttu-id="71ef0-218">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="71ef0-218">-ResourceId</span></span>
<span data-ttu-id="71ef0-219">Идентификатор ресурса хранилища.</span><span class="sxs-lookup"><span data-stu-id="71ef0-219">Vault Resource Id.</span></span>

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

### <span data-ttu-id="71ef0-220">-Size</span><span class="sxs-lookup"><span data-stu-id="71ef0-220">-Size</span></span>
<span data-ttu-id="71ef0-221">Размер ключа RSA в битах.</span><span class="sxs-lookup"><span data-stu-id="71ef0-221">RSA key size, in bits.</span></span> <span data-ttu-id="71ef0-222">Если он не указан, служба обеспечивает безопасность по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="71ef0-222">If not specified, the service will provide a safe default.</span></span>

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

### <span data-ttu-id="71ef0-223">-Тег</span><span class="sxs-lookup"><span data-stu-id="71ef0-223">-Tag</span></span>
<span data-ttu-id="71ef0-224">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="71ef0-224">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="71ef0-225">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="71ef0-225">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="71ef0-226">-VaultName</span><span class="sxs-lookup"><span data-stu-id="71ef0-226">-VaultName</span></span>
<span data-ttu-id="71ef0-227">Указывает имя хранилища ключей, к которому этот командлет добавляет ключ.</span><span class="sxs-lookup"><span data-stu-id="71ef0-227">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="71ef0-228">Этот командлет создает полное доменное имя хранилища ключей, основываясь на имени, указанном этим параметром, и текущей среде.</span><span class="sxs-lookup"><span data-stu-id="71ef0-228">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="71ef0-229">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71ef0-229">-Confirm</span></span>
<span data-ttu-id="71ef0-230">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="71ef0-230">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71ef0-231">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71ef0-231">-WhatIf</span></span>
<span data-ttu-id="71ef0-232">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="71ef0-232">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71ef0-233">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="71ef0-233">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71ef0-234">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71ef0-234">CommonParameters</span></span>
<span data-ttu-id="71ef0-235">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="71ef0-235">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71ef0-236">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71ef0-236">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71ef0-237">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="71ef0-237">INPUTS</span></span>

### <span data-ttu-id="71ef0-238">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="71ef0-238">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="71ef0-239">Параметры: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="71ef0-239">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="71ef0-240">System. String</span><span class="sxs-lookup"><span data-stu-id="71ef0-240">System.String</span></span>

## <span data-ttu-id="71ef0-241">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="71ef0-241">OUTPUTS</span></span>

### <span data-ttu-id="71ef0-242">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="71ef0-242">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="71ef0-243">Пуск</span><span class="sxs-lookup"><span data-stu-id="71ef0-243">NOTES</span></span>

## <span data-ttu-id="71ef0-244">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="71ef0-244">RELATED LINKS</span></span>

[<span data-ttu-id="71ef0-245">Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="71ef0-245">Backup-AzureKeyVaultKey</span></span>](./Backup-AzureKeyVaultKey.md)

[<span data-ttu-id="71ef0-246">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="71ef0-246">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="71ef0-247">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="71ef0-247">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="71ef0-248">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="71ef0-248">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)
