---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchComputeNodeUser.md
ms.openlocfilehash: a57707b10fc103e860fe579e75d7d4ad09cfd0e3
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93913146"
---
# <span data-ttu-id="c4a16-101">Remove-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="c4a16-101">Remove-AzBatchComputeNodeUser</span></span>

## <span data-ttu-id="c4a16-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c4a16-102">SYNOPSIS</span></span>
<span data-ttu-id="c4a16-103">Удаление учетной записи пользователя из пакетно-вычисляемого узла.</span><span class="sxs-lookup"><span data-stu-id="c4a16-103">Deletes a user account from a Batch compute node.</span></span>

## <span data-ttu-id="c4a16-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c4a16-104">SYNTAX</span></span>

```
Remove-AzBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4a16-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4a16-105">DESCRIPTION</span></span>
<span data-ttu-id="c4a16-106">Командлет **Remove-AzBatchComputeNodeUser** удаляет учетную запись пользователя из пакетного узла Azure recomputeing Node.</span><span class="sxs-lookup"><span data-stu-id="c4a16-106">The **Remove-AzBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="c4a16-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c4a16-107">EXAMPLES</span></span>

### <span data-ttu-id="c4a16-108">Пример 1: Удаление пользователя из вычислительного узла без подтверждения</span><span class="sxs-lookup"><span data-stu-id="c4a16-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="c4a16-109">Эта команда удаляет пользователя с именем User14 из COMPUTE node с именем ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="c4a16-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="c4a16-110">Вычислительный узел находится в пуле с именем Pool01.</span><span class="sxs-lookup"><span data-stu-id="c4a16-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="c4a16-111">Эта команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="c4a16-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="c4a16-112">Таким образом, команда не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="c4a16-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="c4a16-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c4a16-113">PARAMETERS</span></span>

### <span data-ttu-id="c4a16-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c4a16-114">-BatchContext</span></span>
<span data-ttu-id="c4a16-115">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="c4a16-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c4a16-116">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="c4a16-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="c4a16-117">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="c4a16-117">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="c4a16-118">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="c4a16-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="c4a16-119">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="c4a16-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="c4a16-120">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="c4a16-120">-ComputeNodeId</span></span>
<span data-ttu-id="c4a16-121">Указывает идентификатор вычислительного узла, на котором этот командлет удаляет учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="c4a16-121">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4a16-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4a16-122">-DefaultProfile</span></span>
<span data-ttu-id="c4a16-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c4a16-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4a16-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c4a16-124">-Name</span></span>
<span data-ttu-id="c4a16-125">Указывает имя учетной записи пользователя, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="c4a16-125">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="c4a16-126">Подстановочные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="c4a16-126">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4a16-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="c4a16-127">-PoolId</span></span>
<span data-ttu-id="c4a16-128">Указывает идентификатор пула, который содержит вычислительный узел, на который нужно удалить учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="c4a16-128">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

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

### <span data-ttu-id="c4a16-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4a16-129">-Confirm</span></span>
<span data-ttu-id="c4a16-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c4a16-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4a16-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4a16-131">-WhatIf</span></span>
<span data-ttu-id="c4a16-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c4a16-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4a16-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c4a16-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4a16-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4a16-134">CommonParameters</span></span>
<span data-ttu-id="c4a16-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c4a16-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4a16-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4a16-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4a16-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c4a16-137">INPUTS</span></span>

### <span data-ttu-id="c4a16-138">System. String</span><span class="sxs-lookup"><span data-stu-id="c4a16-138">System.String</span></span>

### <span data-ttu-id="c4a16-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c4a16-139">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c4a16-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4a16-140">OUTPUTS</span></span>

### <span data-ttu-id="c4a16-141">System. void</span><span class="sxs-lookup"><span data-stu-id="c4a16-141">System.Void</span></span>

## <span data-ttu-id="c4a16-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="c4a16-142">NOTES</span></span>

## <span data-ttu-id="c4a16-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4a16-143">RELATED LINKS</span></span>

[<span data-ttu-id="c4a16-144">New-AzBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="c4a16-144">New-AzBatchComputeNodeUser</span></span>](./New-AzBatchComputeNodeUser.md)

[<span data-ttu-id="c4a16-145">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c4a16-145">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="c4a16-146">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="c4a16-146">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


