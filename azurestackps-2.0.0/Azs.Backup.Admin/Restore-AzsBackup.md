---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/restore-azsbackup
schema: 2.0.0
ms.openlocfilehash: d441c74817ccaf1b32b7caf6fe811f6a5a4789da
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911679"
---
# <span data-ttu-id="3b91e-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="3b91e-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="3b91e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3b91e-102">SYNOPSIS</span></span>
<span data-ttu-id="3b91e-103">Восстановите резервную копию.</span><span class="sxs-lookup"><span data-stu-id="3b91e-103">Restore a backup.</span></span>

## <span data-ttu-id="3b91e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3b91e-104">SYNTAX</span></span>

### <span data-ttu-id="3b91e-105">RestoreExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3b91e-105">RestoreExpanded (Default)</span></span>
```
Restore-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DecryptionCertPassword <SecureString>] [-DecryptionCertPath <String>] [-RoleName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="3b91e-106">Восстановление</span><span class="sxs-lookup"><span data-stu-id="3b91e-106">Restore</span></span>
```
Restore-AzsBackup -Name <String> -RestoreOption <IRestoreOptions> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3b91e-107">RestoreViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3b91e-107">RestoreViaIdentity</span></span>
```
Restore-AzsBackup -InputObject <IBackupAdminIdentity> -RestoreOption <IRestoreOptions>
 [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="3b91e-108">RestoreViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3b91e-108">RestoreViaIdentityExpanded</span></span>
```
Restore-AzsBackup -InputObject <IBackupAdminIdentity> [-DecryptionCertPassword <SecureString>]
 [-DecryptionCertPath <String>] [-RoleName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3b91e-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b91e-109">DESCRIPTION</span></span>
<span data-ttu-id="3b91e-110">Восстановите резервную копию.</span><span class="sxs-lookup"><span data-stu-id="3b91e-110">Restore a backup.</span></span>

## <span data-ttu-id="3b91e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3b91e-111">EXAMPLES</span></span>

### <span data-ttu-id="3b91e-112">Пример 1: восстановление резервной копии</span><span class="sxs-lookup"><span data-stu-id="3b91e-112">Example 1: Restore Backup</span></span>
```powershell
PS C:\> Restore-AzsBackup -Name $backupResourceName -DecryptionCertPath $decryptionCertPath -DecryptionCertPassword $decryptionCertPassword

```

<span data-ttu-id="3b91e-113">Восстановление из резервной копии стека Azure.</span><span class="sxs-lookup"><span data-stu-id="3b91e-113">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="3b91e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3b91e-114">PARAMETERS</span></span>

### <span data-ttu-id="3b91e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3b91e-115">-AsJob</span></span>
<span data-ttu-id="3b91e-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="3b91e-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3b91e-117">-DecryptionCertPassword</span><span class="sxs-lookup"><span data-stu-id="3b91e-117">-DecryptionCertPassword</span></span>
<span data-ttu-id="3b91e-118">Пароль сертификата расшифровки.</span><span class="sxs-lookup"><span data-stu-id="3b91e-118">The password for the decryption certificate.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RestoreExpanded, RestoreViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3b91e-119">-DecryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="3b91e-119">-DecryptionCertPath</span></span>
<span data-ttu-id="3b91e-120">Путь к файлу сертификата расшифровки с закрытым ключом (PFX).</span><span class="sxs-lookup"><span data-stu-id="3b91e-120">Path to the decryption cert file with private key (.pfx).</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreExpanded, RestoreViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3b91e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b91e-121">-DefaultProfile</span></span>
<span data-ttu-id="3b91e-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3b91e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3b91e-123">-Force</span><span class="sxs-lookup"><span data-stu-id="3b91e-123">-Force</span></span>
<span data-ttu-id="3b91e-124">Не запрашивать подтверждение</span><span class="sxs-lookup"><span data-stu-id="3b91e-124">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="3b91e-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b91e-125">-InputObject</span></span>
<span data-ttu-id="3b91e-126">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="3b91e-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity
Parameter Sets: RestoreViaIdentity, RestoreViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="3b91e-127">-Location</span><span class="sxs-lookup"><span data-stu-id="3b91e-127">-Location</span></span>
<span data-ttu-id="3b91e-128">Имя расположения резервной копии.</span><span class="sxs-lookup"><span data-stu-id="3b91e-128">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3b91e-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3b91e-129">-Name</span></span>
<span data-ttu-id="3b91e-130">Имя резервной копии.</span><span class="sxs-lookup"><span data-stu-id="3b91e-130">Name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3b91e-131">-Wait</span><span class="sxs-lookup"><span data-stu-id="3b91e-131">-NoWait</span></span>
<span data-ttu-id="3b91e-132">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="3b91e-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3b91e-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b91e-133">-PassThru</span></span>
<span data-ttu-id="3b91e-134">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="3b91e-134">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3b91e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b91e-135">-ResourceGroupName</span></span>
<span data-ttu-id="3b91e-136">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3b91e-136">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3b91e-137">-RestoreOption</span><span class="sxs-lookup"><span data-stu-id="3b91e-137">-RestoreOption</span></span>
<span data-ttu-id="3b91e-138">Свойства параметров восстановления.</span><span class="sxs-lookup"><span data-stu-id="3b91e-138">Properties for restore options.</span></span>
<span data-ttu-id="3b91e-139">Для конструирования ознакомьтесь с разделом "Заметки" для свойств RESTOREOPTION и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="3b91e-139">To construct, see NOTES section for RESTOREOPTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IRestoreOptions
Parameter Sets: Restore, RestoreViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3b91e-140">-RoleName</span><span class="sxs-lookup"><span data-stu-id="3b91e-140">-RoleName</span></span>
<span data-ttu-id="3b91e-141">Имя роли стека Azure для восстановления, установите для нее значение Empty для всех ролей инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="3b91e-141">The Azure Stack role name for restore, set it to empty for all infrastructure role</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreExpanded, RestoreViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3b91e-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3b91e-142">-SubscriptionId</span></span>
<span data-ttu-id="3b91e-143">Учетные данные подписки, однозначно определяющие подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3b91e-143">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3b91e-144">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="3b91e-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3b91e-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b91e-145">-Confirm</span></span>
<span data-ttu-id="3b91e-146">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3b91e-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b91e-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b91e-147">-WhatIf</span></span>
<span data-ttu-id="3b91e-148">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3b91e-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b91e-149">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3b91e-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b91e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b91e-150">CommonParameters</span></span>
<span data-ttu-id="3b91e-151">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3b91e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b91e-152">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3b91e-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b91e-153">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3b91e-153">INPUTS</span></span>

### <span data-ttu-id="3b91e-154">Microsoft. Azure. PowerShell. командлеты. BackupAdmin. Models. IBackupAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="3b91e-154">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="3b91e-155">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b91e-155">OUTPUTS</span></span>

### <span data-ttu-id="3b91e-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3b91e-156">System.Boolean</span></span>



## <span data-ttu-id="3b91e-157">Пуск</span><span class="sxs-lookup"><span data-stu-id="3b91e-157">NOTES</span></span>

<span data-ttu-id="3b91e-158">Свойства сложных параметров для создания описанных ниже параметров создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3b91e-158">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3b91e-159">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3b91e-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="3b91e-160">INPUTOBJECT <IBackupAdminIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="3b91e-160">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3b91e-161">`[Backup <String>]`: Имя резервной копии.</span><span class="sxs-lookup"><span data-stu-id="3b91e-161">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="3b91e-162">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="3b91e-162">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3b91e-163">`[Location <String>]`: Имя расположения резервной копии.</span><span class="sxs-lookup"><span data-stu-id="3b91e-163">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="3b91e-164">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3b91e-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="3b91e-165">`[SubscriptionId <String>]`: Учетные данные подписки, которые однозначно определяют подписку Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3b91e-165">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3b91e-166">Идентификатор подписки образует часть URI для каждого вызова службы.</span><span class="sxs-lookup"><span data-stu-id="3b91e-166">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="3b91e-167">RESTOREOPTION <IRestoreOptions> : свойства для параметров восстановления.</span><span class="sxs-lookup"><span data-stu-id="3b91e-167">RESTOREOPTION <IRestoreOptions>: Properties for restore options.</span></span>
  - <span data-ttu-id="3b91e-168">`[DecryptionCertBase64 <String>]`: Необработанные данные файла сертификата в строке Base64.</span><span class="sxs-lookup"><span data-stu-id="3b91e-168">`[DecryptionCertBase64 <String>]`: The certificate file raw data in Base64 string.</span></span> <span data-ttu-id="3b91e-169">Это должен быть PFX-файл с закрытым ключом.</span><span class="sxs-lookup"><span data-stu-id="3b91e-169">This should be the .pfx file with the private key.</span></span>
  - <span data-ttu-id="3b91e-170">`[DecryptionCertPassword <String>]`: Пароль сертификата расшифровки.</span><span class="sxs-lookup"><span data-stu-id="3b91e-170">`[DecryptionCertPassword <String>]`: The password for the decryption certificate.</span></span>
  - <span data-ttu-id="3b91e-171">`[RoleName <String>]`: Имя роли стека Azure для восстановления, назначение пустого значения для всех ролей инфраструктуры</span><span class="sxs-lookup"><span data-stu-id="3b91e-171">`[RoleName <String>]`: The Azure Stack role name for restore, set it to empty for all infrastructure role</span></span>

## <span data-ttu-id="3b91e-172">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b91e-172">RELATED LINKS</span></span>

