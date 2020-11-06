---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Add-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 585e0cd6a3cd74c8077833f6b5599b076c2a5db6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559876"
---
# <span data-ttu-id="ca349-101">Add-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ca349-101">Add-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="ca349-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ca349-102">SYNOPSIS</span></span>
<span data-ttu-id="ca349-103">Добавляет правило брандмауэра к учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="ca349-103">Adds a firewall rule to a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca349-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ca349-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [-Name] <String> [-StartIpAddress] <String>
 [-EndIpAddress] <String> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca349-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca349-105">DESCRIPTION</span></span>
<span data-ttu-id="ca349-106">Командлет **Add-AzureRmDataLakeAnalyticsFirewallRule** добавляет правило брандмауэра в учетную запись Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="ca349-106">The **Add-AzureRmDataLakeAnalyticsFirewallRule** cmdlet adds a firewall rule to an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="ca349-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ca349-107">EXAMPLES</span></span>

### <span data-ttu-id="ca349-108">Пример 1: Добавление правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="ca349-108">Example 1: Add a firewall rule</span></span>
```
PS C:\>Add-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule" -StartIpAddress 127.0.0.1 -EndIpAddress 127.0.0.10
```

<span data-ttu-id="ca349-109">Эта команда добавляет правило брандмауэра с именем "Мое правило брандмауэра" из учетной записи "ContosoAdlAcct" с IP-адресом: 127.0.0.1-127.0.0.10</span><span class="sxs-lookup"><span data-stu-id="ca349-109">This command adds the firewall rule named "my firewall rule" from account "ContosoAdlAcct" with the IP range: 127.0.0.1 - 127.0.0.10</span></span>

## <span data-ttu-id="ca349-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ca349-110">PARAMETERS</span></span>

### <span data-ttu-id="ca349-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="ca349-111">-Account</span></span>
<span data-ttu-id="ca349-112">Учетная запись Data Lake Analytics, к которой нужно добавить правило межсетевого экрана</span><span class="sxs-lookup"><span data-stu-id="ca349-112">The Data Lake Analytics account to add the firewall rule to</span></span>

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

### <span data-ttu-id="ca349-113">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="ca349-113">-EndIpAddress</span></span>
<span data-ttu-id="ca349-114">Конец допустимого IP-диапазона для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="ca349-114">The end of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="ca349-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ca349-115">-Name</span></span>
<span data-ttu-id="ca349-116">Имя правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="ca349-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="ca349-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca349-117">-ResourceGroupName</span></span>
<span data-ttu-id="ca349-118">Имя группы ресурсов, в которой требуется получить учетную запись.</span><span class="sxs-lookup"><span data-stu-id="ca349-118">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="ca349-119">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="ca349-119">-StartIpAddress</span></span>
<span data-ttu-id="ca349-120">Начало диапазона допустимых IP-адресов для правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="ca349-120">The start of the valid ip range for the firewall rule</span></span>

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

### <span data-ttu-id="ca349-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca349-121">-Confirm</span></span>
<span data-ttu-id="ca349-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ca349-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca349-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca349-123">-WhatIf</span></span>
<span data-ttu-id="ca349-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ca349-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca349-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ca349-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca349-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca349-126">-DefaultProfile</span></span>
<span data-ttu-id="ca349-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ca349-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca349-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca349-128">CommonParameters</span></span>
<span data-ttu-id="ca349-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ca349-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca349-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca349-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca349-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ca349-131">INPUTS</span></span>

### <span data-ttu-id="ca349-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ca349-132">System.String</span></span>

## <span data-ttu-id="ca349-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ca349-133">OUTPUTS</span></span>

### <span data-ttu-id="ca349-134">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ca349-134">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="ca349-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="ca349-135">NOTES</span></span>

## <span data-ttu-id="ca349-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ca349-136">RELATED LINKS</span></span>

