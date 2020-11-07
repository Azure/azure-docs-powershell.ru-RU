---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 5C6D3792-AA56-4210-B376-D9E656B04FBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodeagentsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeAgentSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeAgentSku.md
ms.openlocfilehash: 8f7228a540456e76e4f7a22d70d00969a9ef568c
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "93731884"
---
# <span data-ttu-id="94cdd-101">Get-AzBatchNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="94cdd-101">Get-AzBatchNodeAgentSku</span></span>

## <span data-ttu-id="94cdd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="94cdd-102">SYNOPSIS</span></span>
<span data-ttu-id="94cdd-103">Возвращает номера SKU агента пакетных узлов, доступные в пакетной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="94cdd-103">Gets Batch node agent SKUs available in a Batch account.</span></span>

## <span data-ttu-id="94cdd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="94cdd-104">SYNTAX</span></span>

```
Get-AzBatchNodeAgentSku [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94cdd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94cdd-105">DESCRIPTION</span></span>
<span data-ttu-id="94cdd-106">Командлет **Get-AzBatchNodeAgentSku** получает номера SKU агента узла, доступные в пакетной учетной записи Azure.</span><span class="sxs-lookup"><span data-stu-id="94cdd-106">The **Get-AzBatchNodeAgentSku** cmdlet gets node agent SKUs that are available in an Azure Batch account.</span></span>
<span data-ttu-id="94cdd-107">Укажите учетную запись с помощью параметра *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="94cdd-107">Specify the account by using the *BatchContext* parameter.</span></span>
<span data-ttu-id="94cdd-108">Вы можете сузить поиск до SKU, который соответствует фильтру Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="94cdd-108">You can narrow your search to SKUs that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="94cdd-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="94cdd-109">EXAMPLES</span></span>

### <span data-ttu-id="94cdd-110">Пример 1: получение всех доступных SKU агента узла</span><span class="sxs-lookup"><span data-stu-id="94cdd-110">Example 1: Get all available node agent SKUs</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchNodeAgentSku -BatchContext $Context 
batch.node.centos 7 Linux {7.0, 7.1, 7.2, OL70} 
batch.node.debian 8 Linux {15.10, 8} 
batch.node.opensuse 13.2 Linux {13.2} 
batch.node.opensuse 42.1 Linux {42.1, 12, 12-SP1, 12} 
batch.node.ubuntu 14.04 Linux {14.04.0-LTS, 14.04.1-LTS, 14.04.2-LTS, 14.04.3-LTS...} 
batch.node.windows amd64 Windows {2008-R2-SP1, 2012-Datacenter, 2012-R2-Datacenter, Windows-Server-Technical-Preview}
```

<span data-ttu-id="94cdd-111">Первая команда получает контекст учетной записи пакета, который включает клавиши доступа для вашей подписки, с помощью **Get-AzBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="94cdd-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKeys**.</span></span>
<span data-ttu-id="94cdd-112">Команда хранит контекст в переменной $Context для использования в следующей команде.</span><span class="sxs-lookup"><span data-stu-id="94cdd-112">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="94cdd-113">Вторая команда получает все доступные SKU агента узла, которые поддерживает пакет.</span><span class="sxs-lookup"><span data-stu-id="94cdd-113">The second command gets all available node agent SKUs that Batch supports.</span></span>

## <span data-ttu-id="94cdd-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="94cdd-114">PARAMETERS</span></span>

### <span data-ttu-id="94cdd-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="94cdd-115">-BatchContext</span></span>
<span data-ttu-id="94cdd-116">Указывает экземпляр **BatchAccountContext** , используемый этим командлетом для взаимодействия со службой пакетной обработки.</span><span class="sxs-lookup"><span data-stu-id="94cdd-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="94cdd-117">Если для получения BatchAccountContext используется командлет Get-AzBatchAccount, проверка подлинности Azure Active Directory будет использоваться при взаимодействии с пакетной службой.</span><span class="sxs-lookup"><span data-stu-id="94cdd-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="94cdd-118">Чтобы использовать проверку подлинности с использованием общего ключа, используйте командлет Get-AzBatchAccountKeys, чтобы получить объект BatchAccountContext с заполненными ключами доступа.</span><span class="sxs-lookup"><span data-stu-id="94cdd-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="94cdd-119">При использовании проверки подлинности с использованием общего ключа по умолчанию используется первичный ключ доступа.</span><span class="sxs-lookup"><span data-stu-id="94cdd-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="94cdd-120">Чтобы изменить ключ на использование, задайте свойство BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="94cdd-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="94cdd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94cdd-121">-DefaultProfile</span></span>
<span data-ttu-id="94cdd-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="94cdd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="94cdd-123">-Фильтр</span><span class="sxs-lookup"><span data-stu-id="94cdd-123">-Filter</span></span>
<span data-ttu-id="94cdd-124">Задает предложение фильтра OData для SKU агента узла.</span><span class="sxs-lookup"><span data-stu-id="94cdd-124">Specifies an OData filter clause for node agent SKUs.</span></span>
<span data-ttu-id="94cdd-125">Если фильтр не указан, этот командлет возвращает все SKU агента узла, которые поддерживает пакет.</span><span class="sxs-lookup"><span data-stu-id="94cdd-125">If you do not specify a filter, this cmdlet returns all node agent SKUs that Batch supports.</span></span>

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

### <span data-ttu-id="94cdd-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="94cdd-126">-MaxCount</span></span>
<span data-ttu-id="94cdd-127">Задает максимальное количество возвращаемых конфигураций агента узла.</span><span class="sxs-lookup"><span data-stu-id="94cdd-127">Specifies the maximum number of node agent SKUs to return.</span></span>

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

### <span data-ttu-id="94cdd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94cdd-128">CommonParameters</span></span>
<span data-ttu-id="94cdd-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="94cdd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94cdd-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="94cdd-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94cdd-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="94cdd-131">INPUTS</span></span>

### <span data-ttu-id="94cdd-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="94cdd-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="94cdd-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="94cdd-133">OUTPUTS</span></span>

### <span data-ttu-id="94cdd-134">Microsoft.Azure.Commands.BatCH. Models. PSNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="94cdd-134">Microsoft.Azure.Commands.Batch.Models.PSNodeAgentSku</span></span>

## <span data-ttu-id="94cdd-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="94cdd-135">NOTES</span></span>

## <span data-ttu-id="94cdd-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94cdd-136">RELATED LINKS</span></span>

[<span data-ttu-id="94cdd-137">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="94cdd-137">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)


