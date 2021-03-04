---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 31e4f1be594735d8ea7afbe9abc5f6ccb21ada1a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957363"
---
# <span data-ttu-id="6b14e-101">Remove-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="6b14e-101">Remove-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="6b14e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b14e-102">SYNOPSIS</span></span>
<span data-ttu-id="6b14e-103">Удаляет правило брандмауэра из учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6b14e-103">Removes a firewall rule from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="6b14e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6b14e-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6b14e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6b14e-105">DESCRIPTION</span></span>
<span data-ttu-id="6b14e-106">С **помощью cmdlet Remove-AzDataLakeAnalyticsFirewallRule** правило брандмауэра удаляется из учетной записи Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="6b14e-106">The **Remove-AzDataLakeAnalyticsFirewallRule** cmdlet removes a firewall rule from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="6b14e-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6b14e-107">EXAMPLES</span></span>

### <span data-ttu-id="6b14e-108">Пример 1. Удаление правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="6b14e-108">Example 1: Remove a firewall rule</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="6b14e-109">Эта команда удаляет правило брандмауэра с именем "Правило брандмауэра" из учетной записи ContosoAdlAcct.</span><span class="sxs-lookup"><span data-stu-id="6b14e-109">This command removes the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="6b14e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b14e-110">PARAMETERS</span></span>

### <span data-ttu-id="6b14e-111">-Account</span><span class="sxs-lookup"><span data-stu-id="6b14e-111">-Account</span></span>
<span data-ttu-id="6b14e-112">Учетная запись Data Lake Analytics для удаления правила брандмауэра из</span><span class="sxs-lookup"><span data-stu-id="6b14e-112">The Data Lake Analytics account to remove the firewall rule from</span></span>

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

### <span data-ttu-id="6b14e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b14e-113">-DefaultProfile</span></span>
<span data-ttu-id="6b14e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6b14e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b14e-115">-Name</span><span class="sxs-lookup"><span data-stu-id="6b14e-115">-Name</span></span>
<span data-ttu-id="6b14e-116">Имя правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="6b14e-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="6b14e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b14e-117">-PassThru</span></span>
<span data-ttu-id="6b14e-118">Указывает на то, что должен быть возвращен boolean response, указывающий на результат операции удаления.</span><span class="sxs-lookup"><span data-stu-id="6b14e-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="6b14e-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b14e-119">-ResourceGroupName</span></span>
<span data-ttu-id="6b14e-120">Имя группы ресурсов, под которой нужно получить учетную запись.</span><span class="sxs-lookup"><span data-stu-id="6b14e-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="6b14e-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6b14e-121">-Confirm</span></span>
<span data-ttu-id="6b14e-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b14e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b14e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b14e-123">-WhatIf</span></span>
<span data-ttu-id="6b14e-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b14e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b14e-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6b14e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b14e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b14e-126">CommonParameters</span></span>
<span data-ttu-id="6b14e-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b14e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b14e-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b14e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b14e-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6b14e-129">INPUTS</span></span>

### <span data-ttu-id="6b14e-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6b14e-130">System.String</span></span>

### <span data-ttu-id="6b14e-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6b14e-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6b14e-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6b14e-132">OUTPUTS</span></span>

### <span data-ttu-id="6b14e-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6b14e-133">System.Boolean</span></span>

## <span data-ttu-id="6b14e-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6b14e-134">NOTES</span></span>

## <span data-ttu-id="6b14e-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6b14e-135">RELATED LINKS</span></span>
