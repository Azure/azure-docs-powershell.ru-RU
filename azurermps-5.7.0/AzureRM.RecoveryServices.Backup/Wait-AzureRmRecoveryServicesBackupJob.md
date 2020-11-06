---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/wait-azurermrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 651c1cd08f8a2c711a4a0cec16ddb965ccfa8211
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558903"
---
# <span data-ttu-id="d252d-101">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="d252d-101">Wait-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="d252d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d252d-102">SYNOPSIS</span></span>
<span data-ttu-id="d252d-103">Ожидание завершения задания резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="d252d-103">Waits for a Backup job to finish.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d252d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d252d-104">SYNTAX</span></span>

```
Wait-AzureRmRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d252d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d252d-105">DESCRIPTION</span></span>
<span data-ttu-id="d252d-106">Командлет **Wait-AzureRmRecoveryServicesBackupJob** ожидает завершения задания резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="d252d-106">The **Wait-AzureRmRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="d252d-107">Задания резервного копирования могут занять много времени.</span><span class="sxs-lookup"><span data-stu-id="d252d-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="d252d-108">Если вы запускаете задание резервного копирования в составе сценария, может потребоваться принудительное ожидание завершения задания, прежде чем продолжить выполнение других задач.</span><span class="sxs-lookup"><span data-stu-id="d252d-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>

<span data-ttu-id="d252d-109">Сценарий, включающий этот командлет, может быть более простым, чем тот, который опрашивает службу резервного копирования для задания состояния.</span><span class="sxs-lookup"><span data-stu-id="d252d-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>

<span data-ttu-id="d252d-110">Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="d252d-110">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="d252d-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d252d-111">EXAMPLES</span></span>

### <span data-ttu-id="d252d-112">Пример 1: ожидание завершения задания</span><span class="sxs-lookup"><span data-stu-id="d252d-112">Example 1: Wait for a job to finish</span></span>
```
PS C:\>
$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status InProgress
    $Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $Job = Get-AzureRmBackAzureRmRecoveryServicesBackupJob -Job $Job
    }
   Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="d252d-113">Этот сценарий опрашивает первое задание, которое выполняется в данный момент, пока задание не будет завершено.</span><span class="sxs-lookup"><span data-stu-id="d252d-113">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="d252d-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d252d-114">PARAMETERS</span></span>

### <span data-ttu-id="d252d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d252d-115">-DefaultProfile</span></span>
<span data-ttu-id="d252d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d252d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d252d-117">-Job</span><span class="sxs-lookup"><span data-stu-id="d252d-117">-Job</span></span>
<span data-ttu-id="d252d-118">Указывает задание, которое нужно дождаться.</span><span class="sxs-lookup"><span data-stu-id="d252d-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="d252d-119">Чтобы получить объект **BackupJob** , используйте командлет Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="d252d-119">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d252d-120">-Timeout</span><span class="sxs-lookup"><span data-stu-id="d252d-120">-Timeout</span></span>
<span data-ttu-id="d252d-121">Задает максимальное время в секундах, в течение которого этот командлет ожидает завершения задания.</span><span class="sxs-lookup"><span data-stu-id="d252d-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="d252d-122">Рекомендуется указать значение времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="d252d-122">It is recommended to specify a time-out value.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d252d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d252d-123">CommonParameters</span></span>
<span data-ttu-id="d252d-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d252d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d252d-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d252d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d252d-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d252d-126">INPUTS</span></span>

### <span data-ttu-id="d252d-127">DataObject</span><span class="sxs-lookup"><span data-stu-id="d252d-127">Object</span></span>
<span data-ttu-id="d252d-128">Параметр "задание" принимает значение типа "Object" из конвейера</span><span class="sxs-lookup"><span data-stu-id="d252d-128">Parameter 'Job' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="d252d-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d252d-129">OUTPUTS</span></span>

### <span data-ttu-id="d252d-130">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="d252d-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

### <span data-ttu-id="d252d-131">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase]</span><span class="sxs-lookup"><span data-stu-id="d252d-131">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase]</span></span>

## <span data-ttu-id="d252d-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="d252d-132">NOTES</span></span>

## <span data-ttu-id="d252d-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d252d-133">RELATED LINKS</span></span>

[<span data-ttu-id="d252d-134">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="d252d-134">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)


