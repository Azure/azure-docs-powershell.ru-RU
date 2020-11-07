---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchcomputenodeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNodeUser.md
ms.openlocfilehash: 668abe661eebfe600625ea85d5694838ef0e12f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734035"
---
# <span data-ttu-id="02a49-101">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="02a49-101">Remove-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="02a49-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="02a49-102">SYNOPSIS</span></span>
<span data-ttu-id="02a49-103">Удаление учетной записи пользователя из пакетно-вычисляемого узла.</span><span class="sxs-lookup"><span data-stu-id="02a49-103">Deletes a user account from a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02a49-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="02a49-104">SYNTAX</span></span>

```
Remove-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="02a49-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="02a49-105">DESCRIPTION</span></span>
<span data-ttu-id="02a49-106">Командлет **Remove-AzureBatchComputeNodeUser** удаляет учетную запись пользователя из пакетного узла Azure recomputeing Node.</span><span class="sxs-lookup"><span data-stu-id="02a49-106">The **Remove-AzureBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="02a49-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="02a49-107">EXAMPLES</span></span>

### <span data-ttu-id="02a49-108">Пример 1: Удаление пользователя из вычислительного узла без подтверждения</span><span class="sxs-lookup"><span data-stu-id="02a49-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzureBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="02a49-109">Эта команда удаляет пользователя с именем User14 из COMPUTE node с именем ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="02a49-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="02a49-110">Вычислительный узел находится в пуле с именем Pool01.</span><span class="sxs-lookup"><span data-stu-id="02a49-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="02a49-111">Эта команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="02a49-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="02a49-112">Таким образом, команда не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="02a49-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="02a49-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="02a49-113">PARAMETERS</span></span>

### <span data-ttu-id="02a49-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="02a49-114">-BatchContext</span></span>
<span data-ttu-id="02a49-115">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="02a49-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="02a49-116">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="02a49-116">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="02a49-117">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="02a49-117">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="02a49-118">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="02a49-118">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="02a49-119">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="02a49-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="02a49-120">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="02a49-120">-ComputeNodeId</span></span>
<span data-ttu-id="02a49-121">Указывает идентификатор вычислительного узла, на котором этот командлет удаляет учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="02a49-121">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02a49-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02a49-122">-DefaultProfile</span></span>
<span data-ttu-id="02a49-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="02a49-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02a49-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="02a49-124">-Name</span></span>
<span data-ttu-id="02a49-125">Указывает имя учетной записи пользователя, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="02a49-125">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="02a49-126">Подстановочные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="02a49-126">You cannot specify wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02a49-127">-PoolId</span><span class="sxs-lookup"><span data-stu-id="02a49-127">-PoolId</span></span>
<span data-ttu-id="02a49-128">Указывает идентификатор пула, который содержит вычислительный узел, на который нужно удалить учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="02a49-128">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

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

### <span data-ttu-id="02a49-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02a49-129">-Confirm</span></span>
<span data-ttu-id="02a49-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="02a49-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02a49-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02a49-131">-WhatIf</span></span>
<span data-ttu-id="02a49-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="02a49-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02a49-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="02a49-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02a49-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02a49-134">CommonParameters</span></span>
<span data-ttu-id="02a49-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="02a49-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02a49-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02a49-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02a49-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="02a49-137">INPUTS</span></span>

### <span data-ttu-id="02a49-138">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="02a49-138">BatchAccountContext</span></span>
<span data-ttu-id="02a49-139">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="02a49-139">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="02a49-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="02a49-140">OUTPUTS</span></span>

## <span data-ttu-id="02a49-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="02a49-141">NOTES</span></span>

## <span data-ttu-id="02a49-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="02a49-142">RELATED LINKS</span></span>

[<span data-ttu-id="02a49-143">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="02a49-143">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="02a49-144">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="02a49-144">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="02a49-145">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="02a49-145">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


