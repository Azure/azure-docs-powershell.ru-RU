---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/backup-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 4ae0f9c046cc1383dddeb790e8277dc2429b173b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505424"
---
# <span data-ttu-id="80abe-101">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="80abe-101">Backup-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="80abe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80abe-102">SYNOPSIS</span></span>

<span data-ttu-id="80abe-103">Запускает резервную копию элемента резервной копии.</span><span class="sxs-lookup"><span data-stu-id="80abe-103">Starts a backup for a Backup item.</span></span>

## <span data-ttu-id="80abe-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="80abe-104">SYNTAX</span></span>

```
Backup-AzRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>] [-BackupType <BackupType>]
 [-EnableCompression] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="80abe-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="80abe-105">DESCRIPTION</span></span>

<span data-ttu-id="80abe-106">Для **резервного копирования azRecoveryServicesBackupItem** требуется резервная копия защищенного элемента резервной копии Azure.</span><span class="sxs-lookup"><span data-stu-id="80abe-106">The **Backup-AzRecoveryServicesBackupItem** cmdlet takes an adhoc backup of protected Azure backup item.</span></span> <span data-ttu-id="80abe-107">С помощью этого cmdlet можно сделать резервную копию сразу же после того, как вы в включить защиту или запустить резервную копию в случае сбой запланированного резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="80abe-107">Using this cmdlet you can do an initial backup immediately after you enable protection or start a backup if a scheduled backup fails.</span></span> <span data-ttu-id="80abe-108">Этот cmdlet также можно использовать для настраиваемого хранения с датой окончания срока действия или без нее — параметры ссылки помогают в тексте дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="80abe-108">This cmdlet can also be used for custom retention with or without expiry date - refer parameters help text for more details.</span></span> 

## <span data-ttu-id="80abe-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="80abe-109">EXAMPLES</span></span>

### <span data-ttu-id="80abe-110">Пример 1. Запуск резервной копии элемента резервной копии</span><span class="sxs-lookup"><span data-stu-id="80abe-110">Example 1: Start a backup for a Backup item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $NamedContainer = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -FriendlyName "pstestv2vm1" -VaultId $vault.ID
PS C:\> $Item = Get-AzRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $Job = Backup-AzRecoveryServicesBackupItem -Item $Item -VaultId $vault.ID
PS C:\> $Job
Operation        Status               StartTime            EndTime                   JOBID
------------     ---------            ------               ---------                 -------
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

<span data-ttu-id="80abe-111">Первая команда получает контейнер резервной копии типа AzureVM pstestv2vm1, а затем сохраняет его в $NamedContainer переменной.</span><span class="sxs-lookup"><span data-stu-id="80abe-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>
<span data-ttu-id="80abe-112">Вторая команда получает элемент резервной копии, соответствующий контейнеру в $NamedContainer, и сохраняет его в переменной $Item.</span><span class="sxs-lookup"><span data-stu-id="80abe-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>
<span data-ttu-id="80abe-113">Последняя команда вызывает резервное копирование элемента резервного копирования в $Item.</span><span class="sxs-lookup"><span data-stu-id="80abe-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

### <span data-ttu-id="80abe-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="80abe-114">Example 2</span></span>

<span data-ttu-id="80abe-115">Запускает резервную копию элемента резервной копии.</span><span class="sxs-lookup"><span data-stu-id="80abe-115">Starts a backup for a Backup item.</span></span> <span data-ttu-id="80abe-116">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="80abe-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Backup-AzRecoveryServicesBackupItem -ExpiryDateTimeUTC <DateTime> -Item $Item -VaultId $vault.ID
```

## <span data-ttu-id="80abe-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="80abe-117">PARAMETERS</span></span>

### <span data-ttu-id="80abe-118">-BackupType</span><span class="sxs-lookup"><span data-stu-id="80abe-118">-BackupType</span></span>

<span data-ttu-id="80abe-119">Тип выполняемой резервной копии</span><span class="sxs-lookup"><span data-stu-id="80abe-119">Type of backup to be performed</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupType
Parameter Sets: (All)
Aliases:
Accepted values: Full, Differential, Log, CopyOnlyFull

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80abe-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80abe-120">-DefaultProfile</span></span>

<span data-ttu-id="80abe-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="80abe-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80abe-122">-EnableCompression</span><span class="sxs-lookup"><span data-stu-id="80abe-122">-EnableCompression</span></span>

<span data-ttu-id="80abe-123">Если требуется включение сжатия</span><span class="sxs-lookup"><span data-stu-id="80abe-123">If enabling compression is required</span></span>

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

### <span data-ttu-id="80abe-124">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="80abe-124">-ExpiryDateTimeUTC</span></span>

<span data-ttu-id="80abe-125">Время окончания срока действия для точки восстановления в качестве объекта даты и времени, если ничего не задано, для точки восстановления требуется значение по умолчанию (30 дней).</span><span class="sxs-lookup"><span data-stu-id="80abe-125">Specifies an expiry time for the Recovery point as a DateTime object, if nothing is given it takes the default value of  30 days.</span></span> <span data-ttu-id="80abe-126">Относится к VM, SQL (только для копирования только для полного типа резервной копии), резервных копий AFS.</span><span class="sxs-lookup"><span data-stu-id="80abe-126">Applicable to VM, SQL (for only Copy-only-full backup type), AFS backup items.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80abe-127">-Item</span><span class="sxs-lookup"><span data-stu-id="80abe-127">-Item</span></span>

<span data-ttu-id="80abe-128">Элемент резервной копии, для которого этот cmdlet запускает операцию резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="80abe-128">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80abe-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="80abe-129">-VaultId</span></span>

<span data-ttu-id="80abe-130">ARM ИД хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="80abe-130">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80abe-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="80abe-131">-Confirm</span></span>

<span data-ttu-id="80abe-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="80abe-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80abe-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80abe-133">-WhatIf</span></span>

<span data-ttu-id="80abe-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80abe-134">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="80abe-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80abe-135">CommonParameters</span></span>
<span data-ttu-id="80abe-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80abe-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80abe-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80abe-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80abe-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="80abe-138">INPUTS</span></span>

### <span data-ttu-id="80abe-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="80abe-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="80abe-140">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="80abe-140">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="80abe-141">System.String</span><span class="sxs-lookup"><span data-stu-id="80abe-141">System.String</span></span>

## <span data-ttu-id="80abe-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="80abe-142">OUTPUTS</span></span>

### <span data-ttu-id="80abe-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="80abe-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="80abe-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="80abe-144">NOTES</span></span>

## <span data-ttu-id="80abe-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="80abe-145">RELATED LINKS</span></span>

[<span data-ttu-id="80abe-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="80abe-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="80abe-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="80abe-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="80abe-148">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="80abe-148">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
