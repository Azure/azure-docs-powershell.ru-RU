---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: C5126E20-0A93-4ACE-8297-F1E8E17BEF53
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
ms.openlocfilehash: 6ee1319881b200b3fcae56e433f81460bfc90274
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568099"
---
# <span data-ttu-id="3e26e-101">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="3e26e-101">Wait-AzureRmBackupJob</span></span>

## <span data-ttu-id="3e26e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e26e-102">SYNOPSIS</span></span>
<span data-ttu-id="3e26e-103">Ожидание завершения задания резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="3e26e-103">Waits for a Backup job to finish.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e26e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e26e-104">SYNTAX</span></span>

```
Wait-AzureRmBackupJob -Job <Object> [-TimeOut <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e26e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e26e-105">DESCRIPTION</span></span>
<span data-ttu-id="3e26e-106">Командлет **Wait-AzureRmBackupJob** ожидает завершения задания резервного копирования Azure.</span><span class="sxs-lookup"><span data-stu-id="3e26e-106">The **Wait-AzureRmBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="3e26e-107">Задания резервного копирования могут занять много времени.</span><span class="sxs-lookup"><span data-stu-id="3e26e-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="3e26e-108">Если вы запускаете задание резервного копирования в составе сценария, может потребоваться принудительное ожидание завершения задания, прежде чем продолжить выполнение других задач.</span><span class="sxs-lookup"><span data-stu-id="3e26e-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>

<span data-ttu-id="3e26e-109">Сценарий, включающий этот командлет, может быть более простым, чем тот, который опрашивает службу резервного копирования для задания состояния.</span><span class="sxs-lookup"><span data-stu-id="3e26e-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>

## <span data-ttu-id="3e26e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e26e-110">EXAMPLES</span></span>

## <span data-ttu-id="3e26e-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e26e-111">PARAMETERS</span></span>

### <span data-ttu-id="3e26e-112">-Job</span><span class="sxs-lookup"><span data-stu-id="3e26e-112">-Job</span></span>
<span data-ttu-id="3e26e-113">Указывает задание, которое отменяется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="3e26e-113">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="3e26e-114">Чтобы получить объект **AzureRmBackupJob** , используйте командлет Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="3e26e-114">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="3e26e-115">-TimeOut</span><span class="sxs-lookup"><span data-stu-id="3e26e-115">-TimeOut</span></span>
<span data-ttu-id="3e26e-116">Задает максимальное время в секундах, в течение которого этот командлет ожидает завершения задания.</span><span class="sxs-lookup"><span data-stu-id="3e26e-116">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="3e26e-117">Рекомендуем указать значение времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="3e26e-117">We recommend that you specify a time-out value.</span></span>

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

### <span data-ttu-id="3e26e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e26e-118">-DefaultProfile</span></span>
<span data-ttu-id="3e26e-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3e26e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e26e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e26e-120">CommonParameters</span></span>
<span data-ttu-id="3e26e-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e26e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e26e-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e26e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e26e-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e26e-123">INPUTS</span></span>

### <span data-ttu-id="3e26e-124">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="3e26e-124">AzureRmBackupJob</span></span>

## <span data-ttu-id="3e26e-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e26e-125">OUTPUTS</span></span>

### <span data-ttu-id="3e26e-126">AzureRmBackupJob[]</span><span class="sxs-lookup"><span data-stu-id="3e26e-126">AzureRmBackupJob[]</span></span>

## <span data-ttu-id="3e26e-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e26e-127">NOTES</span></span>

## <span data-ttu-id="3e26e-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e26e-128">RELATED LINKS</span></span>

[<span data-ttu-id="3e26e-129">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="3e26e-129">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="3e26e-130">Остановить-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="3e26e-130">Stop-AzureRmBackupJob</span></span>](./Stop-AzureRmBackupJob.md)


