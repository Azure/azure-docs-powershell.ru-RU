---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 1dfd9c4d55c9898ce9f4b656f53d7606ced11359
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559864"
---
# <span data-ttu-id="f3436-101">New-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="f3436-101">New-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="f3436-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f3436-102">SYNOPSIS</span></span>
<span data-ttu-id="f3436-103">Создает правило политики COMPUTE Data Lake Analytics для определенной сущности AAD.</span><span class="sxs-lookup"><span data-stu-id="f3436-103">Creates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3436-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f3436-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-ObjectId] <Guid> [-ObjectType] <String> [-MaxDegreeOfParallelismPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3436-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3436-105">DESCRIPTION</span></span>
<span data-ttu-id="f3436-106">**Новый параметр-AzureRmDataLakeAnalyticsComputePolicy** создает указанное правило политики вычислений для определенной сущности AAD в учетной записи Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="f3436-106">The **New-AzureRmDataLakeAnalyticsComputePolicy** creates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="f3436-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f3436-107">EXAMPLES</span></span>

### <span data-ttu-id="f3436-108">Пример 1: Создание политики вычислений с одним правилом</span><span class="sxs-lookup"><span data-stu-id="f3436-108">Example 1: Create a compute policy with only one rule</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxDegreeOfParallelismPerJob 5
```

<span data-ttu-id="f3436-109">Эта команда создает политику с именем "myPolicy" в учетной записи "contosoadla" для пользователя с идентификатором "83cb7ad2-3523-4b82-b909-d478b0d8aea3", гарантирующий, что он не сможет отправлять задания с более чем 5 параллелизмом.</span><span class="sxs-lookup"><span data-stu-id="f3436-109">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 parallelism.</span></span>

### <span data-ttu-id="f3436-110">Пример 2: Создание политики вычислений с обоими наборами правил</span><span class="sxs-lookup"><span data-stu-id="f3436-110">Example 2: Create a compute policy with both rules set</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxDegreeOfParallelismPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="f3436-111">Эта команда создает политику с именем "myPolicy" в учетной записи "contosoadla" для пользователя с идентификатором "83cb7ad2-3523-4b82-b909-d478b0d8aea3", гарантирующий, что он не сможет отправлять задания с более чем 5 параллелизмом или с более низким приоритетом, чем 100</span><span class="sxs-lookup"><span data-stu-id="f3436-111">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 parallelism or with a priority lower than 100</span></span>

## <span data-ttu-id="f3436-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f3436-112">PARAMETERS</span></span>

### <span data-ttu-id="f3436-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="f3436-113">-Account</span></span>
<span data-ttu-id="f3436-114">Имя учетной записи, в которую нужно добавить политику вычисления.</span><span class="sxs-lookup"><span data-stu-id="f3436-114">Name of the account to add the compute policy to.</span></span>

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

### <span data-ttu-id="f3436-115">-MaxDegreeOfParallelismPerJob</span><span class="sxs-lookup"><span data-stu-id="f3436-115">-MaxDegreeOfParallelismPerJob</span></span>
<span data-ttu-id="f3436-116">Максимальная поддерживаемая степень параллелизма для задания в этой политике.</span><span class="sxs-lookup"><span data-stu-id="f3436-116">The maximum supported degree of parallelism per job for this policy.</span></span>
<span data-ttu-id="f3436-117">Необходимо указать значение, MinPriorityPerJob или оба параметра.</span><span class="sxs-lookup"><span data-stu-id="f3436-117">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="f3436-118">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="f3436-118">-MinPriorityPerJob</span></span>
<span data-ttu-id="f3436-119">Минимальный поддерживаемый приоритет для задания в этой политике.</span><span class="sxs-lookup"><span data-stu-id="f3436-119">The minimum supported priority per job for this policy.</span></span>
<span data-ttu-id="f3436-120">Необходимо указать значение, MaxDegreeOfParallelismPerJob или оба параметра.</span><span class="sxs-lookup"><span data-stu-id="f3436-120">Either this, MaxDegreeOfParallelismPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="f3436-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f3436-121">-Name</span></span>
<span data-ttu-id="f3436-122">Имя создаваемой политики вычислений.</span><span class="sxs-lookup"><span data-stu-id="f3436-122">Name of the compute policy to create.</span></span>

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

### <span data-ttu-id="f3436-123">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f3436-123">-ObjectId</span></span>
<span data-ttu-id="f3436-124">Идентификатор объекта Azure Active Directory для пользователя или группы, к которой применяется политика.</span><span class="sxs-lookup"><span data-stu-id="f3436-124">The Azure Active Directory object id for the user or group to apply the policy to.</span></span>

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

### <span data-ttu-id="f3436-125">-ObjectType</span><span class="sxs-lookup"><span data-stu-id="f3436-125">-ObjectType</span></span>
<span data-ttu-id="f3436-126">Тип объекта Azure Active Directory для переданного идентификатора объекта.</span><span class="sxs-lookup"><span data-stu-id="f3436-126">The Azure Active Directory object type for the object ID passed in.</span></span>

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

### <span data-ttu-id="f3436-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3436-127">-ResourceGroupName</span></span>
<span data-ttu-id="f3436-128">Имя группы ресурсов, в которой есть учетная запись.</span><span class="sxs-lookup"><span data-stu-id="f3436-128">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="f3436-129">Необязательный и пытается выяснить, не было ли оно указано.</span><span class="sxs-lookup"><span data-stu-id="f3436-129">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="f3436-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3436-130">-Confirm</span></span>
<span data-ttu-id="f3436-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f3436-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3436-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3436-132">-WhatIf</span></span>
<span data-ttu-id="f3436-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f3436-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3436-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f3436-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3436-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3436-135">-DefaultProfile</span></span>
<span data-ttu-id="f3436-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f3436-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3436-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3436-137">CommonParameters</span></span>
<span data-ttu-id="f3436-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f3436-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3436-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3436-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3436-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f3436-140">INPUTS</span></span>

### <span data-ttu-id="f3436-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f3436-141">System.String</span></span>
<span data-ttu-id="f3436-142">System. GUID System. Int32</span><span class="sxs-lookup"><span data-stu-id="f3436-142">System.Guid System.Int32</span></span>

## <span data-ttu-id="f3436-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3436-143">OUTPUTS</span></span>

### <span data-ttu-id="f3436-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="f3436-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="f3436-145">Пуск</span><span class="sxs-lookup"><span data-stu-id="f3436-145">NOTES</span></span>

## <span data-ttu-id="f3436-146">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3436-146">RELATED LINKS</span></span>

