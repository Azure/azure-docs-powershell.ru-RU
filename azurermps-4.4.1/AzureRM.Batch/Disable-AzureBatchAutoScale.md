---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
ms.openlocfilehash: 124000fdf11b3fa5b90253fc3b9a75c040725ba8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566314"
---
# <span data-ttu-id="fd7e5-101">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="fd7e5-101">Disable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="fd7e5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fd7e5-102">SYNOPSIS</span></span>
<span data-ttu-id="fd7e5-103">Отключение автоматического масштабирования пула.</span><span class="sxs-lookup"><span data-stu-id="fd7e5-103">Disables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd7e5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fd7e5-104">SYNTAX</span></span>

```
Disable-AzureBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd7e5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd7e5-105">DESCRIPTION</span></span>
<span data-ttu-id="fd7e5-106">Командлет **Disable-AzureBatchAutoScale** отключает автоматическое масштабирование указанного пула.</span><span class="sxs-lookup"><span data-stu-id="fd7e5-106">The **Disable-AzureBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="fd7e5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fd7e5-107">EXAMPLES</span></span>

### <span data-ttu-id="fd7e5-108">Пример 1: Отключение автоматического масштабирования пула</span><span class="sxs-lookup"><span data-stu-id="fd7e5-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzureBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="fd7e5-109">Эта команда отключает автоматическое масштабирование для пула с именем MyPool.</span><span class="sxs-lookup"><span data-stu-id="fd7e5-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="fd7e5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fd7e5-110">PARAMETERS</span></span>

### <span data-ttu-id="fd7e5-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="fd7e5-111">-BatchContext</span></span>
<span data-ttu-id="fd7e5-112">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="fd7e5-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="fd7e5-113">Чтобы получить объект **BatchAccountContext** , содержащий клавиши доступа для вашей подписки, используйте командлет Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="fd7e5-113">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="fd7e5-114">-ID</span><span class="sxs-lookup"><span data-stu-id="fd7e5-114">-Id</span></span>
<span data-ttu-id="fd7e5-115">Указывает идентификатор объекта пула.</span><span class="sxs-lookup"><span data-stu-id="fd7e5-115">Specifies the object ID of the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd7e5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd7e5-116">-DefaultProfile</span></span>
<span data-ttu-id="fd7e5-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fd7e5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd7e5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd7e5-118">CommonParameters</span></span>
<span data-ttu-id="fd7e5-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fd7e5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd7e5-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd7e5-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd7e5-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fd7e5-121">INPUTS</span></span>

### <span data-ttu-id="fd7e5-122">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="fd7e5-122">BatchAccountContext</span></span>
<span data-ttu-id="fd7e5-123">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="fd7e5-123">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="fd7e5-124">Подстрок</span><span class="sxs-lookup"><span data-stu-id="fd7e5-124">String</span></span>
<span data-ttu-id="fd7e5-125">Параметр ID принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="fd7e5-125">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="fd7e5-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd7e5-126">OUTPUTS</span></span>

## <span data-ttu-id="fd7e5-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="fd7e5-127">NOTES</span></span>

## <span data-ttu-id="fd7e5-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd7e5-128">RELATED LINKS</span></span>

[<span data-ttu-id="fd7e5-129">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="fd7e5-129">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="fd7e5-130">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="fd7e5-130">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="fd7e5-131">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="fd7e5-131">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


