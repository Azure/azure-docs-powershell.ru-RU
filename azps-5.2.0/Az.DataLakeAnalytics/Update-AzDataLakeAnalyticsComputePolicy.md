---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/update-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 5dd36c9dbd263dc2e5c72cc6d57f95e29c456c41
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418111"
---
# <span data-ttu-id="3ee14-101">Update-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="3ee14-101">Update-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="3ee14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ee14-102">SYNOPSIS</span></span>
<span data-ttu-id="3ee14-103">Обновляет правило политики AAD для определенной сущности.</span><span class="sxs-lookup"><span data-stu-id="3ee14-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="3ee14-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3ee14-104">SYNTAX</span></span>

```
Update-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ee14-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ee14-105">DESCRIPTION</span></span>
<span data-ttu-id="3ee14-106">**Update-AzDataLakeAnalyticsComputePolicy** обновляет указанное правило политики вычисления для определенной сущности AAD в учетной записи Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="3ee14-106">The **Update-AzDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="3ee14-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3ee14-107">EXAMPLES</span></span>

### <span data-ttu-id="3ee14-108">Пример 1. Обновление одного правила в политике расчета</span><span class="sxs-lookup"><span data-stu-id="3ee14-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="3ee14-109">Эта команда обновляет политику myPolicy в учетной записи contosoadla, чтобы гарантировать, что пользователь не может отправить задание с более чем 5 аналитическими единицами.</span><span class="sxs-lookup"><span data-stu-id="3ee14-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="3ee14-110">Пример 2. Создание вычисляемой политики с обновлением обоих правил</span><span class="sxs-lookup"><span data-stu-id="3ee14-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="3ee14-111">Эта команда создает политику myPolicy в учетной записи contosoadla, чтобы гарантировать, что пользователь не может отправить задание с более чем 5 аналитическими блоками или более 100 единицами приоритета.</span><span class="sxs-lookup"><span data-stu-id="3ee14-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="3ee14-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ee14-112">PARAMETERS</span></span>

### <span data-ttu-id="3ee14-113">-Account</span><span class="sxs-lookup"><span data-stu-id="3ee14-113">-Account</span></span>
<span data-ttu-id="3ee14-114">Имя учетной записи для обновления политики вычислений.</span><span class="sxs-lookup"><span data-stu-id="3ee14-114">Name of the account to update the compute policy in.</span></span>

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

### <span data-ttu-id="3ee14-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ee14-115">-DefaultProfile</span></span>
<span data-ttu-id="3ee14-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3ee14-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ee14-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="3ee14-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="3ee14-118">Максимальное количество аналитических единиц для каждого задания этой политики.</span><span class="sxs-lookup"><span data-stu-id="3ee14-118">The maximum supported analytics units per job for this policy.</span></span> <span data-ttu-id="3ee14-119">Это, MinPriorityPerJob или оба параметра должны быть указаны.</span><span class="sxs-lookup"><span data-stu-id="3ee14-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelismPerJob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ee14-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="3ee14-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="3ee14-121">Минимальный поддерживаемый приоритет для задания для этой политики.</span><span class="sxs-lookup"><span data-stu-id="3ee14-121">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="3ee14-122">Это, MaxAnalyticsUnitsPerJob или оба параметра должны быть указаны.</span><span class="sxs-lookup"><span data-stu-id="3ee14-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ee14-123">-Name</span><span class="sxs-lookup"><span data-stu-id="3ee14-123">-Name</span></span>
<span data-ttu-id="3ee14-124">Имя обновляемой политики.</span><span class="sxs-lookup"><span data-stu-id="3ee14-124">Name of the compute policy to update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ee14-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ee14-125">-ResourceGroupName</span></span>
<span data-ttu-id="3ee14-126">Имя группы ресурсов, под которой вы и есть учетная запись.</span><span class="sxs-lookup"><span data-stu-id="3ee14-126">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="3ee14-127">Необязательный и попытается найти, если он не предоставлен.</span><span class="sxs-lookup"><span data-stu-id="3ee14-127">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="3ee14-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ee14-128">-Confirm</span></span>
<span data-ttu-id="3ee14-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ee14-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee14-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ee14-130">-WhatIf</span></span>
<span data-ttu-id="3ee14-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ee14-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3ee14-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3ee14-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ee14-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ee14-133">CommonParameters</span></span>
<span data-ttu-id="3ee14-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ee14-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ee14-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ee14-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ee14-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3ee14-136">INPUTS</span></span>

### <span data-ttu-id="3ee14-137">System.String</span><span class="sxs-lookup"><span data-stu-id="3ee14-137">System.String</span></span>

### <span data-ttu-id="3ee14-138">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3ee14-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="3ee14-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3ee14-139">OUTPUTS</span></span>

### <span data-ttu-id="3ee14-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDAtaLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="3ee14-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="3ee14-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3ee14-141">NOTES</span></span>

## <span data-ttu-id="3ee14-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ee14-142">RELATED LINKS</span></span>
