---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: D077DB50-12BC-45AB-8EAC-57810DA83035
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchremotedesktopprotocolfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchRemoteDesktopProtocolFile.md
ms.openlocfilehash: 3e1b4ce662e7a904fcfb8d4b938f7fe5bbef0f7e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315911"
---
# <span data-ttu-id="ff58d-101">Get-AzBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="ff58d-101">Get-AzBatchRemoteDesktopProtocolFile</span></span>

## <span data-ttu-id="ff58d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ff58d-102">SYNOPSIS</span></span>
<span data-ttu-id="ff58d-103">Получает RDP-файл из вычислительного узла.</span><span class="sxs-lookup"><span data-stu-id="ff58d-103">Gets an RDP file from a compute node.</span></span>

## <span data-ttu-id="ff58d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ff58d-104">SYNTAX</span></span>

### <span data-ttu-id="ff58d-105">Id_Path (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ff58d-105">Id_Path (Default)</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff58d-106">Id_Stream</span><span class="sxs-lookup"><span data-stu-id="ff58d-106">Id_Stream</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff58d-107">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="ff58d-107">InputObject_Path</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff58d-108">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="ff58d-108">InputObject_Stream</span></span>
```
Get-AzBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff58d-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff58d-109">DESCRIPTION</span></span>
<span data-ttu-id="ff58d-110">Командлет **Get-AzBatchRemoteDesktopProtocolFile** получает файл протокола удаленного рабочего стола (RDP) из вычислительного узла и сохраняет его в виде файла или потока, который пользователь ввел.</span><span class="sxs-lookup"><span data-stu-id="ff58d-110">The **Get-AzBatchRemoteDesktopProtocolFile** cmdlet gets a Remote Desktop Protocol (RDP) file from a compute node and saves it as a file or to a user supplied stream.</span></span>

## <span data-ttu-id="ff58d-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ff58d-111">EXAMPLES</span></span>

### <span data-ttu-id="ff58d-112">Пример 1: получение RDP-файла с указанного вычислительного узла и сохранение файла</span><span class="sxs-lookup"><span data-stu-id="ff58d-112">Example 1: Get an RDP file from a specified compute node and save the file</span></span>
```
PS C:\>Get-AzBatchRemoteDesktopProtocolFile -PoolId "Pool06" -ComputeNodeId "ComputeNode01" -DestinationPath "C:\PowerShell\ComputeNode01.rdp" -BatchContext $Context
```

<span data-ttu-id="ff58d-113">Эта команда получает RDP-файл из COMPUTE Node, имеющий идентификатор ComputeNode01 в пуле с ИД Pool06.</span><span class="sxs-lookup"><span data-stu-id="ff58d-113">This command gets an RDP file from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="ff58d-114">С помощью команды файл. rdp сохраняется в виде C:\PowerShell\MyComputeNode.rdp.</span><span class="sxs-lookup"><span data-stu-id="ff58d-114">The command saves the .rdp file as C:\PowerShell\MyComputeNode.rdp.</span></span>
<span data-ttu-id="ff58d-115">Используйте командлет Get-AzBatchAccountKey для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="ff58d-115">Use the Get-AzBatchAccountKey cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="ff58d-116">Пример 2: получение RDP-файла из вычислительного узла и сохранение файла с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="ff58d-116">Example 2: Get an RDP file from a compute node and save the file by using the pipeline</span></span>
```
PS C:\>Get-AzBatchComputeNode -PoolId "Pool06" -Id "ComputeNode02" -BatchContext $Context | Get-AzBatchRemoteDesktopProtocolFile -DestinationPath "C:\PowerShell\MyComputeNode02.rdp" -BatchContext $Context
```

<span data-ttu-id="ff58d-117">Эта команда возвращает узел COMPUTE node с ИД ComputeNode02 в пуле с ИД Pool06.</span><span class="sxs-lookup"><span data-stu-id="ff58d-117">This command gets the compute node that has the ID ComputeNode02 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="ff58d-118">Команда передает этот вычислительный узел текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="ff58d-118">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ff58d-119">Текущий командлет получает файл RPD из COMPUTE node и сохраняет его в виде файла с именем C:\PowerShell\MyComputeNode02.rdp.</span><span class="sxs-lookup"><span data-stu-id="ff58d-119">The current cmdlet gets an .rpd file from the compute node, and then saves the contents as a file that is named C:\PowerShell\MyComputeNode02.rdp.</span></span>

### <span data-ttu-id="ff58d-120">Пример 3: получение RDP-файла с указанного вычислительного узла и его направление в поток</span><span class="sxs-lookup"><span data-stu-id="ff58d-120">Example 3: Get a RDP file from a specified compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchRemoteDesktopProtocolFile "Pool06" -ComputeNodeId "ComputeNode03" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="ff58d-121">Первая команда создает поток с помощью командлета New-Object и сохраняет его в переменной $Stream.</span><span class="sxs-lookup"><span data-stu-id="ff58d-121">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="ff58d-122">Вторая команда получает RDP-файл из COMPUTE Node, имеющий идентификатор ComputeNode03 в пуле с ИД Pool06.</span><span class="sxs-lookup"><span data-stu-id="ff58d-122">The second command gets an .rdp file from the compute node that has the ID ComputeNode03 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="ff58d-123">Команда направляет содержимое файла в поток в $Stream.</span><span class="sxs-lookup"><span data-stu-id="ff58d-123">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="ff58d-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ff58d-124">PARAMETERS</span></span>

### <span data-ttu-id="ff58d-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="ff58d-125">-BatchContext</span></span>
<span data-ttu-id="ff58d-126">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="ff58d-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="ff58d-127">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="ff58d-127">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="ff58d-128">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="ff58d-128">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="ff58d-129">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="ff58d-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="ff58d-130">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="ff58d-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="ff58d-131">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="ff58d-131">-ComputeNode</span></span>
<span data-ttu-id="ff58d-132">Задает вычислительный узел как объект **PSComputeNode** , на который указывает RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="ff58d-132">Specifies a compute node, as a **PSComputeNode** object, to which the .rdp file points.</span></span>
<span data-ttu-id="ff58d-133">Чтобы получить объект COMPUTE Node, используйте командлет Get-AzBatchComputeNode.</span><span class="sxs-lookup"><span data-stu-id="ff58d-133">To obtain a compute node object, use the Get-AzBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="ff58d-134">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="ff58d-134">-ComputeNodeId</span></span>
<span data-ttu-id="ff58d-135">Указывает идентификатор вычислительного узла, на который указывает RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="ff58d-135">Specifies the ID of the compute node to which the .rdp file points.</span></span>

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

### <span data-ttu-id="ff58d-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff58d-136">-DefaultProfile</span></span>
<span data-ttu-id="ff58d-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ff58d-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff58d-138">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="ff58d-138">-DestinationPath</span></span>
<span data-ttu-id="ff58d-139">Указывает путь к файлу, в котором командлет сохраняет RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="ff58d-139">Specifies the file path where this cmdlet saves the .rdp file.</span></span>

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

### <span data-ttu-id="ff58d-140">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="ff58d-140">-DestinationStream</span></span>
<span data-ttu-id="ff58d-141">Указывает поток, в который этот командлет направляет данные RDP.</span><span class="sxs-lookup"><span data-stu-id="ff58d-141">Specifies the stream into which this cmdlet directs the RDP data.</span></span>
<span data-ttu-id="ff58d-142">Этот командлет не закрывает и не перематывает этот поток.</span><span class="sxs-lookup"><span data-stu-id="ff58d-142">This cmdlet does not close or rewind this stream.</span></span>

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

### <span data-ttu-id="ff58d-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="ff58d-143">-PoolId</span></span>
<span data-ttu-id="ff58d-144">Указывает идентификатор пула, который содержит вычислительный узел, на основе которого этот командлет получает RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="ff58d-144">Specifies the ID of the pool that contains the compute node from which this cmdlet gets an .rdp file.</span></span>

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

### <span data-ttu-id="ff58d-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff58d-145">CommonParameters</span></span>
<span data-ttu-id="ff58d-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ff58d-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff58d-147">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ff58d-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff58d-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ff58d-148">INPUTS</span></span>

### <span data-ttu-id="ff58d-149">System. String</span><span class="sxs-lookup"><span data-stu-id="ff58d-149">System.String</span></span>

### <span data-ttu-id="ff58d-150">Microsoft.Azure.Commands.BatCH. Models. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="ff58d-150">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>

### <span data-ttu-id="ff58d-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ff58d-151">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="ff58d-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff58d-152">OUTPUTS</span></span>

### <span data-ttu-id="ff58d-153">System. void</span><span class="sxs-lookup"><span data-stu-id="ff58d-153">System.Void</span></span>

## <span data-ttu-id="ff58d-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="ff58d-154">NOTES</span></span>

## <span data-ttu-id="ff58d-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff58d-155">RELATED LINKS</span></span>

[<span data-ttu-id="ff58d-156">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ff58d-156">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="ff58d-157">Get-AzBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="ff58d-157">Get-AzBatchComputeNode</span></span>](./Get-AzBatchComputeNode.md)

[<span data-ttu-id="ff58d-158">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="ff58d-158">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
