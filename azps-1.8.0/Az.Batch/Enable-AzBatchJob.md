---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
ms.openlocfilehash: 608d4aaba26b6f9631d4f1c35e889ac5a7480154
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93731905"
---
# <span data-ttu-id="f4fa5-101">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="f4fa5-101">Enable-AzBatchJob</span></span>

## <span data-ttu-id="f4fa5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f4fa5-102">SYNOPSIS</span></span>
<span data-ttu-id="f4fa5-103">Включает пакетное задание.</span><span class="sxs-lookup"><span data-stu-id="f4fa5-103">Enables a Batch job.</span></span>

## <span data-ttu-id="f4fa5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f4fa5-104">SYNTAX</span></span>

```
Enable-AzBatchJob [-Id] <String> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f4fa5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4fa5-105">DESCRIPTION</span></span>
<span data-ttu-id="f4fa5-106">Командлет **Enable-AzBatchJob** включает пакетное задание Azure.</span><span class="sxs-lookup"><span data-stu-id="f4fa5-106">The **Enable-AzBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="f4fa5-107">После включения задания может выполняться новая задача.</span><span class="sxs-lookup"><span data-stu-id="f4fa5-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="f4fa5-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f4fa5-108">EXAMPLES</span></span>

### <span data-ttu-id="f4fa5-109">Пример 1: Включение пакетного задания</span><span class="sxs-lookup"><span data-stu-id="f4fa5-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="f4fa5-110">Эта команда включает задание с ИД задания-000001.</span><span class="sxs-lookup"><span data-stu-id="f4fa5-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="f4fa5-111">Используйте командлет Get-AzBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="f4fa5-111">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="f4fa5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f4fa5-112">PARAMETERS</span></span>

### <span data-ttu-id="f4fa5-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f4fa5-113">-BatchContext</span></span>
<span data-ttu-id="f4fa5-114">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="f4fa5-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f4fa5-115">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="f4fa5-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f4fa5-116">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="f4fa5-116">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f4fa5-117">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="f4fa5-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f4fa5-118">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="f4fa5-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f4fa5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4fa5-119">-DefaultProfile</span></span>
<span data-ttu-id="f4fa5-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4fa5-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4fa5-121">-ID</span><span class="sxs-lookup"><span data-stu-id="f4fa5-121">-Id</span></span>
<span data-ttu-id="f4fa5-122">Указывает ИД задания, которое включает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f4fa5-122">Specifies the ID of the job that this cmdlet enables.</span></span>

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

### <span data-ttu-id="f4fa5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4fa5-123">CommonParameters</span></span>
<span data-ttu-id="f4fa5-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f4fa5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4fa5-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4fa5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4fa5-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f4fa5-126">INPUTS</span></span>

### <span data-ttu-id="f4fa5-127">System. String</span><span class="sxs-lookup"><span data-stu-id="f4fa5-127">System.String</span></span>

### <span data-ttu-id="f4fa5-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f4fa5-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f4fa5-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4fa5-129">OUTPUTS</span></span>

### <span data-ttu-id="f4fa5-130">System. void</span><span class="sxs-lookup"><span data-stu-id="f4fa5-130">System.Void</span></span>

## <span data-ttu-id="f4fa5-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="f4fa5-131">NOTES</span></span>

## <span data-ttu-id="f4fa5-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4fa5-132">RELATED LINKS</span></span>

[<span data-ttu-id="f4fa5-133">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="f4fa5-133">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="f4fa5-134">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="f4fa5-134">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="f4fa5-135">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="f4fa5-135">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="f4fa5-136">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="f4fa5-136">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="f4fa5-137">Остановить-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="f4fa5-137">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="f4fa5-138">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="f4fa5-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


