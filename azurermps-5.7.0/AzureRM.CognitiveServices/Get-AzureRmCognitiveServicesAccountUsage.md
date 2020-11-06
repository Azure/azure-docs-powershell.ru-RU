---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccountusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountUsage.md
ms.openlocfilehash: a549e6c94ae43c8c1cc267448552565f932aa63d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557575"
---
# <span data-ttu-id="f9bd1-101">Get-AzureRmCognitiveServicesAccountUsage</span><span class="sxs-lookup"><span data-stu-id="f9bd1-101">Get-AzureRmCognitiveServicesAccountUsage</span></span>

## <span data-ttu-id="f9bd1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f9bd1-102">SYNOPSIS</span></span>
<span data-ttu-id="f9bd1-103">Получение текущих использований для учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="f9bd1-103">Get current usages for a Cognitive Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9bd1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f9bd1-104">SYNTAX</span></span>

### <span data-ttu-id="f9bd1-105">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9bd1-105">InputObjectParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-InputObject] <PSCognitiveServicesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9bd1-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9bd1-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f9bd1-107">ResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9bd1-107">ResourceNameParameterSet</span></span>
```
Get-AzureRmCognitiveServicesAccountUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9bd1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9bd1-108">DESCRIPTION</span></span>
<span data-ttu-id="f9bd1-109">Командлет **Get-AzureRmCognitiveServicesAccountUsage** получает текущее использование для учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="f9bd1-109">The **Get-AzureRmCognitiveServicesAccountUsage** cmdlet gets current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="f9bd1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f9bd1-110">EXAMPLES</span></span>

### <span data-ttu-id="f9bd1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f9bd1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountUsage -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="f9bd1-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="f9bd1-112">Example 2</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzureRmCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzureRmCognitiveServicesAccountUsage -InputObject $acc


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="f9bd1-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="f9bd1-113">Example 3</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzureRmCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzureRmCognitiveServicesAccountUsage -ResourceId $acc.Id


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

## <span data-ttu-id="f9bd1-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f9bd1-114">PARAMETERS</span></span>

### <span data-ttu-id="f9bd1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9bd1-115">-DefaultProfile</span></span>
<span data-ttu-id="f9bd1-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f9bd1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9bd1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9bd1-117">-InputObject</span></span>
<span data-ttu-id="f9bd1-118">Объект учетной записи самообслуживания служб.</span><span class="sxs-lookup"><span data-stu-id="f9bd1-118">Cognitive Services Account Object.</span></span>
```yaml
Type: PSCognitiveServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9bd1-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f9bd1-119">-Name</span></span>
<span data-ttu-id="f9bd1-120">Имя учетной записи для самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="f9bd1-120">Cognitive Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9bd1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9bd1-121">-ResourceGroupName</span></span>
<span data-ttu-id="f9bd1-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f9bd1-122">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9bd1-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9bd1-123">-ResourceId</span></span>
<span data-ttu-id="f9bd1-124">Идентификатор ресурса для учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="f9bd1-124">Cognitive Services Account Resource ID.</span></span>
```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9bd1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9bd1-125">CommonParameters</span></span>
<span data-ttu-id="f9bd1-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f9bd1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9bd1-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9bd1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9bd1-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f9bd1-128">INPUTS</span></span>

### <span data-ttu-id="f9bd1-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f9bd1-129">System.String</span></span>

## <span data-ttu-id="f9bd1-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9bd1-130">OUTPUTS</span></span>

### <span data-ttu-id="f9bd1-131">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesUsage</span><span class="sxs-lookup"><span data-stu-id="f9bd1-131">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span></span>

## <span data-ttu-id="f9bd1-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="f9bd1-132">NOTES</span></span>

## <span data-ttu-id="f9bd1-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f9bd1-133">RELATED LINKS</span></span>
