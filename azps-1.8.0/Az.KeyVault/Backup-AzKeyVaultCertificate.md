---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultCertificate.md
ms.openlocfilehash: 0c92dbea0127db82a1b1f4605cd581f31c872a57
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93900249"
---
# <span data-ttu-id="7bac2-101">Backup-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="7bac2-101">Backup-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="7bac2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7bac2-102">SYNOPSIS</span></span>
<span data-ttu-id="7bac2-103">Создание резервной копии сертификата в хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="7bac2-103">Backs up a certificate in a key vault.</span></span>

## <span data-ttu-id="7bac2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7bac2-104">SYNTAX</span></span>

### <span data-ttu-id="7bac2-105">ByCertificateName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7bac2-105">ByCertificateName (Default)</span></span>
```
Backup-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bac2-106">ByCertificate</span><span class="sxs-lookup"><span data-stu-id="7bac2-106">ByCertificate</span></span>
```
Backup-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [[-OutputFile] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bac2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7bac2-107">DESCRIPTION</span></span>
<span data-ttu-id="7bac2-108">Командлет **BACKUP-AzKeyVaultCertificate** производит резервное копирование указанного сертификата в хранилище ключей, загружая его и сохраняя в файле.</span><span class="sxs-lookup"><span data-stu-id="7bac2-108">The **Backup-AzKeyVaultCertificate** cmdlet backs up a specified certificate in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="7bac2-109">Если у сертификата есть несколько версий, все их версии будут включены в резервную копию.</span><span class="sxs-lookup"><span data-stu-id="7bac2-109">If the certificate has multiple versions, all its versions will be included in the backup.</span></span>
<span data-ttu-id="7bac2-110">Поскольку загруженное содержимое зашифровано, оно не может использоваться за пределами хранилища ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="7bac2-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="7bac2-111">Вы можете восстановить резервную копию сертификата в любом хранилище ключей в подписке, из которой она была создана, пока она находится в том же географическом расположении Azure.</span><span class="sxs-lookup"><span data-stu-id="7bac2-111">You can restore a backed-up certificate to any key vault in the subscription that it was backed up from, as long as the vault is in the same Azure geography.</span></span>
<span data-ttu-id="7bac2-112">Ниже приведены основные причины использования этого командлета.</span><span class="sxs-lookup"><span data-stu-id="7bac2-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="7bac2-113">Вы хотите сохранить автономную копию сертификата на случай, если вы случайно удалили оригинал из хранилища.</span><span class="sxs-lookup"><span data-stu-id="7bac2-113">You want to retain an offline copy of the certificate in case you accidentally delete the original from the vault.</span></span>
 
- <span data-ttu-id="7bac2-114">Вы создали сертификат с помощью ключа Vault и теперь хотите клонировать объект в другой регион Azure, чтобы его можно было использовать из всех экземпляров распределенного приложения.</span><span class="sxs-lookup"><span data-stu-id="7bac2-114">You created a certificate using Key Vault and now want to clone the object into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="7bac2-115">С помощью командлета **BACKUP-AzKeyVaultCertificate** можно получить сертификат в зашифрованном формате, а затем использовать командлет **RESTORE-AzKeyVaultCertificate** и указав для него хранилище ключей во втором регионе.</span><span class="sxs-lookup"><span data-stu-id="7bac2-115">Use the **Backup-AzKeyVaultCertificate** cmdlet to retrieve the certificate in encrypted format and then use the **Restore-AzKeyVaultCertificate** cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="7bac2-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7bac2-116">EXAMPLES</span></span>

### <span data-ttu-id="7bac2-117">Пример 1: создание резервной копии сертификата с автоматически сгенерированным именем файла</span><span class="sxs-lookup"><span data-stu-id="7bac2-117">Example 1: Back up a certificate with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultCertificate -VaultName 'mykeyvault' -Name 'mycert'

C:\Users\username\mykeyvault-mycert-1527029447.01191
```

<span data-ttu-id="7bac2-118">Эта команда извлекает сертификат с именем MyCert из хранилища ключей с именем MyKeyVault и сохраняет резервную копию этого сертификата в файл с автоматическим именем и выводит имя файла.</span><span class="sxs-lookup"><span data-stu-id="7bac2-118">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="7bac2-119">Пример 2: создание резервной копии сертификата для указанного имени файла</span><span class="sxs-lookup"><span data-stu-id="7bac2-119">Example 2: Back up a certificate to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyCert' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="7bac2-120">Эта команда извлекает сертификат с именем MyCert из хранилища ключей с именем MyKeyVault и сохраняет резервную копию этого сертификата в файле с именем Backup. BLOB.</span><span class="sxs-lookup"><span data-stu-id="7bac2-120">This command retrieves the certificate named MyCert from the key vault named MyKeyVault and saves a backup of that certificate to a file named Backup.blob.</span></span>

### <span data-ttu-id="7bac2-121">Пример 3: создание резервной копии ранее полученного сертификата по указанному имени файла с перезазаписьм конечного файла без запроса.</span><span class="sxs-lookup"><span data-stu-id="7bac2-121">Example 3: Back up a previously retrieved certificate to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $cert = Get-AzKeyVaultCertificate -VaultName 'MyKeyVault' -Name 'MyCert'
PS C:\> Backup-AzKeyVaultCertificate -Certificate $cert -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="7bac2-122">Эта команда создает резервную копию сертификата с именем $cert. Имя в хранилище с именем $cert. VaultName файл с именем Backup. BLOB, перезапись файла без уведомления, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="7bac2-122">This command creates a backup of the certificate named $cert.Name in the vault named $cert.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="7bac2-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7bac2-123">PARAMETERS</span></span>

### <span data-ttu-id="7bac2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bac2-124">-DefaultProfile</span></span>
<span data-ttu-id="7bac2-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7bac2-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bac2-126">-Force</span><span class="sxs-lookup"><span data-stu-id="7bac2-126">-Force</span></span>
<span data-ttu-id="7bac2-127">Перезаписать заданный файл, если он существует</span><span class="sxs-lookup"><span data-stu-id="7bac2-127">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="7bac2-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7bac2-128">-InputObject</span></span>
<span data-ttu-id="7bac2-129">Секрет, для которого необходимо создать резервную копию, конвейер из результатов запроса на получение.</span><span class="sxs-lookup"><span data-stu-id="7bac2-129">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="7bac2-130">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="7bac2-130">-Name</span></span>
<span data-ttu-id="7bac2-131">Имя секрета.</span><span class="sxs-lookup"><span data-stu-id="7bac2-131">Secret name.</span></span>
<span data-ttu-id="7bac2-132">Командлет создает полное доменное имя секрета из имени хранилища, выбранного в настоящее время среды и имени секрета.</span><span class="sxs-lookup"><span data-stu-id="7bac2-132">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="7bac2-133">-Выходной_файл</span><span class="sxs-lookup"><span data-stu-id="7bac2-133">-OutputFile</span></span>
<span data-ttu-id="7bac2-134">Выходной файл.</span><span class="sxs-lookup"><span data-stu-id="7bac2-134">Output file.</span></span>
<span data-ttu-id="7bac2-135">Выходной файл, в котором будет храниться резервная копия сертификата.</span><span class="sxs-lookup"><span data-stu-id="7bac2-135">The output file to store the backup of the certificate.</span></span>
<span data-ttu-id="7bac2-136">Если не указано, будет создано имя файла по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7bac2-136">If not specified, a default filename will be generated.</span></span>

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

### <span data-ttu-id="7bac2-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="7bac2-137">-VaultName</span></span>
<span data-ttu-id="7bac2-138">Имя хранилища.</span><span class="sxs-lookup"><span data-stu-id="7bac2-138">Vault name.</span></span>
<span data-ttu-id="7bac2-139">Командлет создает полное доменное имя хранилища на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="7bac2-139">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="7bac2-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7bac2-140">-Confirm</span></span>
<span data-ttu-id="7bac2-141">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7bac2-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bac2-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bac2-142">-WhatIf</span></span>
<span data-ttu-id="7bac2-143">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7bac2-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bac2-144">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7bac2-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bac2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bac2-145">CommonParameters</span></span>
<span data-ttu-id="7bac2-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7bac2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bac2-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7bac2-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bac2-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7bac2-148">INPUTS</span></span>

### <span data-ttu-id="7bac2-149">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="7bac2-149">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="7bac2-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7bac2-150">OUTPUTS</span></span>

### <span data-ttu-id="7bac2-151">System. String</span><span class="sxs-lookup"><span data-stu-id="7bac2-151">System.String</span></span>

## <span data-ttu-id="7bac2-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="7bac2-152">NOTES</span></span>

## <span data-ttu-id="7bac2-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7bac2-153">RELATED LINKS</span></span>
