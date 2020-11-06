---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/remove-azurermdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 239e9325532b18140a36e4b8f9a8f291e508a91c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560936"
---
# <span data-ttu-id="23dea-101">Remove-AzureRmDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="23dea-101">Remove-AzureRmDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="23dea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="23dea-102">SYNOPSIS</span></span>
<span data-ttu-id="23dea-103">Удаляет правило брандмауэра из учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="23dea-103">Removes a firewall rule from a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23dea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="23dea-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [-PassThru]
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="23dea-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23dea-105">DESCRIPTION</span></span>
<span data-ttu-id="23dea-106">Командлет **Remove-AzureRmDataLakeAnalyticsFirewallRule** удаляет правило брандмауэра из учетной записи Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="23dea-106">The **Remove-AzureRmDataLakeAnalyticsFirewallRule** cmdlet removes a firewall rule from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="23dea-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="23dea-107">EXAMPLES</span></span>

### <span data-ttu-id="23dea-108">Пример 1: Удаление правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="23dea-108">Example 1: Remove a firewall rule</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="23dea-109">Эта команда удаляет правило брандмауэра с именем "Мое правило брандмауэра" из учетной записи "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="23dea-109">This command removes the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="23dea-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="23dea-110">PARAMETERS</span></span>

### <span data-ttu-id="23dea-111">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="23dea-111">-Account</span></span>
<span data-ttu-id="23dea-112">Учетная запись Data Lake Analytics, из которой нужно удалить правило межсетевого экрана</span><span class="sxs-lookup"><span data-stu-id="23dea-112">The Data Lake Analytics account to remove the firewall rule from</span></span>

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

### <span data-ttu-id="23dea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23dea-113">-DefaultProfile</span></span>
<span data-ttu-id="23dea-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="23dea-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23dea-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="23dea-115">-Name</span></span>
<span data-ttu-id="23dea-116">Имя правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="23dea-116">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="23dea-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23dea-117">-PassThru</span></span>
<span data-ttu-id="23dea-118">Указывает, что должен возвращаться логический ответ, указывающий результат операции удаления.</span><span class="sxs-lookup"><span data-stu-id="23dea-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="23dea-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23dea-119">-ResourceGroupName</span></span>
<span data-ttu-id="23dea-120">Имя группы ресурсов, в которой требуется получить учетную запись.</span><span class="sxs-lookup"><span data-stu-id="23dea-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="23dea-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23dea-121">-Confirm</span></span>
<span data-ttu-id="23dea-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="23dea-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23dea-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23dea-123">-WhatIf</span></span>
<span data-ttu-id="23dea-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="23dea-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23dea-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="23dea-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23dea-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23dea-126">CommonParameters</span></span>
<span data-ttu-id="23dea-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="23dea-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23dea-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23dea-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23dea-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="23dea-129">INPUTS</span></span>

### <span data-ttu-id="23dea-130">System. String</span><span class="sxs-lookup"><span data-stu-id="23dea-130">System.String</span></span>

### <span data-ttu-id="23dea-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="23dea-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="23dea-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="23dea-132">OUTPUTS</span></span>

### <span data-ttu-id="23dea-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="23dea-133">System.Boolean</span></span>

## <span data-ttu-id="23dea-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="23dea-134">NOTES</span></span>

## <span data-ttu-id="23dea-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23dea-135">RELATED LINKS</span></span>
