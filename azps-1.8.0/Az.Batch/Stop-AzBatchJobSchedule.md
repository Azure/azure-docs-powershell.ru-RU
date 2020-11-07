---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D1C5B35C-5419-4739-9D57-6C4228E98DAC
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/stop-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Stop-AzBatchJobSchedule.md
ms.openlocfilehash: 94c4fe3292e07045382e432377111d0849db2668
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93913100"
---
# <span data-ttu-id="3bcec-101">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3bcec-101">Stop-AzBatchJobSchedule</span></span>

## <span data-ttu-id="3bcec-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3bcec-102">SYNOPSIS</span></span>
<span data-ttu-id="3bcec-103">Остановка пакетного задания в расписании.</span><span class="sxs-lookup"><span data-stu-id="3bcec-103">Stops a Batch job schedule.</span></span>

## <span data-ttu-id="3bcec-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3bcec-104">SYNTAX</span></span>

```
Stop-AzBatchJobSchedule [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bcec-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3bcec-105">DESCRIPTION</span></span>
<span data-ttu-id="3bcec-106">Командлет **Stop-AzBatchJobSchedule** прекращает выполнение пакетного задания Azure.</span><span class="sxs-lookup"><span data-stu-id="3bcec-106">The **Stop-AzBatchJobSchedule** cmdlet stops an Azure Batch job schedule.</span></span>

## <span data-ttu-id="3bcec-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3bcec-107">EXAMPLES</span></span>

### <span data-ttu-id="3bcec-108">Пример 1: остановка расписания задания</span><span class="sxs-lookup"><span data-stu-id="3bcec-108">Example 1: Stop a job schedule</span></span>
```
PS C:\>Stop-AzBatchJobSchedule -Id "JobSchedule17" -BatchContext $Context
```

<span data-ttu-id="3bcec-109">Эта команда останавливает расписание задач с ИДЕНТИФИКАТОРом JobSchedule17.</span><span class="sxs-lookup"><span data-stu-id="3bcec-109">This command stops the job schedule that has the ID JobSchedule17.</span></span>
<span data-ttu-id="3bcec-110">Используйте командлет Get-AzBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="3bcec-110">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="3bcec-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3bcec-111">PARAMETERS</span></span>

### <span data-ttu-id="3bcec-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="3bcec-112">-BatchContext</span></span>
<span data-ttu-id="3bcec-113">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="3bcec-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="3bcec-114">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="3bcec-114">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="3bcec-115">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="3bcec-115">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="3bcec-116">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="3bcec-116">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="3bcec-117">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="3bcec-117">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="3bcec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bcec-118">-DefaultProfile</span></span>
<span data-ttu-id="3bcec-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3bcec-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3bcec-120">-ID</span><span class="sxs-lookup"><span data-stu-id="3bcec-120">-Id</span></span>
<span data-ttu-id="3bcec-121">Указывает идентификатор расписания задания, которое останавливает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3bcec-121">Specifies the ID of the job schedule that this cmdlet stops.</span></span>

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

### <span data-ttu-id="3bcec-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bcec-122">CommonParameters</span></span>
<span data-ttu-id="3bcec-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3bcec-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bcec-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3bcec-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bcec-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3bcec-125">INPUTS</span></span>

### <span data-ttu-id="3bcec-126">System. String</span><span class="sxs-lookup"><span data-stu-id="3bcec-126">System.String</span></span>

### <span data-ttu-id="3bcec-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3bcec-127">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="3bcec-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3bcec-128">OUTPUTS</span></span>

### <span data-ttu-id="3bcec-129">System. void</span><span class="sxs-lookup"><span data-stu-id="3bcec-129">System.Void</span></span>

## <span data-ttu-id="3bcec-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="3bcec-130">NOTES</span></span>

## <span data-ttu-id="3bcec-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3bcec-131">RELATED LINKS</span></span>

[<span data-ttu-id="3bcec-132">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3bcec-132">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="3bcec-133">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3bcec-133">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="3bcec-134">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="3bcec-134">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="3bcec-135">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3bcec-135">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="3bcec-136">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3bcec-136">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="3bcec-137">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="3bcec-137">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="3bcec-138">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="3bcec-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


