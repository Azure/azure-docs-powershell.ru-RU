---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
ms.openlocfilehash: 5e26bd47c9c53b88442505aeb66d81a96c137b1a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556811"
---
# <span data-ttu-id="83fa8-101">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="83fa8-101">Set-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="83fa8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="83fa8-102">SYNOPSIS</span></span>
<span data-ttu-id="83fa8-103">Задает расписание задания.</span><span class="sxs-lookup"><span data-stu-id="83fa8-103">Sets a job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83fa8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="83fa8-104">SYNTAX</span></span>

```
Set-AzureBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83fa8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="83fa8-105">DESCRIPTION</span></span>
<span data-ttu-id="83fa8-106">Командлет **Set-AzureBatchJobSchedule** задает расписание заданий в пакетной службе Azure.</span><span class="sxs-lookup"><span data-stu-id="83fa8-106">The **Set-AzureBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="83fa8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="83fa8-107">EXAMPLES</span></span>

## <span data-ttu-id="83fa8-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="83fa8-108">PARAMETERS</span></span>

### <span data-ttu-id="83fa8-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="83fa8-109">-BatchContext</span></span>
<span data-ttu-id="83fa8-110">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="83fa8-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="83fa8-111">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="83fa8-111">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="83fa8-112">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="83fa8-112">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="83fa8-113">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="83fa8-113">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="83fa8-114">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="83fa8-114">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="83fa8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83fa8-115">-DefaultProfile</span></span>
<span data-ttu-id="83fa8-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="83fa8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83fa8-117">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="83fa8-117">-JobSchedule</span></span>
<span data-ttu-id="83fa8-118">Указывает объект **PSCloudJobSchedule** , который представляет расписание задания.</span><span class="sxs-lookup"><span data-stu-id="83fa8-118">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="83fa8-119">Чтобы получить объект **PSCloudJobSchedule** , используйте командлет Get-AzureBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="83fa8-119">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="83fa8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83fa8-120">CommonParameters</span></span>
<span data-ttu-id="83fa8-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="83fa8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83fa8-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83fa8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83fa8-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="83fa8-123">INPUTS</span></span>

### <span data-ttu-id="83fa8-124">Microsoft.Azure.Commands.BatCH. Models. PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="83fa8-124">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>
<span data-ttu-id="83fa8-125">Параметры: JobSchedule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="83fa8-125">Parameters: JobSchedule (ByValue)</span></span>

### <span data-ttu-id="83fa8-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="83fa8-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="83fa8-127">Параметры: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="83fa8-127">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="83fa8-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="83fa8-128">OUTPUTS</span></span>

### <span data-ttu-id="83fa8-129">System. void</span><span class="sxs-lookup"><span data-stu-id="83fa8-129">System.Void</span></span>

## <span data-ttu-id="83fa8-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="83fa8-130">NOTES</span></span>

## <span data-ttu-id="83fa8-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="83fa8-131">RELATED LINKS</span></span>

[<span data-ttu-id="83fa8-132">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="83fa8-132">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="83fa8-133">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="83fa8-133">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="83fa8-134">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="83fa8-134">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="83fa8-135">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="83fa8-135">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="83fa8-136">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="83fa8-136">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="83fa8-137">Остановить-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="83fa8-137">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


