---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: deafb0cb68ab58997df83bc0280b50a4cc4a0de0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721373"
---
# <span data-ttu-id="11366-101">Remove-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="11366-101">Remove-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="11366-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="11366-102">SYNOPSIS</span></span>
<span data-ttu-id="11366-103">Удаляет указанную политику вычисления данных Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="11366-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

## <span data-ttu-id="11366-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="11366-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11366-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11366-105">DESCRIPTION</span></span>
<span data-ttu-id="11366-106">Параметр **Remove-AzDataLakeAnalyticsComputePolicy** удаляет указанную политику вычисления Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="11366-106">The **Remove-AzDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="11366-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="11366-107">EXAMPLES</span></span>

### <span data-ttu-id="11366-108">Пример 1: Удаление политики вычислений</span><span class="sxs-lookup"><span data-stu-id="11366-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="11366-109">Эта команда удаляет указанную политику вычислений с именем "myPolicy" в учетной записи "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="11366-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="11366-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="11366-110">PARAMETERS</span></span>

### <span data-ttu-id="11366-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="11366-111">-Account</span></span>
<span data-ttu-id="11366-112">Имя учетной записи, из которой нужно удалить политику вычислений.</span><span class="sxs-lookup"><span data-stu-id="11366-112">Name of the account to remove the compute policy from.</span></span>

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

### <span data-ttu-id="11366-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11366-113">-DefaultProfile</span></span>
<span data-ttu-id="11366-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="11366-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="11366-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="11366-115">-Name</span></span>
<span data-ttu-id="11366-116">Имя удаляемой политики вычисления.</span><span class="sxs-lookup"><span data-stu-id="11366-116">Name of the compute policy to remove.</span></span>

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

### <span data-ttu-id="11366-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11366-117">-PassThru</span></span>
<span data-ttu-id="11366-118">При успешном удалении возвращает значение "истина".</span><span class="sxs-lookup"><span data-stu-id="11366-118">Return true upon successful deletion.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11366-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11366-119">-ResourceGroupName</span></span>
<span data-ttu-id="11366-120">Имя группы ресурсов, в которой есть учетная запись.</span><span class="sxs-lookup"><span data-stu-id="11366-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="11366-121">Необязательный и пытается выяснить, не было ли оно указано.</span><span class="sxs-lookup"><span data-stu-id="11366-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="11366-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11366-122">-Confirm</span></span>
<span data-ttu-id="11366-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="11366-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11366-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11366-124">-WhatIf</span></span>
<span data-ttu-id="11366-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="11366-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11366-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="11366-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11366-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11366-127">CommonParameters</span></span>
<span data-ttu-id="11366-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="11366-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11366-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11366-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11366-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="11366-130">INPUTS</span></span>

### <span data-ttu-id="11366-131">System. String</span><span class="sxs-lookup"><span data-stu-id="11366-131">System.String</span></span>

## <span data-ttu-id="11366-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="11366-132">OUTPUTS</span></span>

### <span data-ttu-id="11366-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="11366-133">System.Boolean</span></span>

## <span data-ttu-id="11366-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="11366-134">NOTES</span></span>

## <span data-ttu-id="11366-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11366-135">RELATED LINKS</span></span>
