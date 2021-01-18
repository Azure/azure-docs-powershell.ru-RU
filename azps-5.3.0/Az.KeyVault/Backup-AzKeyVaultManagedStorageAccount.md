---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultmanagedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultManagedStorageAccount.md
ms.openlocfilehash: c01d07f9408804b229921394c24e444b2a4deb8b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98518358"
---
# <span data-ttu-id="85c1c-101">Backup-AzKeyVaultManagedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="85c1c-101">Backup-AzKeyVaultManagedStorageAccount</span></span>

## <span data-ttu-id="85c1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="85c1c-103">Backs up a KeyVault-managed storage account.</span><span class="sxs-lookup"><span data-stu-id="85c1c-103">Backs up a KeyVault-managed storage account.</span></span>

## <span data-ttu-id="85c1c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="85c1c-104">SYNTAX</span></span>

### <span data-ttu-id="85c1c-105">ByStorageAccountName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="85c1c-105">ByStorageAccountName (Default)</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85c1c-106">ByStorageAccount</span><span class="sxs-lookup"><span data-stu-id="85c1c-106">ByStorageAccount</span></span>
```
Backup-AzKeyVaultManagedStorageAccount [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [[-OutputFile] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="85c1c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="85c1c-107">DESCRIPTION</span></span>
<span data-ttu-id="85c1c-108">С **помощью cmdlet Backup-AzKeyVaultManagedStorageAccount** можно создать резервную копию указанной учетной записи управляемого хранилища в хранилище ключа, скачав ее и храня в файле.</span><span class="sxs-lookup"><span data-stu-id="85c1c-108">The **Backup-AzKeyVaultManagedStorageAccount** cmdlet backs up a specified managed storage account in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="85c1c-109">Так как скачаное содержимое зашифровано, его невозможно использовать за пределами хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="85c1c-109">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="85c1c-110">Вы можете восстановить запасную учетную запись хранения в любом хранилище ключей в подписке, из какой подписки она была, если хранилище находится в той же географической области Azure.</span><span class="sxs-lookup"><span data-stu-id="85c1c-110">You can restore a backed-up storage account to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="85c1c-111">Этот cmdlet обычно используется по одной из причин:</span><span class="sxs-lookup"><span data-stu-id="85c1c-111">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="85c1c-112">Вы хотите сохранить автономный экземпляр учетной записи хранения на случай случайного удаления оригинала из хранилища.</span><span class="sxs-lookup"><span data-stu-id="85c1c-112">You want to retain an offline copy of the storage account in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="85c1c-113">Вы создали учетную запись хранения с помощью хранилища ключей и хотите клонировать объект в другой регион Azure, чтобы его можно было использовать из всех экземпляров распределенного приложения.</span><span class="sxs-lookup"><span data-stu-id="85c1c-113">You created a managed storage account using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="85c1c-114">Используйте cmdlet **Backup-AzKeyVaultManagedStorageAccount** для получения учетной записи управляемого хранилища в зашифрованном формате, а затем используйте **cmdlet Restore-AzKeyVaultManagedStorageAccount** и укажите ключевое хранилище во втором регионе.</span><span class="sxs-lookup"><span data-stu-id="85c1c-114">Use the **Backup-AzKeyVaultManagedStorageAccount** cmdlet to retrieve the managed storage account in encrypted format and then use the **Restore-AzKeyVaultManagedStorageAccount** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="85c1c-115">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="85c1c-115">EXAMPLES</span></span>

### <span data-ttu-id="85c1c-116">Пример 1. Архивная запись управляемого хранилища с автоматически созданным именем файла</span><span class="sxs-lookup"><span data-stu-id="85c1c-116">Example 1: Back up a managed storage account with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'

C:\Users\username\mykeyvault-mymsak-1527029447.01191
```

<span data-ttu-id="85c1c-117">Эта команда извлекает учетную запись управляемого хранилища MyMSAK из ключного хранилища MyKeyVault и сохраняет резервную копию этой учетной записи хранения в файл, который автоматически именуется вам, и отображает имя файла.</span><span class="sxs-lookup"><span data-stu-id="85c1c-117">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="85c1c-118">Пример 2. Архивная запись управляемого хранилища с указанным именем файла</span><span class="sxs-lookup"><span data-stu-id="85c1c-118">Example 2: Back up a managed storage account to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyMSAK' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="85c1c-119">Эта команда извлекает учетную запись управляемого хранилища MyMSAK из ключного хранилища MyKeyVault и сохраняет ее резервную копию в файл Backup.blob.</span><span class="sxs-lookup"><span data-stu-id="85c1c-119">This command retrieves the managed storage account named MyMSAK from the key vault named MyKeyVault and saves a backup of that managed storage account to a file named Backup.blob.</span></span>

### <span data-ttu-id="85c1c-120">Пример 3. Архивная копия ранее восстановленной учетной записи управляемого хранилища на указанное имя файла, переописав файл назначения без запроса.</span><span class="sxs-lookup"><span data-stu-id="85c1c-120">Example 3: Back up a previously retrieved managed storage account to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $msak = Get-AzKeyVaultManagedStorageAccount -VaultName 'MyKeyVault' -Name 'MyMSAK'
PS C:\> Backup-AzKeyVaultManagedStorageAccount -StorageAccount $msak -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="85c1c-121">Эта команда создает резервную копию управляемой учетной записи хранения с именем $msak. Имя в хранилище с именем $msak. VaultName в файл Backup.blob, автоматически переописав файл, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="85c1c-121">This command creates a backup of the managed storage account named $msak.Name in the vault named $msak.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="85c1c-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85c1c-122">PARAMETERS</span></span>

### <span data-ttu-id="85c1c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85c1c-123">-DefaultProfile</span></span>
<span data-ttu-id="85c1c-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="85c1c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85c1c-125">-Force</span><span class="sxs-lookup"><span data-stu-id="85c1c-125">-Force</span></span>
<span data-ttu-id="85c1c-126">Переописывать файл, если он существует</span><span class="sxs-lookup"><span data-stu-id="85c1c-126">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="85c1c-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85c1c-127">-InputObject</span></span>
<span data-ttu-id="85c1c-128">Пакет учетной записи хранения, который будет иметь запас, который будет совсююстрироваться с учетом результатов ирисовки звонка.</span><span class="sxs-lookup"><span data-stu-id="85c1c-128">Storage account bundle to be backed up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="85c1c-129">-Name</span><span class="sxs-lookup"><span data-stu-id="85c1c-129">-Name</span></span>
<span data-ttu-id="85c1c-130">Секретное имя.</span><span class="sxs-lookup"><span data-stu-id="85c1c-130">Secret name.</span></span>
<span data-ttu-id="85c1c-131">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span><span class="sxs-lookup"><span data-stu-id="85c1c-131">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="85c1c-132">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="85c1c-132">-OutputFile</span></span>
<span data-ttu-id="85c1c-133">Выходной файл.</span><span class="sxs-lookup"><span data-stu-id="85c1c-133">Output file.</span></span>
<span data-ttu-id="85c1c-134">Выходной файл для хранения резервной копии учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="85c1c-134">The output file to store the storage account backup.</span></span>
<span data-ttu-id="85c1c-135">Если он не задан, будет сгенерировано имя файла по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="85c1c-135">If not specified, a default filename will be generated.</span></span>

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

### <span data-ttu-id="85c1c-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="85c1c-136">-VaultName</span></span>
<span data-ttu-id="85c1c-137">Имя сейфа.</span><span class="sxs-lookup"><span data-stu-id="85c1c-137">Vault name.</span></span>
<span data-ttu-id="85c1c-138">С его учетом именем и выбранной средой строится FQDN хранилища.</span><span class="sxs-lookup"><span data-stu-id="85c1c-138">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="85c1c-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85c1c-139">-Confirm</span></span>
<span data-ttu-id="85c1c-140">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85c1c-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85c1c-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85c1c-141">-WhatIf</span></span>
<span data-ttu-id="85c1c-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85c1c-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85c1c-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="85c1c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85c1c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85c1c-144">CommonParameters</span></span>
<span data-ttu-id="85c1c-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85c1c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85c1c-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85c1c-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85c1c-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="85c1c-147">INPUTS</span></span>

### <span data-ttu-id="85c1c-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="85c1c-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="85c1c-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="85c1c-149">OUTPUTS</span></span>

### <span data-ttu-id="85c1c-150">System.String</span><span class="sxs-lookup"><span data-stu-id="85c1c-150">System.String</span></span>

## <span data-ttu-id="85c1c-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="85c1c-151">NOTES</span></span>

## <span data-ttu-id="85c1c-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="85c1c-152">RELATED LINKS</span></span>
