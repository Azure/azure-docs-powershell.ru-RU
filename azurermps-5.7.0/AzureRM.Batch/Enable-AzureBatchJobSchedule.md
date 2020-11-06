---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
ms.openlocfilehash: 3081721db5cb113d48417ddf28d8a96512d27f99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568017"
---
# <span data-ttu-id="bb5b1-101">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bb5b1-101">Enable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="bb5b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bb5b1-102">SYNOPSIS</span></span>
<span data-ttu-id="bb5b1-103">Включает расписание пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="bb5b1-103">Enables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb5b1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bb5b1-104">SYNTAX</span></span>

```
Enable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb5b1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb5b1-105">DESCRIPTION</span></span>
<span data-ttu-id="bb5b1-106">Командлет **Enable-AzureBatchJobSchedule** включает расписание пакетного задания Azure.</span><span class="sxs-lookup"><span data-stu-id="bb5b1-106">The **Enable-AzureBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="bb5b1-107">После включения расписания задания можно создавать задания в соответствии с этим расписанием.</span><span class="sxs-lookup"><span data-stu-id="bb5b1-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="bb5b1-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bb5b1-108">EXAMPLES</span></span>

### <span data-ttu-id="bb5b1-109">Пример 1: включение расписания задания</span><span class="sxs-lookup"><span data-stu-id="bb5b1-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="bb5b1-110">Эта команда включает расписание задания с ИДЕНТИФИКАТОРом JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="bb5b1-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="bb5b1-111">Используйте командлет **Get-AzureRmBatchAccountKeys** , чтобы назначить контекст переменной $context.</span><span class="sxs-lookup"><span data-stu-id="bb5b1-111">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="bb5b1-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bb5b1-112">PARAMETERS</span></span>

### <span data-ttu-id="bb5b1-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="bb5b1-113">-BatchContext</span></span>
<span data-ttu-id="bb5b1-114">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="bb5b1-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bb5b1-115">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="bb5b1-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="bb5b1-116">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="bb5b1-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="bb5b1-117">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="bb5b1-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="bb5b1-118">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="bb5b1-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb5b1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb5b1-119">-DefaultProfile</span></span>
<span data-ttu-id="bb5b1-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bb5b1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb5b1-121">-ID</span><span class="sxs-lookup"><span data-stu-id="bb5b1-121">-Id</span></span>
<span data-ttu-id="bb5b1-122">Указывает идентификатор расписания задания, который включает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="bb5b1-122">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb5b1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb5b1-123">CommonParameters</span></span>
<span data-ttu-id="bb5b1-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bb5b1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb5b1-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb5b1-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb5b1-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bb5b1-126">INPUTS</span></span>

### <span data-ttu-id="bb5b1-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bb5b1-127">BatchAccountContext</span></span>
<span data-ttu-id="bb5b1-128">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="bb5b1-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="bb5b1-129">Подстрок</span><span class="sxs-lookup"><span data-stu-id="bb5b1-129">String</span></span>
<span data-ttu-id="bb5b1-130">Параметр ID принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="bb5b1-130">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="bb5b1-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bb5b1-131">OUTPUTS</span></span>

## <span data-ttu-id="bb5b1-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="bb5b1-132">NOTES</span></span>

## <span data-ttu-id="bb5b1-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bb5b1-133">RELATED LINKS</span></span>

[<span data-ttu-id="bb5b1-134">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bb5b1-134">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="bb5b1-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="bb5b1-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="bb5b1-136">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bb5b1-136">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="bb5b1-137">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bb5b1-137">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="bb5b1-138">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bb5b1-138">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="bb5b1-139">Остановить-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="bb5b1-139">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="bb5b1-140">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="bb5b1-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


