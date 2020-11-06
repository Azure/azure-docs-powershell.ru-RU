---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/enable-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Enable-AzureBatchJobSchedule.md
ms.openlocfilehash: e84bf86a3a784e47088ff1ed71047faac99239f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565925"
---
# <span data-ttu-id="052d4-101">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="052d4-101">Enable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="052d4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="052d4-102">SYNOPSIS</span></span>
<span data-ttu-id="052d4-103">Включает расписание пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="052d4-103">Enables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="052d4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="052d4-104">SYNTAX</span></span>

```
Enable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="052d4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="052d4-105">DESCRIPTION</span></span>
<span data-ttu-id="052d4-106">Командлет **Enable-AzureBatchJobSchedule** включает расписание пакетного задания Azure.</span><span class="sxs-lookup"><span data-stu-id="052d4-106">The **Enable-AzureBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="052d4-107">После включения расписания задания можно создавать задания в соответствии с этим расписанием.</span><span class="sxs-lookup"><span data-stu-id="052d4-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="052d4-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="052d4-108">EXAMPLES</span></span>

### <span data-ttu-id="052d4-109">Пример 1: включение расписания задания</span><span class="sxs-lookup"><span data-stu-id="052d4-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="052d4-110">Эта команда включает расписание задания с ИДЕНТИФИКАТОРом JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="052d4-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="052d4-111">Используйте командлет **Get-AzureRmBatchAccountKeys** , чтобы назначить контекст переменной $context.</span><span class="sxs-lookup"><span data-stu-id="052d4-111">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="052d4-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="052d4-112">PARAMETERS</span></span>

### <span data-ttu-id="052d4-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="052d4-113">-BatchContext</span></span>
<span data-ttu-id="052d4-114">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="052d4-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="052d4-115">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="052d4-115">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="052d4-116">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="052d4-116">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="052d4-117">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="052d4-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="052d4-118">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="052d4-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="052d4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="052d4-119">-DefaultProfile</span></span>
<span data-ttu-id="052d4-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="052d4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="052d4-121">-ID</span><span class="sxs-lookup"><span data-stu-id="052d4-121">-Id</span></span>
<span data-ttu-id="052d4-122">Указывает идентификатор расписания задания, который включает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="052d4-122">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="052d4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="052d4-123">CommonParameters</span></span>
<span data-ttu-id="052d4-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="052d4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="052d4-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="052d4-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="052d4-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="052d4-126">INPUTS</span></span>

### <span data-ttu-id="052d4-127">System. String</span><span class="sxs-lookup"><span data-stu-id="052d4-127">System.String</span></span>

### <span data-ttu-id="052d4-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="052d4-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="052d4-129">Параметры: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="052d4-129">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="052d4-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="052d4-130">OUTPUTS</span></span>

### <span data-ttu-id="052d4-131">System. void</span><span class="sxs-lookup"><span data-stu-id="052d4-131">System.Void</span></span>

## <span data-ttu-id="052d4-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="052d4-132">NOTES</span></span>

## <span data-ttu-id="052d4-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="052d4-133">RELATED LINKS</span></span>

[<span data-ttu-id="052d4-134">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="052d4-134">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="052d4-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="052d4-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="052d4-136">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="052d4-136">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="052d4-137">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="052d4-137">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="052d4-138">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="052d4-138">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="052d4-139">Остановить-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="052d4-139">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="052d4-140">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="052d4-140">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


