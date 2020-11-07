---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
ms.openlocfilehash: 665d7b64f3e8d83dd45ebc8de0cc36da960f8c35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734905"
---
# <span data-ttu-id="10716-101">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="10716-101">Enable-AzureBatchJob</span></span>

## <span data-ttu-id="10716-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="10716-102">SYNOPSIS</span></span>
<span data-ttu-id="10716-103">Включает пакетное задание.</span><span class="sxs-lookup"><span data-stu-id="10716-103">Enables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10716-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="10716-104">SYNTAX</span></span>

```
Enable-AzureBatchJob [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10716-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="10716-105">DESCRIPTION</span></span>
<span data-ttu-id="10716-106">Командлет **Enable-AzureBatchJob** включает пакетное задание Azure.</span><span class="sxs-lookup"><span data-stu-id="10716-106">The **Enable-AzureBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="10716-107">После включения задания может выполняться новая задача.</span><span class="sxs-lookup"><span data-stu-id="10716-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="10716-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="10716-108">EXAMPLES</span></span>

### <span data-ttu-id="10716-109">Пример 1: Включение пакетного задания</span><span class="sxs-lookup"><span data-stu-id="10716-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="10716-110">Эта команда включает задание с ИД задания-000001.</span><span class="sxs-lookup"><span data-stu-id="10716-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="10716-111">Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="10716-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="10716-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="10716-112">PARAMETERS</span></span>

### <span data-ttu-id="10716-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="10716-113">-BatchContext</span></span>
<span data-ttu-id="10716-114">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="10716-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="10716-115">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="10716-115">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="10716-116">-ID</span><span class="sxs-lookup"><span data-stu-id="10716-116">-Id</span></span>
<span data-ttu-id="10716-117">Указывает ИД задания, которое включает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="10716-117">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="10716-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10716-118">-DefaultProfile</span></span>
<span data-ttu-id="10716-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="10716-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10716-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10716-120">CommonParameters</span></span>
<span data-ttu-id="10716-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="10716-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10716-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10716-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10716-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="10716-123">INPUTS</span></span>

### <span data-ttu-id="10716-124">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="10716-124">BatchAccountContext</span></span>
<span data-ttu-id="10716-125">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="10716-125">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="10716-126">Подстрок</span><span class="sxs-lookup"><span data-stu-id="10716-126">String</span></span>
<span data-ttu-id="10716-127">Параметр ID принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="10716-127">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="10716-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="10716-128">OUTPUTS</span></span>

## <span data-ttu-id="10716-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="10716-129">NOTES</span></span>

## <span data-ttu-id="10716-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="10716-130">RELATED LINKS</span></span>

[<span data-ttu-id="10716-131">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="10716-131">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="10716-132">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="10716-132">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="10716-133">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="10716-133">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="10716-134">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="10716-134">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="10716-135">Остановить-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="10716-135">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="10716-136">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="10716-136">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


