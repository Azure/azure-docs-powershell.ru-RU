---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
ms.openlocfilehash: 81ace9fd18b916f8f4788cf5878af1a620a61882
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734038"
---
# <span data-ttu-id="40382-101">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="40382-101">Enable-AzureBatchJob</span></span>

## <span data-ttu-id="40382-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="40382-102">SYNOPSIS</span></span>
<span data-ttu-id="40382-103">Включает пакетное задание.</span><span class="sxs-lookup"><span data-stu-id="40382-103">Enables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40382-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="40382-104">SYNTAX</span></span>

```
Enable-AzureBatchJob [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40382-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40382-105">DESCRIPTION</span></span>
<span data-ttu-id="40382-106">Командлет **Enable-AzureBatchJob** включает пакетное задание Azure.</span><span class="sxs-lookup"><span data-stu-id="40382-106">The **Enable-AzureBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="40382-107">После включения задания может выполняться новая задача.</span><span class="sxs-lookup"><span data-stu-id="40382-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="40382-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="40382-108">EXAMPLES</span></span>

### <span data-ttu-id="40382-109">Пример 1: Включение пакетного задания</span><span class="sxs-lookup"><span data-stu-id="40382-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="40382-110">Эта команда включает задание с ИД задания-000001.</span><span class="sxs-lookup"><span data-stu-id="40382-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="40382-111">Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="40382-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="40382-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="40382-112">PARAMETERS</span></span>

### <span data-ttu-id="40382-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="40382-113">-BatchContext</span></span>
<span data-ttu-id="40382-114">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="40382-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="40382-115">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="40382-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="40382-116">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="40382-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="40382-117">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="40382-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="40382-118">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="40382-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="40382-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40382-119">-DefaultProfile</span></span>
<span data-ttu-id="40382-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40382-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40382-121">-ID</span><span class="sxs-lookup"><span data-stu-id="40382-121">-Id</span></span>
<span data-ttu-id="40382-122">Указывает ИД задания, которое включает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="40382-122">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="40382-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40382-123">CommonParameters</span></span>
<span data-ttu-id="40382-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="40382-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40382-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40382-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40382-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="40382-126">INPUTS</span></span>

### <span data-ttu-id="40382-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="40382-127">BatchAccountContext</span></span>
<span data-ttu-id="40382-128">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="40382-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="40382-129">Подстрок</span><span class="sxs-lookup"><span data-stu-id="40382-129">String</span></span>
<span data-ttu-id="40382-130">Параметр ID принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="40382-130">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="40382-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="40382-131">OUTPUTS</span></span>

## <span data-ttu-id="40382-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="40382-132">NOTES</span></span>

## <span data-ttu-id="40382-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40382-133">RELATED LINKS</span></span>

[<span data-ttu-id="40382-134">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="40382-134">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="40382-135">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="40382-135">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="40382-136">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="40382-136">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="40382-137">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="40382-137">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="40382-138">Остановить-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="40382-138">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="40382-139">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="40382-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


