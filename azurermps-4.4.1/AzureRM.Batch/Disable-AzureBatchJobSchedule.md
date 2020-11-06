---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
ms.openlocfilehash: 73d80d3547ea895e5cbd35b2d514d9a757164bed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93569731"
---
# <span data-ttu-id="33a68-101">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="33a68-101">Disable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="33a68-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="33a68-102">SYNOPSIS</span></span>
<span data-ttu-id="33a68-103">Отключение расписания пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="33a68-103">Disables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33a68-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="33a68-104">SYNTAX</span></span>

```
Disable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33a68-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="33a68-105">DESCRIPTION</span></span>
<span data-ttu-id="33a68-106">Командлет **Disable-AzureBatchJobSchedule** отключает расписание пакетного задания Azure.</span><span class="sxs-lookup"><span data-stu-id="33a68-106">The **Disable-AzureBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="33a68-107">При отключении расписания задания не создаются в соответствии с расписанием.</span><span class="sxs-lookup"><span data-stu-id="33a68-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="33a68-108">Вы можете включить отключенное расписание позже.</span><span class="sxs-lookup"><span data-stu-id="33a68-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="33a68-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="33a68-109">EXAMPLES</span></span>

### <span data-ttu-id="33a68-110">Пример 1: Отключение расписания задания</span><span class="sxs-lookup"><span data-stu-id="33a68-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="33a68-111">Эта команда отключает расписание заданий с ИДЕНТИФИКАТОРом JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="33a68-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="33a68-112">Используйте командлет **Get-AzureRmBatchAccountKeys** , чтобы назначить контекст переменной $context.</span><span class="sxs-lookup"><span data-stu-id="33a68-112">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="33a68-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="33a68-113">PARAMETERS</span></span>

### <span data-ttu-id="33a68-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="33a68-114">-BatchContext</span></span>
<span data-ttu-id="33a68-115">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="33a68-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="33a68-116">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="33a68-116">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="33a68-117">-ID</span><span class="sxs-lookup"><span data-stu-id="33a68-117">-Id</span></span>
<span data-ttu-id="33a68-118">Указывает идентификатор расписания задания, которое отключается этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="33a68-118">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="33a68-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33a68-119">-DefaultProfile</span></span>
<span data-ttu-id="33a68-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="33a68-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33a68-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33a68-121">CommonParameters</span></span>
<span data-ttu-id="33a68-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="33a68-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33a68-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33a68-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33a68-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="33a68-124">INPUTS</span></span>

### <span data-ttu-id="33a68-125">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="33a68-125">BatchAccountContext</span></span>
<span data-ttu-id="33a68-126">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="33a68-126">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="33a68-127">Подстрок</span><span class="sxs-lookup"><span data-stu-id="33a68-127">String</span></span>
<span data-ttu-id="33a68-128">Параметр ID принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="33a68-128">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="33a68-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="33a68-129">OUTPUTS</span></span>

## <span data-ttu-id="33a68-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="33a68-130">NOTES</span></span>

## <span data-ttu-id="33a68-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="33a68-131">RELATED LINKS</span></span>

[<span data-ttu-id="33a68-132">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="33a68-132">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="33a68-133">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="33a68-133">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="33a68-134">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="33a68-134">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="33a68-135">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="33a68-135">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="33a68-136">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="33a68-136">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="33a68-137">Остановить-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="33a68-137">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="33a68-138">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="33a68-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


