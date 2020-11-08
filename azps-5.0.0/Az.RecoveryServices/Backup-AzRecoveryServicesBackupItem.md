---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/backup-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 4ae0f9c046cc1383dddeb790e8277dc2429b173b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247554"
---
# <span data-ttu-id="420bc-101">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="420bc-101">Backup-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="420bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="420bc-102">SYNOPSIS</span></span>

<span data-ttu-id="420bc-103">Запуск резервного копирования для элемента резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="420bc-103">Starts a backup for a Backup item.</span></span>

## <span data-ttu-id="420bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="420bc-104">SYNTAX</span></span>

```
Backup-AzRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>] [-BackupType <BackupType>]
 [-EnableCompression] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="420bc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="420bc-105">DESCRIPTION</span></span>

<span data-ttu-id="420bc-106">Командлет **BACKUP-AzRecoveryServicesBackupItem** задействует нерегламентированное резервное копирование защищенного элемента резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="420bc-106">The **Backup-AzRecoveryServicesBackupItem** cmdlet takes an adhoc backup of protected Azure backup item.</span></span> <span data-ttu-id="420bc-107">С помощью этого командлета вы можете немедленно выполнить начальную архивацию, когда вы включите защиту или начнете создание резервной копии в случае сбоя архивации по расписанию.</span><span class="sxs-lookup"><span data-stu-id="420bc-107">Using this cmdlet you can do an initial backup immediately after you enable protection or start a backup if a scheduled backup fails.</span></span> <span data-ttu-id="420bc-108">Этот командлет также можно использовать для настраиваемого хранения с датой окончания срока действия (или без нее). Дополнительные сведения можно найти в тексте справки.</span><span class="sxs-lookup"><span data-stu-id="420bc-108">This cmdlet can also be used for custom retention with or without expiry date - refer parameters help text for more details.</span></span> 

## <span data-ttu-id="420bc-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="420bc-109">EXAMPLES</span></span>

### <span data-ttu-id="420bc-110">Пример 1: Начало резервного копирования для элемента резервного копирования</span><span class="sxs-lookup"><span data-stu-id="420bc-110">Example 1: Start a backup for a Backup item</span></span>

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

<span data-ttu-id="420bc-111">Первая команда получает контейнер резервного копирования типа AzureVM с именем pstestv2vm1 и сохраняет его в переменной $NamedContainer.</span><span class="sxs-lookup"><span data-stu-id="420bc-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>
<span data-ttu-id="420bc-112">Вторая команда возвращает элемент резервного копирования, соответствующий контейнеру в $NamedContainer, и сохраняет его в переменной $Item.</span><span class="sxs-lookup"><span data-stu-id="420bc-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>
<span data-ttu-id="420bc-113">Последняя команда запускает задание резервного копирования для элемента резервного копирования в $Item.</span><span class="sxs-lookup"><span data-stu-id="420bc-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

### <span data-ttu-id="420bc-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="420bc-114">Example 2</span></span>

<span data-ttu-id="420bc-115">Запуск резервного копирования для элемента резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="420bc-115">Starts a backup for a Backup item.</span></span> <span data-ttu-id="420bc-116">(автоматически сформированные)</span><span class="sxs-lookup"><span data-stu-id="420bc-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Backup-AzRecoveryServicesBackupItem -ExpiryDateTimeUTC <DateTime> -Item $Item -VaultId $vault.ID
```

## <span data-ttu-id="420bc-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="420bc-117">PARAMETERS</span></span>

### <span data-ttu-id="420bc-118">-BackupType</span><span class="sxs-lookup"><span data-stu-id="420bc-118">-BackupType</span></span>

<span data-ttu-id="420bc-119">Тип резервной копии, которую нужно выполнить</span><span class="sxs-lookup"><span data-stu-id="420bc-119">Type of backup to be performed</span></span>

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

### <span data-ttu-id="420bc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="420bc-120">-DefaultProfile</span></span>

<span data-ttu-id="420bc-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="420bc-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="420bc-122">-EnableCompression</span><span class="sxs-lookup"><span data-stu-id="420bc-122">-EnableCompression</span></span>

<span data-ttu-id="420bc-123">Если требуется включить сжатие</span><span class="sxs-lookup"><span data-stu-id="420bc-123">If enabling compression is required</span></span>

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

### <span data-ttu-id="420bc-124">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="420bc-124">-ExpiryDateTimeUTC</span></span>

<span data-ttu-id="420bc-125">Задает время истечения срока действия точки восстановления в качестве объекта DateTime, если не задано значение по умолчанию, которое составляет 30 дней.</span><span class="sxs-lookup"><span data-stu-id="420bc-125">Specifies an expiry time for the Recovery point as a DateTime object, if nothing is given it takes the default value of  30 days.</span></span> <span data-ttu-id="420bc-126">Применимо к ВМ, SQL (только для типа "только для копирования-полного резервного копирования"), элементов резервного копирования AFS.</span><span class="sxs-lookup"><span data-stu-id="420bc-126">Applicable to VM, SQL (for only Copy-only-full backup type), AFS backup items.</span></span>

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

### <span data-ttu-id="420bc-127">-Item</span><span class="sxs-lookup"><span data-stu-id="420bc-127">-Item</span></span>

<span data-ttu-id="420bc-128">Указывает элемент резервного копирования, для которого этот командлет запускает операцию резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="420bc-128">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

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

### <span data-ttu-id="420bc-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="420bc-129">-VaultId</span></span>

<span data-ttu-id="420bc-130">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="420bc-130">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="420bc-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="420bc-131">-Confirm</span></span>

<span data-ttu-id="420bc-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="420bc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="420bc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="420bc-133">-WhatIf</span></span>

<span data-ttu-id="420bc-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="420bc-134">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="420bc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="420bc-135">CommonParameters</span></span>
<span data-ttu-id="420bc-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="420bc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="420bc-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="420bc-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="420bc-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="420bc-138">INPUTS</span></span>

### <span data-ttu-id="420bc-139">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="420bc-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="420bc-140">System. Nullable "1 [[System. DateTime, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="420bc-140">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="420bc-141">System. String</span><span class="sxs-lookup"><span data-stu-id="420bc-141">System.String</span></span>

## <span data-ttu-id="420bc-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="420bc-142">OUTPUTS</span></span>

### <span data-ttu-id="420bc-143">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="420bc-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="420bc-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="420bc-144">NOTES</span></span>

## <span data-ttu-id="420bc-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="420bc-145">RELATED LINKS</span></span>

[<span data-ttu-id="420bc-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="420bc-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="420bc-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="420bc-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="420bc-148">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="420bc-148">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
