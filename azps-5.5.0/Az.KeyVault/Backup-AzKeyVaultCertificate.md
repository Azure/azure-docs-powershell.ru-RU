---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
ms.openlocfilehash: 51d322ea738a56e4b1fa24cccdb7bb59a6cd0d21
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100214540"
---
# <span data-ttu-id="9972f-101">Backup-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="9972f-101">Backup-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="9972f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9972f-102">SYNOPSIS</span></span>
<span data-ttu-id="9972f-103">Backs up a certificate in a key vault.</span><span class="sxs-lookup"><span data-stu-id="9972f-103">Backs up a certificate in a key vault.</span></span>

## <span data-ttu-id="9972f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9972f-104">SYNTAX</span></span>

### <span data-ttu-id="9972f-105">ByCertificateName (Default)</span><span class="sxs-lookup"><span data-stu-id="9972f-105">ByCertificateName (Default)</span></span>
```
Backup-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9972f-106">ByCertificate</span><span class="sxs-lookup"><span data-stu-id="9972f-106">ByCertificate</span></span>
```
Backup-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9972f-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9972f-107">DESCRIPTION</span></span>
<span data-ttu-id="9972f-108">**Cmdlet Backup-AzKeyVaultCertificate** резервное копирование указанного сертификата в хранилище ключа путем его скачивания и хранения в файле.</span><span class="sxs-lookup"><span data-stu-id="9972f-108">The **Backup-AzKeyVaultCertificate** cmdlet backs up a specified certificate in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="9972f-109">Если сертификат содержит несколько версий, все его версии будут включены в резервную копию.</span><span class="sxs-lookup"><span data-stu-id="9972f-109">If the certificate has multiple versions, all its versions will be included in the backup.</span></span>
<span data-ttu-id="9972f-110">Так как скачаное содержимое зашифровано, его невозможно использовать за пределами хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="9972f-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="9972f-111">Вы можете восстановить снова заданный сертификат в любом хранилище ключей в подписке, из какой подписки он был, если хранилище находится в той же географической области Azure.</span><span class="sxs-lookup"><span data-stu-id="9972f-111">You can restore a backed-up certificate to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="9972f-112">Этот cmdlet обычно используется по одной из причин:</span><span class="sxs-lookup"><span data-stu-id="9972f-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="9972f-113">Вы хотите сохранить автономный экземпляр сертификата в случае случайного удаления исходного сертификата из хранилища.</span><span class="sxs-lookup"><span data-stu-id="9972f-113">You want to retain an offline copy of the certificate in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="9972f-114">Вы создали сертификат с помощью хранилища ключей и хотите клонировать объект в другой регион Azure, чтобы его можно было использовать из всех экземпляров распределенного приложения.</span><span class="sxs-lookup"><span data-stu-id="9972f-114">You created a certificate using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="9972f-115">Используйте cmdlet **Backup-AzKeyVaultCertificate,** чтобы получить сертификат в зашифрованном формате, а затем используйте cmdlet **Restore-AzKeyVaultCertificate** и укажите хранилище ключа во втором регионе.</span><span class="sxs-lookup"><span data-stu-id="9972f-115">Use the **Backup-AzKeyVaultCertificate** cmdlet to retrieve the certificate in encrypted format and then use the **Restore-AzKeyVaultCertificate** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="9972f-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9972f-116">EXAMPLES</span></span>

### <span data-ttu-id="9972f-117">Пример 1. Архивная система сертификата с автоматически созданным именем файла</span><span class="sxs-lookup"><span data-stu-id="9972f-117">Example 1: Back up a certificate with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

<span data-ttu-id="9972f-118">Эта команда извлекает сертификат MyCert из хранилища ключей MyKeyVault и сохраняет его резервную копию в файл, который автоматически именуется вам, и отображает имя файла.</span><span class="sxs-lookup"><span data-stu-id="9972f-118">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="9972f-119">Пример 2. Архивная up a certificate to a specified file name</span><span class="sxs-lookup"><span data-stu-id="9972f-119">Example 2: Back up a certificate to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="9972f-120">Эта команда извлекает сертификат MyCert из хранилища ключей MyKeyVault и сохраняет его резервную копию в файле Backup.blob.</span><span class="sxs-lookup"><span data-stu-id="9972f-120">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file named Backup.blob.</span></span>

### <span data-ttu-id="9972f-121">Пример 3. Архивная копия ранее восстановленного сертификата на указанное имя файла, переописыв файл назначения без запроса.</span><span class="sxs-lookup"><span data-stu-id="9972f-121">Example 3: Back up a previously retrieved certificate to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $cert = Get-AzKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="9972f-122">Эта команда создает резервную копию сертификата с именем $cert. Имя в хранилище с именем $cert. VaultName в файл Backup.blob, автоматически переописав файл, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="9972f-122">This command creates a backup of the certificate named $cert.Name in the vault named $cert.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="9972f-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9972f-123">PARAMETERS</span></span>

### <span data-ttu-id="9972f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9972f-124">-DefaultProfile</span></span>
<span data-ttu-id="9972f-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9972f-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9972f-126">-Force</span><span class="sxs-lookup"><span data-stu-id="9972f-126">-Force</span></span>
<span data-ttu-id="9972f-127">Переописывать файл, если он существует</span><span class="sxs-lookup"><span data-stu-id="9972f-127">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="9972f-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9972f-128">-InputObject</span></span>
<span data-ttu-id="9972f-129">Секретная возможность, которая будет иметь подархив, отспроизводя ее на итоге ирисовки звонка.</span><span class="sxs-lookup"><span data-stu-id="9972f-129">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByCertificate
Aliases: Certificate

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9972f-130">-Name</span><span class="sxs-lookup"><span data-stu-id="9972f-130">-Name</span></span>
<span data-ttu-id="9972f-131">Секретное имя.</span><span class="sxs-lookup"><span data-stu-id="9972f-131">Secret name.</span></span>
<span data-ttu-id="9972f-132">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span><span class="sxs-lookup"><span data-stu-id="9972f-132">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9972f-133">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="9972f-133">-OutputFile</span></span>
<span data-ttu-id="9972f-134">Выходной файл.</span><span class="sxs-lookup"><span data-stu-id="9972f-134">Output file.</span></span>
<span data-ttu-id="9972f-135">Выходной файл для хранения резервной копии сертификата.</span><span class="sxs-lookup"><span data-stu-id="9972f-135">The output file to store the backup of the certificate.</span></span>
<span data-ttu-id="9972f-136">Если он не задан, будет сгенерировано имя файла по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9972f-136">If not specified, a default filename will be generated.</span></span>

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

### <span data-ttu-id="9972f-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9972f-137">-VaultName</span></span>
<span data-ttu-id="9972f-138">Имя сейфа.</span><span class="sxs-lookup"><span data-stu-id="9972f-138">Vault name.</span></span>
<span data-ttu-id="9972f-139">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span><span class="sxs-lookup"><span data-stu-id="9972f-139">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9972f-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9972f-140">-Confirm</span></span>
<span data-ttu-id="9972f-141">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9972f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9972f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9972f-142">-WhatIf</span></span>
<span data-ttu-id="9972f-143">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9972f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9972f-144">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9972f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9972f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9972f-145">CommonParameters</span></span>
<span data-ttu-id="9972f-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9972f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9972f-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9972f-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9972f-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9972f-148">INPUTS</span></span>

### <span data-ttu-id="9972f-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="9972f-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="9972f-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9972f-150">OUTPUTS</span></span>

### <span data-ttu-id="9972f-151">System.String</span><span class="sxs-lookup"><span data-stu-id="9972f-151">System.String</span></span>

## <span data-ttu-id="9972f-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9972f-152">NOTES</span></span>

## <span data-ttu-id="9972f-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9972f-153">RELATED LINKS</span></span>
