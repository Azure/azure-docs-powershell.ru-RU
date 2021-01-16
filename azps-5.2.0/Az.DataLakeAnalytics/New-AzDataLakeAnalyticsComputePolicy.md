---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 76df1cb780220a09ccc0d571fd88223e746eefe6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397540"
---
# <span data-ttu-id="82f5b-101">New-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="82f5b-101">New-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="82f5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82f5b-102">SYNOPSIS</span></span>
<span data-ttu-id="82f5b-103">Создает правило политики AAD для определенной сущности.</span><span class="sxs-lookup"><span data-stu-id="82f5b-103">Creates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="82f5b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="82f5b-104">SYNTAX</span></span>

```
New-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-ObjectId] <Guid> [-ObjectType] <String> [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82f5b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82f5b-105">DESCRIPTION</span></span>
<span data-ttu-id="82f5b-106">**New-AzDataLakeAnalyticsComputePolicy** создает указанное правило политики вычисления для определенного объекта AAD в учетной записи Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="82f5b-106">The **New-AzDataLakeAnalyticsComputePolicy** creates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="82f5b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="82f5b-107">EXAMPLES</span></span>

### <span data-ttu-id="82f5b-108">Пример 1. Создание вычисляемой политики с одним правилом</span><span class="sxs-lookup"><span data-stu-id="82f5b-108">Example 1: Create a compute policy with only one rule</span></span>
```
PS C:\>New-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="82f5b-109">Эта команда создает политику myPolicy в учетной записи contosoadla для пользователя с ид "83cb7ad2-3523-4b82-b909-d478b0d8aea3", которая гарантирует, что пользователь не сможет отправить задание с более чем 5 аналитическими единицами.</span><span class="sxs-lookup"><span data-stu-id="82f5b-109">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="82f5b-110">Пример 2. Создание вычисляемой политики с установленными обоими правилами</span><span class="sxs-lookup"><span data-stu-id="82f5b-110">Example 2: Create a compute policy with both rules set</span></span>
```
PS C:\>New-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="82f5b-111">Эта команда создает политику "myPolicy" в учетной записи contosoadla для пользователя с ид "83cb7ad2-3523-4b82-b909-d478b0d8aea3", которая гарантирует, что пользователь не сможет отправить задание с более чем 5 аналитическими единицами или приоритетом менее 100.</span><span class="sxs-lookup"><span data-stu-id="82f5b-111">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="82f5b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82f5b-112">PARAMETERS</span></span>

### <span data-ttu-id="82f5b-113">-Account</span><span class="sxs-lookup"><span data-stu-id="82f5b-113">-Account</span></span>
<span data-ttu-id="82f5b-114">Имя учетной записи, для которого нужно добавить вычисляемую политику.</span><span class="sxs-lookup"><span data-stu-id="82f5b-114">Name of the account to add the compute policy to.</span></span>

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

### <span data-ttu-id="82f5b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82f5b-115">-DefaultProfile</span></span>
<span data-ttu-id="82f5b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="82f5b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82f5b-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="82f5b-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="82f5b-118">Максимальное количество аналитических единиц для каждого задания этой политики.</span><span class="sxs-lookup"><span data-stu-id="82f5b-118">The maximum supported analytics units per job for this policy.</span></span>
<span data-ttu-id="82f5b-119">Это, MinPriorityPerJob или оба параметра должны быть указаны.</span><span class="sxs-lookup"><span data-stu-id="82f5b-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="82f5b-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="82f5b-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="82f5b-121">Минимальный поддерживаемый приоритет для задания для этой политики.</span><span class="sxs-lookup"><span data-stu-id="82f5b-121">The minimum supported priority per job for this policy.</span></span>
<span data-ttu-id="82f5b-122">Это, MaxAnalyticsUnitsPerJob или оба параметра должны быть указаны.</span><span class="sxs-lookup"><span data-stu-id="82f5b-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="82f5b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="82f5b-123">-Name</span></span>
<span data-ttu-id="82f5b-124">Имя вычисляемой политики, которая будет создаваться.</span><span class="sxs-lookup"><span data-stu-id="82f5b-124">Name of the compute policy to create.</span></span>

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

### <span data-ttu-id="82f5b-125">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="82f5b-125">-ObjectId</span></span>
<span data-ttu-id="82f5b-126">ИД объекта Azure Active Directory для применения политики пользователем или группой.</span><span class="sxs-lookup"><span data-stu-id="82f5b-126">The Azure Active Directory object id for the user or group to apply the policy to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82f5b-127">-ObjectType</span><span class="sxs-lookup"><span data-stu-id="82f5b-127">-ObjectType</span></span>
<span data-ttu-id="82f5b-128">Тип объекта Azure Active Directory для переданного ИД объекта.</span><span class="sxs-lookup"><span data-stu-id="82f5b-128">The Azure Active Directory object type for the object ID passed in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: User, Group, ServicePrincipal

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82f5b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82f5b-129">-ResourceGroupName</span></span>
<span data-ttu-id="82f5b-130">Имя группы ресурсов, под которой вы и есть учетная запись.</span><span class="sxs-lookup"><span data-stu-id="82f5b-130">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="82f5b-131">Необязательный и попытается найти, если он не предоставлен.</span><span class="sxs-lookup"><span data-stu-id="82f5b-131">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="82f5b-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82f5b-132">-Confirm</span></span>
<span data-ttu-id="82f5b-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82f5b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82f5b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82f5b-134">-WhatIf</span></span>
<span data-ttu-id="82f5b-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82f5b-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="82f5b-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="82f5b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82f5b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82f5b-137">CommonParameters</span></span>
<span data-ttu-id="82f5b-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82f5b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82f5b-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82f5b-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82f5b-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82f5b-140">INPUTS</span></span>

### <span data-ttu-id="82f5b-141">System.String</span><span class="sxs-lookup"><span data-stu-id="82f5b-141">System.String</span></span>

### <span data-ttu-id="82f5b-142">System.Guid</span><span class="sxs-lookup"><span data-stu-id="82f5b-142">System.Guid</span></span>

### <span data-ttu-id="82f5b-143">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="82f5b-143">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="82f5b-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="82f5b-144">OUTPUTS</span></span>

### <span data-ttu-id="82f5b-145">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDAtaLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="82f5b-145">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="82f5b-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="82f5b-146">NOTES</span></span>

## <span data-ttu-id="82f5b-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82f5b-147">RELATED LINKS</span></span>