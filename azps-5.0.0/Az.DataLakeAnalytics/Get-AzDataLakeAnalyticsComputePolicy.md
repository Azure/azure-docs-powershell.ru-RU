---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 56b1a9378914a7fa2220e948b64c357b06f6f4dc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313619"
---
# <span data-ttu-id="c368a-101">Get-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="c368a-101">Get-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="c368a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c368a-102">SYNOPSIS</span></span>
<span data-ttu-id="c368a-103">Возвращает политику вычислений Data Lake Analytics или список политик вычислений.</span><span class="sxs-lookup"><span data-stu-id="c368a-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

## <span data-ttu-id="c368a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c368a-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c368a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c368a-105">DESCRIPTION</span></span>
<span data-ttu-id="c368a-106">Параметр **Get-AzDataLakeAnalyticsComputePolicy** получает указанную политику вычисления Azure Data Lake Analytics или список политик.</span><span class="sxs-lookup"><span data-stu-id="c368a-106">The **Get-AzDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="c368a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c368a-107">EXAMPLES</span></span>

### <span data-ttu-id="c368a-108">Пример 1: получение указанной политики вычислений</span><span class="sxs-lookup"><span data-stu-id="c368a-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="c368a-109">Эта команда получает указанную политику вычислений с именем "myPolicy" в учетной записи "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="c368a-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="c368a-110">Пример 2: получение списка всех политик вычислений в учетной записи</span><span class="sxs-lookup"><span data-stu-id="c368a-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="c368a-111">Эта команда получает список всех политик вычислений в учетной записи "contosoadla"</span><span class="sxs-lookup"><span data-stu-id="c368a-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="c368a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c368a-112">PARAMETERS</span></span>

### <span data-ttu-id="c368a-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="c368a-113">-Account</span></span>
<span data-ttu-id="c368a-114">Имя учетной записи, для которой нужно получить политику расчета или политики.</span><span class="sxs-lookup"><span data-stu-id="c368a-114">Name of the account to get the compute policy or policies from.</span></span>

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

### <span data-ttu-id="c368a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c368a-115">-DefaultProfile</span></span>
<span data-ttu-id="c368a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c368a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c368a-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c368a-117">-Name</span></span>
<span data-ttu-id="c368a-118">Имя получаемой политики вычисления.</span><span class="sxs-lookup"><span data-stu-id="c368a-118">Name of the compute policy to get.</span></span>

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

### <span data-ttu-id="c368a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c368a-119">-ResourceGroupName</span></span>
<span data-ttu-id="c368a-120">Имя группы ресурсов, в которой есть учетная запись.</span><span class="sxs-lookup"><span data-stu-id="c368a-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="c368a-121">Необязательный и пытается выяснить, не было ли оно указано.</span><span class="sxs-lookup"><span data-stu-id="c368a-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="c368a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c368a-122">CommonParameters</span></span>
<span data-ttu-id="c368a-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c368a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c368a-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c368a-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c368a-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c368a-125">INPUTS</span></span>

### <span data-ttu-id="c368a-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c368a-126">System.String</span></span>

## <span data-ttu-id="c368a-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c368a-127">OUTPUTS</span></span>

### <span data-ttu-id="c368a-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="c368a-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="c368a-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="c368a-129">NOTES</span></span>

## <span data-ttu-id="c368a-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c368a-130">RELATED LINKS</span></span>
