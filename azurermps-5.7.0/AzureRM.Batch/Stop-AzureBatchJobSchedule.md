---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/stop-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Stop-AzureBatchJobSchedule.md
ms.openlocfilehash: 719c743281102f83c08f55093d221856be4194bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732174"
---
# <span data-ttu-id="d15e8-101">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d15e8-101">Stop-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="d15e8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d15e8-102">SYNOPSIS</span></span>
<span data-ttu-id="d15e8-103">Остановка пакетного задания в расписании.</span><span class="sxs-lookup"><span data-stu-id="d15e8-103">Stops a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d15e8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d15e8-104">SYNTAX</span></span>

```
Stop-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d15e8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d15e8-105">DESCRIPTION</span></span>
<span data-ttu-id="d15e8-106">Командлет **Stop-AzureBatchJobSchedule** прекращает выполнение пакетного задания Azure.</span><span class="sxs-lookup"><span data-stu-id="d15e8-106">The **Stop-AzureBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="d15e8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d15e8-107">EXAMPLES</span></span>

### <span data-ttu-id="d15e8-108">Пример 1: остановка расписания задания</span><span class="sxs-lookup"><span data-stu-id="d15e8-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="d15e8-109">Эта команда останавливает расписание задач с ИДЕНТИФИКАТОРом JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="d15e8-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="d15e8-110">Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="d15e8-110">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="d15e8-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d15e8-111">PARAMETERS</span></span>

### <span data-ttu-id="d15e8-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d15e8-112">-BatchContext</span></span>
<span data-ttu-id="d15e8-113">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="d15e8-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d15e8-114">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="d15e8-114">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="d15e8-115">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="d15e8-115">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="d15e8-116">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="d15e8-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="d15e8-117">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="d15e8-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="d15e8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d15e8-118">-DefaultProfile</span></span>
<span data-ttu-id="d15e8-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d15e8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d15e8-120">-ID</span><span class="sxs-lookup"><span data-stu-id="d15e8-120">-Id</span></span>
<span data-ttu-id="d15e8-121">Указывает идентификатор расписания задания, которое останавливает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d15e8-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="d15e8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d15e8-122">CommonParameters</span></span>
<span data-ttu-id="d15e8-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d15e8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d15e8-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d15e8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d15e8-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d15e8-125">INPUTS</span></span>

### <span data-ttu-id="d15e8-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d15e8-126">BatchAccountContext</span></span>
<span data-ttu-id="d15e8-127">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="d15e8-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="d15e8-128">Подстрок</span><span class="sxs-lookup"><span data-stu-id="d15e8-128">String</span></span>
<span data-ttu-id="d15e8-129">Параметр ID принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="d15e8-129">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="d15e8-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d15e8-130">OUTPUTS</span></span>

## <span data-ttu-id="d15e8-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="d15e8-131">NOTES</span></span>

## <span data-ttu-id="d15e8-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d15e8-132">RELATED LINKS</span></span>

[<span data-ttu-id="d15e8-133">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d15e8-133">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="d15e8-134">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d15e8-134">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="d15e8-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d15e8-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="d15e8-136">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d15e8-136">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="d15e8-137">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d15e8-137">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="d15e8-138">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="d15e8-138">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="d15e8-139">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="d15e8-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


