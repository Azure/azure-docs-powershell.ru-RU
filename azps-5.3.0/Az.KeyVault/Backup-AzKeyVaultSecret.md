---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
ms.openlocfilehash: a171f967a937873b85adcfca732987037e6db0a6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425855"
---
# <span data-ttu-id="c4844-101">Backup-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c4844-101">Backup-AzKeyVaultSecret</span></span>

## <span data-ttu-id="c4844-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4844-102">SYNOPSIS</span></span>
<span data-ttu-id="c4844-103">Backs up a secret in a key vault.</span><span class="sxs-lookup"><span data-stu-id="c4844-103">Backs up a secret in a key vault.</span></span>

## <span data-ttu-id="c4844-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c4844-104">SYNTAX</span></span>

### <span data-ttu-id="c4844-105">BySecretName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c4844-105">BySecretName (Default)</span></span>
```
Backup-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4844-106">BySecret</span><span class="sxs-lookup"><span data-stu-id="c4844-106">BySecret</span></span>
```
Backup-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4844-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4844-107">DESCRIPTION</span></span>
<span data-ttu-id="c4844-108">С **помощью cmdlet Backup-AzKeyVaultSecret** можно вернуть указанный секрет в хранилище ключей, скачав его и храня в файле.</span><span class="sxs-lookup"><span data-stu-id="c4844-108">The **Backup-AzKeyVaultSecret** cmdlet backs up a specified secret in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="c4844-109">Если существует несколько версий секрета, в резервную копию включаются все версии.</span><span class="sxs-lookup"><span data-stu-id="c4844-109">If there are multiple versions of the secret, all versions are included in the backup.</span></span>
<span data-ttu-id="c4844-110">Так как скачаное содержимое зашифровано, его невозможно использовать за пределами хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="c4844-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="c4844-111">Вы можете восстановить скрытую секретную фигуру в любом хранилище ключей в подписке, из какой подписки она была.</span><span class="sxs-lookup"><span data-stu-id="c4844-111">You can restore a backed-up secret to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="c4844-112">Этот cmdlet обычно используется по одной из причин:</span><span class="sxs-lookup"><span data-stu-id="c4844-112">Typical reasons to use this cmdlet are:</span></span>
- <span data-ttu-id="c4844-113">Вы хотите escrow a copy of your secret, so that you have anfline copy in case you accidentally delete your secret in your key vault.</span><span class="sxs-lookup"><span data-stu-id="c4844-113">You want to escrow a copy of your secret, so that you have an offline copy in case you accidentally delete your secret in your key vault.</span></span>
- <span data-ttu-id="c4844-114">Вы добавили секрет в хранилище ключей и хотите клонировать его в другой регион Azure, чтобы использовать его из всех экземпляров распределенного приложения.</span><span class="sxs-lookup"><span data-stu-id="c4844-114">You added a secret to a key vault and now want to clone the secret into a different Azure region, so that you can use it from all instances of your distributed application.</span></span> <span data-ttu-id="c4844-115">Используйте Backup-AzKeyVaultSecret для извлечения секрета в зашифрованном формате, а затем используйте Restore-AzKeyVaultSecret и укажите хранилище ключей во второй области.</span><span class="sxs-lookup"><span data-stu-id="c4844-115">Use the Backup-AzKeyVaultSecret cmdlet to retrieve the secret in encrypted format and then use the Restore-AzKeyVaultSecret cmdlet and specify a key vault in the second region.</span></span> <span data-ttu-id="c4844-116">(Обратите внимание, что регионы должны принадлежать к одному географическому региону.)</span><span class="sxs-lookup"><span data-stu-id="c4844-116">(Note that the regions must belong to the same geography.)</span></span>

## <span data-ttu-id="c4844-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c4844-117">EXAMPLES</span></span>

### <span data-ttu-id="c4844-118">Пример 1. Архивная система секретов с автоматически созданным именем файла</span><span class="sxs-lookup"><span data-stu-id="c4844-118">Example 1: Back up a secret with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'

C:\Users\username\mykeyvault-mysecret-1527029447.01191
```

<span data-ttu-id="c4844-119">Эта команда извлекает секрет с именем MySecret из хранилища ключей MyKeyVault и сохраняет ее резервную копию в файл, который автоматически именуется вам, и отображает имя файла.</span><span class="sxs-lookup"><span data-stu-id="c4844-119">This command retrieves the secret named MySecret from the key vault named MyKeyVault and saves a backup of that secret to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="c4844-120">Пример 2. Архивная копия секретного файла на указанное имя, переописыв существующий файл без запроса</span><span class="sxs-lookup"><span data-stu-id="c4844-120">Example 2: Back up a secret to a specified file name, overwriting the existing file without prompting</span></span>
```powershell
PS C:\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="c4844-121">Эта команда извлекает секретную папку MySecret из ключа MyKeyVault и сохраняет ее резервную копию в файле Backup.blob.</span><span class="sxs-lookup"><span data-stu-id="c4844-121">This command retrieves the secret named MySecret from the key vaultnamed MyKeyVault and saves a backup of that secret to a file named Backup.blob.</span></span>

### <span data-ttu-id="c4844-122">Пример 3. Архивная up a secret previously retrieved to a specified file name</span><span class="sxs-lookup"><span data-stu-id="c4844-122">Example 3: Back up a secret previously retrieved to a specified file name</span></span>
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\> Backup-AzKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="c4844-123">Эта команда использует имя $secret и имя объекта, чтобы извлечь секрет и сохранить его резервную копию в файле Backup.blob.</span><span class="sxs-lookup"><span data-stu-id="c4844-123">This command uses the $secret object's vault name and name to retrieves the secret and saves its backup to a file named Backup.blob.</span></span>

## <span data-ttu-id="c4844-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4844-124">PARAMETERS</span></span>

### <span data-ttu-id="c4844-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4844-125">-DefaultProfile</span></span>
<span data-ttu-id="c4844-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c4844-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c4844-127">-Force</span><span class="sxs-lookup"><span data-stu-id="c4844-127">-Force</span></span>
<span data-ttu-id="c4844-128">Запросит подтверждение перед переописью выходного файла, если он существует.</span><span class="sxs-lookup"><span data-stu-id="c4844-128">Prompts you for confirmation before overwriting the output file, if that exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4844-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c4844-129">-InputObject</span></span>
<span data-ttu-id="c4844-130">Секретная возможность, которая должна быть совсю в результатах ирисовки звонка.</span><span class="sxs-lookup"><span data-stu-id="c4844-130">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: BySecret
Aliases: Secret

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4844-131">-Name</span><span class="sxs-lookup"><span data-stu-id="c4844-131">-Name</span></span>
<span data-ttu-id="c4844-132">Имя секретного имени, который нужно сделать.</span><span class="sxs-lookup"><span data-stu-id="c4844-132">Specifies the name of the secret to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4844-133">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="c4844-133">-OutputFile</span></span>
<span data-ttu-id="c4844-134">Определяет выходной файл, в котором хранится BLOB-файл резервной копии.</span><span class="sxs-lookup"><span data-stu-id="c4844-134">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="c4844-135">Если этот параметр не задан, этот cmdlet создает имя файла.</span><span class="sxs-lookup"><span data-stu-id="c4844-135">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="c4844-136">Если указать имя существующего выходного файла, операция не будет завершена и выдаст сообщение об ошибке, указывающую, что файл резервной копии уже существует.</span><span class="sxs-lookup"><span data-stu-id="c4844-136">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="c4844-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c4844-137">-VaultName</span></span>
<span data-ttu-id="c4844-138">Имя сейфа ключа, содержаного секрет, который нужно сделать.</span><span class="sxs-lookup"><span data-stu-id="c4844-138">Specifies the name of the key vault that contains the secret to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4844-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4844-139">-Confirm</span></span>
<span data-ttu-id="c4844-140">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4844-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4844-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4844-141">-WhatIf</span></span>
<span data-ttu-id="c4844-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4844-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4844-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c4844-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4844-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4844-144">CommonParameters</span></span>
<span data-ttu-id="c4844-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4844-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4844-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4844-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4844-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4844-147">INPUTS</span></span>

### <span data-ttu-id="c4844-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="c4844-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="c4844-149">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c4844-149">OUTPUTS</span></span>

### <span data-ttu-id="c4844-150">System.String</span><span class="sxs-lookup"><span data-stu-id="c4844-150">System.String</span></span>

## <span data-ttu-id="c4844-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c4844-151">NOTES</span></span>

## <span data-ttu-id="c4844-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4844-152">RELATED LINKS</span></span>

[<span data-ttu-id="c4844-153">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c4844-153">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="c4844-154">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c4844-154">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="c4844-155">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c4844-155">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="c4844-156">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="c4844-156">Restore-AzKeyVaultSecret</span></span>](./Restore-AzKeyVaultSecret.md)

