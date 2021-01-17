---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchsupportedimage.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
ms.openlocfilehash: e06b9957b8e9b58e25b52b69d4064aca1a69035a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98404836"
---
# <span data-ttu-id="84e77-101">Get-AzBatchSupportedImage</span><span class="sxs-lookup"><span data-stu-id="84e77-101">Get-AzBatchSupportedImage</span></span>

## <span data-ttu-id="84e77-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84e77-102">SYNOPSIS</span></span>
<span data-ttu-id="84e77-103">Получает поддерживаемые пакетом изображения для учетной записи пакета.</span><span class="sxs-lookup"><span data-stu-id="84e77-103">Gets Batch supported images for a Batch account.</span></span>

## <span data-ttu-id="84e77-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="84e77-104">SYNTAX</span></span>

```
Get-AzBatchSupportedImage [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84e77-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="84e77-105">DESCRIPTION</span></span>
<span data-ttu-id="84e77-106">Для получения поддерживаемых изображений виртуальных машин, доступных в учетной записи Azure Batch, поддерживается cmdlet **Get-AzBatchSupportedImage.**</span><span class="sxs-lookup"><span data-stu-id="84e77-106">The **Get-AzBatchSupportedImage** cmdlet gets supported virtual machine images that are available in an Azure Batch account.</span></span>
<span data-ttu-id="84e77-107">Укажите учетную запись с помощью *параметра BatchContext.*</span><span class="sxs-lookup"><span data-stu-id="84e77-107">Specify the account by using the *BatchContext* parameter.</span></span>

## <span data-ttu-id="84e77-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="84e77-108">EXAMPLES</span></span>

### <span data-ttu-id="84e77-109">Пример 1. Получить все доступные поддерживаемые изображения</span><span class="sxs-lookup"><span data-stu-id="84e77-109">Example 1: Get all available supported images</span></span>

```powershell
PS C:\>$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchSupportedImage -BatchContext $Context
BatchSupportEndOfLife :
Capabilities          :
ImageReference        : canonical:ubuntuserver:16.04-lts:latest
NodeAgentSkuId        : batch.node.ubuntu 16.04
OSType                : Linux
VerificationType      : Verified

BatchSupportEndOfLife :
Capabilities          :
ImageReference        : canonical:ubuntuserver:18.04-lts:latest
NodeAgentSkuId        : batch.node.ubuntu 18.04
OSType                : Linux
VerificationType      : Verified

BatchSupportEndOfLife :
Capabilities          :
ImageReference        : credativ:debian:8:latest
NodeAgentSkuId        : batch.node.debian 8
OSType                : Linux
VerificationType      : Verified

BatchSupportEndOfLife :
Capabilities          :
ImageReference        : microsoftwindowsserver:windowsserver:2016-datacenter:latest
NodeAgentSkuId        : batch.node.windows amd64
OSType                : Windows
VerificationType      : Verified

...
```

<span data-ttu-id="84e77-110">Первая команда получает контекст пакетной учетной записи, содержащего ключи доступа для вашей подписки, с помощью **Get-AzBatchAccountKey.**</span><span class="sxs-lookup"><span data-stu-id="84e77-110">The first command gets a Batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="84e77-111">Команда сохраняет контекст в переменной $Context для использования в следующей команде.</span><span class="sxs-lookup"><span data-stu-id="84e77-111">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="84e77-112">Вторая команда получает все поддерживаемые изображения для этой учетной записи Пакета.</span><span class="sxs-lookup"><span data-stu-id="84e77-112">The second command gets all available supported images for that Batch account.</span></span>

## <span data-ttu-id="84e77-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84e77-113">PARAMETERS</span></span>

### <span data-ttu-id="84e77-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="84e77-114">-BatchContext</span></span>
<span data-ttu-id="84e77-115">Экземпляр BatchAccountContext, который используется при взаимодействии со службой batch.</span><span class="sxs-lookup"><span data-stu-id="84e77-115">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="84e77-116">Если для Get-AzBatchAccount BatchAccountContext используется Get-AzBatchAccount, при взаимодействии со службой пакета будет использоваться проверка подлинности Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="84e77-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="84e77-117">Чтобы использовать проверку подлинности общего ключа, используйте Get-AzBatchAccountKey для получения объекта BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="84e77-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="84e77-118">При использовании проверки подлинности общего ключа первичный ключ доступа используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="84e77-118">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="84e77-119">Чтобы изменить ключ, за установите свойство BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="84e77-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="84e77-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84e77-120">-DefaultProfile</span></span>
<span data-ttu-id="84e77-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="84e77-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84e77-122">-Filter</span><span class="sxs-lookup"><span data-stu-id="84e77-122">-Filter</span></span>
<span data-ttu-id="84e77-123">Предложение фильтра OData для поддерживаемых изображений.</span><span class="sxs-lookup"><span data-stu-id="84e77-123">Specifies an OData filter clause for supported images.</span></span>
<span data-ttu-id="84e77-124">Если не указать фильтр, этот cmdlet возвращает все изображения, поддерживаемые учетной записью Batch.</span><span class="sxs-lookup"><span data-stu-id="84e77-124">If you do not specify a filter, this cmdlet returns all images the Batch account supports.</span></span>

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

### <span data-ttu-id="84e77-125">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="84e77-125">-MaxCount</span></span>
<span data-ttu-id="84e77-126">Указывает максимальное количество поддерживаемых изображений, которые нужно вернуть.</span><span class="sxs-lookup"><span data-stu-id="84e77-126">Specifies the maximum number of supported images to return.</span></span>

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

### <span data-ttu-id="84e77-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84e77-127">CommonParameters</span></span>
<span data-ttu-id="84e77-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84e77-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84e77-129">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84e77-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84e77-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="84e77-130">INPUTS</span></span>

### <span data-ttu-id="84e77-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="84e77-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="84e77-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="84e77-132">OUTPUTS</span></span>

### <span data-ttu-id="84e77-133">Microsoft.Azure.Commands.Batch. Models.PSImageInformation</span><span class="sxs-lookup"><span data-stu-id="84e77-133">Microsoft.Azure.Commands.Batch.Models.PSImageInformation</span></span>

## <span data-ttu-id="84e77-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="84e77-134">NOTES</span></span>

## <span data-ttu-id="84e77-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="84e77-135">RELATED LINKS</span></span>

[<span data-ttu-id="84e77-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="84e77-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)