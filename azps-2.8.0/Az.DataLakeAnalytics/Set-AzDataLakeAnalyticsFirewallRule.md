---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 8d69a3297f23fdc9e4095a695ee790ae2476a136
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721355"
---
# <span data-ttu-id="c5cd7-101">Set-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c5cd7-101">Set-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="c5cd7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c5cd7-102">SYNOPSIS</span></span>
<span data-ttu-id="c5cd7-103">Обновляет правило брандмауэра в учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c5cd7-103">Updates a firewall rule in a Data Lake Analytics account.</span></span>

## <span data-ttu-id="c5cd7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c5cd7-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [[-StartIpAddress] <String>]
 [[-EndIpAddress] <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5cd7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5cd7-105">DESCRIPTION</span></span>
<span data-ttu-id="c5cd7-106">Командлет **Set-AzDataLakeAnalyticsFirewallRule** обновляет правило брандмауэра в учетной записи Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c5cd7-106">The **Set-AzDataLakeAnalyticsFirewallRule** cmdlet updates a firewall rule in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="c5cd7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c5cd7-107">EXAMPLES</span></span>

### <span data-ttu-id="c5cd7-108">Пример 1: обновление правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="c5cd7-108">Example 1: Update a firewall rule</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="c5cd7-109">Эта команда обновляет правило брандмауэра с именем "Мое правило брандмауэра" в учетной записи "ContosoAdlAcct", чтобы создать диапазон IP-адресов: 127.0.0.1-127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="c5cd7-109">This command updates the firewall rule named "my firewall rule" in account "ContosoAdlAcct" to have the new IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="c5cd7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c5cd7-110">PARAMETERS</span></span>

### <span data-ttu-id="c5cd7-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="c5cd7-111">-Account</span></span>
<span data-ttu-id="c5cd7-112">Учетная запись Data Lake Analytics для обновления правила брандмауэра в</span><span class="sxs-lookup"><span data-stu-id="c5cd7-112">The Data Lake Analytics account to update the firewall rule in</span></span>

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

### <span data-ttu-id="c5cd7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5cd7-113">-DefaultProfile</span></span>
<span data-ttu-id="c5cd7-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c5cd7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5cd7-115">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="c5cd7-115">-EndIpAddress</span></span>
<span data-ttu-id="c5cd7-116">Конец допустимого IP-диапазона для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="c5cd7-116">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="c5cd7-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="c5cd7-117">-Name</span></span>
<span data-ttu-id="c5cd7-118">Имя правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="c5cd7-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="c5cd7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5cd7-119">-ResourceGroupName</span></span>
<span data-ttu-id="c5cd7-120">Имя группы ресурсов, в которой требуется получить учетную запись.</span><span class="sxs-lookup"><span data-stu-id="c5cd7-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="c5cd7-121">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="c5cd7-121">-StartIpAddress</span></span>
<span data-ttu-id="c5cd7-122">Начало диапазона допустимых IP-адресов для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="c5cd7-122">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="c5cd7-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5cd7-123">-Confirm</span></span>
<span data-ttu-id="c5cd7-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c5cd7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5cd7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5cd7-125">-WhatIf</span></span>
<span data-ttu-id="c5cd7-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c5cd7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5cd7-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c5cd7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5cd7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5cd7-128">CommonParameters</span></span>
<span data-ttu-id="c5cd7-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c5cd7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5cd7-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5cd7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5cd7-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c5cd7-131">INPUTS</span></span>

### <span data-ttu-id="c5cd7-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c5cd7-132">System.String</span></span>

## <span data-ttu-id="c5cd7-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c5cd7-133">OUTPUTS</span></span>

### <span data-ttu-id="c5cd7-134">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c5cd7-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="c5cd7-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="c5cd7-135">NOTES</span></span>

## <span data-ttu-id="c5cd7-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c5cd7-136">RELATED LINKS</span></span>
