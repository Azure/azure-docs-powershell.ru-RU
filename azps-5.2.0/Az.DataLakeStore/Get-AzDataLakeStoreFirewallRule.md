---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: c681ba089487868b556bd6e0ae198384a0dadd8c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98398567"
---
# <span data-ttu-id="8f2a8-101">Get-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8f2a8-101">Get-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="8f2a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f2a8-102">SYNOPSIS</span></span>
<span data-ttu-id="8f2a8-103">Получает указанные правила брандмауэра в указанном магазине data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8f2a8-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="8f2a8-104">Если правило брандмауэра не задано, будут перечислены все правила брандмауэра для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="8f2a8-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="8f2a8-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8f2a8-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8f2a8-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8f2a8-106">DESCRIPTION</span></span>
<span data-ttu-id="8f2a8-107">Этот Get-AzDataLakeStoreFirewallRule получает указанные правила брандмауэра в указанном магазине.</span><span class="sxs-lookup"><span data-stu-id="8f2a8-107">The Get-AzDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="8f2a8-108">Если правило брандмауэра не задано, будут перечислены все правила брандмауэра для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="8f2a8-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="8f2a8-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8f2a8-109">EXAMPLES</span></span>

### <span data-ttu-id="8f2a8-110">Пример 1. Извлечение определенного правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="8f2a8-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="8f2a8-111">Возвращает правило брандмауэра MyFirewallRule из учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="8f2a8-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="8f2a8-112">Пример 2. Список всех правил брандмауэра в учетной записи</span><span class="sxs-lookup"><span data-stu-id="8f2a8-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="8f2a8-113">Возвращает все правила брандмауэра в учетной записи ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="8f2a8-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="8f2a8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8f2a8-114">PARAMETERS</span></span>

### <span data-ttu-id="8f2a8-115">-Account</span><span class="sxs-lookup"><span data-stu-id="8f2a8-115">-Account</span></span>
<span data-ttu-id="8f2a8-116">Учетная запись Магазина данных для получения правила брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="8f2a8-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

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

### <span data-ttu-id="8f2a8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f2a8-117">-DefaultProfile</span></span>
<span data-ttu-id="8f2a8-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="8f2a8-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f2a8-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8f2a8-119">-Name</span></span>
<span data-ttu-id="8f2a8-120">Имя правила брандмауэра, которое нужно восстановить</span><span class="sxs-lookup"><span data-stu-id="8f2a8-120">The name of the firewall rule to retrieve</span></span>

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

### <span data-ttu-id="8f2a8-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f2a8-121">-ResourceGroupName</span></span>
<span data-ttu-id="8f2a8-122">Имя группы ресурсов, для которой нужно получить указанное правило брандмауэра указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="8f2a8-122">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

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

### <span data-ttu-id="8f2a8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f2a8-123">CommonParameters</span></span>
<span data-ttu-id="8f2a8-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f2a8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f2a8-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f2a8-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f2a8-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8f2a8-126">INPUTS</span></span>

### <span data-ttu-id="8f2a8-127">System.String</span><span class="sxs-lookup"><span data-stu-id="8f2a8-127">System.String</span></span>

## <span data-ttu-id="8f2a8-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8f2a8-128">OUTPUTS</span></span>

### <span data-ttu-id="8f2a8-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="8f2a8-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="8f2a8-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8f2a8-130">NOTES</span></span>

## <span data-ttu-id="8f2a8-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8f2a8-131">RELATED LINKS</span></span>
