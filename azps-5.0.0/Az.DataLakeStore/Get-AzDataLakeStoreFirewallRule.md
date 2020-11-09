---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 7D27F7B1-BAF8-4A01-8BA7-A75A4CFAE370
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorefirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreFirewallRule.md
ms.openlocfilehash: c681ba089487868b556bd6e0ae198384a0dadd8c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94313373"
---
# <span data-ttu-id="93205-101">Get-AzDataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="93205-101">Get-AzDataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="93205-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="93205-102">SYNOPSIS</span></span>
<span data-ttu-id="93205-103">Получает указанные правила брандмауэра в заданном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="93205-103">Gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="93205-104">Если не указано правило брандмауэра, выводится список всех правил брандмауэра для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="93205-104">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="93205-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="93205-105">SYNTAX</span></span>

```
Get-AzDataLakeStoreFirewallRule [-Account] <String> [[-Name] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93205-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="93205-106">DESCRIPTION</span></span>
<span data-ttu-id="93205-107">Командлет Get-AzDataLakeStoreFirewallRule получает указанные правила брандмауэра в указанном Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="93205-107">The Get-AzDataLakeStoreFirewallRule cmdlet gets the specified firewall rules in the specified Data Lake Store.</span></span>
<span data-ttu-id="93205-108">Если не указано правило брандмауэра, выводится список всех правил брандмауэра для учетной записи.</span><span class="sxs-lookup"><span data-stu-id="93205-108">If no firewall rule is specified, then lists all firewall rules for the account.</span></span>

## <span data-ttu-id="93205-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="93205-109">EXAMPLES</span></span>

### <span data-ttu-id="93205-110">Пример 1: получение определенного правила брандмауэра</span><span class="sxs-lookup"><span data-stu-id="93205-110">Example 1: Retrieve a specific firewall rule</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL" -Name MyFirewallRule
```

<span data-ttu-id="93205-111">Возвращает правило брандмауэра с именем "MyFirewallRule" из учетной записи "ContosoADL"</span><span class="sxs-lookup"><span data-stu-id="93205-111">Returns the firewall rule named "MyFirewallRule" from account "ContosoADL"</span></span>

### <span data-ttu-id="93205-112">Пример 2: список всех правил брандмауэра в учетной записи</span><span class="sxs-lookup"><span data-stu-id="93205-112">Example 2: List all firewall rules in an account</span></span>
```
PS C:\> Get-AzDataLakeStoreFirewallRule -AccountName "ContosoADL"
```

<span data-ttu-id="93205-113">Возвращает все правила брандмауэра в учетной записи "ContosoADL".</span><span class="sxs-lookup"><span data-stu-id="93205-113">Returns all firewall rules in account "ContosoADL"</span></span>

## <span data-ttu-id="93205-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="93205-114">PARAMETERS</span></span>

### <span data-ttu-id="93205-115">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="93205-115">-Account</span></span>
<span data-ttu-id="93205-116">Учетная запись Data Lake Store, из которой нужно получить правило брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="93205-116">The Data Lake Store account to retrieve the firewall rule from.</span></span>

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

### <span data-ttu-id="93205-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93205-117">-DefaultProfile</span></span>
<span data-ttu-id="93205-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="93205-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="93205-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="93205-119">-Name</span></span>
<span data-ttu-id="93205-120">Имя правила межсетевого экрана, которое требуется получить</span><span class="sxs-lookup"><span data-stu-id="93205-120">The name of the firewall rule to retrieve</span></span>

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

### <span data-ttu-id="93205-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93205-121">-ResourceGroupName</span></span>
<span data-ttu-id="93205-122">Имя группы ресурсов, для которой требуется извлечь указанное правило брандмауэра для указанной учетной записи.</span><span class="sxs-lookup"><span data-stu-id="93205-122">Name of resource group under which want to retrieve the specified account's specified firewall rule.</span></span>

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

### <span data-ttu-id="93205-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93205-123">CommonParameters</span></span>
<span data-ttu-id="93205-124">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="93205-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93205-125">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93205-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93205-126">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="93205-126">INPUTS</span></span>

### <span data-ttu-id="93205-127">System. String</span><span class="sxs-lookup"><span data-stu-id="93205-127">System.String</span></span>

## <span data-ttu-id="93205-128">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="93205-128">OUTPUTS</span></span>

### <span data-ttu-id="93205-129">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreFirewallRule</span><span class="sxs-lookup"><span data-stu-id="93205-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreFirewallRule</span></span>

## <span data-ttu-id="93205-130">Пуск</span><span class="sxs-lookup"><span data-stu-id="93205-130">NOTES</span></span>

## <span data-ttu-id="93205-131">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="93205-131">RELATED LINKS</span></span>