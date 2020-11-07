---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: 39450f979a4c79e453c66845b522aba91757f672
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721318"
---
# <span data-ttu-id="97f59-101">Get-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="97f59-101">Get-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="97f59-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="97f59-102">SYNOPSIS</span></span>
<span data-ttu-id="97f59-103">Получает указанные правила брандмауэра в заданном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="97f59-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="97f59-104">Если не указано правило брандмауэра, выводится список всех правил брандмауэра для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="97f59-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="97f59-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="97f59-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97f59-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="97f59-106">DESCRIPTION</span></span>
<span data-ttu-id="97f59-107">Командлет Get-AzDataLakeStoreFirewallRule получает указанные правила брандмауэра в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="97f59-107">The Get-AzDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="97f59-108">Если не указано правило брандмауэра, выводится список всех правил брандмауэра для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="97f59-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="97f59-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="97f59-109">EXAMPLES</span></span>

### <span data-ttu-id="97f59-110">Пример 1: получение определенного правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="97f59-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="97f59-111">Возвращает правило брандмауэра с именем "MyFirewallRule" из учетной записи "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="97f59-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="97f59-112">Пример 2: список всех правил брандмауэра в учетной записи</span><span class="sxs-lookup"><span data-stu-id="97f59-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="97f59-113">Возвращает все правила брандмауэра в учетной записи "ContosoADL".</span><span class="sxs-lookup"><span data-stu-id="97f59-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="97f59-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="97f59-114">PARAMETERS</span></span>

### <span data-ttu-id="97f59-115">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="97f59-115">-Account</span></span>
<span data-ttu-id="97f59-116">Учетная запись Data Lake Store, из которой нужно получить правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="97f59-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

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

### <span data-ttu-id="97f59-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97f59-117">-DefaultProfile</span></span>
<span data-ttu-id="97f59-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="97f59-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="97f59-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="97f59-119">-Name</span></span>
<span data-ttu-id="97f59-120">Имя правила межсетевого экрана, которое требуется получить</span><span class="sxs-lookup"><span data-stu-id="97f59-120">The name of the firewall rule to retrieve</span></span>

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

### <span data-ttu-id="97f59-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97f59-121">-ResourceGroupName</span></span>
<span data-ttu-id="97f59-122">Имя группы ресурсов, для которой требуется извлечь указанное правило брандмауэра для указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="97f59-122">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

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

### <span data-ttu-id="97f59-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97f59-123">CommonParameters</span></span>
<span data-ttu-id="97f59-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="97f59-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97f59-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97f59-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97f59-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="97f59-126">INPUTS</span></span>

### <span data-ttu-id="97f59-127">System. String</span><span class="sxs-lookup"><span data-stu-id="97f59-127">System.String</span></span>

## <span data-ttu-id="97f59-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="97f59-128">OUTPUTS</span></span>

### <span data-ttu-id="97f59-129">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="97f59-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="97f59-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="97f59-130">NOTES</span></span>

## <span data-ttu-id="97f59-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="97f59-131">RELATED LINKS</span></span>
