---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D077DB50-12BC-45AB-8EAC-57810DA83035
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremotedesktopprotocolfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
ms.openlocfilehash: 3e1b4ce662e7a904fcfb8d4b938f7fe5bbef0f7e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100231169"
---
# <span data-ttu-id="34760-101">Get-AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="34760-101">Get-AzBatchRemoteDesktopProtocolFile</span></span>

## <span data-ttu-id="34760-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34760-102">SYNOPSIS</span></span>
<span data-ttu-id="34760-103">Получает RDP-файл из узла для вычислений.</span><span class="sxs-lookup"><span data-stu-id="34760-103">Gets an RDP file from a compute node.</span></span>

## <span data-ttu-id="34760-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="34760-104">SYNTAX</span></span>

### <span data-ttu-id="34760-105">Id_Path (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="34760-105">Id_Path (Default)</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34760-106">Id_Stream</span><span class="sxs-lookup"><span data-stu-id="34760-106">Id_Stream</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34760-107">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="34760-107">InputObject_Path</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34760-108">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="34760-108">InputObject_Stream</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34760-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34760-109">DESCRIPTION</span></span>
<span data-ttu-id="34760-110">Cmdlet **Get-AzBatchRemoteDesktopProtocolFile** получает файл протокола удаленного рабочего стола (RDP) из узла вычислений и сохраняет его как файл или поток, предоставленный пользователем.</span><span class="sxs-lookup"><span data-stu-id="34760-110">The **Get-AzBatchRemoteDesktopProtocolFile** cmdlet gets a Remote Desktop Protocol (RDP) file from a compute node and saves it as a file or to a user supplied stream.</span></span>

## <span data-ttu-id="34760-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="34760-111">EXAMPLES</span></span>

### <span data-ttu-id="34760-112">Пример 1. Получите RDP-файл из указанного узла вычислений и сохраните его</span><span class="sxs-lookup"><span data-stu-id="34760-112">Example 1: Get an RDP file from a specified compute node and save the file</span></span>
```
PS C:\>Get-AzBatchRemoteDesktopProtocolFile -PoolId "Pool06" -ComputeNodeId "ComputeNode01" -DestinationPath "C:\PowerShell\ComputeNode01.rdp" -BatchContext $Context
```

<span data-ttu-id="34760-113">Эта команда получает RDP-файл из узла вычислений, который содержит файл ID ComputeNode01 в пуле, который содержит пул ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="34760-113">This command gets an RDP file from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="34760-114">Команда сохраняет RDP-файл в папке C:\PowerShell\MyComputeNode.rdp.</span><span class="sxs-lookup"><span data-stu-id="34760-114">The command saves the .rdp file as C:\PowerShell\MyComputeNode.rdp.</span></span>
<span data-ttu-id="34760-115">Используйте Get-AzBatchAccountKey для назначения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="34760-115">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="34760-116">Пример 2. Получите RDP-файл из узла вычислений и сохраните его с помощью конвейера.</span><span class="sxs-lookup"><span data-stu-id="34760-116">Example 2: Get an RDP file from a compute node and save the file by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Id "ComputeNode02" -BatchContext $Context | Get-AzBatchRemoteDesktopProtocolFile -DestinationPath "C:\PowerShell\MyComputeNode02.rdp" -BatchContext $Context
```

<span data-ttu-id="34760-117">Эта команда возвращает узел вычислений, который содержит ID ComputeNode02 в пуле, который содержит пул ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="34760-117">This command gets the compute node that has the ID ComputeNode02 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="34760-118">Эта команда передает этот узел текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="34760-118">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="34760-119">Текущий cmdlet получает RPD-файл из узла вычислений, а затем сохраняет его в файл с именем C:\PowerShell\MyComputeNode02.rdp.</span><span class="sxs-lookup"><span data-stu-id="34760-119">The current cmdlet gets an .rpd file from the compute node, and then saves the contents as a file that is named C:\PowerShell\MyComputeNode02.rdp.</span></span>

### <span data-ttu-id="34760-120">Пример 3. Получите RDP-файл из указанного узла вычислений и перенаправь его в поток</span><span class="sxs-lookup"><span data-stu-id="34760-120">Example 3: Get a RDP file from a specified compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchRemoteDesktopProtocolFile "Pool06" -ComputeNodeId "ComputeNode03" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="34760-121">Первая команда создает поток с помощью New-Object командлета, а затем сохраняет его в $Stream переменной.</span><span class="sxs-lookup"><span data-stu-id="34760-121">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="34760-122">Вторая команда получает RDP-файл из узла вычислений, который содержит ID ComputeNode03 в пуле, который содержит пул ID Pool06.</span><span class="sxs-lookup"><span data-stu-id="34760-122">The second command gets an .rdp file from the compute node that has the ID ComputeNode03 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="34760-123">Команда направляет содержимое файла в поток в $Stream.</span><span class="sxs-lookup"><span data-stu-id="34760-123">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="34760-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34760-124">PARAMETERS</span></span>

### <span data-ttu-id="34760-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="34760-125">-BatchContext</span></span>
<span data-ttu-id="34760-126">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="34760-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="34760-127">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой batchy будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="34760-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="34760-128">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="34760-128">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="34760-129">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="34760-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="34760-130">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="34760-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="34760-131">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="34760-131">-ComputeNode</span></span>
<span data-ttu-id="34760-132">Определяет узел вычислений в качестве объекта **PSComputeNode,** в котором указывается RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="34760-132">Specifies a compute node, as a **PSComputeNode** object, to which the .rdp file points.</span></span>
<span data-ttu-id="34760-133">Чтобы получить объект вычислительного узла, воспользуйтесь Get-AzBatchComputeNode..</span><span class="sxs-lookup"><span data-stu-id="34760-133">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSComputeNode
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34760-134">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="34760-134">-ComputeNodeId</span></span>
<span data-ttu-id="34760-135">Определяет ИД узла вычислений, в который указывается RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="34760-135">Specifies the ID of the compute node to which the .rdp file points.</span></span>

```yaml
Type: System.String
Parameter Sets: Id_Path, Id_Stream
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34760-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34760-136">-DefaultProfile</span></span>
<span data-ttu-id="34760-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="34760-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="34760-138">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="34760-138">-DestinationPath</span></span>
<span data-ttu-id="34760-139">Путь к файлу, в котором этот cmdlet сохраняет RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="34760-139">Specifies the file path where this cmdlet saves the .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Id_Path, InputObject_Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34760-140">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="34760-140">-DestinationStream</span></span>
<span data-ttu-id="34760-141">Определяет поток, в который этот cmdlet направляет данные RDP.</span><span class="sxs-lookup"><span data-stu-id="34760-141">Specifies the stream into which this cmdlet directs the RDP data.</span></span>
<span data-ttu-id="34760-142">Этот cmdlet не закрывает и не перемотать этот поток.</span><span class="sxs-lookup"><span data-stu-id="34760-142">This cmdlet does not close or rewind this stream.</span></span>

```yaml
Type: System.IO.Stream
Parameter Sets: Id_Stream, InputObject_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34760-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="34760-143">-PoolId</span></span>
<span data-ttu-id="34760-144">Определяет код пула, который содержит узел вычислений, из которого этот cmdlet получает RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="34760-144">Specifies the ID of the pool that contains the compute node from which this cmdlet gets an .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Id_Path, Id_Stream
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34760-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34760-145">CommonParameters</span></span>
<span data-ttu-id="34760-146">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34760-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34760-147">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34760-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34760-148">INPUTS</span><span class="sxs-lookup"><span data-stu-id="34760-148">INPUTS</span></span>

### <span data-ttu-id="34760-149">System.String</span><span class="sxs-lookup"><span data-stu-id="34760-149">System.String</span></span>

### <span data-ttu-id="34760-150">Microsoft.Azure.Commands.Batch. Models.PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="34760-150">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="34760-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="34760-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="34760-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="34760-152">OUTPUTS</span></span>

### <span data-ttu-id="34760-153">System.Void</span><span class="sxs-lookup"><span data-stu-id="34760-153">System.Void</span></span>

## <span data-ttu-id="34760-154">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="34760-154">NOTES</span></span>

## <span data-ttu-id="34760-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34760-155">RELATED LINKS</span></span>

[<span data-ttu-id="34760-156">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="34760-156">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="34760-157">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="34760-157">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="34760-158">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="34760-158">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
