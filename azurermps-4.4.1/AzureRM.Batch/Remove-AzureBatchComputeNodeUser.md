---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNodeUser.md
ms.openlocfilehash: ec050d4410e50e0838512879856e6534196108af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567676"
---
# <span data-ttu-id="182d8-101">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="182d8-101">Remove-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="182d8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="182d8-102">SYNOPSIS</span></span>
<span data-ttu-id="182d8-103">Удаление учетной записи пользователя из пакетно-вычисляемого узла.</span><span class="sxs-lookup"><span data-stu-id="182d8-103">Deletes a user account from a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="182d8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="182d8-104">SYNTAX</span></span>

```
Remove-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="182d8-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="182d8-105">DESCRIPTION</span></span>
<span data-ttu-id="182d8-106">Командлет **Remove-AzureBatchComputeNodeUser** удаляет учетную запись пользователя из пакетного узла Azure recomputeing Node.</span><span class="sxs-lookup"><span data-stu-id="182d8-106">The **Remove-AzureBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="182d8-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="182d8-107">EXAMPLES</span></span>

### <span data-ttu-id="182d8-108">Пример 1: Удаление пользователя из вычислительного узла без подтверждения</span><span class="sxs-lookup"><span data-stu-id="182d8-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzureBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="182d8-109">Эта команда удаляет пользователя с именем User14 из COMPUTE node с именем ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="182d8-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="182d8-110">Вычислительный узел находится в пуле с именем Pool01.</span><span class="sxs-lookup"><span data-stu-id="182d8-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="182d8-111">Эта команда задает параметр *Force* .</span><span class="sxs-lookup"><span data-stu-id="182d8-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="182d8-112">Таким образом, команда не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="182d8-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="182d8-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="182d8-113">PARAMETERS</span></span>

### <span data-ttu-id="182d8-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="182d8-114">-BatchContext</span></span>
<span data-ttu-id="182d8-115">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="182d8-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="182d8-116">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="182d8-116">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="182d8-117">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="182d8-117">-ComputeNodeId</span></span>
<span data-ttu-id="182d8-118">Указывает идентификатор вычислительного узла, на котором этот командлет удаляет учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="182d8-118">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

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

### <span data-ttu-id="182d8-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="182d8-119">-Name</span></span>
<span data-ttu-id="182d8-120">Указывает имя учетной записи пользователя, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="182d8-120">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="182d8-121">Подстановочные знаки указывать нельзя.</span><span class="sxs-lookup"><span data-stu-id="182d8-121">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="182d8-122">-PoolId</span><span class="sxs-lookup"><span data-stu-id="182d8-122">-PoolId</span></span>
<span data-ttu-id="182d8-123">Указывает идентификатор пула, который содержит вычислительный узел, на который нужно удалить учетную запись пользователя.</span><span class="sxs-lookup"><span data-stu-id="182d8-123">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

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

### <span data-ttu-id="182d8-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="182d8-124">-Confirm</span></span>
<span data-ttu-id="182d8-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="182d8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="182d8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="182d8-126">-WhatIf</span></span>
<span data-ttu-id="182d8-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="182d8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="182d8-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="182d8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="182d8-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="182d8-129">-DefaultProfile</span></span>
<span data-ttu-id="182d8-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="182d8-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="182d8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="182d8-131">CommonParameters</span></span>
<span data-ttu-id="182d8-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="182d8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="182d8-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="182d8-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="182d8-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="182d8-134">INPUTS</span></span>

### <span data-ttu-id="182d8-135">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="182d8-135">BatchAccountContext</span></span>
<span data-ttu-id="182d8-136">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="182d8-136">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="182d8-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="182d8-137">OUTPUTS</span></span>

## <span data-ttu-id="182d8-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="182d8-138">NOTES</span></span>

## <span data-ttu-id="182d8-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="182d8-139">RELATED LINKS</span></span>

[<span data-ttu-id="182d8-140">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="182d8-140">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="182d8-141">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="182d8-141">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="182d8-142">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="182d8-142">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


