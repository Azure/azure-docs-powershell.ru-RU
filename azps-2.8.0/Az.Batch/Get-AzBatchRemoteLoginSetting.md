---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremoteloginsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
ms.openlocfilehash: 03c37bb1cf70dfefc5373e9211d6365feb133ad4
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93913178"
---
# <span data-ttu-id="d338d-101">Get-AzBatchRemoteLoginSetting</span><span class="sxs-lookup"><span data-stu-id="d338d-101">Get-AzBatchRemoteLoginSetting</span></span>

## <span data-ttu-id="d338d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d338d-102">SYNOPSIS</span></span>
<span data-ttu-id="d338d-103">Получает параметры удаленного входа для вычислительного узла.</span><span class="sxs-lookup"><span data-stu-id="d338d-103">Gets remote logon settings for a compute node.</span></span>

## <span data-ttu-id="d338d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d338d-104">SYNTAX</span></span>

### <span data-ttu-id="d338d-105">ID (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d338d-105">Id (Default)</span></span>
```
Get-AzBatchRemoteLoginSetting [-PoolId] <String> [-ComputeNodeId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d338d-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="d338d-106">InputObject</span></span>
```
Get-AzBatchRemoteLoginSetting [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d338d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d338d-107">DESCRIPTION</span></span>
<span data-ttu-id="d338d-108">Командлет **Get-AzBatchRemoteLoginSetting** получает параметры удаленного входа для вычислительного узла в пуле на основе инфраструктуры виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="d338d-108">The **Get-AzBatchRemoteLoginSetting** cmdlet gets remote logon settings for a compute node in a virtual machines infrastructure-based pool.</span></span>

## <span data-ttu-id="d338d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d338d-109">EXAMPLES</span></span>

### <span data-ttu-id="d338d-110">Пример 1: получение параметров удаленного входа для всех узлов в пуле</span><span class="sxs-lookup"><span data-stu-id="d338d-110">Example 1: Get remote logon settings for all nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzBatchRemoteLoginSetting -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

<span data-ttu-id="d338d-111">Первая команда получает контекст учетной записи пакета, который включает клавиши доступа для вашей подписки, с помощью **Get-AzBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="d338d-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKeys**.</span></span>
<span data-ttu-id="d338d-112">Команда хранит контекст в переменной $Context для использования в следующей команде.</span><span class="sxs-lookup"><span data-stu-id="d338d-112">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="d338d-113">Вторая команда получает каждый вычислительный узел в пуле с ИД ContosoPool с помощью **Get-AzBatchComputeNode**.</span><span class="sxs-lookup"><span data-stu-id="d338d-113">The second command gets each compute node in the pool that has the ID ContosoPool by using **Get-AzBatchComputeNode**.</span></span>
<span data-ttu-id="d338d-114">Команда передает каждый узел компьютера в текущий командлет с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="d338d-114">The command passes each computer node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="d338d-115">Команда получает параметры удаленного входа для каждого вычислительного узла.</span><span class="sxs-lookup"><span data-stu-id="d338d-115">The command gets the remote logon settings for each compute node.</span></span>

### <span data-ttu-id="d338d-116">Пример 2: получение параметров удаленного входа для узла</span><span class="sxs-lookup"><span data-stu-id="d338d-116">Example 2: Get remote logon settings for a node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchRemoteLoginSetting -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

<span data-ttu-id="d338d-117">Первая команда получает контекст учетной записи пакета, который содержит клавиши доступа для вашей подписки, а затем сохраняет его в переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="d338d-117">The first command gets a batch account context that contains access keys for your subscription, and then stores it in the $Context variable.</span></span>
<span data-ttu-id="d338d-118">Вторая команда получает параметры удаленного входа для вычислительного узла с указанным ИДЕНТИФИКАТОРом в пуле с ИДЕНТИФИКАТОРом ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="d338d-118">The second command gets the remote logon settings for the compute node that has the specified ID in the pool that has the ID ContosoPool.</span></span>

## <span data-ttu-id="d338d-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d338d-119">PARAMETERS</span></span>

### <span data-ttu-id="d338d-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="d338d-120">-BatchContext</span></span>
<span data-ttu-id="d338d-121">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="d338d-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="d338d-122">Чтобы получить **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="d338d-122">To obtain a **BatchAccountContext** that contains access keys for your subscription, use the Get-AzBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="d338d-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="d338d-123">-ComputeNode</span></span>
<span data-ttu-id="d338d-124">Задает вычислительный узел, как объект **PSComputeNode** , для которого этот командлет получает параметры удаленного входа.</span><span class="sxs-lookup"><span data-stu-id="d338d-124">Specifies a compute node, as a **PSComputeNode** object, for which this cmdlet gets remote logon settings.</span></span>
<span data-ttu-id="d338d-125">Чтобы получить объект COMPUTE Node, используйте командлет Get-AzBatchComputeNode.</span><span class="sxs-lookup"><span data-stu-id="d338d-125">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d338d-126">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="d338d-126">-ComputeNodeId</span></span>
<span data-ttu-id="d338d-127">Указывает идентификатор вычислительного узла, для которого нужно получить параметры удаленного входа.</span><span class="sxs-lookup"><span data-stu-id="d338d-127">Specifies the ID of the compute node for which to get the remote logon settings.</span></span>
<span data-ttu-id="d338d-128">, для которого этот командлет получает параметры удаленного входа.</span><span class="sxs-lookup"><span data-stu-id="d338d-128">for which this cmdlet gets remote logon settings.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d338d-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d338d-129">-DefaultProfile</span></span>
<span data-ttu-id="d338d-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d338d-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d338d-131">-PoolId</span><span class="sxs-lookup"><span data-stu-id="d338d-131">-PoolId</span></span>
<span data-ttu-id="d338d-132">Указывает идентификатор пула, который содержит виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="d338d-132">Specifies the ID of the pool that contains the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: Id
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d338d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d338d-133">CommonParameters</span></span>
<span data-ttu-id="d338d-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d338d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d338d-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d338d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d338d-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d338d-136">INPUTS</span></span>

### <span data-ttu-id="d338d-137">Microsoft.Azure.Commands.BatCH. Models. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="d338d-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="d338d-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="d338d-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="d338d-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d338d-139">OUTPUTS</span></span>

### <span data-ttu-id="d338d-140">Microsoft.Azure.Commands.BatCH. Models. PSRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="d338d-140">Microsoft.Azure.Commands.Batch.Models.PSRemoteLoginSettings</span></span>

## <span data-ttu-id="d338d-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="d338d-141">NOTES</span></span>

## <span data-ttu-id="d338d-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d338d-142">RELATED LINKS</span></span>

[<span data-ttu-id="d338d-143">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="d338d-143">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="d338d-144">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="d338d-144">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="d338d-145">Get-AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="d338d-145">Get-AzBatchRemoteDesktopProtocolFile</span></span>](./Get-AzBatchRemoteDesktopProtocolFile.md)

[<span data-ttu-id="d338d-146">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="d338d-146">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


