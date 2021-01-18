---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 879897b6d89e5a1e34ee9f61714628aa741a670f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504620"
---
# <span data-ttu-id="82416-101">Remove-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="82416-101">Remove-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="82416-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82416-102">SYNOPSIS</span></span>
<span data-ttu-id="82416-103">Удаляет правило брандмауэра из учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="82416-103">Removes a firewall rule from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="82416-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="82416-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="82416-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="82416-105">DESCRIPTION</span></span>
<span data-ttu-id="82416-106">С **помощью cmdlet Remove-AzDataLakeAnalyticsFirewallRule** правило брандмауэра удаляется из учетной записи Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="82416-106">The **Remove-AzDataLakeAnalyticsFirewallRule** cmdlet removes a firewall rule from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="82416-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="82416-107">EXAMPLES</span></span>

### <span data-ttu-id="82416-108">Пример 1. Удаление правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="82416-108">Example 1: Remove a firewall rule</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="82416-109">Эта команда удаляет правило брандмауэра под названием "Правило брандмауэра" из учетной записи ContosoAdlAcct.</span><span class="sxs-lookup"><span data-stu-id="82416-109">This command removes the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="82416-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82416-110">PARAMETERS</span></span>

### <span data-ttu-id="82416-111">-Account</span><span class="sxs-lookup"><span data-stu-id="82416-111">-Account</span></span>
<span data-ttu-id="82416-112">Учетная запись Data Lake Analytics для удаления правила брандмауэра из</span><span class="sxs-lookup"><span data-stu-id="82416-112">The Data Lake Analytics account to remove the firewall rule from</span></span>

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

### <span data-ttu-id="82416-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82416-113">-DefaultProfile</span></span>
<span data-ttu-id="82416-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="82416-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82416-115">-Name</span><span class="sxs-lookup"><span data-stu-id="82416-115">-Name</span></span>
<span data-ttu-id="82416-116">Имя правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="82416-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="82416-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82416-117">-PassThru</span></span>
<span data-ttu-id="82416-118">Указывает на то, что должен быть возвращен boolean response, указывающий на результат операции удаления.</span><span class="sxs-lookup"><span data-stu-id="82416-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="82416-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82416-119">-ResourceGroupName</span></span>
<span data-ttu-id="82416-120">Имя группы ресурсов, под которой вы хотите получить учетную запись.</span><span class="sxs-lookup"><span data-stu-id="82416-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="82416-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82416-121">-Confirm</span></span>
<span data-ttu-id="82416-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82416-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82416-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82416-123">-WhatIf</span></span>
<span data-ttu-id="82416-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="82416-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82416-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="82416-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82416-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82416-126">CommonParameters</span></span>
<span data-ttu-id="82416-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82416-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82416-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82416-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82416-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="82416-129">INPUTS</span></span>

### <span data-ttu-id="82416-130">System.String</span><span class="sxs-lookup"><span data-stu-id="82416-130">System.String</span></span>

### <span data-ttu-id="82416-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="82416-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="82416-132">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="82416-132">OUTPUTS</span></span>

### <span data-ttu-id="82416-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="82416-133">System.Boolean</span></span>

## <span data-ttu-id="82416-134">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="82416-134">NOTES</span></span>

## <span data-ttu-id="82416-135">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="82416-135">RELATED LINKS</span></span>
