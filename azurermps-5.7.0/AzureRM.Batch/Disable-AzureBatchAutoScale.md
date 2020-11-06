---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
ms.openlocfilehash: 1a53e72cd31d3ca43cf5c9a4e6a66de4bc2bd59d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570267"
---
# <span data-ttu-id="2b8d4-101">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="2b8d4-101">Disable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="2b8d4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2b8d4-102">SYNOPSIS</span></span>
<span data-ttu-id="2b8d4-103">Отключение автоматического масштабирования пула.</span><span class="sxs-lookup"><span data-stu-id="2b8d4-103">Disables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b8d4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2b8d4-104">SYNTAX</span></span>

```
Disable-AzureBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b8d4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b8d4-105">DESCRIPTION</span></span>
<span data-ttu-id="2b8d4-106">Командлет **Disable-AzureBatchAutoScale** отключает автоматическое масштабирование указанного пула.</span><span class="sxs-lookup"><span data-stu-id="2b8d4-106">The **Disable-AzureBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="2b8d4-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2b8d4-107">EXAMPLES</span></span>

### <span data-ttu-id="2b8d4-108">Пример 1: Отключение автоматического масштабирования пула</span><span class="sxs-lookup"><span data-stu-id="2b8d4-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzureBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="2b8d4-109">Эта команда отключает автоматическое масштабирование для пула с именем MyPool.</span><span class="sxs-lookup"><span data-stu-id="2b8d4-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="2b8d4-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2b8d4-110">PARAMETERS</span></span>

### <span data-ttu-id="2b8d4-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2b8d4-111">-BatchContext</span></span>
<span data-ttu-id="2b8d4-112">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="2b8d4-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2b8d4-113">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="2b8d4-113">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2b8d4-114">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="2b8d4-114">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2b8d4-115">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="2b8d4-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2b8d4-116">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="2b8d4-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b8d4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b8d4-117">-DefaultProfile</span></span>
<span data-ttu-id="2b8d4-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2b8d4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b8d4-119">-ID</span><span class="sxs-lookup"><span data-stu-id="2b8d4-119">-Id</span></span>
<span data-ttu-id="2b8d4-120">Указывает идентификатор объекта пула.</span><span class="sxs-lookup"><span data-stu-id="2b8d4-120">Specifies the object ID of the pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b8d4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b8d4-121">CommonParameters</span></span>
<span data-ttu-id="2b8d4-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2b8d4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b8d4-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b8d4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b8d4-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2b8d4-124">INPUTS</span></span>

### <span data-ttu-id="2b8d4-125">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2b8d4-125">BatchAccountContext</span></span>
<span data-ttu-id="2b8d4-126">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="2b8d4-126">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="2b8d4-127">Подстрок</span><span class="sxs-lookup"><span data-stu-id="2b8d4-127">String</span></span>
<span data-ttu-id="2b8d4-128">Параметр ID принимает значение типа String из конвейера.</span><span class="sxs-lookup"><span data-stu-id="2b8d4-128">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="2b8d4-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2b8d4-129">OUTPUTS</span></span>

## <span data-ttu-id="2b8d4-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="2b8d4-130">NOTES</span></span>

## <span data-ttu-id="2b8d4-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2b8d4-131">RELATED LINKS</span></span>

[<span data-ttu-id="2b8d4-132">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="2b8d4-132">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="2b8d4-133">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="2b8d4-133">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="2b8d4-134">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="2b8d4-134">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


