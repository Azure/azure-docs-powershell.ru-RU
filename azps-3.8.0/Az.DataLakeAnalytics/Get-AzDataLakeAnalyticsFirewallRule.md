---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticsfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsFirewallRule.md
ms.openlocfilehash: 40c44ff157fca6a276cac8ece508e9d540b526ed
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065315"
---
# <span data-ttu-id="8bc0a-101">Get-AzDataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8bc0a-101">Get-AzDataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="8bc0a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8bc0a-102">SYNOPSIS</span></span>
<span data-ttu-id="8bc0a-103">Получение правила брандмауэра или списка правил брандмауэра из учетной записи Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="8bc0a-103">Retrieves a firewall rule or list of firewall rules from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="8bc0a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8bc0a-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8bc0a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8bc0a-105">DESCRIPTION</span></span>
<span data-ttu-id="8bc0a-106">Командлет **Get-AzDataLakeAnalyticsFirewallRule** извлекает правило брандмауэра или список правил брандмауэра из учетной записи Azure Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="8bc0a-106">The **Get-AzDataLakeAnalyticsFirewallRule** cmdlet retrieves a firewall rule or list of firewall rules from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="8bc0a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8bc0a-107">EXAMPLES</span></span>

### <span data-ttu-id="8bc0a-108">Пример 1: получение правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="8bc0a-108">Example 1: Get a firewall rule</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct" -Name "My firewall rule"
```

<span data-ttu-id="8bc0a-109">Эта команда получает правило брандмауэра с именем "Мое правило брандмауэра" из учетной записи "ContosoAdlAcct".</span><span class="sxs-lookup"><span data-stu-id="8bc0a-109">This command gets the firewall rule named "my firewall rule" from account "ContosoAdlAcct"</span></span>

### <span data-ttu-id="8bc0a-110">Пример 2: список всех правил брандмауэра</span><span class="sxs-lookup"><span data-stu-id="8bc0a-110">Example 2: List all firewall rules</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsFirewallRule -Account "ContosoAdlAcct"
```

<span data-ttu-id="8bc0a-111">Эта команда получает все правила брандмауэра из учетной записи "ContosoAdlAcct"</span><span class="sxs-lookup"><span data-stu-id="8bc0a-111">This command gets all firewall rules from account "ContosoAdlAcct"</span></span>

## <span data-ttu-id="8bc0a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8bc0a-112">PARAMETERS</span></span>

### <span data-ttu-id="8bc0a-113">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="8bc0a-113">-Account</span></span>
<span data-ttu-id="8bc0a-114">Учетная запись Data Lake Analytics, из которой нужно получить правило межсетевого экрана</span><span class="sxs-lookup"><span data-stu-id="8bc0a-114">The Data Lake Analytics account to get the firewall rule from</span></span>

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

### <span data-ttu-id="8bc0a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bc0a-115">-DefaultProfile</span></span>
<span data-ttu-id="8bc0a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8bc0a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8bc0a-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8bc0a-117">-Name</span></span>
<span data-ttu-id="8bc0a-118">Имя правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="8bc0a-118">The name of the firewall rule.</span></span>

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

### <span data-ttu-id="8bc0a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8bc0a-119">-ResourceGroupName</span></span>
<span data-ttu-id="8bc0a-120">Имя группы ресурсов, в которой требуется получить учетную запись.</span><span class="sxs-lookup"><span data-stu-id="8bc0a-120">Name of resource group under which want to retrieve the account.</span></span>

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

### <span data-ttu-id="8bc0a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bc0a-121">CommonParameters</span></span>
<span data-ttu-id="8bc0a-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8bc0a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bc0a-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bc0a-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bc0a-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8bc0a-124">INPUTS</span></span>

### <span data-ttu-id="8bc0a-125">System. String</span><span class="sxs-lookup"><span data-stu-id="8bc0a-125">System.String</span></span>

## <span data-ttu-id="8bc0a-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8bc0a-126">OUTPUTS</span></span>

### <span data-ttu-id="8bc0a-127">Microsoft. Azure. Commands. DataLakeAnalytics. Models. DataLakeAnalyticsFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8bc0a-127">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsFirewallRule</span></span>

## <span data-ttu-id="8bc0a-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="8bc0a-128">NOTES</span></span>

## <span data-ttu-id="8bc0a-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8bc0a-129">RELATED LINKS</span></span>
