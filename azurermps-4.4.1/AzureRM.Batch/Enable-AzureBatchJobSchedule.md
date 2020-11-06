---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
ms.openlocfilehash: c012fe266bc25752729b14192c4d9c0a42cd8961
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569723"
---
# <span data-ttu-id="063bc-101">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="063bc-101">Enable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="063bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="063bc-102">SYNOPSIS</span></span>
<span data-ttu-id="063bc-103">Включает расписание пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="063bc-103">Enables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="063bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="063bc-104">SYNTAX</span></span>

```
Enable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="063bc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="063bc-105">DESCRIPTION</span></span>
<span data-ttu-id="063bc-106">Командлет **Enable-AzureBatchJobSchedule** включает расписание пакетного задания Azure.</span><span class="sxs-lookup"><span data-stu-id="063bc-106">The **Enable-AzureBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="063bc-107">После включения расписания задания можно создавать задания в соответствии с этим расписанием.</span><span class="sxs-lookup"><span data-stu-id="063bc-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="063bc-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="063bc-108">EXAMPLES</span></span>

### <span data-ttu-id="063bc-109">Пример 1: включение расписания задания</span><span class="sxs-lookup"><span data-stu-id="063bc-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="063bc-110">Эта команда включает расписание задания с ИДЕНТИФИКАТОРом JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="063bc-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="063bc-111">Используйте командлет **Get-AzureRmBatchAccountKeys** , чтобы назначить контекст переменной $context.</span><span class="sxs-lookup"><span data-stu-id="063bc-111">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="063bc-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="063bc-112">PARAMETERS</span></span>

### <span data-ttu-id="063bc-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="063bc-113">-BatchContext</span></span>
<span data-ttu-id="063bc-114">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="063bc-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="063bc-115">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="063bc-115">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="063bc-116">-ID</span><span class="sxs-lookup"><span data-stu-id="063bc-116">-Id</span></span>
<span data-ttu-id="063bc-117">Указывает идентификатор расписания задания, который включает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="063bc-117">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="063bc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="063bc-118">-DefaultProfile</span></span>
<span data-ttu-id="063bc-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="063bc-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="063bc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="063bc-120">CommonParameters</span></span>
<span data-ttu-id="063bc-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="063bc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="063bc-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="063bc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="063bc-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="063bc-123">INPUTS</span></span>

### <span data-ttu-id="063bc-124">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="063bc-124">BatchAccountContext</span></span>
<span data-ttu-id="063bc-125">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="063bc-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="063bc-126">Подстрок</span><span class="sxs-lookup"><span data-stu-id="063bc-126">String</span></span>
<span data-ttu-id="063bc-127">Параметр ID принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="063bc-127">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="063bc-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="063bc-128">OUTPUTS</span></span>

## <span data-ttu-id="063bc-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="063bc-129">NOTES</span></span>

## <span data-ttu-id="063bc-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="063bc-130">RELATED LINKS</span></span>

[<span data-ttu-id="063bc-131">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="063bc-131">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="063bc-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="063bc-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="063bc-133">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="063bc-133">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="063bc-134">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="063bc-134">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="063bc-135">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="063bc-135">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="063bc-136">Остановить-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="063bc-136">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="063bc-137">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="063bc-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


