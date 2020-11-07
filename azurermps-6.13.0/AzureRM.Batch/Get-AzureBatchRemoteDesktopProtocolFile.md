---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: D077DB50-12BC-45AB-8EAC-57810DA83035
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchremotedesktopprotocolfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteDesktopProtocolFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchRemoteDesktopProtocolFile.md
ms.openlocfilehash: 812edce5ba6a9c1aa4582538c3fda510efdb7175
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733176"
---
# <span data-ttu-id="9046c-101">Get-AzureBatchRemoteDesktopProtocolFile</span><span class="sxs-lookup"><span data-stu-id="9046c-101">Get-AzureBatchRemoteDesktopProtocolFile</span></span>

## <span data-ttu-id="9046c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9046c-102">SYNOPSIS</span></span>
<span data-ttu-id="9046c-103">Получает RDP-файл из вычислительного узла.</span><span class="sxs-lookup"><span data-stu-id="9046c-103">Gets an RDP file from a compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9046c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9046c-104">SYNTAX</span></span>

### <span data-ttu-id="9046c-105">Id_Path (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9046c-105">Id_Path (Default)</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String> -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9046c-106">Id_Stream</span><span class="sxs-lookup"><span data-stu-id="9046c-106">Id_Stream</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [-PoolId] <String> [-ComputeNodeId] <String>
 -DestinationStream <Stream> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9046c-107">InputObject_Path</span><span class="sxs-lookup"><span data-stu-id="9046c-107">InputObject_Path</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationPath <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9046c-108">InputObject_Stream</span><span class="sxs-lookup"><span data-stu-id="9046c-108">InputObject_Stream</span></span>
```
Get-AzureBatchRemoteDesktopProtocolFile [[-ComputeNode] <PSComputeNode>] -DestinationStream <Stream>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9046c-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9046c-109">DESCRIPTION</span></span>
<span data-ttu-id="9046c-110">Командлет **Get-AzureBatchRemoteDesktopProtocolFile** получает файл протокола удаленного рабочего стола (RDP) из вычислительного узла и сохраняет его в виде файла или потока, который пользователь ввел.</span><span class="sxs-lookup"><span data-stu-id="9046c-110">The **Get-AzureBatchRemoteDesktopProtocolFile** cmdlet gets a Remote Desktop Protocol (RDP) file from a compute node and saves it as a file or to a user supplied stream.</span></span>

## <span data-ttu-id="9046c-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9046c-111">EXAMPLES</span></span>

### <span data-ttu-id="9046c-112">Пример 1: получение RDP-файла с указанного вычислительного узла и сохранение файла</span><span class="sxs-lookup"><span data-stu-id="9046c-112">Example 1: Get an RDP file from a specified compute node and save the file</span></span>
```
PS C:\>Get-AzureBatchRemoteDesktopProtocolFile -PoolId "Pool06" -ComputeNodeId "ComputeNode01" -DestinationPath "C:\PowerShell\ComputeNode01.rdp" -BatchContext $Context
```

<span data-ttu-id="9046c-113">Эта команда получает RDP-файл из COMPUTE Node, имеющий идентификатор ComputeNode01 в пуле с ИД Pool06.</span><span class="sxs-lookup"><span data-stu-id="9046c-113">This command gets an RDP file from the compute node that has the ID ComputeNode01 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="9046c-114">С помощью команды файл. rdp сохраняется в виде C:\PowerShell\MyComputeNode.rdp.</span><span class="sxs-lookup"><span data-stu-id="9046c-114">The command saves the .rdp file as C:\PowerShell\MyComputeNode.rdp.</span></span>
<span data-ttu-id="9046c-115">Используйте командлет Get-AzureRmBatchAccountKeys для присвоения контекста переменной $Context.</span><span class="sxs-lookup"><span data-stu-id="9046c-115">Use the Get-AzureRmBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

### <span data-ttu-id="9046c-116">Пример 2: получение RDP-файла из вычислительного узла и сохранение файла с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="9046c-116">Example 2: Get an RDP file from a compute node and save the file by using the pipeline</span></span>
```
PS C:\>Get-AzureBatchComputeNode -PoolId "Pool06" -Id "ComputeNode02" -BatchContext $Context | Get-AzureBatchRemoteDesktopProtocolFile -DestinationPath "C:\PowerShell\MyComputeNode02.rdp" -BatchContext $Context
```

<span data-ttu-id="9046c-117">Эта команда возвращает узел COMPUTE node с ИД ComputeNode02 в пуле с ИД Pool06.</span><span class="sxs-lookup"><span data-stu-id="9046c-117">This command gets the compute node that has the ID ComputeNode02 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="9046c-118">Команда передает этот вычислительный узел текущему командлету с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="9046c-118">The command passes that compute node to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="9046c-119">Текущий командлет получает файл RPD из COMPUTE node и сохраняет его в виде файла с именем C:\PowerShell\MyComputeNode02.rdp.</span><span class="sxs-lookup"><span data-stu-id="9046c-119">The current cmdlet gets an .rpd file from the compute node, and then saves the contents as a file that is named C:\PowerShell\MyComputeNode02.rdp.</span></span>

### <span data-ttu-id="9046c-120">Пример 3: получение RDP-файла с указанного вычислительного узла и его направление в поток</span><span class="sxs-lookup"><span data-stu-id="9046c-120">Example 3: Get a RDP file from a specified compute node and direct it to a stream</span></span>
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzureBatchRemoteDesktopProtocolFile "Pool06" -ComputeNodeId "ComputeNode03" -DestinationStream $Stream -BatchContext $Context
```

<span data-ttu-id="9046c-121">Первая команда создает поток с помощью командлета New-Object и сохраняет его в переменной $Stream.</span><span class="sxs-lookup"><span data-stu-id="9046c-121">The first command creates a stream by using the New-Object cmdlet, and then stores it in the $Stream variable.</span></span>
<span data-ttu-id="9046c-122">Вторая команда получает RDP-файл из COMPUTE Node, имеющий идентификатор ComputeNode03 в пуле с ИД Pool06.</span><span class="sxs-lookup"><span data-stu-id="9046c-122">The second command gets an .rdp file from the compute node that has the ID ComputeNode03 in the pool that has the ID Pool06.</span></span>
<span data-ttu-id="9046c-123">Команда направляет содержимое файла в поток в $Stream.</span><span class="sxs-lookup"><span data-stu-id="9046c-123">The command directs file contents to the stream in $Stream.</span></span>

## <span data-ttu-id="9046c-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9046c-124">PARAMETERS</span></span>

### <span data-ttu-id="9046c-125">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="9046c-125">-BatchContext</span></span>
<span data-ttu-id="9046c-126">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="9046c-126">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="9046c-127">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="9046c-127">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="9046c-128">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="9046c-128">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="9046c-129">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="9046c-129">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="9046c-130">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="9046c-130">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="9046c-131">-ComputeNode</span><span class="sxs-lookup"><span data-stu-id="9046c-131">-ComputeNode</span></span>
<span data-ttu-id="9046c-132">Задает вычислительный узел как объект **PSComputeNode** , на который указывает RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="9046c-132">Specifies a compute node, as a **PSComputeNode** object, to which the .rdp file points.</span></span>
<span data-ttu-id="9046c-133">Чтобы получить объект COMPUTE Node, используйте командлет Get-AzureBatchComputeNode.</span><span class="sxs-lookup"><span data-stu-id="9046c-133">To obtain a compute node object, use the Get-AzureBatchComputeNode cmdlet.</span></span>

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

### <span data-ttu-id="9046c-134">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="9046c-134">-ComputeNodeId</span></span>
<span data-ttu-id="9046c-135">Указывает идентификатор вычислительного узла, на который указывает RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="9046c-135">Specifies the ID of the compute node to which the .rdp file points.</span></span>

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

### <span data-ttu-id="9046c-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9046c-136">-DefaultProfile</span></span>
<span data-ttu-id="9046c-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9046c-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9046c-138">-DestinationPath</span><span class="sxs-lookup"><span data-stu-id="9046c-138">-DestinationPath</span></span>
<span data-ttu-id="9046c-139">Указывает путь к файлу, в котором командлет сохраняет RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="9046c-139">Specifies the file path where this cmdlet saves the .rdp file.</span></span>

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

### <span data-ttu-id="9046c-140">-DestinationStream</span><span class="sxs-lookup"><span data-stu-id="9046c-140">-DestinationStream</span></span>
<span data-ttu-id="9046c-141">Указывает поток, в который этот командлет направляет данные RDP.</span><span class="sxs-lookup"><span data-stu-id="9046c-141">Specifies the stream into which this cmdlet directs the RDP data.</span></span>
<span data-ttu-id="9046c-142">Этот командлет не закрывает и не перематывает этот поток.</span><span class="sxs-lookup"><span data-stu-id="9046c-142">This cmdlet does not close or rewind this stream.</span></span>

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

### <span data-ttu-id="9046c-143">-PoolId</span><span class="sxs-lookup"><span data-stu-id="9046c-143">-PoolId</span></span>
<span data-ttu-id="9046c-144">Указывает идентификатор пула, который содержит вычислительный узел, на основе которого этот командлет получает RDP-файл.</span><span class="sxs-lookup"><span data-stu-id="9046c-144">Specifies the ID of the pool that contains the compute node from which this cmdlet gets an .rdp file.</span></span>

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

### <span data-ttu-id="9046c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9046c-145">CommonParameters</span></span>
<span data-ttu-id="9046c-146">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9046c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9046c-147">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9046c-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9046c-148">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9046c-148">INPUTS</span></span>

### <span data-ttu-id="9046c-149">System. String</span><span class="sxs-lookup"><span data-stu-id="9046c-149">System.String</span></span>

### <span data-ttu-id="9046c-150">Microsoft.Azure.Commands.BatCH. Models. PSComputeNode</span><span class="sxs-lookup"><span data-stu-id="9046c-150">Microsoft.Azure.Commands.Batch.Models.PSComputeNode</span></span>
<span data-ttu-id="9046c-151">Параметры: ComputeNode (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9046c-151">Parameters: ComputeNode (ByValue)</span></span>

### <span data-ttu-id="9046c-152">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9046c-152">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="9046c-153">Параметры: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9046c-153">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="9046c-154">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9046c-154">OUTPUTS</span></span>

### <span data-ttu-id="9046c-155">System. void</span><span class="sxs-lookup"><span data-stu-id="9046c-155">System.Void</span></span>

## <span data-ttu-id="9046c-156">Пуск</span><span class="sxs-lookup"><span data-stu-id="9046c-156">NOTES</span></span>

## <span data-ttu-id="9046c-157">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9046c-157">RELATED LINKS</span></span>

[<span data-ttu-id="9046c-158">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="9046c-158">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="9046c-159">Get-AzureBatchComputeNode</span><span class="sxs-lookup"><span data-stu-id="9046c-159">Get-AzureBatchComputeNode</span></span>](./Get-AzureBatchComputeNode.md)

[<span data-ttu-id="9046c-160">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="9046c-160">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


