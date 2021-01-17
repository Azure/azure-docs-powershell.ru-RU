---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 91941fbef7363a56da8a8021294750cc862aab55
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98401356"
---
# <span data-ttu-id="f2260-101">Set-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f2260-101">Set-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="f2260-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2260-102">SYNOPSIS</span></span>
<span data-ttu-id="f2260-103">Обновляет правило брандмауэра в учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="f2260-103">Updates a firewall rule in a Data Lake Analytics account.</span></span>

## <span data-ttu-id="f2260-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f2260-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2260-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2260-105">DESCRIPTION</span></span>
<span data-ttu-id="f2260-106">Cmdlet **Set-AzDataLakeAnalyticsFirewallRule** обновляет правило брандмауэра в учетной записи Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="f2260-106">The **Set-AzDataLakeAnalyticsFirewallRule** cmdlet updates a firewall rule in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="f2260-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f2260-107">EXAMPLES</span></span>

### <span data-ttu-id="f2260-108">Пример 1. Обновление правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="f2260-108">Example 1: Update a firewall rule</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="f2260-109">Эта команда обновляет правило брандмауэра под названием "Правило брандмауэра" в учетной записи ContosoAdlAcct, чтобы иметь новый диапазон IP-адресов: 127.0.0.1–127.0.10</span><span class="sxs-lookup"><span data-stu-id="f2260-109">This command updates the firewall rule named "my firewall rule" in account "ContosoAdlAcct" to have the new IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="f2260-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2260-110">PARAMETERS</span></span>

### <span data-ttu-id="f2260-111">-Account</span><span class="sxs-lookup"><span data-stu-id="f2260-111">-Account</span></span>
<span data-ttu-id="f2260-112">Учетная запись Data Lake Analytics для обновления правила брандмауэра в</span><span class="sxs-lookup"><span data-stu-id="f2260-112">The Data Lake Analytics account to update the firewall rule in</span></span>

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

### <span data-ttu-id="f2260-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2260-113">-DefaultProfile</span></span>
<span data-ttu-id="f2260-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f2260-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f2260-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="f2260-115">-EndIpAddress</span></span>
<span data-ttu-id="f2260-116">Конец допустимого диапазона IP-адресов для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="f2260-116">The end of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2260-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f2260-117">-Name</span></span>
<span data-ttu-id="f2260-118">Имя правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="f2260-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="f2260-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2260-119">-ResourceGroupName</span></span>
<span data-ttu-id="f2260-120">Имя группы ресурсов, под которой нужно получить учетную запись.</span><span class="sxs-lookup"><span data-stu-id="f2260-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="f2260-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="f2260-121">-StartIpAddress</span></span>
<span data-ttu-id="f2260-122">Начало допустимого диапазона IP-адресов для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="f2260-122">The start of the valid ip range for the firewall rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2260-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2260-123">-Confirm</span></span>
<span data-ttu-id="f2260-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f2260-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2260-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2260-125">-WhatIf</span></span>
<span data-ttu-id="f2260-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2260-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2260-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f2260-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2260-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2260-128">CommonParameters</span></span>
<span data-ttu-id="f2260-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2260-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2260-130">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2260-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2260-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f2260-131">INPUTS</span></span>

### <span data-ttu-id="f2260-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f2260-132">System.String</span></span>

## <span data-ttu-id="f2260-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f2260-133">OUTPUTS</span></span>

### <span data-ttu-id="f2260-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f2260-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="f2260-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f2260-135">NOTES</span></span>

## <span data-ttu-id="f2260-136">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2260-136">RELATED LINKS</span></span>
