---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
ms.openlocfilehash: a42e6876336e409cca8df9e0fc72e65e8b6e1b3f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568245"
---
# <span data-ttu-id="58ecf-101">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="58ecf-101">Remove-AzureBatchPool</span></span>

## <span data-ttu-id="58ecf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="58ecf-102">SYNOPSIS</span></span>
<span data-ttu-id="58ecf-103">Удаление указанного пула пакетов.</span><span class="sxs-lookup"><span data-stu-id="58ecf-103">Deletes the specified Batch pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58ecf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="58ecf-104">SYNTAX</span></span>

```
Remove-AzureBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58ecf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="58ecf-105">DESCRIPTION</span></span>
<span data-ttu-id="58ecf-106">Командлет **Remove-AzureBatchPool** удаляет указанный пакетный пул Azure.</span><span class="sxs-lookup"><span data-stu-id="58ecf-106">The **Remove-AzureBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="58ecf-107">Вам будет предложено подтвердить подтверждение, если не используется параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="58ecf-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="58ecf-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="58ecf-108">EXAMPLES</span></span>

### <span data-ttu-id="58ecf-109">Пример 1: Удаление пула пакетов по ИДЕНТИФИКАТОРу пула</span><span class="sxs-lookup"><span data-stu-id="58ecf-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzureBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="58ecf-110">Эта команда удаляет пул с ИДЕНТИФИКАТОРом MyPool.</span><span class="sxs-lookup"><span data-stu-id="58ecf-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="58ecf-111">Перед выполнением операции удаления пользователю будет предложено подтвердить подтверждение.</span><span class="sxs-lookup"><span data-stu-id="58ecf-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="58ecf-112">Пример 2: удаление всех пулов пакетов путем принудительного применения</span><span class="sxs-lookup"><span data-stu-id="58ecf-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzureBatchPool -BatchContext $Context | Remove-AzureBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="58ecf-113">Эта команда удаляет все пулы пакетов.</span><span class="sxs-lookup"><span data-stu-id="58ecf-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="58ecf-114">Так как параметр *Force* присутствует, запрос на подтверждение подавлен.</span><span class="sxs-lookup"><span data-stu-id="58ecf-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="58ecf-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="58ecf-115">PARAMETERS</span></span>

### <span data-ttu-id="58ecf-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="58ecf-116">-BatchContext</span></span>
<span data-ttu-id="58ecf-117">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="58ecf-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="58ecf-118">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="58ecf-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="58ecf-119">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="58ecf-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="58ecf-120">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="58ecf-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="58ecf-121">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="58ecf-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58ecf-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58ecf-122">-DefaultProfile</span></span>
<span data-ttu-id="58ecf-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="58ecf-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58ecf-124">-Force</span><span class="sxs-lookup"><span data-stu-id="58ecf-124">-Force</span></span>
<span data-ttu-id="58ecf-125">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="58ecf-125">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58ecf-126">-ID</span><span class="sxs-lookup"><span data-stu-id="58ecf-126">-Id</span></span>
<span data-ttu-id="58ecf-127">Указывает идентификатор удаляемого пула.</span><span class="sxs-lookup"><span data-stu-id="58ecf-127">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="58ecf-128">Подстановочные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="58ecf-128">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58ecf-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58ecf-129">-Confirm</span></span>
<span data-ttu-id="58ecf-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="58ecf-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58ecf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58ecf-131">-WhatIf</span></span>
<span data-ttu-id="58ecf-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="58ecf-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58ecf-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="58ecf-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58ecf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58ecf-134">CommonParameters</span></span>
<span data-ttu-id="58ecf-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="58ecf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58ecf-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58ecf-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58ecf-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="58ecf-137">INPUTS</span></span>

### <span data-ttu-id="58ecf-138">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="58ecf-138">BatchAccountContext</span></span>
<span data-ttu-id="58ecf-139">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="58ecf-139">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="58ecf-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="58ecf-140">OUTPUTS</span></span>

## <span data-ttu-id="58ecf-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="58ecf-141">NOTES</span></span>

## <span data-ttu-id="58ecf-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="58ecf-142">RELATED LINKS</span></span>

[<span data-ttu-id="58ecf-143">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="58ecf-143">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="58ecf-144">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="58ecf-144">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="58ecf-145">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="58ecf-145">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="58ecf-146">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="58ecf-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


