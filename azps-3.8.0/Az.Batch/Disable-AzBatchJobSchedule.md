---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B4737AE8-F57C-4B95-B81E-74802EF8E7AE
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchJobSchedule.md
ms.openlocfilehash: 06fc7496a4e25dce8638b887a7f04afdda705261
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94077190"
---
# <span data-ttu-id="f45b2-101">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f45b2-101">Disable-AzBatchJobSchedule</span></span>

## <span data-ttu-id="f45b2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f45b2-102">SYNOPSIS</span></span>
<span data-ttu-id="f45b2-103">Отключение расписания пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="f45b2-103">Disables a Batch job schedule.</span></span>

## <span data-ttu-id="f45b2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f45b2-104">SYNTAX</span></span>

```
Disable-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f45b2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f45b2-105">DESCRIPTION</span></span>
<span data-ttu-id="f45b2-106">Командлет **Disable-AzBatchJobSchedule** отключает расписание пакетного задания Azure.</span><span class="sxs-lookup"><span data-stu-id="f45b2-106">The **Disable-AzBatchJobSchedule** cmdlet disables an Azure Batch job schedule.</span></span>
<span data-ttu-id="f45b2-107">При отключении расписания задания не создаются в соответствии с расписанием.</span><span class="sxs-lookup"><span data-stu-id="f45b2-107">If you disable a schedule, jobs are not created according to that schedule.</span></span>
<span data-ttu-id="f45b2-108">Вы можете включить отключенное расписание позже.</span><span class="sxs-lookup"><span data-stu-id="f45b2-108">You can enable a disabled schedule later.</span></span>

## <span data-ttu-id="f45b2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f45b2-109">EXAMPLES</span></span>

### <span data-ttu-id="f45b2-110">Пример 1: Отключение расписания задания</span><span class="sxs-lookup"><span data-stu-id="f45b2-110">Example 1: Disable a job schedule</span></span>
```
PS C:\>Disable-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="f45b2-111">Эта команда отключает расписание заданий с ИДЕНТИФИКАТОРом JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="f45b2-111">This command disables the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="f45b2-112">Используйте командлет **Get-AzBatchAccountKey** , чтобы назначить контекст переменной $context.</span><span class="sxs-lookup"><span data-stu-id="f45b2-112">Use the **Get-AzBatchAccountKey** cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="f45b2-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f45b2-113">PARAMETERS</span></span>

### <span data-ttu-id="f45b2-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f45b2-114">-BatchContext</span></span>
<span data-ttu-id="f45b2-115">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="f45b2-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f45b2-116">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="f45b2-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f45b2-117">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="f45b2-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f45b2-118">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="f45b2-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f45b2-119">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="f45b2-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f45b2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f45b2-120">-DefaultProfile</span></span>
<span data-ttu-id="f45b2-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f45b2-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f45b2-122">-ID</span><span class="sxs-lookup"><span data-stu-id="f45b2-122">-Id</span></span>
<span data-ttu-id="f45b2-123">Указывает идентификатор расписания задания, которое отключается этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="f45b2-123">Specifies the ID of the job schedule that this cmdlet disables.</span></span>

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

### <span data-ttu-id="f45b2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f45b2-124">CommonParameters</span></span>
<span data-ttu-id="f45b2-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f45b2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f45b2-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f45b2-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f45b2-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f45b2-127">INPUTS</span></span>

### <span data-ttu-id="f45b2-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f45b2-128">System.String</span></span>

### <span data-ttu-id="f45b2-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f45b2-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f45b2-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f45b2-130">OUTPUTS</span></span>

### <span data-ttu-id="f45b2-131">System. void</span><span class="sxs-lookup"><span data-stu-id="f45b2-131">System.Void</span></span>

## <span data-ttu-id="f45b2-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="f45b2-132">NOTES</span></span>

## <span data-ttu-id="f45b2-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f45b2-133">RELATED LINKS</span></span>

[<span data-ttu-id="f45b2-134">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f45b2-134">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="f45b2-135">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="f45b2-135">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f45b2-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f45b2-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="f45b2-137">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f45b2-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="f45b2-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f45b2-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="f45b2-139">Остановить-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="f45b2-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)

[<span data-ttu-id="f45b2-140">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="f45b2-140">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


