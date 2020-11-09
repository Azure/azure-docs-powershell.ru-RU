---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountUsage.md
ms.openlocfilehash: c287fd6aafcfe63a26c5f1dfd01503adb741428d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315869"
---
# <span data-ttu-id="d346b-101">Get-AzCognitiveServicesAccountUsage</span><span class="sxs-lookup"><span data-stu-id="d346b-101">Get-AzCognitiveServicesAccountUsage</span></span>

## <span data-ttu-id="d346b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d346b-102">SYNOPSIS</span></span>
<span data-ttu-id="d346b-103">Получение текущих использований для учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="d346b-103">Get current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="d346b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d346b-104">SYNTAX</span></span>

### <span data-ttu-id="d346b-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d346b-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d346b-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d346b-106">InputObjectParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-InputObject] <PSCognitiveServicesAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d346b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d346b-107">ResourceIdParameterSet</span></span>
```
Get-AzCognitiveServicesAccountUsage [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d346b-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d346b-108">DESCRIPTION</span></span>
<span data-ttu-id="d346b-109">Командлет **Get-AzCognitiveServicesAccountUsage** получает текущее использование для учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="d346b-109">The **Get-AzCognitiveServicesAccountUsage** cmdlet gets current usages for a Cognitive Services account.</span></span>

## <span data-ttu-id="d346b-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d346b-110">EXAMPLES</span></span>

### <span data-ttu-id="d346b-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d346b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountUsage -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="d346b-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d346b-112">Example 2</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzCognitiveServicesAccountUsage -InputObject $acc


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

### <span data-ttu-id="d346b-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d346b-113">Example 3</span></span>
```powershell
PS C:\GitHub> $acc = Get-AzCognitiveServicesAccount -ResourceGroupName TestUsages -Name TestCVUsages_Prediction

PS C:\GitHub> Get-AzCognitiveServicesAccountUsage -ResourceId $acc.Id


CurrentValue  : 0
Name          : CustomVision.Prediction.Transactions
Limit         : 10000
Status        : Included
Unit          : Count
QuotaPeriod   : 30.00:00:00
NextResetTime : 0001-01-01T00:00:00Z
```

## <span data-ttu-id="d346b-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d346b-114">PARAMETERS</span></span>

### <span data-ttu-id="d346b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d346b-115">-DefaultProfile</span></span>
<span data-ttu-id="d346b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d346b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d346b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d346b-117">-InputObject</span></span>
<span data-ttu-id="d346b-118">Объект учетной записи самообслуживания служб.</span><span class="sxs-lookup"><span data-stu-id="d346b-118">Cognitive Services Account Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d346b-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d346b-119">-Name</span></span>
<span data-ttu-id="d346b-120">Имя учетной записи для самообслуживания.</span><span class="sxs-lookup"><span data-stu-id="d346b-120">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d346b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d346b-121">-ResourceGroupName</span></span>
<span data-ttu-id="d346b-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d346b-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d346b-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d346b-123">-ResourceId</span></span>
<span data-ttu-id="d346b-124">Идентификатор ресурса для учетной записи службы.</span><span class="sxs-lookup"><span data-stu-id="d346b-124">Cognitive Services Account Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d346b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d346b-125">CommonParameters</span></span>
<span data-ttu-id="d346b-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d346b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d346b-127">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d346b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d346b-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d346b-128">INPUTS</span></span>

### <span data-ttu-id="d346b-129">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d346b-129">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

### <span data-ttu-id="d346b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d346b-130">System.String</span></span>

## <span data-ttu-id="d346b-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d346b-131">OUTPUTS</span></span>

### <span data-ttu-id="d346b-132">Microsoft. Azure. Commands. Management. CognitiveServices. Models. PSCognitiveServicesUsage</span><span class="sxs-lookup"><span data-stu-id="d346b-132">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesUsage</span></span>

## <span data-ttu-id="d346b-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="d346b-133">NOTES</span></span>

## <span data-ttu-id="d346b-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d346b-134">RELATED LINKS</span></span>
