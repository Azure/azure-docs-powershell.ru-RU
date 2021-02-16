---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 556cc10b415b2e37b832f144a01d307a2b69e52d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100228860"
---
# <span data-ttu-id="d4674-101">Remove-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="d4674-101">Remove-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="d4674-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4674-102">SYNOPSIS</span></span>
<span data-ttu-id="d4674-103">Удаление указанной политики вычисления Azure Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="d4674-103">Removes a specified Azure Data Lake Analytics compute policy</span></span>

## <span data-ttu-id="d4674-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d4674-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4674-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4674-105">DESCRIPTION</span></span>
<span data-ttu-id="d4674-106">Политика **Remove-AzDataLakeAnalyticsComputePolicy** удаляет указанную политику azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="d4674-106">The **Remove-AzDataLakeAnalyticsComputePolicy** removes a specified Azure Data Lake Analytics compute policy.</span></span>

## <span data-ttu-id="d4674-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d4674-107">EXAMPLES</span></span>

### <span data-ttu-id="d4674-108">Пример 1. Удаление политики расчета</span><span class="sxs-lookup"><span data-stu-id="d4674-108">Example 1: Remove a compute policy</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="d4674-109">Эта команда удаляет указанную вычисляемую политику с именем myPolicy в учетной записи contosoadla.</span><span class="sxs-lookup"><span data-stu-id="d4674-109">This command removes the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

## <span data-ttu-id="d4674-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4674-110">PARAMETERS</span></span>

### <span data-ttu-id="d4674-111">-Account</span><span class="sxs-lookup"><span data-stu-id="d4674-111">-Account</span></span>
<span data-ttu-id="d4674-112">Имя учетной записи, из которого нужно удалить вычисляемую политику.</span><span class="sxs-lookup"><span data-stu-id="d4674-112">Name of the account to remove the compute policy from.</span></span>

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

### <span data-ttu-id="d4674-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4674-113">-DefaultProfile</span></span>
<span data-ttu-id="d4674-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d4674-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4674-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d4674-115">-Name</span></span>
<span data-ttu-id="d4674-116">Имя удаляемой политики.</span><span class="sxs-lookup"><span data-stu-id="d4674-116">Name of the compute policy to remove.</span></span>

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

### <span data-ttu-id="d4674-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4674-117">-PassThru</span></span>
<span data-ttu-id="d4674-118">Возвращается истина после успешного удаления.</span><span class="sxs-lookup"><span data-stu-id="d4674-118">Return true upon successful deletion.</span></span>

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

### <span data-ttu-id="d4674-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4674-119">-ResourceGroupName</span></span>
<span data-ttu-id="d4674-120">Имя группы ресурсов, под которой вы и есть учетная запись.</span><span class="sxs-lookup"><span data-stu-id="d4674-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="d4674-121">Необязательный и попытается найти, если он не предоставлен.</span><span class="sxs-lookup"><span data-stu-id="d4674-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="d4674-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4674-122">-Confirm</span></span>
<span data-ttu-id="d4674-123">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4674-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4674-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4674-124">-WhatIf</span></span>
<span data-ttu-id="d4674-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4674-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4674-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d4674-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4674-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4674-127">CommonParameters</span></span>
<span data-ttu-id="d4674-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4674-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4674-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4674-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4674-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4674-130">INPUTS</span></span>

### <span data-ttu-id="d4674-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d4674-131">System.String</span></span>

## <span data-ttu-id="d4674-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d4674-132">OUTPUTS</span></span>

### <span data-ttu-id="d4674-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d4674-133">System.Boolean</span></span>

## <span data-ttu-id="d4674-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d4674-134">NOTES</span></span>

## <span data-ttu-id="d4674-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4674-135">RELATED LINKS</span></span>
