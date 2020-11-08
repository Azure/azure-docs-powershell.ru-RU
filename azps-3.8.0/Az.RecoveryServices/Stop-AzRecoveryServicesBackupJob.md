---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: A8FDC5A3-F309-49B3-B417-8E0A1535BAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/stop-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 6f8aa4220ec73f013ab5b1c797c0dacb5be7fde4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066083"
---
# <span data-ttu-id="86f91-101">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="86f91-101">Stop-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="86f91-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="86f91-102">SYNOPSIS</span></span>
<span data-ttu-id="86f91-103">Отменяет запущенное задание.</span><span class="sxs-lookup"><span data-stu-id="86f91-103">Cancels a running job.</span></span>

## <span data-ttu-id="86f91-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="86f91-104">SYNTAX</span></span>

### <span data-ttu-id="86f91-105">JobFilterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="86f91-105">JobFilterSet (Default)</span></span>
```
Stop-AzRecoveryServicesBackupJob [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86f91-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="86f91-106">IdFilterSet</span></span>
```
Stop-AzRecoveryServicesBackupJob [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86f91-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86f91-107">DESCRIPTION</span></span>
<span data-ttu-id="86f91-108">Командлет **Stop-AzRecoveryServicesBackupJob** отменяет существующее задание резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="86f91-108">The **Stop-AzRecoveryServicesBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="86f91-109">Используйте этот командлет для остановки задания, которое занимает слишком много времени и блокирует другие действия.</span><span class="sxs-lookup"><span data-stu-id="86f91-109">Use this cmdlet to stop a job that takes too long and blocks other activities.</span></span>
<span data-ttu-id="86f91-110">Вы можете отменить только типы заданий резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="86f91-110">You can cancel only Backup and Restore job types.</span></span>
<span data-ttu-id="86f91-111">Настройте контекст хранилища с помощью командлета Set-AzRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="86f91-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="86f91-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="86f91-112">EXAMPLES</span></span>

### <span data-ttu-id="86f91-113">Пример 1: Остановка задания архивации</span><span class="sxs-lookup"><span data-stu-id="86f91-113">Example 1: Stop a backup job</span></span>
```
PS C:\>$Job = Get-AzRecoveryServicesBackupJob -Operation Backup
PS C:\> Stop-AzRecoveryServicesBackupJob -JobID $Job.InstanceId
```

<span data-ttu-id="86f91-114">Первая команда получает задание резервного копирования, а затем сохраняет задание в переменной $Job.</span><span class="sxs-lookup"><span data-stu-id="86f91-114">The first command gets a backup job, and then stores the job in the $Job variable.</span></span>
<span data-ttu-id="86f91-115">Последняя команда останавливает задание с указанием идентификатора экземпляра задания резервного копирования в $Job.</span><span class="sxs-lookup"><span data-stu-id="86f91-115">The last command stops the job by specifying the Instance ID of the backup job in $Job.</span></span>

## <span data-ttu-id="86f91-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="86f91-116">PARAMETERS</span></span>

### <span data-ttu-id="86f91-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86f91-117">-DefaultProfile</span></span>
<span data-ttu-id="86f91-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="86f91-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86f91-119">-Job</span><span class="sxs-lookup"><span data-stu-id="86f91-119">-Job</span></span>
<span data-ttu-id="86f91-120">Указывает задание, которое отменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="86f91-120">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="86f91-121">Чтобы получить объект **BackupJob** , используйте командлет Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="86f91-121">To obtain a **BackupJob** object, use the Get-AzRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: JobFilterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86f91-122">-JobId</span><span class="sxs-lookup"><span data-stu-id="86f91-122">-JobId</span></span>
<span data-ttu-id="86f91-123">Указывает идентификатор задания, которое нужно отменить.</span><span class="sxs-lookup"><span data-stu-id="86f91-123">Specifies the ID of the job to cancel.</span></span>
<span data-ttu-id="86f91-124">Идентификатор — это свойство InstanceId объекта **BackupJob** .</span><span class="sxs-lookup"><span data-stu-id="86f91-124">The ID is the InstanceId property of a **BackupJob** object.</span></span>
<span data-ttu-id="86f91-125">Чтобы получить объект **BackupJob** , используйте Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="86f91-125">To obtain an **BackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

```yaml
Type: System.String
Parameter Sets: IdFilterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86f91-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="86f91-126">-VaultId</span></span>
<span data-ttu-id="86f91-127">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="86f91-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="86f91-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86f91-128">-Confirm</span></span>
<span data-ttu-id="86f91-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="86f91-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86f91-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86f91-130">-WhatIf</span></span>
<span data-ttu-id="86f91-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="86f91-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="86f91-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="86f91-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86f91-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86f91-133">CommonParameters</span></span>
<span data-ttu-id="86f91-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="86f91-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86f91-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="86f91-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86f91-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="86f91-136">INPUTS</span></span>

### <span data-ttu-id="86f91-137">System. String</span><span class="sxs-lookup"><span data-stu-id="86f91-137">System.String</span></span>

## <span data-ttu-id="86f91-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="86f91-138">OUTPUTS</span></span>

### <span data-ttu-id="86f91-139">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="86f91-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="86f91-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="86f91-140">NOTES</span></span>

## <span data-ttu-id="86f91-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86f91-141">RELATED LINKS</span></span>

[<span data-ttu-id="86f91-142">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="86f91-142">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="86f91-143">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="86f91-143">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)


