---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 56b1a9378914a7fa2220e948b64c357b06f6f4dc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073605"
---
# <span data-ttu-id="fe50e-101">Get-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="fe50e-101">Get-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="fe50e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fe50e-102">SYNOPSIS</span></span>
<span data-ttu-id="fe50e-103">Возвращает политику вычислений Data Lake Analytics или список политик вычислений.</span><span class="sxs-lookup"><span data-stu-id="fe50e-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

## <span data-ttu-id="fe50e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fe50e-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe50e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe50e-105">DESCRIPTION</span></span>
<span data-ttu-id="fe50e-106">Параметр **Get-AzDataLakeAnalyticsComputePolicy** получает указанную политику вычисления Azure Data Lake Analytics или список политик.</span><span class="sxs-lookup"><span data-stu-id="fe50e-106">The **Get-AzDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="fe50e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fe50e-107">EXAMPLES</span></span>

### <span data-ttu-id="fe50e-108">Пример 1: получение указанной политики вычислений</span><span class="sxs-lookup"><span data-stu-id="fe50e-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="fe50e-109">Эта команда получает указанную политику вычислений с именем "myPolicy" в учетной записи "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="fe50e-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="fe50e-110">Пример 2: получение списка всех политик вычислений в учетной записи</span><span class="sxs-lookup"><span data-stu-id="fe50e-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="fe50e-111">Эта команда получает список всех политик вычислений в учетной записи "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="fe50e-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="fe50e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fe50e-112">PARAMETERS</span></span>

### <span data-ttu-id="fe50e-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="fe50e-113">-Account</span></span>
<span data-ttu-id="fe50e-114">Имя учетной записи, для которой нужно получить политику расчета или политики.</span><span class="sxs-lookup"><span data-stu-id="fe50e-114">Name of the account to get the compute policy or policies from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe50e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe50e-115">-DefaultProfile</span></span>
<span data-ttu-id="fe50e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="fe50e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe50e-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fe50e-117">-Name</span></span>
<span data-ttu-id="fe50e-118">Имя получаемой политики вычисления.</span><span class="sxs-lookup"><span data-stu-id="fe50e-118">Name of the compute policy to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe50e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe50e-119">-ResourceGroupName</span></span>
<span data-ttu-id="fe50e-120">Имя группы ресурсов, в которой есть учетная запись.</span><span class="sxs-lookup"><span data-stu-id="fe50e-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="fe50e-121">Необязательный и пытается выяснить, не было ли оно указано.</span><span class="sxs-lookup"><span data-stu-id="fe50e-121">Optional and will attempt to discover if not provided.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe50e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe50e-122">CommonParameters</span></span>
<span data-ttu-id="fe50e-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fe50e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe50e-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe50e-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe50e-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fe50e-125">INPUTS</span></span>

### <span data-ttu-id="fe50e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="fe50e-126">System.String</span></span>

## <span data-ttu-id="fe50e-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe50e-127">OUTPUTS</span></span>

### <span data-ttu-id="fe50e-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="fe50e-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="fe50e-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="fe50e-129">NOTES</span></span>

## <span data-ttu-id="fe50e-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe50e-130">RELATED LINKS</span></span>
