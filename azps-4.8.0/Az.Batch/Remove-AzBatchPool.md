---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
ms.openlocfilehash: 575c2e8a7e510f3c8b3808b4ed6ce9169cd4f21f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079182"
---
# <span data-ttu-id="b9712-101">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="b9712-101">Remove-AzBatchPool</span></span>

## <span data-ttu-id="b9712-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b9712-102">SYNOPSIS</span></span>
<span data-ttu-id="b9712-103">Удаление указанного пула пакетов.</span><span class="sxs-lookup"><span data-stu-id="b9712-103">Deletes the specified Batch pool.</span></span>

## <span data-ttu-id="b9712-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b9712-104">SYNTAX</span></span>

```
Remove-AzBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9712-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9712-105">DESCRIPTION</span></span>
<span data-ttu-id="b9712-106">Командлет **Remove-AzBatchPool** удаляет указанный пакетный пул Azure.</span><span class="sxs-lookup"><span data-stu-id="b9712-106">The **Remove-AzBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="b9712-107">Вам будет предложено подтвердить подтверждение, если не используется параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="b9712-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="b9712-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b9712-108">EXAMPLES</span></span>

### <span data-ttu-id="b9712-109">Пример 1: Удаление пула пакетов по ИДЕНТИФИКАТОРу пула</span><span class="sxs-lookup"><span data-stu-id="b9712-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="b9712-110">Эта команда удаляет пул с ИДЕНТИФИКАТОРом MyPool.</span><span class="sxs-lookup"><span data-stu-id="b9712-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="b9712-111">Перед выполнением операции удаления пользователю будет предложено подтвердить подтверждение.</span><span class="sxs-lookup"><span data-stu-id="b9712-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="b9712-112">Пример 2: удаление всех пулов пакетов путем принудительного применения</span><span class="sxs-lookup"><span data-stu-id="b9712-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzBatchPool -BatchContext $Context | Remove-AzBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="b9712-113">Эта команда удаляет все пулы пакетов.</span><span class="sxs-lookup"><span data-stu-id="b9712-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="b9712-114">Так как параметр *Force* присутствует, запрос на подтверждение подавлен.</span><span class="sxs-lookup"><span data-stu-id="b9712-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="b9712-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b9712-115">PARAMETERS</span></span>

### <span data-ttu-id="b9712-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="b9712-116">-BatchContext</span></span>
<span data-ttu-id="b9712-117">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="b9712-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b9712-118">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="b9712-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="b9712-119">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="b9712-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="b9712-120">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="b9712-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="b9712-121">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="b9712-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="b9712-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9712-122">-DefaultProfile</span></span>
<span data-ttu-id="b9712-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b9712-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9712-124">-Force</span><span class="sxs-lookup"><span data-stu-id="b9712-124">-Force</span></span>
<span data-ttu-id="b9712-125">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="b9712-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b9712-126">-ID</span><span class="sxs-lookup"><span data-stu-id="b9712-126">-Id</span></span>
<span data-ttu-id="b9712-127">Указывает идентификатор удаляемого пула.</span><span class="sxs-lookup"><span data-stu-id="b9712-127">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="b9712-128">Подстановочные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="b9712-128">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="b9712-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b9712-129">-Confirm</span></span>
<span data-ttu-id="b9712-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b9712-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9712-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9712-131">-WhatIf</span></span>
<span data-ttu-id="b9712-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b9712-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9712-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b9712-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9712-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9712-134">CommonParameters</span></span>
<span data-ttu-id="b9712-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b9712-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9712-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9712-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9712-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b9712-137">INPUTS</span></span>

### <span data-ttu-id="b9712-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b9712-138">System.String</span></span>

### <span data-ttu-id="b9712-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b9712-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="b9712-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9712-140">OUTPUTS</span></span>

### <span data-ttu-id="b9712-141">System. void</span><span class="sxs-lookup"><span data-stu-id="b9712-141">System.Void</span></span>

## <span data-ttu-id="b9712-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="b9712-142">NOTES</span></span>

## <span data-ttu-id="b9712-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9712-143">RELATED LINKS</span></span>

[<span data-ttu-id="b9712-144">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="b9712-144">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="b9712-145">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="b9712-145">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="b9712-146">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="b9712-146">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="b9712-147">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="b9712-147">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)