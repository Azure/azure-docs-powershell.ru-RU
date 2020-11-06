---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/get-azurermdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: f19c4f9d39837534ea5ddd5b16daa055ee54aef6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563607"
---
# <span data-ttu-id="42452-101">Get-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="42452-101">Get-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="42452-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="42452-102">SYNOPSIS</span></span>
<span data-ttu-id="42452-103">Возвращает политику вычислений Data Lake Analytics или список политик вычислений.</span><span class="sxs-lookup"><span data-stu-id="42452-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42452-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="42452-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42452-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="42452-105">DESCRIPTION</span></span>
<span data-ttu-id="42452-106">Параметр **Get-AzureRmDataLakeAnalyticsComputePolicy** получает указанную политику вычисления Azure Data Lake Analytics или список политик.</span><span class="sxs-lookup"><span data-stu-id="42452-106">The **Get-AzureRmDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="42452-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="42452-107">EXAMPLES</span></span>

### <span data-ttu-id="42452-108">Пример 1: получение указанной политики вычислений</span><span class="sxs-lookup"><span data-stu-id="42452-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="42452-109">Эта команда получает указанную политику вычислений с именем "myPolicy" в учетной записи "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="42452-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="42452-110">Пример 2: получение списка всех политик вычислений в учетной записи</span><span class="sxs-lookup"><span data-stu-id="42452-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="42452-111">Эта команда получает список всех политик вычислений в учетной записи "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="42452-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="42452-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="42452-112">PARAMETERS</span></span>

### <span data-ttu-id="42452-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="42452-113">-Account</span></span>
<span data-ttu-id="42452-114">Имя учетной записи, для которой нужно получить политику расчета или политики.</span><span class="sxs-lookup"><span data-stu-id="42452-114">Name of the account to get the compute policy or policies from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42452-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42452-115">-DefaultProfile</span></span>
<span data-ttu-id="42452-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="42452-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42452-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="42452-117">-Name</span></span>
<span data-ttu-id="42452-118">Имя получаемой политики вычисления.</span><span class="sxs-lookup"><span data-stu-id="42452-118">Name of the compute policy to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42452-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42452-119">-ResourceGroupName</span></span>
<span data-ttu-id="42452-120">Имя группы ресурсов, в которой есть учетная запись.</span><span class="sxs-lookup"><span data-stu-id="42452-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="42452-121">Необязательный и пытается выяснить, не было ли оно указано.</span><span class="sxs-lookup"><span data-stu-id="42452-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="42452-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42452-122">CommonParameters</span></span>
<span data-ttu-id="42452-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="42452-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42452-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42452-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42452-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="42452-125">INPUTS</span></span>

### <span data-ttu-id="42452-126">System. String</span><span class="sxs-lookup"><span data-stu-id="42452-126">System.String</span></span>

## <span data-ttu-id="42452-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="42452-127">OUTPUTS</span></span>

### <span data-ttu-id="42452-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="42452-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>
<span data-ttu-id="42452-129">System. Collections. Generic. IEnumerable ' 1 [[Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy, Microsoft. Azure. Commands. DataLakeAnalytics, Version = 3.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="42452-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy, Microsoft.Azure.Commands.DataLakeAnalytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="42452-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="42452-130">NOTES</span></span>

## <span data-ttu-id="42452-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="42452-131">RELATED LINKS</span></span>

