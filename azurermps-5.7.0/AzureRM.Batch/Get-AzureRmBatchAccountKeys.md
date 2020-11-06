---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchaccountkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
ms.openlocfilehash: 8e6e10c45034402e5339ed5cb6d60a9319362450
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557584"
---
# <span data-ttu-id="c1b1b-101">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="c1b1b-101">Get-AzureRmBatchAccountKeys</span></span>

## <span data-ttu-id="c1b1b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c1b1b-102">SYNOPSIS</span></span>
<span data-ttu-id="c1b1b-103">Возвращает ключи учетной записи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="c1b1b-103">Gets the keys of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1b1b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c1b1b-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccountKeys [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1b1b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1b1b-105">DESCRIPTION</span></span>
<span data-ttu-id="c1b1b-106">Командлет **Get-AzureRmBatchAccountKeys** получает ключи учетной записи пакетной службы Azure в текущей подписке.</span><span class="sxs-lookup"><span data-stu-id="c1b1b-106">The **Get-AzureRmBatchAccountKeys** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="c1b1b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c1b1b-107">EXAMPLES</span></span>

## <span data-ttu-id="c1b1b-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c1b1b-108">PARAMETERS</span></span>

### <span data-ttu-id="c1b1b-109">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="c1b1b-109">-AccountName</span></span>
<span data-ttu-id="c1b1b-110">Указывает имя учетной записи, для которой этот командлет получает ключи.</span><span class="sxs-lookup"><span data-stu-id="c1b1b-110">Specifies the name of the account for which this cmdlet gets keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1b1b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1b1b-111">-DefaultProfile</span></span>
<span data-ttu-id="c1b1b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c1b1b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1b1b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1b1b-113">-ResourceGroupName</span></span>
<span data-ttu-id="c1b1b-114">Указывает имя группы ресурсов, которая содержит учетную запись, для которой этот командлет получает ключи.</span><span class="sxs-lookup"><span data-stu-id="c1b1b-114">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1b1b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1b1b-115">CommonParameters</span></span>
<span data-ttu-id="c1b1b-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c1b1b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1b1b-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1b1b-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1b1b-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c1b1b-118">INPUTS</span></span>

### <span data-ttu-id="c1b1b-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="c1b1b-119">None</span></span>
<span data-ttu-id="c1b1b-120">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="c1b1b-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c1b1b-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c1b1b-121">OUTPUTS</span></span>

### <span data-ttu-id="c1b1b-122">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="c1b1b-122">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="c1b1b-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="c1b1b-123">NOTES</span></span>

## <span data-ttu-id="c1b1b-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c1b1b-124">RELATED LINKS</span></span>

[<span data-ttu-id="c1b1b-125">New-AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="c1b1b-125">New-AzureRmBatchAccountKey</span></span>](./New-AzureRmBatchAccountKey.md)

[<span data-ttu-id="c1b1b-126">Командлеты пакетной службы Azure</span><span class="sxs-lookup"><span data-stu-id="c1b1b-126">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


