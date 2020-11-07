---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchJobSchedule.md
ms.openlocfilehash: 0f9d20cdd1d2acabbd644fda91f5f8d22ff1ccd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734900"
---
# <span data-ttu-id="b6a67-101">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b6a67-101">Set-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="b6a67-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b6a67-102">SYNOPSIS</span></span>
<span data-ttu-id="b6a67-103">Задает расписание задания.</span><span class="sxs-lookup"><span data-stu-id="b6a67-103">Sets a job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6a67-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b6a67-104">SYNTAX</span></span>

```
Set-AzureBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6a67-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6a67-105">DESCRIPTION</span></span>
<span data-ttu-id="b6a67-106">Командлет **Set-AzureBatchJobSchedule** задает расписание заданий в пакетной службе Azure.</span><span class="sxs-lookup"><span data-stu-id="b6a67-106">The **Set-AzureBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="b6a67-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b6a67-107">EXAMPLES</span></span>

## <span data-ttu-id="b6a67-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b6a67-108">PARAMETERS</span></span>

### <span data-ttu-id="b6a67-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b6a67-109">-BatchContext</span></span>
<span data-ttu-id="b6a67-110">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="b6a67-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b6a67-111">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="b6a67-111">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="b6a67-112">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="b6a67-112">-JobSchedule</span></span>
<span data-ttu-id="b6a67-113">Указывает объект **PSCloudJobSchedule** , который представляет расписание задания.</span><span class="sxs-lookup"><span data-stu-id="b6a67-113">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="b6a67-114">Чтобы получить объект **PSCloudJobSchedule** , используйте командлет Get-AzureBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="b6a67-114">To obtain a **PSCloudJobSchedule** object, use the Get-AzureBatchJobSchedule cmdlet.</span></span>

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

### <span data-ttu-id="b6a67-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6a67-115">-DefaultProfile</span></span>
<span data-ttu-id="b6a67-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b6a67-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6a67-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6a67-117">CommonParameters</span></span>
<span data-ttu-id="b6a67-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b6a67-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6a67-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6a67-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6a67-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b6a67-120">INPUTS</span></span>

### <span data-ttu-id="b6a67-121">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b6a67-121">BatchAccountContext</span></span>
<span data-ttu-id="b6a67-122">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="b6a67-122">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="b6a67-123">PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b6a67-123">PSCloudJobSchedule</span></span>
<span data-ttu-id="b6a67-124">Параметр "JobSchedule" принимает значение типа "PSCloudJobSchedule" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="b6a67-124">Parameter 'JobSchedule' accepts value of type 'PSCloudJobSchedule' from the pipeline</span></span>

## <span data-ttu-id="b6a67-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b6a67-125">OUTPUTS</span></span>

## <span data-ttu-id="b6a67-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="b6a67-126">NOTES</span></span>

## <span data-ttu-id="b6a67-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b6a67-127">RELATED LINKS</span></span>

[<span data-ttu-id="b6a67-128">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b6a67-128">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="b6a67-129">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b6a67-129">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="b6a67-130">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b6a67-130">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="b6a67-131">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b6a67-131">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="b6a67-132">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b6a67-132">Remove-AzureBatchJobSchedule</span></span>](./Remove-AzureBatchJobSchedule.md)

[<span data-ttu-id="b6a67-133">Остановить-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="b6a67-133">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


