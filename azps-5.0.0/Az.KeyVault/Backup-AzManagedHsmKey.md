---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmKey.md
ms.openlocfilehash: 9e75b6de483f0103103434518d31b472660f4a70
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312377"
---
# <span data-ttu-id="2a133-101">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="2a133-101">Backup-AzManagedHsmKey</span></span>

## <span data-ttu-id="2a133-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2a133-102">SYNOPSIS</span></span>
<span data-ttu-id="2a133-103">Резервное копирование ключа в управляемом HSM.</span><span class="sxs-lookup"><span data-stu-id="2a133-103">Backs up a key in a managed HSM.</span></span>

## <span data-ttu-id="2a133-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2a133-104">SYNTAX</span></span>

### <span data-ttu-id="2a133-105">ByKeyName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2a133-105">ByKeyName (Default)</span></span>
```
Backup-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2a133-106">ByKey</span><span class="sxs-lookup"><span data-stu-id="2a133-106">ByKey</span></span>
```
Backup-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a133-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a133-107">DESCRIPTION</span></span>
<span data-ttu-id="2a133-108">Командлет **BACKUP-AzManagedHsmKey** используется для резервного копирования указанного ключа в управляемом HSM, загружая его и сохраняя в файле.</span><span class="sxs-lookup"><span data-stu-id="2a133-108">The **Backup-AzManagedHsmKey** cmdlet backs up a specified key in a managed HSM by downloading it and storing it in a file.</span></span>
<span data-ttu-id="2a133-109">Если вы используете несколько версий ключа, в резервную копию включаются все версии.</span><span class="sxs-lookup"><span data-stu-id="2a133-109">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="2a133-110">Поскольку загруженное содержимое зашифровано, оно не может использоваться за пределами управляемого HSM-модуля Azure.</span><span class="sxs-lookup"><span data-stu-id="2a133-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Managed HSM.</span></span>
<span data-ttu-id="2a133-111">Вы можете восстановить резервную копию ключа на любой управляемый HSM-файл в подписке, из которой она была создана.</span><span class="sxs-lookup"><span data-stu-id="2a133-111">You can restore a backed-up key to any managed HSM in the subscription that it was backed up from.</span></span>
<span data-ttu-id="2a133-112">Ниже приведены основные причины использования этого командлета.</span><span class="sxs-lookup"><span data-stu-id="2a133-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="2a133-113">Вы хотите пополнить свою копию ключа, чтобы иметь возможность использовать автономную копию на случай, если вы случайно удалили ключ в управляемом HSM-коде.</span><span class="sxs-lookup"><span data-stu-id="2a133-113">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your managed HSM.</span></span>
 
- <span data-ttu-id="2a133-114">Вы создали ключ, используя управляемый HSM-файл, и теперь хотите клонировать ключ в другой регион Azure, чтобы его можно было использовать из всех экземпляров распределенного приложения.</span><span class="sxs-lookup"><span data-stu-id="2a133-114">You created a key using Managed HSM and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="2a133-115">С помощью командлета **BACKUP-AzManagedHsmKey** можно получить ключ в зашифрованном формате, а затем использовать командлет Restore-AzManagedHsmKey и указать управляемый HSM-код во втором регионе.</span><span class="sxs-lookup"><span data-stu-id="2a133-115">Use the **Backup-AzManagedHsmKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzManagedHsmKey cmdlet and specify a managed HSM in the second region.</span></span>

## <span data-ttu-id="2a133-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2a133-116">EXAMPLES</span></span>

### <span data-ttu-id="2a133-117">Пример 1: создание резервной копии ключа с автоматически сгенерированным именем файла</span><span class="sxs-lookup"><span data-stu-id="2a133-117">Example 1: Back up a key with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzManagedHsmKey -HsmName testmhsm -Name testkey

C:\Users\username\testmhsm-testkey-1602664728.7106073
```

<span data-ttu-id="2a133-118">Эта команда извлекает ключ с именем TestKey из управляемого HSM-файла с именем testmhsm и сохраняет резервную копию этого ключа в файле с автоматическим именем и выводит имя файла.</span><span class="sxs-lookup"><span data-stu-id="2a133-118">This command retrieves the key named testkey from the managed HSM named testmhsm and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

## <span data-ttu-id="2a133-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2a133-119">PARAMETERS</span></span>

### <span data-ttu-id="2a133-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a133-120">-DefaultProfile</span></span>
<span data-ttu-id="2a133-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a133-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a133-122">-Force</span><span class="sxs-lookup"><span data-stu-id="2a133-122">-Force</span></span>
<span data-ttu-id="2a133-123">Перезаписать заданный файл, если он существует</span><span class="sxs-lookup"><span data-stu-id="2a133-123">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="2a133-124">-HsmName</span><span class="sxs-lookup"><span data-stu-id="2a133-124">-HsmName</span></span>
<span data-ttu-id="2a133-125">Имя HSM.</span><span class="sxs-lookup"><span data-stu-id="2a133-125">HSM name.</span></span> <span data-ttu-id="2a133-126">Командлет создает полное доменное имя управляемого HSM-файла на основе имени и выбранной в данный момент среды.</span><span class="sxs-lookup"><span data-stu-id="2a133-126">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="2a133-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a133-127">-InputObject</span></span>
<span data-ttu-id="2a133-128">Набор ключей для резервного копирования, конвейера из выходных данных вызова.</span><span class="sxs-lookup"><span data-stu-id="2a133-128">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="2a133-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2a133-129">-Name</span></span>
<span data-ttu-id="2a133-130">Имя ключа.</span><span class="sxs-lookup"><span data-stu-id="2a133-130">Key name.</span></span>
<span data-ttu-id="2a133-131">Командлет конструирует полное доменное имя ключа из управляемого имени HSM, в настоящее время выбранной среды и имени ключа.</span><span class="sxs-lookup"><span data-stu-id="2a133-131">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="2a133-132">-Выходной_файл</span><span class="sxs-lookup"><span data-stu-id="2a133-132">-OutputFile</span></span>
<span data-ttu-id="2a133-133">Выходной файл.</span><span class="sxs-lookup"><span data-stu-id="2a133-133">Output file.</span></span>
<span data-ttu-id="2a133-134">Выходной файл, в котором хранится резервный объект Key.</span><span class="sxs-lookup"><span data-stu-id="2a133-134">The output file to store the backed up key blob in.</span></span>
<span data-ttu-id="2a133-135">Если он отсутствует, выбирается имя файла по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2a133-135">If not present, a default filename is chosen.</span></span>

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

### <span data-ttu-id="2a133-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a133-136">-Confirm</span></span>
<span data-ttu-id="2a133-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2a133-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a133-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a133-138">-WhatIf</span></span>
<span data-ttu-id="2a133-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2a133-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a133-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2a133-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a133-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a133-141">CommonParameters</span></span>
<span data-ttu-id="2a133-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2a133-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a133-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a133-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a133-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2a133-144">INPUTS</span></span>

### <span data-ttu-id="2a133-145">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="2a133-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="2a133-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a133-146">OUTPUTS</span></span>

### <span data-ttu-id="2a133-147">System. String</span><span class="sxs-lookup"><span data-stu-id="2a133-147">System.String</span></span>

## <span data-ttu-id="2a133-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="2a133-148">NOTES</span></span>

## <span data-ttu-id="2a133-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a133-149">RELATED LINKS</span></span>

[<span data-ttu-id="2a133-150">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="2a133-150">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="2a133-151">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="2a133-151">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="2a133-152">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="2a133-152">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="2a133-153">Undo-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="2a133-153">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="2a133-154">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="2a133-154">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="2a133-155">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="2a133-155">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)