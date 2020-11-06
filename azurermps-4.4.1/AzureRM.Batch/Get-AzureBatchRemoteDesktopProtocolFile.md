---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D077DB50-12BC-45AB-8EAC-57810DA83035
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteDesktopProtocolFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteDesktopProtocolFile.md
ms.openlocfilehash: 37d91dc6fd9d90291c7b619fdb9839d6d9af83b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570127"
---
# <span data-ttu-id="fd342-101">Get-AzureBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="fd342-101">Get-AzureBatchRemoteDesktopProtocolFile</span></span>

## <span data-ttu-id="fd342-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fd342-102">SYNOPSIS</span></span>
<span data-ttu-id="fd342-103">Получает RDP-файл из вычислительного узла.</span><span class="sxs-lookup"><span data-stu-id="fd342-103">Gets an RDP file from a compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd342-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fd342-104">SYNTAX</span></span>

### <span data-ttu-id="fd342-105">Id_Path (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fd342-105">Id_Path (Default)</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd342-106">Id_Stream</span><span class="sxs-lookup"><span data-stu-id="fd342-106">Id_Stream</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String>
 -DestinationStream <Stream> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fd342-107">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="fd342-107">InputObject_Path</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fd342-108">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="fd342-108">InputObject_Stream</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd342-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd342-109">DESCRIPTION</span></span>
<span data-ttu-id="fd342-110">Командлет **Get-AzureBatchRemoteDesktopProtocolFile** получает файл протокола удаленного рабочего стола (RDP) из вычислительного узла и сохраняет его в виде файла или потока, который пользователь ввел.</span><span class="sxs-lookup"><span data-stu-id="fd342-110">The **Get-AzureBatchRemoteDesktopProtocolFile** cmdlet gets a Remote Desktop Protocol (RDP) file from a compute node and saves it as a file or to a user supplied stream.</span></span>

## <span data-ttu-id="fd342-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fd342-111">EXAMPLES</span></span>

### <span data-ttu-id="fd342-112">Пример 1: получение RDP-файла с указанного вычислительного узла и сохранение файла</span><span class="sxs-lookup"><span data-stu-id="fd342-112">Example 1: Get an RDP file from a specified compute node and save the file</span></span>
```
PS C:\>Get-AzureBatchRemoteDesktopProtocolFile -PoolId "Pool06" -ComputeNodeId "ComputeNode01" -DestinationPath "C:\PowerShell\ComputeNode01.rdp" -BatchContext $Context
```

<span data-ttu-id="fd342-113">Эта команда получает RDP-файл из COMPUTE Node, имеющий идентификатор ComputeNode01 в пуле с ИД Pool06.</span><span class="sxs-lookup"><span data-stu-id="fd342-113">This command gets an RDP file from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="fd342-114">С помощью команды файл. rdp сохраняется в виде C:\PowerShell\MyComputeNode.rdp.</span><span class="sxs-lookup"><span data-stu-id="fd342-114">The command saves the .rdp file as C:\PowerShell\MyComputeNode.rdp.</span></span>
<span data-ttu-id="fd342-115">Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="fd342-115">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="fd342-116">Пример 2: получение RDP-файла из вычислительного узла и сохранение файла с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="fd342-116">Example 2: Get an RDP file from a compute node and save the file by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool06" -Id "ComputeNode02" -BatchContext $Context | Get-AzureBatchRemoteDesktopProtocolFile -DestinationPath "C:\PowerShell\MyComputeNode02.rdp" -BatchContext $Context
```

<span data-ttu-id="fd342-117">Эта команда возвращает узел COMPUTE node с ИД ComputeNode02 в пуле с ИД Pool06.</span><span class="sxs-lookup"><span data-stu-id="fd342-117">This command gets the compute node that has the ID ComputeNode02 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="fd342-118">Команда передает этот вычислительный узел текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="fd342-118">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="fd342-119">Текущий командлет получает файл RPD из COMPUTE node и сохраняет его в виде файла с именем C:\PowerShell\MyComputeNode02.rdp.</span><span class="sxs-lookup"><span data-stu-id="fd342-119">The current cmdlet gets an .rpd file from the compute node, and then saves the contents as a file that is named C:\PowerShell\MyComputeNode02.rdp.</span></span>

### <span data-ttu-id="fd342-120">Пример 3: получение RDP-файла с указанного вычислительного узла и его направление в поток</span><span class="sxs-lookup"><span data-stu-id="fd342-120">Example 3: Get a RDP file from a specified compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchRemoteDesktopProtocolFile "Pool06" -ComputeNodeId "ComputeNode03" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="fd342-121">Первая команда создает поток с помощью командлета New-Object и сохраняет его в переменной $Stream.</span><span class="sxs-lookup"><span data-stu-id="fd342-121">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>

<span data-ttu-id="fd342-122">Вторая команда получает RDP-файл из COMPUTE Node, имеющий идентификатор ComputeNode03 в пуле с ИД Pool06.</span><span class="sxs-lookup"><span data-stu-id="fd342-122">The second command gets an .rdp file from the compute node that has the ID ComputeNode03 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="fd342-123">Команда направляет содержимое файла в поток в $Stream.</span><span class="sxs-lookup"><span data-stu-id="fd342-123">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="fd342-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fd342-124">PARAMETERS</span></span>

### <span data-ttu-id="fd342-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="fd342-125">-BatchContext</span></span>
<span data-ttu-id="fd342-126">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="fd342-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="fd342-127">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="fd342-127">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="fd342-128">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="fd342-128">-ComputeNode</span></span>
<span data-ttu-id="fd342-129">Задает вычислительный узел как объект **PSComputeNode** , на который указывает RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="fd342-129">Specifies a compute node, as a **PSComputeNode** object, to which the .rdp file points.</span></span>
<span data-ttu-id="fd342-130">Чтобы получить объект COMPUTE Node, используйте командлет Get-AzureBatchComputeNode.</span><span class="sxs-lookup"><span data-stu-id="fd342-130">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="fd342-131">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="fd342-131">-ComputeNodeId</span></span>
<span data-ttu-id="fd342-132">Указывает идентификатор вычислительного узла, на который указывает RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="fd342-132">Specifies the ID of the compute node to which the .rdp file points.</span></span>

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

### <span data-ttu-id="fd342-133">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="fd342-133">-DestinationPath</span></span>
<span data-ttu-id="fd342-134">Указывает путь к файлу, в котором командлет сохраняет RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="fd342-134">Specifies the file path where this cmdlet saves the .rdp file.</span></span>

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

### <span data-ttu-id="fd342-135">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="fd342-135">-DestinationStream</span></span>
<span data-ttu-id="fd342-136">Указывает поток, в который этот командлет направляет данные RDP.</span><span class="sxs-lookup"><span data-stu-id="fd342-136">Specifies the stream into which this cmdlet directs the RDP data.</span></span>
<span data-ttu-id="fd342-137">Этот командлет не закрывает и не перематывает этот поток.</span><span class="sxs-lookup"><span data-stu-id="fd342-137">This cmdlet does not close or rewind this stream.</span></span>

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

### <span data-ttu-id="fd342-138">-PoolId</span><span class="sxs-lookup"><span data-stu-id="fd342-138">-PoolId</span></span>
<span data-ttu-id="fd342-139">Указывает идентификатор пула, который содержит вычислительный узел, на основе которого этот командлет получает RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="fd342-139">Specifies the ID of the pool that contains the compute node from which this cmdlet gets an .rdp file.</span></span>

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

### <span data-ttu-id="fd342-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd342-140">-DefaultProfile</span></span>
<span data-ttu-id="fd342-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fd342-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd342-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd342-142">CommonParameters</span></span>
<span data-ttu-id="fd342-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fd342-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd342-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd342-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd342-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fd342-145">INPUTS</span></span>

### <span data-ttu-id="fd342-146">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="fd342-146">BatchAccountContext</span></span>
<span data-ttu-id="fd342-147">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="fd342-147">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="fd342-148">PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="fd342-148">PSComputeNode</span></span>
<span data-ttu-id="fd342-149">Параметр "ComputeNode" принимает значение типа "PSComputeNode" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="fd342-149">Parameter 'ComputeNode' accepts value of type 'PSComputeNode' from the pipeline</span></span>

## <span data-ttu-id="fd342-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd342-150">OUTPUTS</span></span>

## <span data-ttu-id="fd342-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="fd342-151">NOTES</span></span>

## <span data-ttu-id="fd342-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd342-152">RELATED LINKS</span></span>

[<span data-ttu-id="fd342-153">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="fd342-153">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="fd342-154">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="fd342-154">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="fd342-155">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="fd342-155">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


