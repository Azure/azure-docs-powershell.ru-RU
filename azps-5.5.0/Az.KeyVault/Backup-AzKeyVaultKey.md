---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: 88decaffa736f015b8e65aa1217eab4899b07c7c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214516"
---
# <span data-ttu-id="94161-101">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="94161-101">Backup-AzKeyVaultKey</span></span>

## <span data-ttu-id="94161-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94161-102">SYNOPSIS</span></span>
<span data-ttu-id="94161-103">Backs up a key in a key vault.</span><span class="sxs-lookup"><span data-stu-id="94161-103">Backs up a key in a key vault.</span></span>

## <span data-ttu-id="94161-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="94161-104">SYNTAX</span></span>

### <span data-ttu-id="94161-105">ByKeyName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="94161-105">ByKeyName (Default)</span></span>
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94161-106">HsmByKeyName</span><span class="sxs-lookup"><span data-stu-id="94161-106">HsmByKeyName</span></span>
```
Backup-AzKeyVaultKey -HsmName <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94161-107">ByKey</span><span class="sxs-lookup"><span data-stu-id="94161-107">ByKey</span></span>
```
Backup-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94161-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94161-108">DESCRIPTION</span></span>
<span data-ttu-id="94161-109">С **помощью cmdlet Backup-AzKeyVaultKey** можно сделать резервную копию указанного ключа в хранилище ключей, скачав и храня его в файле.</span><span class="sxs-lookup"><span data-stu-id="94161-109">The **Backup-AzKeyVaultKey** cmdlet backs up a specified key in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="94161-110">Если есть несколько версий ключа, все версии включаются в резервную копию.</span><span class="sxs-lookup"><span data-stu-id="94161-110">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="94161-111">Так как скачаное содержимое зашифровано, его невозможно использовать за пределами хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="94161-111">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="94161-112">Вы можете восстановить подпапавную клавишу в любое хранилище ключей в подписке, из какой подписки она была.</span><span class="sxs-lookup"><span data-stu-id="94161-112">You can restore a backed-up key to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="94161-113">Этот cmdlet обычно используется по одной из причин:</span><span class="sxs-lookup"><span data-stu-id="94161-113">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="94161-114">Вы хотите escrow a copy of your key, so that you have anfline copy in case you accidentally delete your key in your key vault.</span><span class="sxs-lookup"><span data-stu-id="94161-114">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your key vault.</span></span>
 
- <span data-ttu-id="94161-115">Вы создали ключ с помощью хранилища ключей и хотите клонировать его в другой регион Azure, чтобы его можно было использовать из всех экземпляров распределенного приложения.</span><span class="sxs-lookup"><span data-stu-id="94161-115">You created a key using Key Vault and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="94161-116">Используйте Restore-AzKeyVaultKey **Backup-AzKeyVaultKey** для получения ключа в зашифрованном формате, а затем используйте Restore-AzKeyVaultKey и укажите хранилище ключа во втором регионе.</span><span class="sxs-lookup"><span data-stu-id="94161-116">Use the **Backup-AzKeyVaultKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzKeyVaultKey cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="94161-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="94161-117">EXAMPLES</span></span>

### <span data-ttu-id="94161-118">Пример 1. Архивная архивная система ключа с автоматически созданным именем файла</span><span class="sxs-lookup"><span data-stu-id="94161-118">Example 1: Back up a key with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'

C:\Users\username\mykeyvault-mykey-1527029447.01191
```

<span data-ttu-id="94161-119">Эта команда извлекает ключ MyKey из хранилища ключей MyKeyVault и сохраняет его резервную копию в файл, который автоматически именуется вам, и отображает имя файла.</span><span class="sxs-lookup"><span data-stu-id="94161-119">This command retrieves the key named MyKey from the key vault named MyKeyVault and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="94161-120">Пример 2. Архивная архивная up a key to a specified file name</span><span class="sxs-lookup"><span data-stu-id="94161-120">Example 2: Back up a key to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="94161-121">Эта команда извлекает ключ MyKey из ключа MyKeyVault и сохраняет его резервную копию в файле Backup.blob.</span><span class="sxs-lookup"><span data-stu-id="94161-121">This command retrieves the key named MyKey from the key vaultnamed MyKeyVault and saves a backup of that key to a file named Backup.blob.</span></span>

### <span data-ttu-id="94161-122">Пример 3. Архивная копия ранее извлеченного ключа на указанное имя файла, переописав файл без запроса.</span><span class="sxs-lookup"><span data-stu-id="94161-122">Example 3: Back up a previously retrieved key to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\> Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="94161-123">Эта команда создает резервную копию ключа с $key. Имя в хранилище с именем $key. VaultName в файл Backup.blob, автоматически переописав файл, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="94161-123">This command creates a backup of the key named $key.Name in the vault named $key.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="94161-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94161-124">PARAMETERS</span></span>

### <span data-ttu-id="94161-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94161-125">-DefaultProfile</span></span>
<span data-ttu-id="94161-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="94161-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94161-127">-Force</span><span class="sxs-lookup"><span data-stu-id="94161-127">-Force</span></span>
<span data-ttu-id="94161-128">Переописывать файл, если он существует</span><span class="sxs-lookup"><span data-stu-id="94161-128">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="94161-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="94161-129">-HsmName</span></span>
<span data-ttu-id="94161-130">Имя HSM.</span><span class="sxs-lookup"><span data-stu-id="94161-130">HSM name.</span></span> <span data-ttu-id="94161-131">С его учетом именем и выбранной средой строится FQDN управляемой HSM- среды.</span><span class="sxs-lookup"><span data-stu-id="94161-131">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByKeyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94161-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94161-132">-InputObject</span></span>
<span data-ttu-id="94161-133">Пакет ключей для повторного, проинтестрироваться на итоге ирисовки звонка.</span><span class="sxs-lookup"><span data-stu-id="94161-133">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="94161-134">-Name</span><span class="sxs-lookup"><span data-stu-id="94161-134">-Name</span></span>
<span data-ttu-id="94161-135">Указывает имя ключа, который нужно сделать.</span><span class="sxs-lookup"><span data-stu-id="94161-135">Specifies the name of the key to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, HsmByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94161-136">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="94161-136">-OutputFile</span></span>
<span data-ttu-id="94161-137">Определяет выходной файл, в котором хранится BLOB-файл резервной копии.</span><span class="sxs-lookup"><span data-stu-id="94161-137">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="94161-138">Если этот параметр не задан, этот cmdlet создает имя файла.</span><span class="sxs-lookup"><span data-stu-id="94161-138">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="94161-139">Если указать имя существующего выходного файла, операция не будет завершена и выдаст сообщение об ошибке, указывающую, что файл резервной копии уже существует.</span><span class="sxs-lookup"><span data-stu-id="94161-139">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="94161-140">-VaultName</span><span class="sxs-lookup"><span data-stu-id="94161-140">-VaultName</span></span>
<span data-ttu-id="94161-141">Имя хранилища ключей, содержаного ключ для скайпа.</span><span class="sxs-lookup"><span data-stu-id="94161-141">Specifies the name of the key vault that contains the key to back up.</span></span>

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

### <span data-ttu-id="94161-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94161-142">-Confirm</span></span>
<span data-ttu-id="94161-143">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="94161-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94161-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94161-144">-WhatIf</span></span>
<span data-ttu-id="94161-145">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94161-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94161-146">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="94161-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94161-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94161-147">CommonParameters</span></span>
<span data-ttu-id="94161-148">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94161-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94161-149">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94161-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94161-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="94161-150">INPUTS</span></span>

### <span data-ttu-id="94161-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="94161-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="94161-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="94161-152">OUTPUTS</span></span>

### <span data-ttu-id="94161-153">System.String</span><span class="sxs-lookup"><span data-stu-id="94161-153">System.String</span></span>

## <span data-ttu-id="94161-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="94161-154">NOTES</span></span>

## <span data-ttu-id="94161-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94161-155">RELATED LINKS</span></span>

[<span data-ttu-id="94161-156">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="94161-156">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="94161-157">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="94161-157">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="94161-158">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="94161-158">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="94161-159">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="94161-159">Restore-AzKeyVaultKey</span></span>](./Restore-AzKeyVaultKey.md)

