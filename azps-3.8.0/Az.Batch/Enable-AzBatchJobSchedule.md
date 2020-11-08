---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 02F91510-F14F-4401-BC5F-06B0874AEB4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJobSchedule.md
ms.openlocfilehash: 0684652dd5e5a0232e5808119ae8453be8f9ade8
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94077184"
---
# <span data-ttu-id="ba3f4-101">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ba3f4-101">Enable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="ba3f4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ba3f4-102">SYNOPSIS</span></span>
<span data-ttu-id="ba3f4-103">Включает расписание пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="ba3f4-103">Enables a Batch job schedule.</span></span>

## <span data-ttu-id="ba3f4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ba3f4-104">SYNTAX</span></span>

```
Enable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba3f4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba3f4-105">DESCRIPTION</span></span>
<span data-ttu-id="ba3f4-106">Командлет **Enable-AzBatchJobSchedule** включает расписание пакетного задания Azure.</span><span class="sxs-lookup"><span data-stu-id="ba3f4-106">The **Enable-AzBatchJobSchedule** cmdlet enables an Azure Batch job schedule.</span></span>
<span data-ttu-id="ba3f4-107">После включения расписания задания можно создавать задания в соответствии с этим расписанием.</span><span class="sxs-lookup"><span data-stu-id="ba3f4-107">After you enable a job schedule, jobs can be created according to that schedule.</span></span>

## <span data-ttu-id="ba3f4-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ba3f4-108">EXAMPLES</span></span>

### <span data-ttu-id="ba3f4-109">Пример 1: включение расписания задания</span><span class="sxs-lookup"><span data-stu-id="ba3f4-109">Example 1: Enable a job schedule</span></span>
```
PS C:\>Enable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="ba3f4-110">Эта команда включает расписание задания с ИДЕНТИФИКАТОРом JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="ba3f4-110">This command enables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="ba3f4-111">Используйте командлет **Get-AzBatchAccountKey** , чтобы назначить контекст переменной $context.</span><span class="sxs-lookup"><span data-stu-id="ba3f4-111">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="ba3f4-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ba3f4-112">PARAMETERS</span></span>

### <span data-ttu-id="ba3f4-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ba3f4-113">-BatchContext</span></span>
<span data-ttu-id="ba3f4-114">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="ba3f4-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ba3f4-115">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="ba3f4-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ba3f4-116">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="ba3f4-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ba3f4-117">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="ba3f4-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ba3f4-118">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="ba3f4-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ba3f4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba3f4-119">-DefaultProfile</span></span>
<span data-ttu-id="ba3f4-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ba3f4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba3f4-121">-ID</span><span class="sxs-lookup"><span data-stu-id="ba3f4-121">-Id</span></span>
<span data-ttu-id="ba3f4-122">Указывает идентификатор расписания задания, который включает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ba3f4-122">Specifies the ID of the job schedule that this cmdlet enables.</span></span>

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

### <span data-ttu-id="ba3f4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba3f4-123">CommonParameters</span></span>
<span data-ttu-id="ba3f4-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ba3f4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba3f4-125">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ba3f4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba3f4-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ba3f4-126">INPUTS</span></span>

### <span data-ttu-id="ba3f4-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ba3f4-127">System.String</span></span>

### <span data-ttu-id="ba3f4-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ba3f4-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ba3f4-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba3f4-129">OUTPUTS</span></span>

### <span data-ttu-id="ba3f4-130">System. void</span><span class="sxs-lookup"><span data-stu-id="ba3f4-130">System.Void</span></span>

## <span data-ttu-id="ba3f4-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="ba3f4-131">NOTES</span></span>

## <span data-ttu-id="ba3f4-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba3f4-132">RELATED LINKS</span></span>

[<span data-ttu-id="ba3f4-133">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ba3f4-133">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="ba3f4-134">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ba3f4-134">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ba3f4-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ba3f4-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="ba3f4-136">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ba3f4-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="ba3f4-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ba3f4-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="ba3f4-138">Остановить-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="ba3f4-138">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="ba3f4-139">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="ba3f4-139">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)

