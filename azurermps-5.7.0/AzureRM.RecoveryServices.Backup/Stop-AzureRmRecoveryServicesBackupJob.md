---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: A8FDC5A3-F309-49B3-B417-8E0A1535BAF4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/stop-azurermrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Stop-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Stop-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: ba6f0ad6caee1ae5bac2e67855ef6ed5e9435068
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558907"
---
# <span data-ttu-id="9386f-101">Stop-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="9386f-101">Stop-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="9386f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9386f-102">SYNOPSIS</span></span>
<span data-ttu-id="9386f-103">Отменяет запущенное задание.</span><span class="sxs-lookup"><span data-stu-id="9386f-103">Cancels a running job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9386f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9386f-104">SYNTAX</span></span>

### <span data-ttu-id="9386f-105">JobFilterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9386f-105">JobFilterSet (Default)</span></span>
```
Stop-AzureRmRecoveryServicesBackupJob [-Job] <JobBase> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9386f-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="9386f-106">IdFilterSet</span></span>
```
Stop-AzureRmRecoveryServicesBackupJob [-JobId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9386f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9386f-107">DESCRIPTION</span></span>
<span data-ttu-id="9386f-108">Командлет **Stop-AzureRmRecoveryServicesBackupJob** отменяет существующее задание резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="9386f-108">The **Stop-AzureRmRecoveryServicesBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="9386f-109">Используйте этот командлет для остановки задания, которое занимает слишком много времени и блокирует другие действия.</span><span class="sxs-lookup"><span data-stu-id="9386f-109">Use this cmdlet to stop a job that takes too long and blocks other activities.</span></span>

<span data-ttu-id="9386f-110">Вы можете отменить только типы заданий резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="9386f-110">You can cancel only Backup and Restore job types.</span></span>

<span data-ttu-id="9386f-111">Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="9386f-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="9386f-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9386f-112">EXAMPLES</span></span>

### <span data-ttu-id="9386f-113">Пример 1: Остановка задания архивации</span><span class="sxs-lookup"><span data-stu-id="9386f-113">Example 1: Stop a backup job</span></span>
```
PS C:\>$Job = Get-AzureRmRecoveryServicesBackupJob -Operation Backup
PS C:\> Stop-AzureRmRecoveryServicesBackupJob -JobID $Job.InstanceId
```

<span data-ttu-id="9386f-114">Первая команда получает задание резервного копирования, а затем сохраняет задание в переменной $Job.</span><span class="sxs-lookup"><span data-stu-id="9386f-114">The first command gets a backup job, and then stores the job in the $Job variable.</span></span>

<span data-ttu-id="9386f-115">Последняя команда останавливает задание с указанием идентификатора экземпляра задания резервного копирования в $Job.</span><span class="sxs-lookup"><span data-stu-id="9386f-115">The last command stops the job by specifying the Instance ID of the backup job in $Job.</span></span>

## <span data-ttu-id="9386f-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9386f-116">PARAMETERS</span></span>

### <span data-ttu-id="9386f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9386f-117">-DefaultProfile</span></span>
<span data-ttu-id="9386f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9386f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9386f-119">-Job</span><span class="sxs-lookup"><span data-stu-id="9386f-119">-Job</span></span>
<span data-ttu-id="9386f-120">Указывает задание, которое отменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="9386f-120">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="9386f-121">Чтобы получить объект **BackupJob** , используйте командлет Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="9386f-121">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: JobBase
Parameter Sets: JobFilterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9386f-122">-JobId</span><span class="sxs-lookup"><span data-stu-id="9386f-122">-JobId</span></span>
<span data-ttu-id="9386f-123">Указывает идентификатор задания, которое нужно отменить.</span><span class="sxs-lookup"><span data-stu-id="9386f-123">Specifies the ID of the job to cancel.</span></span>
<span data-ttu-id="9386f-124">Идентификатор — это свойство InstanceId объекта **BackupJob** .</span><span class="sxs-lookup"><span data-stu-id="9386f-124">The ID is the InstanceId property of a **BackupJob** object.</span></span>
<span data-ttu-id="9386f-125">Чтобы получить объект **BackupJob** , используйте Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="9386f-125">To obtain an **BackupJob** object, use Get-AzureRmRecoveryServicesBackupJob.</span></span>

```yaml
Type: String
Parameter Sets: IdFilterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9386f-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9386f-126">-Confirm</span></span>
<span data-ttu-id="9386f-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9386f-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9386f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9386f-128">-WhatIf</span></span>
<span data-ttu-id="9386f-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9386f-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9386f-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9386f-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9386f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9386f-131">CommonParameters</span></span>
<span data-ttu-id="9386f-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9386f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9386f-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9386f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9386f-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9386f-134">INPUTS</span></span>

### <span data-ttu-id="9386f-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="9386f-135">None</span></span>
<span data-ttu-id="9386f-136">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="9386f-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9386f-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9386f-137">OUTPUTS</span></span>

### <span data-ttu-id="9386f-138">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="9386f-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="9386f-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="9386f-139">NOTES</span></span>

## <span data-ttu-id="9386f-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9386f-140">RELATED LINKS</span></span>

[<span data-ttu-id="9386f-141">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="9386f-141">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)

[<span data-ttu-id="9386f-142">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="9386f-142">Wait-AzureRmRecoveryServicesBackupJob</span></span>](./Wait-AzureRmRecoveryServicesBackupJob.md)


