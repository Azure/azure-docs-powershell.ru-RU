---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
ms.openlocfilehash: 01098a20ebb754d4445a85dd5a6bb0d327453234
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565641"
---
# <span data-ttu-id="ea5d7-101">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="ea5d7-101">Remove-AzureBatchPool</span></span>

## <span data-ttu-id="ea5d7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ea5d7-102">SYNOPSIS</span></span>
<span data-ttu-id="ea5d7-103">Удаление указанного пула пакетов.</span><span class="sxs-lookup"><span data-stu-id="ea5d7-103">Deletes the specified Batch pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea5d7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ea5d7-104">SYNTAX</span></span>

```
Remove-AzureBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea5d7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea5d7-105">DESCRIPTION</span></span>
<span data-ttu-id="ea5d7-106">Командлет **Remove-AzureBatchPool** удаляет указанный пакетный пул Azure.</span><span class="sxs-lookup"><span data-stu-id="ea5d7-106">The **Remove-AzureBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="ea5d7-107">Вам будет предложено подтвердить подтверждение, если не используется параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="ea5d7-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="ea5d7-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ea5d7-108">EXAMPLES</span></span>

### <span data-ttu-id="ea5d7-109">Пример 1: Удаление пула пакетов по ИДЕНТИФИКАТОРу пула</span><span class="sxs-lookup"><span data-stu-id="ea5d7-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzureBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="ea5d7-110">Эта команда удаляет пул с ИДЕНТИФИКАТОРом MyPool.</span><span class="sxs-lookup"><span data-stu-id="ea5d7-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="ea5d7-111">Перед выполнением операции удаления пользователю будет предложено подтвердить подтверждение.</span><span class="sxs-lookup"><span data-stu-id="ea5d7-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="ea5d7-112">Пример 2: удаление всех пулов пакетов путем принудительного применения</span><span class="sxs-lookup"><span data-stu-id="ea5d7-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzureBatchPool -BatchContext $Context | Remove-AzureBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="ea5d7-113">Эта команда удаляет все пулы пакетов.</span><span class="sxs-lookup"><span data-stu-id="ea5d7-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="ea5d7-114">Так как параметр *Force* присутствует, запрос на подтверждение подавлен.</span><span class="sxs-lookup"><span data-stu-id="ea5d7-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="ea5d7-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ea5d7-115">PARAMETERS</span></span>

### <span data-ttu-id="ea5d7-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ea5d7-116">-BatchContext</span></span>
<span data-ttu-id="ea5d7-117">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="ea5d7-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ea5d7-118">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="ea5d7-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="ea5d7-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ea5d7-119">-Force</span></span>
<span data-ttu-id="ea5d7-120">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ea5d7-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ea5d7-121">-ID</span><span class="sxs-lookup"><span data-stu-id="ea5d7-121">-Id</span></span>
<span data-ttu-id="ea5d7-122">Указывает идентификатор удаляемого пула.</span><span class="sxs-lookup"><span data-stu-id="ea5d7-122">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="ea5d7-123">Подстановочные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="ea5d7-123">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="ea5d7-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea5d7-124">-Confirm</span></span>
<span data-ttu-id="ea5d7-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ea5d7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea5d7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea5d7-126">-WhatIf</span></span>
<span data-ttu-id="ea5d7-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ea5d7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea5d7-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ea5d7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea5d7-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea5d7-129">-DefaultProfile</span></span>
<span data-ttu-id="ea5d7-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ea5d7-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea5d7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea5d7-131">CommonParameters</span></span>
<span data-ttu-id="ea5d7-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ea5d7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea5d7-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea5d7-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea5d7-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ea5d7-134">INPUTS</span></span>

### <span data-ttu-id="ea5d7-135">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ea5d7-135">BatchAccountContext</span></span>
<span data-ttu-id="ea5d7-136">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="ea5d7-136">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="ea5d7-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea5d7-137">OUTPUTS</span></span>

## <span data-ttu-id="ea5d7-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="ea5d7-138">NOTES</span></span>

## <span data-ttu-id="ea5d7-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea5d7-139">RELATED LINKS</span></span>

[<span data-ttu-id="ea5d7-140">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ea5d7-140">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="ea5d7-141">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="ea5d7-141">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="ea5d7-142">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="ea5d7-142">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="ea5d7-143">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="ea5d7-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


