---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 9C755BE8-0624-4CF7-AE7C-34DAF44678E8
online version: https://docs.microsoft.com/powershell/module/az.batch/disable-azbatchautoscale
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Disable-AzBatchAutoScale.md
ms.openlocfilehash: 8b0bf38d68f4dbab815b6de1f056439cd5e88e3f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008131"
---
# <span data-ttu-id="89fbb-101">Disable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="89fbb-101">Disable-AzBatchAutoScale</span></span>

## <span data-ttu-id="89fbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89fbb-102">SYNOPSIS</span></span>
<span data-ttu-id="89fbb-103">Отключает автоматическое масштабирование пула.</span><span class="sxs-lookup"><span data-stu-id="89fbb-103">Disables automatic scaling of a pool.</span></span>

## <span data-ttu-id="89fbb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="89fbb-104">SYNTAX</span></span>

```
Disable-AzBatchAutoScale [-Id] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89fbb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="89fbb-105">DESCRIPTION</span></span>
<span data-ttu-id="89fbb-106">Для отключения автоматического масштабирования указанного пула с его использованием будет отключена функция **disable-AzBatchAutoScale.**</span><span class="sxs-lookup"><span data-stu-id="89fbb-106">The **Disable-AzBatchAutoScale** cmdlet disables automatic scaling of the specified pool.</span></span>

## <span data-ttu-id="89fbb-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="89fbb-107">EXAMPLES</span></span>

### <span data-ttu-id="89fbb-108">Пример 1. Отключение автоматического масштабирования пула</span><span class="sxs-lookup"><span data-stu-id="89fbb-108">Example 1: Disable automatic scaling of a pool</span></span>
```
PS C:\>Disable-AzBatchAutoScale -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="89fbb-109">Эта команда отключает автоматическое масштабирование для пула MyPool.</span><span class="sxs-lookup"><span data-stu-id="89fbb-109">This command disables automatic scaling for the pool named MyPool.</span></span>

## <span data-ttu-id="89fbb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89fbb-110">PARAMETERS</span></span>

### <span data-ttu-id="89fbb-111">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="89fbb-111">-BatchContext</span></span>
<span data-ttu-id="89fbb-112">Указывает экземпляр **BatchAccountContext,** который этот cmdlet использует для взаимодействия со службой Batch.</span><span class="sxs-lookup"><span data-stu-id="89fbb-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="89fbb-113">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="89fbb-113">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="89fbb-114">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="89fbb-114">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="89fbb-115">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="89fbb-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="89fbb-116">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="89fbb-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="89fbb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89fbb-117">-DefaultProfile</span></span>
<span data-ttu-id="89fbb-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="89fbb-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89fbb-119">-Id</span><span class="sxs-lookup"><span data-stu-id="89fbb-119">-Id</span></span>
<span data-ttu-id="89fbb-120">Определяет ИД объекта пула.</span><span class="sxs-lookup"><span data-stu-id="89fbb-120">Specifies the object ID of the pool.</span></span>

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

### <span data-ttu-id="89fbb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89fbb-121">CommonParameters</span></span>
<span data-ttu-id="89fbb-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89fbb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89fbb-123">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89fbb-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89fbb-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="89fbb-124">INPUTS</span></span>

### <span data-ttu-id="89fbb-125">System.String</span><span class="sxs-lookup"><span data-stu-id="89fbb-125">System.String</span></span>

### <span data-ttu-id="89fbb-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="89fbb-126">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="89fbb-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="89fbb-127">OUTPUTS</span></span>

### <span data-ttu-id="89fbb-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="89fbb-128">System.Void</span></span>

## <span data-ttu-id="89fbb-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="89fbb-129">NOTES</span></span>

## <span data-ttu-id="89fbb-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="89fbb-130">RELATED LINKS</span></span>

[<span data-ttu-id="89fbb-131">Enable-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="89fbb-131">Enable-AzBatchAutoScale</span></span>](./Enable-AzBatchAutoScale.md)

[<span data-ttu-id="89fbb-132">Test-AzBatchAutoScale</span><span class="sxs-lookup"><span data-stu-id="89fbb-132">Test-AzBatchAutoScale</span></span>](./Test-AzBatchAutoScale.md)

[<span data-ttu-id="89fbb-133">Пакетные cmdlets Azure</span><span class="sxs-lookup"><span data-stu-id="89fbb-133">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)


