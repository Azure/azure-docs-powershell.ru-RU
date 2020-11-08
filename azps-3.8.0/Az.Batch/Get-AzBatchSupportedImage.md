---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchsupportedimage.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchSupportedImage.md
ms.openlocfilehash: 56ec7eafcea7233697089d692b2799fa6c9b744a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073002"
---
# <span data-ttu-id="1882f-101">Get-AzBatchSupportedImage</span><span class="sxs-lookup"><span data-stu-id="1882f-101">Get-AzBatchSupportedImage</span></span>

## <span data-ttu-id="1882f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1882f-102">SYNOPSIS</span></span>
<span data-ttu-id="1882f-103">Возвращает образы, поддерживаемые пакетной учетной записью пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="1882f-103">Gets Batch supported images for a Batch account.</span></span>

## <span data-ttu-id="1882f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1882f-104">SYNTAX</span></span>

```
Get-AzBatchSupportedImage [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1882f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1882f-105">DESCRIPTION</span></span>
<span data-ttu-id="1882f-106">Командлет **Get-AzBatchSupportedImage** получает поддерживаемые образы виртуальных машин, доступные в пакетной учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="1882f-106">The **Get-AzBatchSupportedImage** cmdlet gets supported virtual machine images that are available in an Azure Batch account.</span></span>
<span data-ttu-id="1882f-107">Укажите учетную запись с помощью параметра *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="1882f-107">Specify the account by using the *BatchContext* parameter.</span></span>

## <span data-ttu-id="1882f-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1882f-108">EXAMPLES</span></span>

### <span data-ttu-id="1882f-109">Пример 1: получение всех доступных поддерживаемых изображений</span><span class="sxs-lookup"><span data-stu-id="1882f-109">Example 1: Get all available supported images</span></span>

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

<span data-ttu-id="1882f-110">Первая команда получает контекст учетной записи пакета, который включает клавиши доступа для вашей подписки, с помощью **Get-AzBatchAccountKey**.</span><span class="sxs-lookup"><span data-stu-id="1882f-110">The first command gets a Batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKey**.</span></span>
<span data-ttu-id="1882f-111">Команда хранит контекст в переменной $Context для использования в следующей команде.</span><span class="sxs-lookup"><span data-stu-id="1882f-111">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="1882f-112">Вторая команда получает все доступные изображения для этой учетной записи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="1882f-112">The second command gets all available supported images for that Batch account.</span></span>

## <span data-ttu-id="1882f-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1882f-113">PARAMETERS</span></span>

### <span data-ttu-id="1882f-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="1882f-114">-BatchContext</span></span>
<span data-ttu-id="1882f-115">Экземпляр BatchAccountContext, который будет использоваться при взаимодействии со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="1882f-115">The BatchAccountContext instance to use when interacting with the Batch service.</span></span>
<span data-ttu-id="1882f-116">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="1882f-116">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span>
<span data-ttu-id="1882f-117">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKey, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="1882f-117">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span>
<span data-ttu-id="1882f-118">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="1882f-118">When using shared key authentication, the primary access key is used by default.</span></span>
<span data-ttu-id="1882f-119">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="1882f-119">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="1882f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1882f-120">-DefaultProfile</span></span>
<span data-ttu-id="1882f-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1882f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1882f-122">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="1882f-122">-Filter</span></span>
<span data-ttu-id="1882f-123">Задает предложение фильтра OData для поддерживаемых изображений.</span><span class="sxs-lookup"><span data-stu-id="1882f-123">Specifies an OData filter clause for supported images.</span></span>
<span data-ttu-id="1882f-124">Если фильтр не указан, этот командлет возвращает все изображения, поддерживаемые пакетной учетной записью.</span><span class="sxs-lookup"><span data-stu-id="1882f-124">If you do not specify a filter, this cmdlet returns all images the Batch account supports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1882f-125">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="1882f-125">-MaxCount</span></span>
<span data-ttu-id="1882f-126">Задает максимальное количество поддерживаемых изображений.</span><span class="sxs-lookup"><span data-stu-id="1882f-126">Specifies the maximum number of supported images to return.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1882f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1882f-127">CommonParameters</span></span>
<span data-ttu-id="1882f-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1882f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1882f-129">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1882f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1882f-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1882f-130">INPUTS</span></span>

### <span data-ttu-id="1882f-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1882f-131">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="1882f-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1882f-132">OUTPUTS</span></span>

### <span data-ttu-id="1882f-133">Microsoft.Azure.Commands.BatCH. Models. PSImageInformation</span><span class="sxs-lookup"><span data-stu-id="1882f-133">Microsoft.Azure.Commands.Batch.Models.PSImageInformation</span></span>

## <span data-ttu-id="1882f-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="1882f-134">NOTES</span></span>

## <span data-ttu-id="1882f-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1882f-135">RELATED LINKS</span></span>
[<span data-ttu-id="1882f-136">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="1882f-136">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)