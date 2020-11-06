---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountskus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
ms.openlocfilehash: ed243f822817c223576fd3bbe0293a8cf18d7a51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559227"
---
# <span data-ttu-id="11025-101">Get-AzureRmCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="11025-101">Get-AzureRmCognitiveServicesAccountSkus</span></span>

## <span data-ttu-id="11025-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="11025-102">SYNOPSIS</span></span>
<span data-ttu-id="11025-103">Возвращает доступные SKU для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="11025-103">Gets the available SKUs for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11025-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="11025-104">SYNTAX</span></span>

```
Get-AzureRmCognitiveServicesAccountSkus [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11025-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11025-105">DESCRIPTION</span></span>
<span data-ttu-id="11025-106">Командлет **Get-AzureRmCognitiveServicesAccountSkus** получает доступные SKU для учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="11025-106">The **Get-AzureRmCognitiveServicesAccountSkus** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>

<span data-ttu-id="11025-107">SKU — это ярусный план для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="11025-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="11025-108">Она определяет цену, ограничение на звонки и ставку для счета.</span><span class="sxs-lookup"><span data-stu-id="11025-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="11025-109">F0 SKU является бесплатным уровнем.</span><span class="sxs-lookup"><span data-stu-id="11025-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="11025-110">Оплаченные уровни включают в себя S0, S1, S2 и т. д.</span><span class="sxs-lookup"><span data-stu-id="11025-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="11025-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="11025-111">EXAMPLES</span></span>

## <span data-ttu-id="11025-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="11025-112">PARAMETERS</span></span>

### <span data-ttu-id="11025-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11025-113">-DefaultProfile</span></span>
<span data-ttu-id="11025-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="11025-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11025-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="11025-115">-Name</span></span>
<span data-ttu-id="11025-116">Указывает имя учетной записи.</span><span class="sxs-lookup"><span data-stu-id="11025-116">Specifies the name of the account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11025-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11025-117">-ResourceGroupName</span></span>
<span data-ttu-id="11025-118">Указывает имя группы ресурсов, которой назначена эта учетная запись.</span><span class="sxs-lookup"><span data-stu-id="11025-118">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11025-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11025-119">CommonParameters</span></span>
<span data-ttu-id="11025-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="11025-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11025-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11025-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11025-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="11025-122">INPUTS</span></span>

### <span data-ttu-id="11025-123">Ничего</span><span class="sxs-lookup"><span data-stu-id="11025-123">None</span></span>
<span data-ttu-id="11025-124">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="11025-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="11025-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="11025-125">OUTPUTS</span></span>

### <span data-ttu-id="11025-126">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesSkus</span><span class="sxs-lookup"><span data-stu-id="11025-126">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesSkus</span></span>

## <span data-ttu-id="11025-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="11025-127">NOTES</span></span>

## <span data-ttu-id="11025-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11025-128">RELATED LINKS</span></span>

