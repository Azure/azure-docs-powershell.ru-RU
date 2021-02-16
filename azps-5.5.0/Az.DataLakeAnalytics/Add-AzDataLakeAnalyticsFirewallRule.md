---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/add-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Add-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: d9e6dd2e3fedff0d97919e04ca4f8b61536e2075
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242744"
---
# <span data-ttu-id="5758d-101">Add-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5758d-101">Add-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="5758d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5758d-102">SYNOPSIS</span></span>
<span data-ttu-id="5758d-103">Добавляет правило брандмауэра в учетную запись Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="5758d-103">Adds a firewall rule to a Data Lake Analytics account.</span></span>

## <span data-ttu-id="5758d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5758d-104">SYNTAX</span></span>

```
Add-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5758d-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5758d-105">DESCRIPTION</span></span>
<span data-ttu-id="5758d-106">Для учетной записи Azure Data Lake Analytics добавляется правило брандмауэра **Add-AzDataLakeAnalyticsFirewallRule.**</span><span class="sxs-lookup"><span data-stu-id="5758d-106">The **Add-AzDataLakeAnalyticsFirewallRule** cmdlet adds a firewall rule to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="5758d-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5758d-107">EXAMPLES</span></span>

### <span data-ttu-id="5758d-108">Пример 1. Добавление правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="5758d-108">Example 1: Add a firewall rule</span></span>
```
PS C:\>Add-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="5758d-109">Эта команда добавляет правило брандмауэра под названием "My firewall rule" из учетной записи ContosoAdlAcct с диапазоном IP-адресов: 127.0.0.1 –127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="5758d-109">This command adds the firewall rule named "my firewall rule" from account "ContosoAdlAcct" with the IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="5758d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5758d-110">PARAMETERS</span></span>

### <span data-ttu-id="5758d-111">-Account</span><span class="sxs-lookup"><span data-stu-id="5758d-111">-Account</span></span>
<span data-ttu-id="5758d-112">Учетная запись Data Lake Analytics для добавления правила брандмауэра в</span><span class="sxs-lookup"><span data-stu-id="5758d-112">The Data Lake Analytics account to add the firewall rule to</span></span>

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

### <span data-ttu-id="5758d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5758d-113">-DefaultProfile</span></span>
<span data-ttu-id="5758d-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5758d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5758d-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="5758d-115">-EndIpAddress</span></span>
<span data-ttu-id="5758d-116">Конец допустимого диапазона IP-адресов для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="5758d-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5758d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5758d-117">-Name</span></span>
<span data-ttu-id="5758d-118">Имя правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="5758d-118">The name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5758d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5758d-119">-ResourceGroupName</span></span>
<span data-ttu-id="5758d-120">Имя группы ресурсов, под которой вы хотите получить учетную запись.</span><span class="sxs-lookup"><span data-stu-id="5758d-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="5758d-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="5758d-121">-StartIpAddress</span></span>
<span data-ttu-id="5758d-122">Начало допустимого диапазона IP-адресов для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="5758d-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5758d-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5758d-123">-Confirm</span></span>
<span data-ttu-id="5758d-124">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5758d-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5758d-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5758d-125">-WhatIf</span></span>
<span data-ttu-id="5758d-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5758d-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5758d-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5758d-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5758d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5758d-128">CommonParameters</span></span>
<span data-ttu-id="5758d-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5758d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5758d-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5758d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5758d-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5758d-131">INPUTS</span></span>

### <span data-ttu-id="5758d-132">System.String</span><span class="sxs-lookup"><span data-stu-id="5758d-132">System.String</span></span>

## <span data-ttu-id="5758d-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5758d-133">OUTPUTS</span></span>

### <span data-ttu-id="5758d-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5758d-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="5758d-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5758d-135">NOTES</span></span>

## <span data-ttu-id="5758d-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5758d-136">RELATED LINKS</span></span>
