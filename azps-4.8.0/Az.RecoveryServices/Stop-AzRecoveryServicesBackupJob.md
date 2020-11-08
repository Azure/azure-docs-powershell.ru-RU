---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: A8FDC5A3-F309-49B3-B417-8E0A1535BAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/stop-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 41234c91d5c833f15a4914d2af2de93c9c5bf288
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079361"
---
# <span data-ttu-id="baf18-101">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="baf18-101">Stop-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="baf18-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="baf18-102">SYNOPSIS</span></span>
<span data-ttu-id="baf18-103">Отменяет запущенное задание.</span><span class="sxs-lookup"><span data-stu-id="baf18-103">Cancels a running job.</span></span>

## <span data-ttu-id="baf18-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="baf18-104">SYNTAX</span></span>

### <span data-ttu-id="baf18-105">JobFilterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="baf18-105">JobFilterSet (Default)</span></span>
```
Stop-AzRecoveryServicesBackupJob [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="baf18-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="baf18-106">IdFilterSet</span></span>
```
Stop-AzRecoveryServicesBackupJob [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="baf18-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="baf18-107">DESCRIPTION</span></span>
<span data-ttu-id="baf18-108">Командлет **Stop-AzRecoveryServicesBackupJob** отменяет существующее задание резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="baf18-108">The **Stop-AzRecoveryServicesBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="baf18-109">Используйте этот командлет для остановки задания, которое занимает слишком много времени и блокирует другие действия.</span><span class="sxs-lookup"><span data-stu-id="baf18-109">Use this cmdlet to stop a job that takes too long and blocks other activities.</span></span>
<span data-ttu-id="baf18-110">Вы можете отменить только типы заданий резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="baf18-110">You can cancel only Backup and Restore job types.</span></span>
<span data-ttu-id="baf18-111">Настройте контекст хранилища с помощью командлета Set-AzRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="baf18-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="baf18-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="baf18-112">EXAMPLES</span></span>

### <span data-ttu-id="baf18-113">Пример 1: Остановка задания архивации</span><span class="sxs-lookup"><span data-stu-id="baf18-113">Example 1: Stop a backup job</span></span>
```
PS C:\>$Job = Get-AzRecoveryServicesBackupJob -Operation Backup
PS C:\> Stop-AzRecoveryServicesBackupJob -JobID $Job.InstanceId
```

<span data-ttu-id="baf18-114">Первая команда получает задание резервного копирования, а затем сохраняет задание в переменной $Job.</span><span class="sxs-lookup"><span data-stu-id="baf18-114">The first command gets a backup job, and then stores the job in the $Job variable.</span></span>
<span data-ttu-id="baf18-115">Последняя команда останавливает задание с указанием идентификатора экземпляра задания резервного копирования в $Job.</span><span class="sxs-lookup"><span data-stu-id="baf18-115">The last command stops the job by specifying the Instance ID of the backup job in $Job.</span></span>

## <span data-ttu-id="baf18-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="baf18-116">PARAMETERS</span></span>

### <span data-ttu-id="baf18-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baf18-117">-DefaultProfile</span></span>
<span data-ttu-id="baf18-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="baf18-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="baf18-119">-Job</span><span class="sxs-lookup"><span data-stu-id="baf18-119">-Job</span></span>
<span data-ttu-id="baf18-120">Указывает задание, которое отменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="baf18-120">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="baf18-121">Чтобы получить объект **BackupJob** , используйте командлет Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="baf18-121">To obtain a **BackupJob** object, use the Get-AzRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="baf18-122">-JobId</span><span class="sxs-lookup"><span data-stu-id="baf18-122">-JobId</span></span>
<span data-ttu-id="baf18-123">Указывает идентификатор задания, которое нужно отменить.</span><span class="sxs-lookup"><span data-stu-id="baf18-123">Specifies the ID of the job to cancel.</span></span>
<span data-ttu-id="baf18-124">Идентификатор — это свойство InstanceId объекта **BackupJob** .</span><span class="sxs-lookup"><span data-stu-id="baf18-124">The ID is the InstanceId property of a **BackupJob** object.</span></span>
<span data-ttu-id="baf18-125">Чтобы получить объект **BackupJob** , используйте Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="baf18-125">To obtain an **BackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="baf18-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="baf18-126">-VaultId</span></span>
<span data-ttu-id="baf18-127">Идентификатор ARM хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="baf18-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="baf18-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="baf18-128">-Confirm</span></span>
<span data-ttu-id="baf18-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="baf18-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="baf18-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="baf18-130">-WhatIf</span></span>
<span data-ttu-id="baf18-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="baf18-131">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="baf18-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baf18-132">CommonParameters</span></span>
<span data-ttu-id="baf18-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="baf18-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baf18-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="baf18-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baf18-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="baf18-135">INPUTS</span></span>

### <span data-ttu-id="baf18-136">System. String</span><span class="sxs-lookup"><span data-stu-id="baf18-136">System.String</span></span>

## <span data-ttu-id="baf18-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="baf18-137">OUTPUTS</span></span>

### <span data-ttu-id="baf18-138">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="baf18-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="baf18-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="baf18-139">NOTES</span></span>

## <span data-ttu-id="baf18-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="baf18-140">RELATED LINKS</span></span>

[<span data-ttu-id="baf18-141">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="baf18-141">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="baf18-142">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="baf18-142">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)


