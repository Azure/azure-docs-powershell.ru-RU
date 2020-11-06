---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 5C6D3792-AA56-4210-B376-D9E656B04FBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurebatchnodeagentsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeAgentSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeAgentSku.md
ms.openlocfilehash: 8c9b48046393a55bc0d37e0fe6d08361dcf04246
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566234"
---
# <span data-ttu-id="7e0fd-101">Get-AzureBatchNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="7e0fd-101">Get-AzureBatchNodeAgentSku</span></span>

## <span data-ttu-id="7e0fd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7e0fd-102">SYNOPSIS</span></span>
<span data-ttu-id="7e0fd-103">Возвращает номера SKU агента пакетных узлов, доступные в пакетной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-103">Gets Batch node agent SKUs available in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e0fd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7e0fd-104">SYNTAX</span></span>

```
Get-AzureBatchNodeAgentSku [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e0fd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e0fd-105">DESCRIPTION</span></span>
<span data-ttu-id="7e0fd-106">Командлет **Get-AzureBatchNodeAgentSku** получает номера SKU агента узла, доступные в пакетной учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-106">The **Get-AzureBatchNodeAgentSku** cmdlet gets node agent SKUs that are available in an Azure Batch account.</span></span>
<span data-ttu-id="7e0fd-107">Укажите учетную запись с помощью параметра *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="7e0fd-107">Specify the account by using the *BatchContext* parameter.</span></span>
<span data-ttu-id="7e0fd-108">Вы можете сузить поиск до SKU, который соответствует фильтру Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="7e0fd-108">You can narrow your search to SKUs that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="7e0fd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7e0fd-109">EXAMPLES</span></span>

### <span data-ttu-id="7e0fd-110">Пример 1: получение всех доступных SKU агента узла</span><span class="sxs-lookup"><span data-stu-id="7e0fd-110">Example 1: Get all available node agent SKUs</span></span>
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

<span data-ttu-id="7e0fd-111">Первая команда получает контекст учетной записи пакета, который включает клавиши доступа для вашей подписки, с помощью **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="7e0fd-112">Команда хранит контекст в переменной $Context для использования в следующей команде.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-112">The command stores the context in the $Context variable to use in the next command.</span></span>

<span data-ttu-id="7e0fd-113">Вторая команда получает все доступные SKU агента узла, которые поддерживает пакет.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-113">The second command gets all available node agent SKUs that Batch supports.</span></span>

## <span data-ttu-id="7e0fd-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7e0fd-114">PARAMETERS</span></span>

### <span data-ttu-id="7e0fd-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7e0fd-115">-BatchContext</span></span>
<span data-ttu-id="7e0fd-116">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7e0fd-117">Если для получения BatchAccountContext используется командлет Get-AzureRmBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-117">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7e0fd-118">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzureRmBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-118">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7e0fd-119">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7e0fd-120">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="7e0fd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e0fd-121">-DefaultProfile</span></span>
<span data-ttu-id="7e0fd-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7e0fd-123">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="7e0fd-123">-Filter</span></span>
<span data-ttu-id="7e0fd-124">Задает предложение фильтра OData для SKU агента узла.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-124">Specifies an OData filter clause for node agent SKUs.</span></span>
<span data-ttu-id="7e0fd-125">Если фильтр не указан, этот командлет возвращает все SKU агента узла, которые поддерживает пакет.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-125">If you do not specify a filter, this cmdlet returns all node agent SKUs that Batch supports.</span></span>

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

### <span data-ttu-id="7e0fd-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="7e0fd-126">-MaxCount</span></span>
<span data-ttu-id="7e0fd-127">Задает максимальное количество возвращаемых конфигураций агента узла.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-127">Specifies the maximum number of node agent SKUs to return.</span></span>

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

### <span data-ttu-id="7e0fd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e0fd-128">CommonParameters</span></span>
<span data-ttu-id="7e0fd-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e0fd-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e0fd-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e0fd-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7e0fd-131">INPUTS</span></span>

### <span data-ttu-id="7e0fd-132">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7e0fd-132">BatchAccountContext</span></span>
<span data-ttu-id="7e0fd-133">Параметр "BatchContext" принимает значение типа "BatchAccountContext" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="7e0fd-133">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="7e0fd-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7e0fd-134">OUTPUTS</span></span>

### <span data-ttu-id="7e0fd-135">Microsoft.Azure.Commands.BatCH. Models. PSNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="7e0fd-135">Microsoft.Azure.Commands.Batch.Models.PSNodeAgentSku</span></span>

## <span data-ttu-id="7e0fd-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="7e0fd-136">NOTES</span></span>

## <span data-ttu-id="7e0fd-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7e0fd-137">RELATED LINKS</span></span>

[<span data-ttu-id="7e0fd-138">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="7e0fd-138">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)


