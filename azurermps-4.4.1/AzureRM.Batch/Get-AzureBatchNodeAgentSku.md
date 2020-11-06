---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 5C6D3792-AA56-4210-B376-D9E656B04FBD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeAgentSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeAgentSku.md
ms.openlocfilehash: e29b5df4a72ff21dbacb0928b298306eb585b493
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568097"
---
# <span data-ttu-id="e7529-101">Get-AzureBatchNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="e7529-101">Get-AzureBatchNodeAgentSku</span></span>

## <span data-ttu-id="e7529-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e7529-102">SYNOPSIS</span></span>
<span data-ttu-id="e7529-103">Возвращает номера SKU агента пакетных узлов, доступные в пакетной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="e7529-103">Gets Batch node agent SKUs available in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e7529-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e7529-104">SYNTAX</span></span>

```
Get-AzureBatchNodeAgentSku [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7529-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7529-105">DESCRIPTION</span></span>
<span data-ttu-id="e7529-106">Командлет **Get-AzureBatchNodeAgentSku** получает номера SKU агента узла, доступные в пакетной учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="e7529-106">The **Get-AzureBatchNodeAgentSku** cmdlet gets node agent SKUs that are available in an Azure Batch account.</span></span>
<span data-ttu-id="e7529-107">Укажите учетную запись с помощью параметра *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="e7529-107">Specify the account by using the *BatchContext* parameter.</span></span>
<span data-ttu-id="e7529-108">Вы можете сузить поиск до SKU, который соответствует фильтру Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="e7529-108">You can narrow your search to SKUs that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="e7529-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e7529-109">EXAMPLES</span></span>

### <span data-ttu-id="e7529-110">Пример 1: получение всех доступных SKU агента узла</span><span class="sxs-lookup"><span data-stu-id="e7529-110">Example 1: Get all available node agent SKUs</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchNodeAgentSku -BatchContext $Context 
batch.node.centos 7 Linux {7.0, 7.1, 7.2, OL70} 
batch.node.debian 8 Linux {15.10, 8} 
batch.node.opensuse 13.2 Linux {13.2} 
batch.node.opensuse 42.1 Linux {42.1, 12, 12-SP1, 12} 
batch.node.ubuntu 14.04 Linux {14.04.0-LTS, 14.04.1-LTS, 14.04.2-LTS, 14.04.3-LTS...} 
batch.node.windows amd64 Windows {2008-R2-SP1, 2012-Datacenter, 2012-R2-Datacenter, Windows-Server-Technical-Preview}
```

<span data-ttu-id="e7529-111">Первая команда получает контекст учетной записи пакета, который включает клавиши доступа для вашей подписки, с помощью **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="e7529-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="e7529-112">Команда хранит контекст в переменной $Context для использования в следующей команде.</span><span class="sxs-lookup"><span data-stu-id="e7529-112">The command stores the context in the $Context variable to use in the next command.</span></span>

<span data-ttu-id="e7529-113">Вторая команда получает все доступные SKU агента узла, которые поддерживает пакет.</span><span class="sxs-lookup"><span data-stu-id="e7529-113">The second command gets all available node agent SKUs that Batch supports.</span></span>

## <span data-ttu-id="e7529-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e7529-114">PARAMETERS</span></span>

### <span data-ttu-id="e7529-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e7529-115">-BatchContext</span></span>
<span data-ttu-id="e7529-116">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="e7529-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e7529-117">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="e7529-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="e7529-118">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="e7529-118">-Filter</span></span>
<span data-ttu-id="e7529-119">Задает предложение фильтра OData для SKU агента узла.</span><span class="sxs-lookup"><span data-stu-id="e7529-119">Specifies an OData filter clause for node agent SKUs.</span></span>
<span data-ttu-id="e7529-120">Если фильтр не указан, этот командлет возвращает все SKU агента узла, которые поддерживает пакет.</span><span class="sxs-lookup"><span data-stu-id="e7529-120">If you do not specify a filter, this cmdlet returns all node agent SKUs that Batch supports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7529-121">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="e7529-121">-MaxCount</span></span>
<span data-ttu-id="e7529-122">Задает максимальное количество возвращаемых конфигураций агента узла.</span><span class="sxs-lookup"><span data-stu-id="e7529-122">Specifies the maximum number of node agent SKUs to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7529-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7529-123">-DefaultProfile</span></span>
<span data-ttu-id="e7529-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e7529-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7529-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7529-125">CommonParameters</span></span>
<span data-ttu-id="e7529-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e7529-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7529-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7529-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7529-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e7529-128">INPUTS</span></span>

### <span data-ttu-id="e7529-129">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e7529-129">BatchAccountContext</span></span>
<span data-ttu-id="e7529-130">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="e7529-130">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="e7529-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e7529-131">OUTPUTS</span></span>

### <span data-ttu-id="e7529-132">Microsoft.Azure.Commands.BatCH. Models. PSNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="e7529-132">Microsoft.Azure.Commands.Batch.Models.PSNodeAgentSku</span></span>

## <span data-ttu-id="e7529-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="e7529-133">NOTES</span></span>

## <span data-ttu-id="e7529-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e7529-134">RELATED LINKS</span></span>

[<span data-ttu-id="e7529-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="e7529-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)


