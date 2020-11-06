---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultKey.md
ms.openlocfilehash: 2eecb6d4bb069b1578b3080c04de4c9df1e42f09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561771"
---
# <span data-ttu-id="cef59-101">Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cef59-101">Backup-AzureKeyVaultKey</span></span>

## <span data-ttu-id="cef59-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cef59-102">SYNOPSIS</span></span>
<span data-ttu-id="cef59-103">Резервное копирование ключа в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="cef59-103">Backs up a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cef59-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cef59-104">SYNTAX</span></span>

### <span data-ttu-id="cef59-105">ByKeyName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cef59-105">ByKeyName (Default)</span></span>
```
Backup-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cef59-106">ByKey</span><span class="sxs-lookup"><span data-stu-id="cef59-106">ByKey</span></span>
```
Backup-AzureKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cef59-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cef59-107">DESCRIPTION</span></span>
<span data-ttu-id="cef59-108">Командлет **BACKUP-AzureKeyVaultKey** используется для резервного копирования указанного ключа в хранилище ключей, загружая его и сохраняя в файле.</span><span class="sxs-lookup"><span data-stu-id="cef59-108">The **Backup-AzureKeyVaultKey** cmdlet backs up a specified key in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="cef59-109">Если вы используете несколько версий ключа, в резервную копию включаются все версии.</span><span class="sxs-lookup"><span data-stu-id="cef59-109">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="cef59-110">Поскольку загруженное содержимое зашифровано, оно не может использоваться за пределами хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="cef59-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="cef59-111">Вы можете восстановить резервную копию ключа в любом хранилище ключей в подписке, из которой она была создана.</span><span class="sxs-lookup"><span data-stu-id="cef59-111">You can restore a backed-up key to any key vault in the subscription that it was backed up from.</span></span>

<span data-ttu-id="cef59-112">Ниже приведены основные причины использования этого командлета.</span><span class="sxs-lookup"><span data-stu-id="cef59-112">Typical reasons to use this cmdlet are:</span></span> 

- <span data-ttu-id="cef59-113">Вы хотите пополнить свою копию ключа, чтобы иметь возможность использовать автономную копию на случай, если вы случайно удалили ключ в своем вашем хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="cef59-113">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your key vault.</span></span>
 
- <span data-ttu-id="cef59-114">Вы создали ключ с помощью ключевого хранилища, и теперь хотите клонировать ключ в другой регион Azure, чтобы его можно было использовать из всех экземпляров распределенного приложения.</span><span class="sxs-lookup"><span data-stu-id="cef59-114">You created a key using Key Vault and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="cef59-115">С помощью командлета **BACKUP-AzureKeyVaultKey** можно получить ключ в зашифрованном формате, а затем воспользоваться командлетом Restore-AzureKeyVaultKey и указать в качестве него ключевое хранилище во втором регионе.</span><span class="sxs-lookup"><span data-stu-id="cef59-115">Use the **Backup-AzureKeyVaultKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzureKeyVaultKey cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="cef59-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cef59-116">EXAMPLES</span></span>

### <span data-ttu-id="cef59-117">Пример 1: создание резервной копии ключа с автоматически сгенерированным именем файла</span><span class="sxs-lookup"><span data-stu-id="cef59-117">Example 1: Back up a key with an automatically generated file name</span></span>
```
PS C:\>Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="cef59-118">Эта команда извлекает ключ с именем MyKey из хранилища ключей с именем MyKeyVault и сохраняет резервную копию этого ключа в файле с автоматическим именем и выводит имя файла.</span><span class="sxs-lookup"><span data-stu-id="cef59-118">This command retrieves the key named MyKey from the key vault named MyKeyVault and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="cef59-119">Пример 2: создание резервной копии ключа для указанного имени файла</span><span class="sxs-lookup"><span data-stu-id="cef59-119">Example 2: Back up a key to a specified file name</span></span>
```
PS C:\>Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'
```

<span data-ttu-id="cef59-120">Эта команда извлекает ключ с именем MyKey из ключа vaultnamed MyKeyVault и сохраняет резервную копию этого ключа в файл с именем Backup. BLOB.</span><span class="sxs-lookup"><span data-stu-id="cef59-120">This command retrieves the key named MyKey from the key vaultnamed MyKeyVault and saves a backup of that key to a file named Backup.blob.</span></span>

### <span data-ttu-id="cef59-121">Пример 3: создание резервной копии ранее полученного ключа в указанном файле, перезапись файла назначения без запроса.</span><span class="sxs-lookup"><span data-stu-id="cef59-121">Example 3: Back up a previously retrieved key to a specified file name, overwriting the destination file without prompting.</span></span>
```
PS C:\>$key = Get-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\>Backup-AzureKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force
```

<span data-ttu-id="cef59-122">Эта команда создает резервную копию ключа с именем $key. Имя в хранилище с именем $key. VaultName файл с именем Backup. BLOB, перезапись файла без уведомления, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="cef59-122">This command creates a backup of the key named $key.Name in the vault named $key.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="cef59-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cef59-123">PARAMETERS</span></span>

### <span data-ttu-id="cef59-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cef59-124">-DefaultProfile</span></span>
<span data-ttu-id="cef59-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="cef59-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cef59-126">-Force</span><span class="sxs-lookup"><span data-stu-id="cef59-126">-Force</span></span>
<span data-ttu-id="cef59-127">Перезаписать заданный файл, если он существует</span><span class="sxs-lookup"><span data-stu-id="cef59-127">Overwrite the given file if it exists</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cef59-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cef59-128">-InputObject</span></span>
<span data-ttu-id="cef59-129">Набор ключей для резервного копирования, конвейера из выходных данных вызова.</span><span class="sxs-lookup"><span data-stu-id="cef59-129">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: PSKeyVaultKeyIdentityItem
Parameter Sets: ByKey
Aliases: Key

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cef59-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cef59-130">-Name</span></span>
<span data-ttu-id="cef59-131">Задает имя ключа для резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="cef59-131">Specifies the name of the key to back up.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cef59-132">-Выходной_файл</span><span class="sxs-lookup"><span data-stu-id="cef59-132">-OutputFile</span></span>
<span data-ttu-id="cef59-133">Указывает выходной файл, в котором хранится резервная копия (BLOB-объект).</span><span class="sxs-lookup"><span data-stu-id="cef59-133">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="cef59-134">Если этот параметр не указан, этот командлет создаст имя файла.</span><span class="sxs-lookup"><span data-stu-id="cef59-134">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="cef59-135">Если вы задаете имя существующего выходного файла, операция не завершится и вернет сообщение об ошибке, в котором файл резервной копии уже существует.</span><span class="sxs-lookup"><span data-stu-id="cef59-135">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cef59-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="cef59-136">-VaultName</span></span>
<span data-ttu-id="cef59-137">Указывает имя хранилища ключей, содержащего ключ для резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="cef59-137">Specifies the name of the key vault that contains the key to back up.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cef59-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cef59-138">-Confirm</span></span>
<span data-ttu-id="cef59-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cef59-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cef59-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cef59-140">-WhatIf</span></span>
<span data-ttu-id="cef59-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cef59-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cef59-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cef59-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cef59-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cef59-143">CommonParameters</span></span>
<span data-ttu-id="cef59-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cef59-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cef59-145">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cef59-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cef59-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cef59-146">INPUTS</span></span>

### <span data-ttu-id="cef59-147">Ничего</span><span class="sxs-lookup"><span data-stu-id="cef59-147">None</span></span>
<span data-ttu-id="cef59-148">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="cef59-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cef59-149">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cef59-149">OUTPUTS</span></span>

### <span data-ttu-id="cef59-150">Подстрок</span><span class="sxs-lookup"><span data-stu-id="cef59-150">String</span></span>
<span data-ttu-id="cef59-151">Командлет возвращает путь к выходному файлу, содержащему резервную копию ключа.</span><span class="sxs-lookup"><span data-stu-id="cef59-151">The cmdlet returns the path of the output file containing the backup of the key.</span></span>

## <span data-ttu-id="cef59-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="cef59-152">NOTES</span></span>

## <span data-ttu-id="cef59-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cef59-153">RELATED LINKS</span></span>

[<span data-ttu-id="cef59-154">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cef59-154">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="cef59-155">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cef59-155">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="cef59-156">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cef59-156">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="cef59-157">Restore-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cef59-157">Restore-AzureKeyVaultKey</span></span>](./Restore-AzureKeyVaultKey.md)

