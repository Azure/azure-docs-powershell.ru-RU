---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/disable-azurebatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Disable-AzureBatchAutoScale.md
ms.openlocfilehash: 403e38ae72f927b4b98107161b62859aa57bacf9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732320"
---
# <span data-ttu-id="e40f3-101">Disable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="e40f3-101">Disable-AzureBatchAutoScale</span></span>

## <span data-ttu-id="e40f3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e40f3-102">SYNOPSIS</span></span>
<span data-ttu-id="e40f3-103">Отключение автоматического масштабирования пула.</span><span class="sxs-lookup"><span data-stu-id="e40f3-103">Disables automatic scaling of a pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e40f3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e40f3-104">SYNTAX</span></span>

```
Disable-AzureBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e40f3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e40f3-105">DESCRIPTION</span></span>
<span data-ttu-id="e40f3-106">Командлет **Disable-AzureBatchAutoScale** отключает автоматическое масштабирование указанного пула.</span><span class="sxs-lookup"><span data-stu-id="e40f3-106">The **Disable-AzureBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="e40f3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e40f3-107">EXAMPLES</span></span>

### <span data-ttu-id="e40f3-108">Пример 1: Отключение автоматического масштабирования пула</span><span class="sxs-lookup"><span data-stu-id="e40f3-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzureBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="e40f3-109">Эта команда отключает автоматическое масштабирование для пула с именем MyPool.</span><span class="sxs-lookup"><span data-stu-id="e40f3-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="e40f3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e40f3-110">PARAMETERS</span></span>

### <span data-ttu-id="e40f3-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="e40f3-111">-BatchContext</span></span>
<span data-ttu-id="e40f3-112">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="e40f3-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="e40f3-113">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="e40f3-113">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="e40f3-114">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="e40f3-114">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="e40f3-115">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="e40f3-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="e40f3-116">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="e40f3-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="e40f3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e40f3-117">-DefaultProfile</span></span>
<span data-ttu-id="e40f3-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e40f3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e40f3-119">-ID</span><span class="sxs-lookup"><span data-stu-id="e40f3-119">-Id</span></span>
<span data-ttu-id="e40f3-120">Указывает идентификатор объекта пула.</span><span class="sxs-lookup"><span data-stu-id="e40f3-120">Specifies the object ID of the pool.</span></span>

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

### <span data-ttu-id="e40f3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e40f3-121">CommonParameters</span></span>
<span data-ttu-id="e40f3-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e40f3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e40f3-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e40f3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e40f3-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e40f3-124">INPUTS</span></span>

### <span data-ttu-id="e40f3-125">System. String</span><span class="sxs-lookup"><span data-stu-id="e40f3-125">System.String</span></span>

### <span data-ttu-id="e40f3-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="e40f3-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="e40f3-127">Параметры: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e40f3-127">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="e40f3-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e40f3-128">OUTPUTS</span></span>

### <span data-ttu-id="e40f3-129">System. void</span><span class="sxs-lookup"><span data-stu-id="e40f3-129">System.Void</span></span>

## <span data-ttu-id="e40f3-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="e40f3-130">NOTES</span></span>

## <span data-ttu-id="e40f3-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e40f3-131">RELATED LINKS</span></span>

[<span data-ttu-id="e40f3-132">Enable-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="e40f3-132">Enable-AzureBatchAutoScale</span></span>](./Enable-AzureBatchAutoScale.md)

[<span data-ttu-id="e40f3-133">Test-AzureBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="e40f3-133">Test-AzureBatchAutoScale</span></span>](./Test-AzureBatchAutoScale.md)

[<span data-ttu-id="e40f3-134">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="e40f3-134">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


