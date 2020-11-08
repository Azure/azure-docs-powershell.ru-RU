---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c01d07f9408804b229921394c24e444b2a4deb8b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245322"
---
# <span data-ttu-id="c1eae-101">Backup-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c1eae-101">Backup-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="c1eae-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c1eae-102">SYNOPSIS</span></span>
<span data-ttu-id="c1eae-103">Создание резервной копии управляемой учетной записи хранения KeyVault.</span><span class="sxs-lookup"><span data-stu-id="c1eae-103">Backs up a KeyVault-managed storage account.</span></span>

## <span data-ttu-id="c1eae-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c1eae-104">SYNTAX</span></span>

### <span data-ttu-id="c1eae-105">ByStorageAccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c1eae-105">ByStorageAccountName (Default)</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1eae-106">ByStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c1eae-106">ByStorageAccount</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1eae-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1eae-107">DESCRIPTION</span></span>
<span data-ttu-id="c1eae-108">Командлет **BACKUP-AzKeyVaultManagedStorageAccount** используется для резервного копирования указанной управляемой учетной записи хранения в хранилище ключей, загружая ее и сохраняя в файле.</span><span class="sxs-lookup"><span data-stu-id="c1eae-108">The **Backup-AzKeyVaultManagedStorageAccount** cmdlet backs up a specified managed storage account in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="c1eae-109">Поскольку загруженное содержимое зашифровано, оно не может использоваться за пределами хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="c1eae-109">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="c1eae-110">Вы можете восстановить резервную учетную запись хранения в любом хранилище ключей в подписке, в которой она была создана из резервной копии, если она находится в том же географическом элементе Azure.</span><span class="sxs-lookup"><span data-stu-id="c1eae-110">You can restore a backed-up storage account to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="c1eae-111">Ниже приведены основные причины использования этого командлета.</span><span class="sxs-lookup"><span data-stu-id="c1eae-111">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="c1eae-112">Вы хотите сохранить автономную копию учетной записи хранения на случай, если вы случайно удалили оригинал из хранилища.</span><span class="sxs-lookup"><span data-stu-id="c1eae-112">You want to retain an offline copy of the storage account in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="c1eae-113">Вы создали управляемую учетную запись хранения с помощью ключа Vault и теперь хотите клонировать объект в другой регион Azure, чтобы его можно было использовать из всех экземпляров распределенного приложения.</span><span class="sxs-lookup"><span data-stu-id="c1eae-113">You created a managed storage account using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="c1eae-114">С помощью командлета **BACKUP-AzKeyVaultManagedStorageAccount** можно получить управляемую учетную запись хранения в зашифрованном формате, а затем использовать командлет **RESTORE-AzKeyVaultManagedStorageAccount** и указав ключевое хранилище во втором регионе.</span><span class="sxs-lookup"><span data-stu-id="c1eae-114">Use the **Backup-AzKeyVaultManagedStorageAccount** cmdlet to retrieve the managed storage account in encrypted format and then use the **Restore-AzKeyVaultManagedStorageAccount** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="c1eae-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c1eae-115">EXAMPLES</span></span>

### <span data-ttu-id="c1eae-116">Пример 1: создание резервной копии управляемой учетной записи хранения с автоматически созданным именем файла</span><span class="sxs-lookup"><span data-stu-id="c1eae-116">Example 1: Back up a managed storage account with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

<span data-ttu-id="c1eae-117">Эта команда извлекает управляемую учетную запись хранения с именем MyMSAK из хранилища ключей с именем MyKeyVault и сохраняет резервную копию этой управляемой учетной записи хранения в файле с автоматическим именем и выводит имя файла.</span><span class="sxs-lookup"><span data-stu-id="c1eae-117">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="c1eae-118">Пример 2: создание резервной копии управляемой учетной записи хранения в указанном имени файла</span><span class="sxs-lookup"><span data-stu-id="c1eae-118">Example 2: Back up a managed storage account to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="c1eae-119">Эта команда извлекает управляемую учетную запись хранения с именем MyMSAK из хранилища ключей с именем MyKeyVault и сохраняет резервную копию этой управляемой учетной записи хранения в файле с именем Backup. BLOB.</span><span class="sxs-lookup"><span data-stu-id="c1eae-119">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file named Backup.blob.</span></span>

### <span data-ttu-id="c1eae-120">Пример 3: создание резервной копии ранее полученной управляемой учетной записи хранения в указанном имени файла с перезазаписьм конечного файла без запроса.</span><span class="sxs-lookup"><span data-stu-id="c1eae-120">Example 3: Back up a previously retrieved managed storage account to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $msak = Get-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="c1eae-121">Эта команда создает резервную копию управляемой учетной записи хранения с именем $msak. Имя в хранилище с именем $msak. VaultName файл с именем Backup. BLOB, перезапись файла без уведомления, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="c1eae-121">This command creates a backup of the managed storage account named $msak.Name in the vault named $msak.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="c1eae-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c1eae-122">PARAMETERS</span></span>

### <span data-ttu-id="c1eae-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1eae-123">-DefaultProfile</span></span>
<span data-ttu-id="c1eae-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c1eae-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1eae-125">-Force</span><span class="sxs-lookup"><span data-stu-id="c1eae-125">-Force</span></span>
<span data-ttu-id="c1eae-126">Перезаписать заданный файл, если он существует</span><span class="sxs-lookup"><span data-stu-id="c1eae-126">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="c1eae-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1eae-127">-InputObject</span></span>
<span data-ttu-id="c1eae-128">Набор учетных записей хранилища для резервного копирования, конвейера, из результатов запроса на получение.</span><span class="sxs-lookup"><span data-stu-id="c1eae-128">Storage account bundle to be backed up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByStorageAccount
Aliases: StorageAccount

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1eae-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c1eae-129">-Name</span></span>
<span data-ttu-id="c1eae-130">Имя секрета.</span><span class="sxs-lookup"><span data-stu-id="c1eae-130">Secret name.</span></span>
<span data-ttu-id="c1eae-131">Командлет создает полное доменное имя секрета из имени хранилища, выбранного в настоящее время среды и имени секрета.</span><span class="sxs-lookup"><span data-stu-id="c1eae-131">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1eae-132">-Выходной_файл</span><span class="sxs-lookup"><span data-stu-id="c1eae-132">-OutputFile</span></span>
<span data-ttu-id="c1eae-133">Выходной файл.</span><span class="sxs-lookup"><span data-stu-id="c1eae-133">Output file.</span></span>
<span data-ttu-id="c1eae-134">Выходной файл для хранения резервной копии учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="c1eae-134">The output file to store the storage account backup.</span></span>
<span data-ttu-id="c1eae-135">Если не указано, будет создано имя файла по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c1eae-135">If not specified, a default filename will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1eae-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c1eae-136">-VaultName</span></span>
<span data-ttu-id="c1eae-137">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="c1eae-137">Vault name.</span></span>
<span data-ttu-id="c1eae-138">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="c1eae-138">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByStorageAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1eae-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1eae-139">-Confirm</span></span>
<span data-ttu-id="c1eae-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c1eae-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1eae-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1eae-141">-WhatIf</span></span>
<span data-ttu-id="c1eae-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c1eae-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1eae-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c1eae-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1eae-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1eae-144">CommonParameters</span></span>
<span data-ttu-id="c1eae-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c1eae-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1eae-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c1eae-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1eae-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c1eae-147">INPUTS</span></span>

### <span data-ttu-id="c1eae-148">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="c1eae-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="c1eae-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1eae-149">OUTPUTS</span></span>

### <span data-ttu-id="c1eae-150">System. String</span><span class="sxs-lookup"><span data-stu-id="c1eae-150">System.String</span></span>

## <span data-ttu-id="c1eae-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="c1eae-151">NOTES</span></span>

## <span data-ttu-id="c1eae-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c1eae-152">RELATED LINKS</span></span>
