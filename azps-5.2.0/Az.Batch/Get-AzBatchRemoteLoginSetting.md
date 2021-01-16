---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 07811B64-6A77-452C-B148-DE8C13E73DEF
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremoteloginsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteLoginSetting.md
ms.openlocfilehash: 0e2360e6c4d0ba7d993f1f1aa21feb1b44115e6b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98322436"
---
# <span data-ttu-id="a92ff-101">Get-AzBatchRemoteLoginSetting</span><span class="sxs-lookup"><span data-stu-id="a92ff-101">Get-AzBatchRemoteLoginSetting</span></span>

## <span data-ttu-id="a92ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a92ff-102">SYNOPSIS</span></span>
<span data-ttu-id="a92ff-103">Возвращает параметры удаленного логона для узла компьютеров.</span><span class="sxs-lookup"><span data-stu-id="a92ff-103">Gets remote logon settings for a compute node.</span></span>

## <span data-ttu-id="a92ff-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a92ff-104">SYNTAX</span></span>

### <span data-ttu-id="a92ff-105">ИД (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a92ff-105">Id (Default)</span></span>
```
Get-AzBatchRemoteLoginSetting [-PoolId] <String> [-ComputeNodeId] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a92ff-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="a92ff-106">InputObject</span></span>
```
Get-AzBatchRemoteLoginSetting [[-ComputeNode] <PSComputeNode>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a92ff-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a92ff-107">DESCRIPTION</span></span>
<span data-ttu-id="a92ff-108">Для узла вычислений в пуле виртуальных машин, основанном на инфраструктуре, командылет **Get-AzBatchRemoteLoginSetting** получают параметры удаленного логина.</span><span class="sxs-lookup"><span data-stu-id="a92ff-108">The **Get-AzBatchRemoteLoginSetting** cmdlet gets remote logon settings for a compute node in a virtual machines infrastructure-based pool.</span></span>

## <span data-ttu-id="a92ff-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a92ff-109">EXAMPLES</span></span>

### <span data-ttu-id="a92ff-110">Пример 1. Настройка удаленных параметров для всех узлов в пуле</span><span class="sxs-lookup"><span data-stu-id="a92ff-110">Example 1: Get remote logon settings for all nodes in a pool</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchComputeNode -PoolId "ContosoPool" -BatchContext $Context | Get-AzBatchRemoteLoginSetting -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50002
10.214.75.221   50001
10.214.75.221   50000
```

<span data-ttu-id="a92ff-111">Первая команда получает контекст пакетной учетной записи, содержащего ключи доступа для вашей подписки, с помощью **Get-AzBatchAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="a92ff-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="a92ff-112">Команда сохраняет контекст в переменной $Context для использования в следующей команде.</span><span class="sxs-lookup"><span data-stu-id="a92ff-112">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="a92ff-113">Вторая команда получает каждый узел вычислений в пуле с ID ContosoPool с помощью **Get-AzBatchComputeNode.**</span><span class="sxs-lookup"><span data-stu-id="a92ff-113">The second command gets each compute node in the pool that has the ID ContosoPool by using **Get-AzBatchComputeNode**.</span></span>
<span data-ttu-id="a92ff-114">Команда передает каждый узел компьютера текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="a92ff-114">The command passes each computer node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="a92ff-115">Команда получает параметры удаленного логона для каждого узла вычислений.</span><span class="sxs-lookup"><span data-stu-id="a92ff-115">The command gets the remote logon settings for each compute node.</span></span>

### <span data-ttu-id="a92ff-116">Пример 2. Настройка удаленных параметров для узла</span><span class="sxs-lookup"><span data-stu-id="a92ff-116">Example 2: Get remote logon settings for a node</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchRemoteLoginSetting -PoolId "ContosoPool" -ComputeNodeId "tvm-1900272697_1-20150330t205553z" -BatchContext $Context
IPAddress       Port
---------       ----
10.214.75.221   50000
```

<span data-ttu-id="a92ff-117">Первая команда получает контекст пакетной учетной записи, содержащий ключи доступа для вашей подписки, и сохраняет ее в переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="a92ff-117">The first command gets a batch account context that contains access keys for your subscription, and then stores it in the $Context variable.</span></span>
<span data-ttu-id="a92ff-118">Вторая команда получает параметры удаленного логотипа для узла вычислений с указанным ИД в пуле с ИД ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="a92ff-118">The second command gets the remote logon settings for the compute node that has the specified ID in the pool that has the ID ContosoPool.</span></span>

## <span data-ttu-id="a92ff-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a92ff-119">PARAMETERS</span></span>

### <span data-ttu-id="a92ff-120">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a92ff-120">-BatchContext</span></span>
<span data-ttu-id="a92ff-121">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="a92ff-121">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a92ff-122">Для получения **пакета BatchAccountContext,** содержащего ключи доступа для подписки, используйте Get-AzBatchAccountKey управления.</span><span class="sxs-lookup"><span data-stu-id="a92ff-122">To obtain a **BatchAccountContext** that contains access keys for your subscription, use the Get-AzBatchAccountKey cmdlet.</span></span>

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

### <span data-ttu-id="a92ff-123">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="a92ff-123">-ComputeNode</span></span>
<span data-ttu-id="a92ff-124">Определяет узел вычислений как объект **PSComputeNode,** для которого этот cmdlet получает параметры удаленного логона.</span><span class="sxs-lookup"><span data-stu-id="a92ff-124">Specifies a compute node, as a **PSComputeNode** object, for which this cmdlet gets remote logon settings.</span></span>
<span data-ttu-id="a92ff-125">Чтобы получить объект вычислительного узла, воспользуйтесь Get-AzBatchComputeNode..</span><span class="sxs-lookup"><span data-stu-id="a92ff-125">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="a92ff-126">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="a92ff-126">-ComputeNodeId</span></span>
<span data-ttu-id="a92ff-127">Определяет ИД узла компьютеров, для которого требуется получить параметры удаленного логона.</span><span class="sxs-lookup"><span data-stu-id="a92ff-127">Specifies the ID of the compute node for which to get the remote logon settings.</span></span>
<span data-ttu-id="a92ff-128">для которого этот cmdlet получает удаленные параметры для логотипа.</span><span class="sxs-lookup"><span data-stu-id="a92ff-128">for which this cmdlet gets remote logon settings.</span></span>

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

### <span data-ttu-id="a92ff-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a92ff-129">-DefaultProfile</span></span>
<span data-ttu-id="a92ff-130">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a92ff-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a92ff-131">-PoolId</span><span class="sxs-lookup"><span data-stu-id="a92ff-131">-PoolId</span></span>
<span data-ttu-id="a92ff-132">Определяет ИД пула, который содержит виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="a92ff-132">Specifies the ID of the pool that contains the virtual machine.</span></span>

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

### <span data-ttu-id="a92ff-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a92ff-133">CommonParameters</span></span>
<span data-ttu-id="a92ff-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a92ff-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a92ff-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a92ff-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a92ff-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a92ff-136">INPUTS</span></span>

### <span data-ttu-id="a92ff-137">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="a92ff-137">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="a92ff-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a92ff-138">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a92ff-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a92ff-139">OUTPUTS</span></span>

### <span data-ttu-id="a92ff-140">Microsoft.Azure.Commands.Batch. Models.PSRemoteLoginSettings</span><span class="sxs-lookup"><span data-stu-id="a92ff-140">Microsoft.Azure.Commands.Batch.Models.PSRemoteLoginSettings</span></span>

## <span data-ttu-id="a92ff-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a92ff-141">NOTES</span></span>

## <span data-ttu-id="a92ff-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a92ff-142">RELATED LINKS</span></span>

[<span data-ttu-id="a92ff-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="a92ff-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="a92ff-144">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="a92ff-144">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="a92ff-145">Get-AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="a92ff-145">Get-AzBatchRemoteDesktopProtocolFile</span></span>](./Get-AzBatchRemoteDesktopProtocolFile.md)

[<span data-ttu-id="a92ff-146">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="a92ff-146">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
