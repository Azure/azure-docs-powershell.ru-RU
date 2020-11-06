---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: A8FDC5A3-F309-49B3-B417-8E0A1535BAF4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Stop-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Stop-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 63d90aa5f98f6710702a70e9609c7625626e34c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568699"
---
# <span data-ttu-id="f7799-101">Stop-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="f7799-101">Stop-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="f7799-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7799-102">SYNOPSIS</span></span>
<span data-ttu-id="f7799-103">Отменяет запущенное задание.</span><span class="sxs-lookup"><span data-stu-id="f7799-103">Cancels a running job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7799-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7799-104">SYNTAX</span></span>

### <span data-ttu-id="f7799-105">JobFilterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f7799-105">JobFilterSet (Default)</span></span>
```
Stop-AzureRmRecoveryServicesBackupJob [-Job] <JobBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f7799-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="f7799-106">IdFilterSet</span></span>
```
Stop-AzureRmRecoveryServicesBackupJob [-JobId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7799-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7799-107">DESCRIPTION</span></span>
<span data-ttu-id="f7799-108">Командлет **Stop-AzureRmRecoveryServicesBackupJob** отменяет существующее задание резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="f7799-108">The **Stop-AzureRmRecoveryServicesBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="f7799-109">Используйте этот командлет для остановки задания, которое занимает слишком много времени и блокирует другие действия.</span><span class="sxs-lookup"><span data-stu-id="f7799-109">Use this cmdlet to stop a job that takes too long and blocks other activities.</span></span>

<span data-ttu-id="f7799-110">Вы можете отменить только типы заданий резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="f7799-110">You can cancel only Backup and Restore job types.</span></span>

<span data-ttu-id="f7799-111">Настройте контекст хранилища с помощью командлета Set-AzureRmRecoveryServicesVaultContext, прежде чем использовать текущий командлет.</span><span class="sxs-lookup"><span data-stu-id="f7799-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="f7799-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7799-112">EXAMPLES</span></span>

### <span data-ttu-id="f7799-113">Пример 1: Остановка задания архивации</span><span class="sxs-lookup"><span data-stu-id="f7799-113">Example 1: Stop a backup job</span></span>
```
PS C:\>$Job = Get-AzureRmRecoveryServicesBackupJob -Operation Backup
PS C:\> Stop-AzureRmRecoveryServicesBackupJob -JobID $Job.InstanceId
```

<span data-ttu-id="f7799-114">Первая команда получает задание резервного копирования, а затем сохраняет задание в переменной $Job.</span><span class="sxs-lookup"><span data-stu-id="f7799-114">The first command gets a backup job, and then stores the job in the $Job variable.</span></span>

<span data-ttu-id="f7799-115">Последняя команда останавливает задание с указанием идентификатора экземпляра задания резервного копирования в $Job.</span><span class="sxs-lookup"><span data-stu-id="f7799-115">The last command stops the job by specifying the Instance ID of the backup job in $Job.</span></span>

## <span data-ttu-id="f7799-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7799-116">PARAMETERS</span></span>

### <span data-ttu-id="f7799-117">-Job</span><span class="sxs-lookup"><span data-stu-id="f7799-117">-Job</span></span>
<span data-ttu-id="f7799-118">Указывает задание, которое отменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="f7799-118">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="f7799-119">Чтобы получить объект **BackupJob** , используйте командлет Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="f7799-119">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="f7799-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="f7799-120">-JobId</span></span>
<span data-ttu-id="f7799-121">Указывает идентификатор задания, которое нужно отменить.</span><span class="sxs-lookup"><span data-stu-id="f7799-121">Specifies the ID of the job to cancel.</span></span>
<span data-ttu-id="f7799-122">Идентификатор — это свойство InstanceId объекта **BackupJob** .</span><span class="sxs-lookup"><span data-stu-id="f7799-122">The ID is the InstanceId property of a **BackupJob** object.</span></span>
<span data-ttu-id="f7799-123">Чтобы получить объект **BackupJob** , используйте Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="f7799-123">To obtain an **BackupJob** object, use Get-AzureRmRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="f7799-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7799-124">-DefaultProfile</span></span>
<span data-ttu-id="f7799-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f7799-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7799-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7799-126">CommonParameters</span></span>
<span data-ttu-id="f7799-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7799-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7799-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7799-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7799-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7799-129">INPUTS</span></span>

## <span data-ttu-id="f7799-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7799-130">OUTPUTS</span></span>

### <span data-ttu-id="f7799-131">Microsoft. Azure. Commands. RecoveryServices. Backup. командлеты. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="f7799-131">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="f7799-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7799-132">NOTES</span></span>

## <span data-ttu-id="f7799-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7799-133">RELATED LINKS</span></span>

[<span data-ttu-id="f7799-134">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="f7799-134">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)

[<span data-ttu-id="f7799-135">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="f7799-135">Wait-AzureRmRecoveryServicesBackupJob</span></span>](./Wait-AzureRmRecoveryServicesBackupJob.md)


