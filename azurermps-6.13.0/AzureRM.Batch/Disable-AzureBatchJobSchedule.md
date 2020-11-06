---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchJobSchedule.md
ms.openlocfilehash: e1eb586ff23f5f56cd9fc117f5039d3ccc841367
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565936"
---
# <span data-ttu-id="443ba-101">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="443ba-101">Disable-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="443ba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="443ba-102">SYNOPSIS</span></span>
<span data-ttu-id="443ba-103">Отключение расписания пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="443ba-103">Disables a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="443ba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="443ba-104">SYNTAX</span></span>

```
Disable-AzureBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="443ba-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="443ba-105">DESCRIPTION</span></span>
<span data-ttu-id="443ba-106">Командлет **Disable-AzureBatchJobSchedule** отключает расписание пакетного задания Azure.</span><span class="sxs-lookup"><span data-stu-id="443ba-106">The **Disable-AzureBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="443ba-107">При отключении расписания задания не создаются в соответствии с расписанием.</span><span class="sxs-lookup"><span data-stu-id="443ba-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="443ba-108">Вы можете включить отключенное расписание позже.</span><span class="sxs-lookup"><span data-stu-id="443ba-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="443ba-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="443ba-109">EXAMPLES</span></span>

### <span data-ttu-id="443ba-110">Пример 1: Отключение расписания задания</span><span class="sxs-lookup"><span data-stu-id="443ba-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzureBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="443ba-111">Эта команда отключает расписание заданий с ИДЕНТИФИКАТОРом JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="443ba-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="443ba-112">Используйте командлет **Get-AzureRmBatchAccountKeys** , чтобы назначить контекст переменной $context.</span><span class="sxs-lookup"><span data-stu-id="443ba-112">Use the **Get-AzureRmBatchAccountKeys** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="443ba-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="443ba-113">PARAMETERS</span></span>

### <span data-ttu-id="443ba-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="443ba-114">-BatchContext</span></span>
<span data-ttu-id="443ba-115">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="443ba-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="443ba-116">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="443ba-116">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="443ba-117">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="443ba-117">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="443ba-118">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="443ba-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="443ba-119">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="443ba-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="443ba-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="443ba-120">-DefaultProfile</span></span>
<span data-ttu-id="443ba-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="443ba-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="443ba-122">-ID</span><span class="sxs-lookup"><span data-stu-id="443ba-122">-Id</span></span>
<span data-ttu-id="443ba-123">Указывает идентификатор расписания задания, которое отключается этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="443ba-123">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="443ba-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="443ba-124">CommonParameters</span></span>
<span data-ttu-id="443ba-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="443ba-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="443ba-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="443ba-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="443ba-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="443ba-127">INPUTS</span></span>

### <span data-ttu-id="443ba-128">System. String</span><span class="sxs-lookup"><span data-stu-id="443ba-128">System.String</span></span>

### <span data-ttu-id="443ba-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="443ba-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="443ba-130">Параметры: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="443ba-130">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="443ba-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="443ba-131">OUTPUTS</span></span>

### <span data-ttu-id="443ba-132">System. void</span><span class="sxs-lookup"><span data-stu-id="443ba-132">System.Void</span></span>

## <span data-ttu-id="443ba-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="443ba-133">NOTES</span></span>

## <span data-ttu-id="443ba-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="443ba-134">RELATED LINKS</span></span>

[<span data-ttu-id="443ba-135">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="443ba-135">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="443ba-136">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="443ba-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="443ba-137">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="443ba-137">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="443ba-138">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="443ba-138">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="443ba-139">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="443ba-139">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="443ba-140">Остановить-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="443ba-140">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)

[<span data-ttu-id="443ba-141">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="443ba-141">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


