---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/disable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
ms.openlocfilehash: f0530b509bea965c1c901992f9a91b351dae9ae3
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "94077202"
---
# <span data-ttu-id="0c8d5-101">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="0c8d5-101">Disable-AzBatchAutoScale</span></span>

## <span data-ttu-id="0c8d5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0c8d5-102">SYNOPSIS</span></span>
<span data-ttu-id="0c8d5-103">Отключение автоматического масштабирования пула.</span><span class="sxs-lookup"><span data-stu-id="0c8d5-103">Disables automatic scaling of a pool.</span></span>

## <span data-ttu-id="0c8d5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0c8d5-104">SYNTAX</span></span>

```
Disable-AzBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c8d5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c8d5-105">DESCRIPTION</span></span>
<span data-ttu-id="0c8d5-106">Командлет **Disable-AzBatchAutoScale** отключает автоматическое масштабирование указанного пула.</span><span class="sxs-lookup"><span data-stu-id="0c8d5-106">The **Disable-AzBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="0c8d5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0c8d5-107">EXAMPLES</span></span>

### <span data-ttu-id="0c8d5-108">Пример 1: Отключение автоматического масштабирования пула</span><span class="sxs-lookup"><span data-stu-id="0c8d5-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="0c8d5-109">Эта команда отключает автоматическое масштабирование для пула с именем MyPool.</span><span class="sxs-lookup"><span data-stu-id="0c8d5-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="0c8d5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0c8d5-110">PARAMETERS</span></span>

### <span data-ttu-id="0c8d5-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0c8d5-111">-BatchContext</span></span>
<span data-ttu-id="0c8d5-112">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="0c8d5-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0c8d5-113">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="0c8d5-113">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0c8d5-114">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="0c8d5-114">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0c8d5-115">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="0c8d5-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0c8d5-116">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="0c8d5-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="0c8d5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c8d5-117">-DefaultProfile</span></span>
<span data-ttu-id="0c8d5-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0c8d5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c8d5-119">-ID</span><span class="sxs-lookup"><span data-stu-id="0c8d5-119">-Id</span></span>
<span data-ttu-id="0c8d5-120">Указывает идентификатор объекта пула.</span><span class="sxs-lookup"><span data-stu-id="0c8d5-120">Specifies the object ID of the pool.</span></span>

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

### <span data-ttu-id="0c8d5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c8d5-121">CommonParameters</span></span>
<span data-ttu-id="0c8d5-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0c8d5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c8d5-123">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c8d5-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c8d5-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0c8d5-124">INPUTS</span></span>

### <span data-ttu-id="0c8d5-125">System. String</span><span class="sxs-lookup"><span data-stu-id="0c8d5-125">System.String</span></span>

### <span data-ttu-id="0c8d5-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0c8d5-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="0c8d5-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c8d5-127">OUTPUTS</span></span>

### <span data-ttu-id="0c8d5-128">System. void</span><span class="sxs-lookup"><span data-stu-id="0c8d5-128">System.Void</span></span>

## <span data-ttu-id="0c8d5-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="0c8d5-129">NOTES</span></span>

## <span data-ttu-id="0c8d5-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c8d5-130">RELATED LINKS</span></span>

[<span data-ttu-id="0c8d5-131">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="0c8d5-131">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="0c8d5-132">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="0c8d5-132">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="0c8d5-133">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="0c8d5-133">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


