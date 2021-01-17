---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 879897b6d89e5a1e34ee9f61714628aa741a670f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400391"
---
# <span data-ttu-id="06e7a-101">Remove-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="06e7a-101">Remove-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="06e7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06e7a-102">SYNOPSIS</span></span>
<span data-ttu-id="06e7a-103">Удаляет правило брандмауэра из учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="06e7a-103">Removes a firewall rule from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="06e7a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="06e7a-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06e7a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="06e7a-105">DESCRIPTION</span></span>
<span data-ttu-id="06e7a-106">С **помощью cmdlet Remove-AzDataLakeAnalyticsFirewallRule** правило брандмауэра удаляется из учетной записи Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="06e7a-106">The **Remove-AzDataLakeAnalyticsFirewallRule** cmdlet removes a firewall rule from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="06e7a-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="06e7a-107">EXAMPLES</span></span>

### <span data-ttu-id="06e7a-108">Пример 1. Удаление правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="06e7a-108">Example 1: Remove a firewall rule</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="06e7a-109">Эта команда удаляет правило брандмауэра под названием "Правило брандмауэра" из учетной записи ContosoAdlAcct.</span><span class="sxs-lookup"><span data-stu-id="06e7a-109">This command removes the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="06e7a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06e7a-110">PARAMETERS</span></span>

### <span data-ttu-id="06e7a-111">-Account</span><span class="sxs-lookup"><span data-stu-id="06e7a-111">-Account</span></span>
<span data-ttu-id="06e7a-112">Учетная запись Data Lake Analytics для удаления правила брандмауэра из</span><span class="sxs-lookup"><span data-stu-id="06e7a-112">The Data Lake Analytics account to remove the firewall rule from</span></span>

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

### <span data-ttu-id="06e7a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06e7a-113">-DefaultProfile</span></span>
<span data-ttu-id="06e7a-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="06e7a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06e7a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="06e7a-115">-Name</span></span>
<span data-ttu-id="06e7a-116">Имя правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="06e7a-116">The name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06e7a-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06e7a-117">-PassThru</span></span>
<span data-ttu-id="06e7a-118">Указывает на то, что должен быть возвращен boolean response, указывающий на результат операции удаления.</span><span class="sxs-lookup"><span data-stu-id="06e7a-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06e7a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06e7a-119">-ResourceGroupName</span></span>
<span data-ttu-id="06e7a-120">Имя группы ресурсов, под которой нужно получить учетную запись.</span><span class="sxs-lookup"><span data-stu-id="06e7a-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="06e7a-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="06e7a-121">-Confirm</span></span>
<span data-ttu-id="06e7a-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="06e7a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06e7a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06e7a-123">-WhatIf</span></span>
<span data-ttu-id="06e7a-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06e7a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06e7a-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="06e7a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06e7a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06e7a-126">CommonParameters</span></span>
<span data-ttu-id="06e7a-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06e7a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06e7a-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06e7a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06e7a-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="06e7a-129">INPUTS</span></span>

### <span data-ttu-id="06e7a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="06e7a-130">System.String</span></span>

### <span data-ttu-id="06e7a-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="06e7a-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="06e7a-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="06e7a-132">OUTPUTS</span></span>

### <span data-ttu-id="06e7a-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="06e7a-133">System.Boolean</span></span>

## <span data-ttu-id="06e7a-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="06e7a-134">NOTES</span></span>

## <span data-ttu-id="06e7a-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="06e7a-135">RELATED LINKS</span></span>
