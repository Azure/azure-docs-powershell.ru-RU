---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
ms.openlocfilehash: 58ac726d722959e3ee32bce84c0abe3c771fcbcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566755"
---
# <span data-ttu-id="4fb1c-101">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4fb1c-101">Stop-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="4fb1c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4fb1c-102">SYNOPSIS</span></span>
<span data-ttu-id="4fb1c-103">Остановка пакетного задания в расписании.</span><span class="sxs-lookup"><span data-stu-id="4fb1c-103">Stops a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4fb1c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4fb1c-104">SYNTAX</span></span>

```
Stop-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fb1c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4fb1c-105">DESCRIPTION</span></span>
<span data-ttu-id="4fb1c-106">Командлет **Stop-AzureBatchJobSchedule** прекращает выполнение пакетного задания Azure.</span><span class="sxs-lookup"><span data-stu-id="4fb1c-106">The **Stop-AzureBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="4fb1c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4fb1c-107">EXAMPLES</span></span>

### <span data-ttu-id="4fb1c-108">Пример 1: остановка расписания задания</span><span class="sxs-lookup"><span data-stu-id="4fb1c-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="4fb1c-109">Эта команда останавливает расписание задач с ИДЕНТИФИКАТОРом JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="4fb1c-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="4fb1c-110">Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="4fb1c-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="4fb1c-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4fb1c-111">PARAMETERS</span></span>

### <span data-ttu-id="4fb1c-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4fb1c-112">-BatchContext</span></span>
<span data-ttu-id="4fb1c-113">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="4fb1c-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4fb1c-114">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="4fb1c-114">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4fb1c-115">-ID</span><span class="sxs-lookup"><span data-stu-id="4fb1c-115">-Id</span></span>
<span data-ttu-id="4fb1c-116">Указывает идентификатор расписания задания, которое останавливает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4fb1c-116">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4fb1c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fb1c-117">-DefaultProfile</span></span>
<span data-ttu-id="4fb1c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4fb1c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fb1c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fb1c-119">CommonParameters</span></span>
<span data-ttu-id="4fb1c-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4fb1c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fb1c-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fb1c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fb1c-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4fb1c-122">INPUTS</span></span>

### <span data-ttu-id="4fb1c-123">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4fb1c-123">BatchAccountContext</span></span>
<span data-ttu-id="4fb1c-124">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="4fb1c-124">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="4fb1c-125">Подстрок</span><span class="sxs-lookup"><span data-stu-id="4fb1c-125">String</span></span>
<span data-ttu-id="4fb1c-126">Параметр ID принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="4fb1c-126">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="4fb1c-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4fb1c-127">OUTPUTS</span></span>

## <span data-ttu-id="4fb1c-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="4fb1c-128">NOTES</span></span>

## <span data-ttu-id="4fb1c-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4fb1c-129">RELATED LINKS</span></span>

[<span data-ttu-id="4fb1c-130">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4fb1c-130">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="4fb1c-131">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4fb1c-131">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="4fb1c-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="4fb1c-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="4fb1c-133">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4fb1c-133">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="4fb1c-134">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4fb1c-134">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="4fb1c-135">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4fb1c-135">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="4fb1c-136">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="4fb1c-136">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


