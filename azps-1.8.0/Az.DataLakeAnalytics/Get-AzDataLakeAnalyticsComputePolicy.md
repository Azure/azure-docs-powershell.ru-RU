---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 776249a7a474e3918ed29003f631c984111ca25c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731101"
---
# <span data-ttu-id="8df96-101">Get-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="8df96-101">Get-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="8df96-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8df96-102">SYNOPSIS</span></span>
<span data-ttu-id="8df96-103">Возвращает политику вычислений Data Lake Analytics или список политик вычислений.</span><span class="sxs-lookup"><span data-stu-id="8df96-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

## <span data-ttu-id="8df96-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8df96-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8df96-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8df96-105">DESCRIPTION</span></span>
<span data-ttu-id="8df96-106">Параметр **Get-AzDataLakeAnalyticsComputePolicy** получает указанную политику вычисления Azure Data Lake Analytics или список политик.</span><span class="sxs-lookup"><span data-stu-id="8df96-106">The **Get-AzDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="8df96-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8df96-107">EXAMPLES</span></span>

### <span data-ttu-id="8df96-108">Пример 1: получение указанной политики вычислений</span><span class="sxs-lookup"><span data-stu-id="8df96-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="8df96-109">Эта команда получает указанную политику вычислений с именем "myPolicy" в учетной записи "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="8df96-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="8df96-110">Пример 2: получение списка всех политик вычислений в учетной записи</span><span class="sxs-lookup"><span data-stu-id="8df96-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="8df96-111">Эта команда получает список всех политик вычислений в учетной записи "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="8df96-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="8df96-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8df96-112">PARAMETERS</span></span>

### <span data-ttu-id="8df96-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="8df96-113">-Account</span></span>
<span data-ttu-id="8df96-114">Имя учетной записи, для которой нужно получить политику расчета или политики.</span><span class="sxs-lookup"><span data-stu-id="8df96-114">Name of the account to get the compute policy or policies from.</span></span>

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

### <span data-ttu-id="8df96-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8df96-115">-DefaultProfile</span></span>
<span data-ttu-id="8df96-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8df96-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8df96-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8df96-117">-Name</span></span>
<span data-ttu-id="8df96-118">Имя получаемой политики вычисления.</span><span class="sxs-lookup"><span data-stu-id="8df96-118">Name of the compute policy to get.</span></span>

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

### <span data-ttu-id="8df96-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8df96-119">-ResourceGroupName</span></span>
<span data-ttu-id="8df96-120">Имя группы ресурсов, в которой есть учетная запись.</span><span class="sxs-lookup"><span data-stu-id="8df96-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="8df96-121">Необязательный и пытается выяснить, не было ли оно указано.</span><span class="sxs-lookup"><span data-stu-id="8df96-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="8df96-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8df96-122">CommonParameters</span></span>
<span data-ttu-id="8df96-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8df96-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8df96-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8df96-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8df96-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8df96-125">INPUTS</span></span>

### <span data-ttu-id="8df96-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8df96-126">System.String</span></span>

## <span data-ttu-id="8df96-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8df96-127">OUTPUTS</span></span>

### <span data-ttu-id="8df96-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="8df96-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="8df96-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="8df96-129">NOTES</span></span>

## <span data-ttu-id="8df96-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8df96-130">RELATED LINKS</span></span>
