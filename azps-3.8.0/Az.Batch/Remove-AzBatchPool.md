---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchPool.md
ms.openlocfilehash: ce2a7c6d01af33de585d4ac8adef83d03dbd33bc
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94077205"
---
# <span data-ttu-id="41da9-101">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="41da9-101">Remove-AzBatchPool</span></span>

## <span data-ttu-id="41da9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="41da9-102">SYNOPSIS</span></span>
<span data-ttu-id="41da9-103">Удаление указанного пула пакетов.</span><span class="sxs-lookup"><span data-stu-id="41da9-103">Deletes the specified Batch pool.</span></span>

## <span data-ttu-id="41da9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="41da9-104">SYNTAX</span></span>

```
Remove-AzBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41da9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="41da9-105">DESCRIPTION</span></span>
<span data-ttu-id="41da9-106">Командлет **Remove-AzBatchPool** удаляет указанный пакетный пул Azure.</span><span class="sxs-lookup"><span data-stu-id="41da9-106">The **Remove-AzBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="41da9-107">Вам будет предложено подтвердить подтверждение, если не используется параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="41da9-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="41da9-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="41da9-108">EXAMPLES</span></span>

### <span data-ttu-id="41da9-109">Пример 1: Удаление пула пакетов по ИДЕНТИФИКАТОРу пула</span><span class="sxs-lookup"><span data-stu-id="41da9-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="41da9-110">Эта команда удаляет пул с ИДЕНТИФИКАТОРом MyPool.</span><span class="sxs-lookup"><span data-stu-id="41da9-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="41da9-111">Перед выполнением операции удаления пользователю будет предложено подтвердить подтверждение.</span><span class="sxs-lookup"><span data-stu-id="41da9-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="41da9-112">Пример 2: удаление всех пулов пакетов путем принудительного применения</span><span class="sxs-lookup"><span data-stu-id="41da9-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzBatchPool -BatchContext $Context | Remove-AzBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="41da9-113">Эта команда удаляет все пулы пакетов.</span><span class="sxs-lookup"><span data-stu-id="41da9-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="41da9-114">Так как параметр *Force* присутствует, запрос на подтверждение подавлен.</span><span class="sxs-lookup"><span data-stu-id="41da9-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="41da9-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="41da9-115">PARAMETERS</span></span>

### <span data-ttu-id="41da9-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="41da9-116">-BatchContext</span></span>
<span data-ttu-id="41da9-117">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="41da9-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="41da9-118">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="41da9-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="41da9-119">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="41da9-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="41da9-120">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="41da9-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="41da9-121">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="41da9-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="41da9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41da9-122">-DefaultProfile</span></span>
<span data-ttu-id="41da9-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="41da9-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41da9-124">-Force</span><span class="sxs-lookup"><span data-stu-id="41da9-124">-Force</span></span>
<span data-ttu-id="41da9-125">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="41da9-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="41da9-126">-ID</span><span class="sxs-lookup"><span data-stu-id="41da9-126">-Id</span></span>
<span data-ttu-id="41da9-127">Указывает идентификатор удаляемого пула.</span><span class="sxs-lookup"><span data-stu-id="41da9-127">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="41da9-128">Подстановочные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="41da9-128">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="41da9-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="41da9-129">-Confirm</span></span>
<span data-ttu-id="41da9-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="41da9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41da9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41da9-131">-WhatIf</span></span>
<span data-ttu-id="41da9-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="41da9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41da9-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="41da9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41da9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41da9-134">CommonParameters</span></span>
<span data-ttu-id="41da9-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="41da9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41da9-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="41da9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41da9-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="41da9-137">INPUTS</span></span>

### <span data-ttu-id="41da9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="41da9-138">System.String</span></span>

### <span data-ttu-id="41da9-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="41da9-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="41da9-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="41da9-140">OUTPUTS</span></span>

### <span data-ttu-id="41da9-141">System. void</span><span class="sxs-lookup"><span data-stu-id="41da9-141">System.Void</span></span>

## <span data-ttu-id="41da9-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="41da9-142">NOTES</span></span>

## <span data-ttu-id="41da9-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="41da9-143">RELATED LINKS</span></span>

[<span data-ttu-id="41da9-144">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="41da9-144">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="41da9-145">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="41da9-145">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="41da9-146">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="41da9-146">New-AzBatchPool</span></span>](./New-AzBatchPool.md)

[<span data-ttu-id="41da9-147">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="41da9-147">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


