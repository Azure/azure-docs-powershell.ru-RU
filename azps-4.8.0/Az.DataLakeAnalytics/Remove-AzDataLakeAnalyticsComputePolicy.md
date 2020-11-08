---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 556cc10b415b2e37b832f144a01d307a2b69e52d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079697"
---
# <span data-ttu-id="86553-101">Remove-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="86553-101">Remove-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="86553-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="86553-102">SYNOPSIS</span></span>
<span data-ttu-id="86553-103">Удаляет указанную политику вычисления данных Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="86553-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

## <span data-ttu-id="86553-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="86553-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86553-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="86553-105">DESCRIPTION</span></span>
<span data-ttu-id="86553-106">Параметр **Remove-AzDataLakeAnalyticsComputePolicy** удаляет указанную политику вычисления Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="86553-106">The **Remove-AzDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="86553-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="86553-107">EXAMPLES</span></span>

### <span data-ttu-id="86553-108">Пример 1: Удаление политики вычислений</span><span class="sxs-lookup"><span data-stu-id="86553-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="86553-109">Эта команда удаляет указанную политику вычислений с именем "myPolicy" в учетной записи "contosoadla".</span><span class="sxs-lookup"><span data-stu-id="86553-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="86553-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="86553-110">PARAMETERS</span></span>

### <span data-ttu-id="86553-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="86553-111">-Account</span></span>
<span data-ttu-id="86553-112">Имя учетной записи, из которой нужно удалить политику вычислений.</span><span class="sxs-lookup"><span data-stu-id="86553-112">Name of the account to remove the compute policy from.</span></span>

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

### <span data-ttu-id="86553-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86553-113">-DefaultProfile</span></span>
<span data-ttu-id="86553-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="86553-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86553-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="86553-115">-Name</span></span>
<span data-ttu-id="86553-116">Имя удаляемой политики вычисления.</span><span class="sxs-lookup"><span data-stu-id="86553-116">Name of the compute policy to remove.</span></span>

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

### <span data-ttu-id="86553-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86553-117">-PassThru</span></span>
<span data-ttu-id="86553-118">При успешном удалении возвращает значение "истина".</span><span class="sxs-lookup"><span data-stu-id="86553-118">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="86553-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86553-119">-ResourceGroupName</span></span>
<span data-ttu-id="86553-120">Имя группы ресурсов, в которой есть учетная запись.</span><span class="sxs-lookup"><span data-stu-id="86553-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="86553-121">Необязательный и пытается выяснить, не было ли оно указано.</span><span class="sxs-lookup"><span data-stu-id="86553-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="86553-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86553-122">-Confirm</span></span>
<span data-ttu-id="86553-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="86553-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86553-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86553-124">-WhatIf</span></span>
<span data-ttu-id="86553-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="86553-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86553-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="86553-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86553-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86553-127">CommonParameters</span></span>
<span data-ttu-id="86553-128">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="86553-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86553-129">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86553-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86553-130">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="86553-130">INPUTS</span></span>

### <span data-ttu-id="86553-131">System. String</span><span class="sxs-lookup"><span data-stu-id="86553-131">System.String</span></span>

## <span data-ttu-id="86553-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="86553-132">OUTPUTS</span></span>

### <span data-ttu-id="86553-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="86553-133">System.Boolean</span></span>

## <span data-ttu-id="86553-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="86553-134">NOTES</span></span>

## <span data-ttu-id="86553-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="86553-135">RELATED LINKS</span></span>