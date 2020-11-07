---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: 28f4550ac850b7bcc5bab4c90ec510128a8e2ab0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912741"
---
# <span data-ttu-id="770cc-101">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="770cc-101">Backup-AzKeyVaultKey</span></span>

## <span data-ttu-id="770cc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="770cc-102">SYNOPSIS</span></span>
<span data-ttu-id="770cc-103">Резервное копирование ключа в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="770cc-103">Backs up a key in a key vault.</span></span>

## <span data-ttu-id="770cc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="770cc-104">SYNTAX</span></span>

### <span data-ttu-id="770cc-105">ByKeyName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="770cc-105">ByKeyName (Default)</span></span>
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="770cc-106">ByKey</span><span class="sxs-lookup"><span data-stu-id="770cc-106">ByKey</span></span>
```
Backup-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="770cc-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="770cc-107">DESCRIPTION</span></span>
<span data-ttu-id="770cc-108">Командлет **BACKUP-AzKeyVaultKey** используется для резервного копирования указанного ключа в хранилище ключей, загружая его и сохраняя в файле.</span><span class="sxs-lookup"><span data-stu-id="770cc-108">The **Backup-AzKeyVaultKey** cmdlet backs up a specified key in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="770cc-109">Если вы используете несколько версий ключа, в резервную копию включаются все версии.</span><span class="sxs-lookup"><span data-stu-id="770cc-109">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="770cc-110">Поскольку загруженное содержимое зашифровано, оно не может использоваться за пределами хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="770cc-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="770cc-111">Вы можете восстановить резервную копию ключа в любом хранилище ключей в подписке, из которой она была создана.</span><span class="sxs-lookup"><span data-stu-id="770cc-111">You can restore a backed-up key to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="770cc-112">Ниже приведены основные причины использования этого командлета.</span><span class="sxs-lookup"><span data-stu-id="770cc-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="770cc-113">Вы хотите пополнить свою копию ключа, чтобы иметь возможность использовать автономную копию на случай, если вы случайно удалили ключ в своем вашем хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="770cc-113">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your key vault.</span></span>
 
- <span data-ttu-id="770cc-114">Вы создали ключ с помощью ключевого хранилища, и теперь хотите клонировать ключ в другой регион Azure, чтобы его можно было использовать из всех экземпляров распределенного приложения.</span><span class="sxs-lookup"><span data-stu-id="770cc-114">You created a key using Key Vault and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="770cc-115">С помощью командлета **BACKUP-AzKeyVaultKey** можно получить ключ в зашифрованном формате, а затем воспользоваться командлетом Restore-AzKeyVaultKey и указать в качестве него ключевое хранилище во втором регионе.</span><span class="sxs-lookup"><span data-stu-id="770cc-115">Use the **Backup-AzKeyVaultKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzKeyVaultKey cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="770cc-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="770cc-116">EXAMPLES</span></span>

### <span data-ttu-id="770cc-117">Пример 1: создание резервной копии ключа с автоматически сгенерированным именем файла</span><span class="sxs-lookup"><span data-stu-id="770cc-117">Example 1: Back up a key with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'

C:\Users\username\mykeyvault-mykey-1527029447.01191
```

<span data-ttu-id="770cc-118">Эта команда извлекает ключ с именем MyKey из хранилища ключей с именем MyKeyVault и сохраняет резервную копию этого ключа в файле с автоматическим именем и выводит имя файла.</span><span class="sxs-lookup"><span data-stu-id="770cc-118">This command retrieves the key named MyKey from the key vault named MyKeyVault and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="770cc-119">Пример 2: создание резервной копии ключа для указанного имени файла</span><span class="sxs-lookup"><span data-stu-id="770cc-119">Example 2: Back up a key to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="770cc-120">Эта команда извлекает ключ с именем MyKey из ключа vaultnamed MyKeyVault и сохраняет резервную копию этого ключа в файл с именем Backup. BLOB.</span><span class="sxs-lookup"><span data-stu-id="770cc-120">This command retrieves the key named MyKey from the key vaultnamed MyKeyVault and saves a backup of that key to a file named Backup.blob.</span></span>

### <span data-ttu-id="770cc-121">Пример 3: создание резервной копии ранее полученного ключа в указанном файле, перезапись файла назначения без запроса.</span><span class="sxs-lookup"><span data-stu-id="770cc-121">Example 3: Back up a previously retrieved key to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\> Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="770cc-122">Эта команда создает резервную копию ключа с именем $key. Имя в хранилище с именем $key. VaultName файл с именем Backup. BLOB, перезапись файла без уведомления, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="770cc-122">This command creates a backup of the key named $key.Name in the vault named $key.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="770cc-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="770cc-123">PARAMETERS</span></span>

### <span data-ttu-id="770cc-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="770cc-124">-DefaultProfile</span></span>
<span data-ttu-id="770cc-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="770cc-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="770cc-126">-Force</span><span class="sxs-lookup"><span data-stu-id="770cc-126">-Force</span></span>
<span data-ttu-id="770cc-127">Перезаписать заданный файл, если он существует</span><span class="sxs-lookup"><span data-stu-id="770cc-127">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="770cc-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="770cc-128">-InputObject</span></span>
<span data-ttu-id="770cc-129">Набор ключей для резервного копирования, конвейера из выходных данных вызова.</span><span class="sxs-lookup"><span data-stu-id="770cc-129">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByKey
Aliases: Key

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="770cc-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="770cc-130">-Name</span></span>
<span data-ttu-id="770cc-131">Задает имя ключа для резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="770cc-131">Specifies the name of the key to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770cc-132">-Выходной_файл</span><span class="sxs-lookup"><span data-stu-id="770cc-132">-OutputFile</span></span>
<span data-ttu-id="770cc-133">Указывает выходной файл, в котором хранится резервная копия (BLOB-объект).</span><span class="sxs-lookup"><span data-stu-id="770cc-133">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="770cc-134">Если этот параметр не указан, этот командлет создаст имя файла.</span><span class="sxs-lookup"><span data-stu-id="770cc-134">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="770cc-135">Если вы задаете имя существующего выходного файла, операция не завершится и вернет сообщение об ошибке, в котором файл резервной копии уже существует.</span><span class="sxs-lookup"><span data-stu-id="770cc-135">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="770cc-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="770cc-136">-VaultName</span></span>
<span data-ttu-id="770cc-137">Указывает имя хранилища ключей, содержащего ключ для резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="770cc-137">Specifies the name of the key vault that contains the key to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="770cc-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="770cc-138">-Confirm</span></span>
<span data-ttu-id="770cc-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="770cc-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="770cc-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="770cc-140">-WhatIf</span></span>
<span data-ttu-id="770cc-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="770cc-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="770cc-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="770cc-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="770cc-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="770cc-143">CommonParameters</span></span>
<span data-ttu-id="770cc-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="770cc-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="770cc-145">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="770cc-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="770cc-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="770cc-146">INPUTS</span></span>

### <span data-ttu-id="770cc-147">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="770cc-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="770cc-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="770cc-148">OUTPUTS</span></span>

### <span data-ttu-id="770cc-149">System. String</span><span class="sxs-lookup"><span data-stu-id="770cc-149">System.String</span></span>

## <span data-ttu-id="770cc-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="770cc-150">NOTES</span></span>

## <span data-ttu-id="770cc-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="770cc-151">RELATED LINKS</span></span>

[<span data-ttu-id="770cc-152">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="770cc-152">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="770cc-153">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="770cc-153">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="770cc-154">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="770cc-154">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="770cc-155">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="770cc-155">Restore-AzKeyVaultKey</span></span>](./Restore-AzKeyVaultKey.md)

