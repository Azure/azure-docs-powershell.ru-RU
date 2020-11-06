---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: C5126E20-0A93-4ACE-8297-F1E8E17BEF53
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/wait-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
ms.openlocfilehash: a5de80561ee0b80c2ce825db26e1de5c6f46b80b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561135"
---
# <span data-ttu-id="a72f5-101">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="a72f5-101">Wait-AzureRmBackupJob</span></span>

## <span data-ttu-id="a72f5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a72f5-102">SYNOPSIS</span></span>
<span data-ttu-id="a72f5-103">Ожидание завершения задания резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="a72f5-103">Waits for a Backup job to finish.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a72f5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a72f5-104">SYNTAX</span></span>

```
Wait-AzureRmBackupJob -Job <Object> [-TimeOut <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a72f5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a72f5-105">DESCRIPTION</span></span>
<span data-ttu-id="a72f5-106">Командлет **Wait-AzureRmBackupJob** ожидает завершения задания резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="a72f5-106">The **Wait-AzureRmBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="a72f5-107">Задания резервного копирования могут занять много времени.</span><span class="sxs-lookup"><span data-stu-id="a72f5-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="a72f5-108">Если вы запускаете задание резервного копирования в составе сценария, может потребоваться принудительное ожидание завершения задания, прежде чем продолжить выполнение других задач.</span><span class="sxs-lookup"><span data-stu-id="a72f5-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>
<span data-ttu-id="a72f5-109">Сценарий, включающий этот командлет, может быть более простым, чем тот, который опрашивает службу резервного копирования для задания состояния.</span><span class="sxs-lookup"><span data-stu-id="a72f5-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>

## <span data-ttu-id="a72f5-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a72f5-110">EXAMPLES</span></span>

## <span data-ttu-id="a72f5-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a72f5-111">PARAMETERS</span></span>

### <span data-ttu-id="a72f5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a72f5-112">-DefaultProfile</span></span>
<span data-ttu-id="a72f5-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a72f5-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a72f5-114">-Job</span><span class="sxs-lookup"><span data-stu-id="a72f5-114">-Job</span></span>
<span data-ttu-id="a72f5-115">Указывает задание, которое отменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="a72f5-115">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="a72f5-116">Чтобы получить объект **AzureRmBackupJob** , используйте командлет Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="a72f5-116">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a72f5-117">-TimeOut</span><span class="sxs-lookup"><span data-stu-id="a72f5-117">-TimeOut</span></span>
<span data-ttu-id="a72f5-118">Задает максимальное время в секундах, в течение которого этот командлет ожидает завершения задания.</span><span class="sxs-lookup"><span data-stu-id="a72f5-118">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="a72f5-119">Рекомендуем указать значение времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="a72f5-119">We recommend that you specify a time-out value.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a72f5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a72f5-120">CommonParameters</span></span>
<span data-ttu-id="a72f5-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a72f5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a72f5-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a72f5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a72f5-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a72f5-123">INPUTS</span></span>

### <span data-ttu-id="a72f5-124">System. Object</span><span class="sxs-lookup"><span data-stu-id="a72f5-124">System.Object</span></span>
<span data-ttu-id="a72f5-125">Параметры: Job (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a72f5-125">Parameters: Job (ByValue)</span></span>

## <span data-ttu-id="a72f5-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a72f5-126">OUTPUTS</span></span>

### <span data-ttu-id="a72f5-127">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="a72f5-127">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="a72f5-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="a72f5-128">NOTES</span></span>

## <span data-ttu-id="a72f5-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a72f5-129">RELATED LINKS</span></span>

[<span data-ttu-id="a72f5-130">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="a72f5-130">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="a72f5-131">Остановить-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="a72f5-131">Stop-AzureRmBackupJob</span></span>](./Stop-AzureRmBackupJob.md)


