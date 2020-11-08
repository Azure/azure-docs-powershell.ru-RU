---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 91941fbef7363a56da8a8021294750cc862aab55
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065068"
---
# <span data-ttu-id="9efbe-101">Set-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9efbe-101">Set-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="9efbe-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9efbe-102">SYNOPSIS</span></span>
<span data-ttu-id="9efbe-103">Обновляет правило брандмауэра в учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="9efbe-103">Updates a firewall rule in a Data Lake Analytics account.</span></span>

## <span data-ttu-id="9efbe-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9efbe-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9efbe-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9efbe-105">DESCRIPTION</span></span>
<span data-ttu-id="9efbe-106">Командлет **Set-AzDataLakeAnalyticsFirewallRule** обновляет правило брандмауэра в учетной записи Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="9efbe-106">The **Set-AzDataLakeAnalyticsFirewallRule** cmdlet updates a firewall rule in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="9efbe-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9efbe-107">EXAMPLES</span></span>

### <span data-ttu-id="9efbe-108">Пример 1: обновление правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="9efbe-108">Example 1: Update a firewall rule</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="9efbe-109">Эта команда обновляет правило брандмауэра с именем "Мое правило брандмауэра" в учетной записи "ContosoAdlAcct", чтобы создать диапазон IP-адресов: 127.0.0.1-127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="9efbe-109">This command updates the firewall rule named "my firewall rule" in account "ContosoAdlAcct" to have the new IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="9efbe-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9efbe-110">PARAMETERS</span></span>

### <span data-ttu-id="9efbe-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="9efbe-111">-Account</span></span>
<span data-ttu-id="9efbe-112">Учетная запись Data Lake Analytics для обновления правила брандмауэра в</span><span class="sxs-lookup"><span data-stu-id="9efbe-112">The Data Lake Analytics account to update the firewall rule in</span></span>

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

### <span data-ttu-id="9efbe-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9efbe-113">-DefaultProfile</span></span>
<span data-ttu-id="9efbe-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9efbe-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9efbe-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="9efbe-115">-EndIpAddress</span></span>
<span data-ttu-id="9efbe-116">Конец допустимого IP-диапазона для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="9efbe-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="9efbe-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9efbe-117">-Name</span></span>
<span data-ttu-id="9efbe-118">Имя правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="9efbe-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="9efbe-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9efbe-119">-ResourceGroupName</span></span>
<span data-ttu-id="9efbe-120">Имя группы ресурсов, в которой требуется получить учетную запись.</span><span class="sxs-lookup"><span data-stu-id="9efbe-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="9efbe-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="9efbe-121">-StartIpAddress</span></span>
<span data-ttu-id="9efbe-122">Начало диапазона допустимых IP-адресов для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="9efbe-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="9efbe-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9efbe-123">-Confirm</span></span>
<span data-ttu-id="9efbe-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9efbe-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9efbe-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9efbe-125">-WhatIf</span></span>
<span data-ttu-id="9efbe-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9efbe-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9efbe-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9efbe-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9efbe-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9efbe-128">CommonParameters</span></span>
<span data-ttu-id="9efbe-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9efbe-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9efbe-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9efbe-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9efbe-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9efbe-131">INPUTS</span></span>

### <span data-ttu-id="9efbe-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9efbe-132">System.String</span></span>

## <span data-ttu-id="9efbe-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9efbe-133">OUTPUTS</span></span>

### <span data-ttu-id="9efbe-134">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9efbe-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="9efbe-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="9efbe-135">NOTES</span></span>

## <span data-ttu-id="9efbe-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9efbe-136">RELATED LINKS</span></span>
