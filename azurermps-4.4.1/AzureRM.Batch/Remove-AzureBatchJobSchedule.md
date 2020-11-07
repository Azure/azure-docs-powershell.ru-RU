---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
ms.openlocfilehash: 673d9e5034b1e7c97d3b6b7cfdd6f89e9a79a34f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732770"
---
# <span data-ttu-id="a351e-101">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a351e-101">Remove-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="a351e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a351e-102">SYNOPSIS</span></span>
<span data-ttu-id="a351e-103">Удаляет расписание пакетного задания.</span><span class="sxs-lookup"><span data-stu-id="a351e-103">Removes a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a351e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a351e-104">SYNTAX</span></span>

```
Remove-AzureBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a351e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a351e-105">DESCRIPTION</span></span>
<span data-ttu-id="a351e-106">Командлет **Remove-AzureBatchJobSchedule** Удаляет расписание пакетного задания Azure.</span><span class="sxs-lookup"><span data-stu-id="a351e-106">The **Remove-AzureBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="a351e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a351e-107">EXAMPLES</span></span>

## <span data-ttu-id="a351e-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a351e-108">PARAMETERS</span></span>

### <span data-ttu-id="a351e-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a351e-109">-BatchContext</span></span>
<span data-ttu-id="a351e-110">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="a351e-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a351e-111">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="a351e-111">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="a351e-112">-Force</span><span class="sxs-lookup"><span data-stu-id="a351e-112">-Force</span></span>
<span data-ttu-id="a351e-113">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="a351e-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a351e-114">-ID</span><span class="sxs-lookup"><span data-stu-id="a351e-114">-Id</span></span>
<span data-ttu-id="a351e-115">Указывает идентификатор расписания задания, которое нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="a351e-115">Specifies the ID of the job schedule to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a351e-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a351e-116">-Confirm</span></span>
<span data-ttu-id="a351e-117">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a351e-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a351e-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a351e-118">-WhatIf</span></span>
<span data-ttu-id="a351e-119">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a351e-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a351e-120">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a351e-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a351e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a351e-121">-DefaultProfile</span></span>
<span data-ttu-id="a351e-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a351e-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a351e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a351e-123">CommonParameters</span></span>
<span data-ttu-id="a351e-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a351e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a351e-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a351e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a351e-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a351e-126">INPUTS</span></span>

### <span data-ttu-id="a351e-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a351e-127">BatchAccountContext</span></span>
<span data-ttu-id="a351e-128">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="a351e-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="a351e-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a351e-129">OUTPUTS</span></span>

## <span data-ttu-id="a351e-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="a351e-130">NOTES</span></span>

## <span data-ttu-id="a351e-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a351e-131">RELATED LINKS</span></span>

[<span data-ttu-id="a351e-132">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a351e-132">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="a351e-133">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a351e-133">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="a351e-134">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a351e-134">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="a351e-135">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a351e-135">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="a351e-136">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a351e-136">Set-AzureBatchJobSchedule</span></span>](./Set-AzureBatchJobSchedule.md)

[<span data-ttu-id="a351e-137">Остановить-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="a351e-137">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


