---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJob.md
ms.openlocfilehash: be73b757bf20a2f688d7f7293ac4022e7bc8f4aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565927"
---
# <span data-ttu-id="54bfa-101">Enable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="54bfa-101">Enable-AzureBatchJob</span></span>

## <span data-ttu-id="54bfa-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="54bfa-102">SYNOPSIS</span></span>
<span data-ttu-id="54bfa-103">Включает пакетное задание.</span><span class="sxs-lookup"><span data-stu-id="54bfa-103">Enables a Batch job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54bfa-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="54bfa-104">SYNTAX</span></span>

```
Enable-AzureBatchJob [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="54bfa-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54bfa-105">DESCRIPTION</span></span>
<span data-ttu-id="54bfa-106">Командлет **Enable-AzureBatchJob** включает пакетное задание Azure.</span><span class="sxs-lookup"><span data-stu-id="54bfa-106">The **Enable-AzureBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="54bfa-107">После включения задания может выполняться новая задача.</span><span class="sxs-lookup"><span data-stu-id="54bfa-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="54bfa-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="54bfa-108">EXAMPLES</span></span>

### <span data-ttu-id="54bfa-109">Пример 1: Включение пакетного задания</span><span class="sxs-lookup"><span data-stu-id="54bfa-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzureBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="54bfa-110">Эта команда включает задание с ИД задания-000001.</span><span class="sxs-lookup"><span data-stu-id="54bfa-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="54bfa-111">Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="54bfa-111">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="54bfa-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="54bfa-112">PARAMETERS</span></span>

### <span data-ttu-id="54bfa-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="54bfa-113">-BatchContext</span></span>
<span data-ttu-id="54bfa-114">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="54bfa-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="54bfa-115">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="54bfa-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="54bfa-116">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="54bfa-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="54bfa-117">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="54bfa-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="54bfa-118">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="54bfa-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="54bfa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54bfa-119">-DefaultProfile</span></span>
<span data-ttu-id="54bfa-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="54bfa-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54bfa-121">-ID</span><span class="sxs-lookup"><span data-stu-id="54bfa-121">-Id</span></span>
<span data-ttu-id="54bfa-122">Указывает ИД задания, которое включает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="54bfa-122">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="54bfa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54bfa-123">CommonParameters</span></span>
<span data-ttu-id="54bfa-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="54bfa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54bfa-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54bfa-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54bfa-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="54bfa-126">INPUTS</span></span>

### <span data-ttu-id="54bfa-127">System. String</span><span class="sxs-lookup"><span data-stu-id="54bfa-127">System.String</span></span>

### <span data-ttu-id="54bfa-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="54bfa-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="54bfa-129">Параметры: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="54bfa-129">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="54bfa-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="54bfa-130">OUTPUTS</span></span>

### <span data-ttu-id="54bfa-131">System. void</span><span class="sxs-lookup"><span data-stu-id="54bfa-131">System.Void</span></span>

## <span data-ttu-id="54bfa-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="54bfa-132">NOTES</span></span>

## <span data-ttu-id="54bfa-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54bfa-133">RELATED LINKS</span></span>

[<span data-ttu-id="54bfa-134">Disable-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="54bfa-134">Disable-AzureBatchJob</span></span>](./Disable-AzureBatchJob.md)

[<span data-ttu-id="54bfa-135">Get-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="54bfa-135">Get-AzureBatchJob</span></span>](./Get-AzureBatchJob.md)

[<span data-ttu-id="54bfa-136">New-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="54bfa-136">New-AzureBatchJob</span></span>](./New-AzureBatchJob.md)

[<span data-ttu-id="54bfa-137">Remove-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="54bfa-137">Remove-AzureBatchJob</span></span>](./Remove-AzureBatchJob.md)

[<span data-ttu-id="54bfa-138">Остановить-AzureBatchJob</span><span class="sxs-lookup"><span data-stu-id="54bfa-138">Stop-AzureBatchJob</span></span>](./Stop-AzureBatchJob.md)

[<span data-ttu-id="54bfa-139">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="54bfa-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


