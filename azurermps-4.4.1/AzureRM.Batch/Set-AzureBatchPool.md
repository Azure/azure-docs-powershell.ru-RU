---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 23893EAE-47F3-45AA-AEB2-354FB8316C25
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPool.md
ms.openlocfilehash: d18a6bdc9a2064e21507c909005692d5d21c63f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566308"
---
# <span data-ttu-id="c5897-101">Set-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="c5897-101">Set-AzureBatchPool</span></span>

## <span data-ttu-id="c5897-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c5897-102">SYNOPSIS</span></span>
<span data-ttu-id="c5897-103">Обновляет свойства пула.</span><span class="sxs-lookup"><span data-stu-id="c5897-103">Updates the properties of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5897-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c5897-104">SYNTAX</span></span>

```
Set-AzureBatchPool [-Pool] <PSCloudPool> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5897-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5897-105">DESCRIPTION</span></span>
<span data-ttu-id="c5897-106">Командлет **Set-AzureBatchPool** обновляет свойства пула в пакетной службе Azure.</span><span class="sxs-lookup"><span data-stu-id="c5897-106">The **Set-AzureBatchPool** cmdlet updates the properties of a pool in the Azure Batch service.</span></span>
<span data-ttu-id="c5897-107">Используйте командлет Get-AzureBatchPool, чтобы получить объект **PSCloudPool** .</span><span class="sxs-lookup"><span data-stu-id="c5897-107">Use the Get-AzureBatchPool cmdlet to get a **PSCloudPool** object.</span></span>
<span data-ttu-id="c5897-108">Измените свойства объекта, а затем используйте текущий командлет для фиксации изменений в пакетной службе.</span><span class="sxs-lookup"><span data-stu-id="c5897-108">Modify the properties of that object, and then use the current cmdlet to commit your changes to the Batch service.</span></span>

## <span data-ttu-id="c5897-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c5897-109">EXAMPLES</span></span>

### <span data-ttu-id="c5897-110">Пример 1: Обновление пула</span><span class="sxs-lookup"><span data-stu-id="c5897-110">Example 1: Update a pool</span></span>
```
PS C:\>$Pool = Get-AzureBatchPool "ContosoPool" -BatchContext $Context
PS C:\> $StartTask = New-Object Microsoft.Azure.Commands.Batch.Models.PSStartTask
PS C:\> $StartTask.CommandLine = "cmd /c echo example"
PS C:\> $Pool.StartTask = $StartTask
PS C:\> Set-AzureBatchPool -Pool $Pool -BatchContext $Context
```

<span data-ttu-id="c5897-111">Первая команда получает пул с помощью **Get-AzureBatchPool** , а затем сохраняет его в переменной $pool.</span><span class="sxs-lookup"><span data-stu-id="c5897-111">The first command gets a pool by using **Get-AzureBatchPool** , and then stores it in the $Pool variable.</span></span>

<span data-ttu-id="c5897-112">Следующие три команды изменяют спецификацию Start Task для объекта $Pool.</span><span class="sxs-lookup"><span data-stu-id="c5897-112">The next three commands modify the start task specification on the $Pool object.</span></span>

<span data-ttu-id="c5897-113">Последняя команда обновляет пакетную службу таким образом, чтобы она соответствовала локальному объекту в $Pool.</span><span class="sxs-lookup"><span data-stu-id="c5897-113">The final command updates the Batch service to match the local object in $Pool.</span></span>

## <span data-ttu-id="c5897-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c5897-114">PARAMETERS</span></span>

### <span data-ttu-id="c5897-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="c5897-115">-BatchContext</span></span>
<span data-ttu-id="c5897-116">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="c5897-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="c5897-117">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="c5897-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="c5897-118">-Пул</span><span class="sxs-lookup"><span data-stu-id="c5897-118">-Pool</span></span>
<span data-ttu-id="c5897-119">Указывает **PSCloudPool** , на который этот командлет обновляет службу пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="c5897-119">Specifies the **PSCloudPool** to which this cmdlet updates the Batch service.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudPool
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5897-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5897-120">-DefaultProfile</span></span>
<span data-ttu-id="c5897-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c5897-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5897-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5897-122">CommonParameters</span></span>
<span data-ttu-id="c5897-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c5897-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5897-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5897-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5897-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c5897-125">INPUTS</span></span>

### <span data-ttu-id="c5897-126">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c5897-126">BatchAccountContext</span></span>
<span data-ttu-id="c5897-127">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c5897-127">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="c5897-128">PSCloudPool</span><span class="sxs-lookup"><span data-stu-id="c5897-128">PSCloudPool</span></span>
<span data-ttu-id="c5897-129">Параметр pool принимает значение типа "PSCloudPool" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="c5897-129">Parameter 'Pool' accepts value of type 'PSCloudPool' from the pipeline</span></span>

## <span data-ttu-id="c5897-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5897-130">OUTPUTS</span></span>

## <span data-ttu-id="c5897-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="c5897-131">NOTES</span></span>

## <span data-ttu-id="c5897-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5897-132">RELATED LINKS</span></span>

[<span data-ttu-id="c5897-133">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="c5897-133">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="c5897-134">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c5897-134">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="c5897-135">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="c5897-135">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="c5897-136">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="c5897-136">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="c5897-137">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="c5897-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


